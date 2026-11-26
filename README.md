# grid-data

Additional grid data files for the [grid](https://github.com/theochem/grid) package.

## Grid families

This repository contains angular grids for the following families:

| Family | Folder | Reference |
| --- | --- | --- |
| Ahrens-Beylkin rotationally invariant quadratures | `ahrens_beylkin/` | [Ahrens & Beylkin, 2009](https://doi.org/10.1098/rspa.2009.0104) |
| Maximum determinant points (MaxDet) | `maxdet/` | [Sloan & Womersley, 2004](https://doi.org/10.1023/B:ACOM.0000016428.25905.da) |
| Symmetric spherical t-designs | `spherical_design/` | [Womersley, 2018](https://doi.org/10.1007/978-3-319-72456-0_57) |

For all grids, points lie on the unit sphere and the weights sum to $4\pi$.

The full reference, source URL and any notes for each family are in its
`metadata/metadata.json`.

The paths in `SHA256SUMS` are relative to the family folder. To verify a family:

```bash
cd <family> && sha256sum -c metadata/SHA256SUMS
```

## License

The [LICENSE](LICENSE) (LGPL-2.1) covers this repository's own files. It does not cover the grid
data. Each family keeps the terms of its original source, which are recorded in the `license`
field of `<family>/metadata/metadata.json`.

Where the source states no license (`maxdet` and `spherical_design`), no license is granted here.
These files are redistributed as published by their authors; check the original source before
reusing them.

### Ahrens-Beylkin grids

The files in `ahrens_beylkin/data/` are derived from the Ahrens-Beylkin tables of
[IntegratorXX](https://github.com/wavefunction91/IntegratorXX/tree/2620fbf3ec6c1556e28f90113e82017c63e6eafb),
which are distributed under the following license:

```text
BSD 3-Clause License

Copyright (c) 2019, David Williams-Young
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its
   contributors may be used to endorse or promote products derived from
   this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```
