# Modifications

This branch is a modified version of [GoFEM/pyGoFEM](https://github.com/GoFEM/pyGoFEM),
licensed under the GNU GPL v3 like the original (see `LICENSE`).

**Based on:** upstream commit `c60b709` (2023-11-15), a README update on top of
`5c56774` (2023-06-21). `c60b709` is no longer in upstream's history, but
`5c56774` is.

## Changes from upstream (2026-11-05)

`gofem/mesh_utils.py`:

- `refine_within_polygon` takes a new `pnorm` argument (default 1). `pnorm=1`
  behaves as before. `pnorm > 1` is an experimental rounded polygon: only cells
  inside a superellipsoid enclosing the polygon are considered.
- `is_within_ellipsoid` no longer asserts `pnorm in [1, 2]`, so fractional
  values can be used.

Packaging:

- Added `pyproject.toml`, so the package can be installed with pip.
- Added this file and the note at the top of `README.md`.
