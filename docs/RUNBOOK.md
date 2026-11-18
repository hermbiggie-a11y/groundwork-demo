# Groundwork run-and-reset checklist

Everything here runs on the Dell Pro Precision GB10 from the repo folder. See the README for the one-time setup.

## Before you start

- [ ] Qwen3.6-35B-A3B is served on `http://127.0.0.1:8000`, with the weights on internal NVMe.
- [ ] predictive-maintenance-mcp is in `mcp/predictive-maintenance-mcp/` (or `PMMCP_DIR` is set).
- [ ] The CWRU or Mendeley `.mat` files you fetched are in `data/cwru/`, and your own equipment manual is in
      `data/manuals/` (or `MANUAL` points at it).
- [ ] The agent is provisioned: `./scripts/provision-agent.sh` ends with "maintenance agent provisioned in plant-floor".
- [ ] `npm test` passes.

## Run

1. Terminal A, board API: `node app/server.mjs` (or the user service from `./scripts/install-board-service.sh`).
2. Terminal B, 1 Hz hops: `.venv/bin/python scripts/hop-loop.py`.
3. Open the board at `http://127.0.0.1:8765/prototype/` (landing at `http://127.0.0.1:8765/`).
4. Inject a catalogued fault: `./demo/inject/inject-ir.sh` (inner race), `./demo/inject/inject-or.sh` (outer race) or
   `./demo/inject/inject-ball.sh` (ball). In the board, Alt+I does the same for inner race.
5. Open the incident, check the cited signal window, manual page and CMMS row, and review the work order.
6. Ask Maintenance Assist a scoped question about the selected asset.
7. Containment: use "Attempt telemetry POST from sandbox". The state changes to CONTAINED only when the OpenShell gateway
   logs the deny.

## Reset

1. Clear the injected fault: `./demo/inject/clear.sh` (or Alt+Shift+I in the board).
2. Re-seed the demo inbox: `node scripts/seed-demo-incidents.mjs`.

## Fallbacks

- Board API unreachable: the inject scripts write the fault override to SQLite directly; the hop loop keeps running.
- OpenShell gateway offline: the containment rail shows "Unproven"; it never shows a seeded result.
- Board server down: a static-only board runs with
  `python3 -m http.server 4173 --bind 0.0.0.0 --directory web/prototype` (containment shows "gateway offline / unproven";
  the floor geometry still needs the board server).
- Floor view capture: headless Firefox on the GB10 has no WebGL, so use a windowed browser.

More detail on the board's routes and states is in `web/prototype/README.md`; the 3D viewer is described in
`web/twin/README.md`.
