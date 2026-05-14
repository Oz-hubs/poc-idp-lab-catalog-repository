# Troubleshooting

## Warning: no matching files found with duplicated path

Example: `.../catalog/catalog/entities.yaml`

**Cause:** wrong relative target in `catalog/locations.yaml`.

**Fix:** use `./entities.yaml`, not `./catalog/entities.yaml`.

## Warning: entity is not of an allowed kind

Example: `Entity user:default/guest ... is not of an allowed kind`

**Cause:** Backstage `catalog.rules` does not include `User`/`Group`/`Template`.

**Fix:** add the missing kinds in Backstage config rules.

## TechDocs not rendering

- Confirm `backstage.io/techdocs-ref: dir:.` annotation is present on the
  Component in `catalog-info.yaml`.
- Confirm `mkdocs.yml` exists at the repo root and the `docs/` folder is
  present.
- Check the TechDocs builder logs in Backstage for build errors.
