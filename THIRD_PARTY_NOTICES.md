# Third-party notices

Groundwork itself is under the terms in `LICENSE`. The components below keep their own licences. Each one's full licence
file stays in place in this repo, and no file's own licence header has been removed.

## three.js

Bundled in `web/twin/vendor/` (`three.module.js`, `three.core.js` and the addons). Licence file: `web/licenses/three.txt`.
File header kept in `three.module.js` and `three.core.js`:

```
@license
Copyright 2010-2026 Three.js Authors
SPDX-License-Identifier: MIT
```

Licence text (verbatim from `web/licenses/three.txt`):

```
The MIT License

Copyright © 2010-2026 three.js authors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```

## Fonts (SIL Open Font License, Version 1.1)

Bundled in `web/landing/fonts/`. The full licence text ships beside each font.

Geist (`web/landing/fonts/geist-OFL.txt`):

```
Copyright 2024 The Geist Project Authors (https://github.com/vercel/geist-font.git)

This Font Software is licensed under the SIL Open Font License, Version 1.1.
This license is copied below, and is also available with a FAQ at:
https://openfontlicense.org
```

Geist Mono (`web/landing/fonts/geistmono-OFL.txt`):

```
Copyright 2024 The Geist Project Authors (https://github.com/vercel/geist-font.git)

This Font Software is licensed under the SIL Open Font License, Version 1.1.
This license is copied below, and is also available with a FAQ at:
https://openfontlicense.org
```

Instrument Serif (`web/landing/fonts/instrumentserif-OFL.txt`):

```
Copyright 2022 The Instrument Serif Project Authors (https://github.com/Instrument/instrument-serif)

This Font Software is licensed under the SIL Open Font License, Version 1.1.
This license is copied below, and is also available with a FAQ at:
https://scripts.sil.org/OFL
```

## VLFT 3D plant geometry (Creative Commons Attribution-NonCommercial 4.0 International)

From the DigitalFactory / VLFT repository (`https://github.com/difactory/repository`). Licence file:
`web/licenses/vlft.txt` (the full CC BY-NC 4.0 text). As the project's credits page (`web/credits.html`) says:
"Geometry adapted from DigitalFactory / VLFT repository, CC BY-NC 4.0: assembled, recolored, and reframed for this
demonstration; landing images render this adapted scene." This material is for non-commercial use only. The station
models are left out of the Dell copy; see the README's Known limits for where to get them.

## predictive-maintenance-mcp

By lgdimaggio (`https://github.com/lgdimaggio/predictive-maintenance-mcp`). Not bundled in this copy: it is a named
prerequisite you place in `mcp/` under its own licence. Its own LICENSE file stays with it.

## Data and documents (not redistributed)

- CWRU (Case Western Reserve University) and Mendeley bearing-vibration datasets: used under their own terms. The repo
  keeps only record metadata, checksums and derived values; you fetch the recordings yourself.
- Equipment manuals (for example the SKF bearing damage analysis manual): third-party copyrighted documents, not in this
  repo. You supply your own manuals.
