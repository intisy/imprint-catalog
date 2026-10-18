# imprint-catalog

How imprint installs things. App recipes, distros, window managers and bootloaders, read offline from the commit imprint pins.

## What is here

- `generated/apps/<id>.json`: one recipe per app, the packages it needs on each distro.
- `curated/distros/`, `curated/window-managers/`, `curated/bootloaders/`: the entries written by hand, in TOML.

Every entry has an `id` of lowercase words joined by hyphens, and every file is named after its `id`.
imprint reads this repository from its `catalog` submodule, pinned to one commit, so two machines on
the same imprint commit install the same packages. Your own entries go in your data repo under
`catalog/`, and replace an entry here with the same `id`.
