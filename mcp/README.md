# mcp/

Groundwork's diagnosis goes through predictive-maintenance-mcp by lgdimaggio
(`https://github.com/lgdimaggio/predictive-maintenance-mcp`). The scripts expect it here:

- `scripts/provision-agent.sh` uploads `mcp/predictive-maintenance-mcp/` into the sandbox (override with `PMMCP_DIR`).
- `scripts/build-prototype-feed.py` uses `mcp/predictive-maintenance-mcp/src` when it is present.

It is not bundled in this copy. It is a named prerequisite: get it from its own project under its own licence and
place it in `mcp/predictive-maintenance-mcp/`, keeping its LICENSE file with it. No version or commit is pinned.
