# Catalog

## Bootstrap

`catalog/locations.yaml` is the entry point. It references:

- `./entities.yaml`
- `./org.yaml`
- `../templates/repo-template/template.yaml`
- `../templates/csharp-repo-template/template.yaml`
- `../catalog-info.yaml` (this repository as a Component)

Paths are relative to the `catalog/` directory.

## Allowed Entity Kinds

Backstage must allow these kinds for this location:

- `Component`
- `System`
- `API`
- `Resource`
- `Location`
- `User`
- `Group`
- `Template`

## Updating Catalog Data

1. Edit files under `catalog/` and/or `templates/`.
2. Open a pull request.
3. Merge to the branch used by Backstage.
4. Backstage refreshes and ingests updated entities.
