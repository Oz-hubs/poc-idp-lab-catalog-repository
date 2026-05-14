# poc-idp-lab-catalog-repository

Welcome to the documentation for the **IDP Lab Backstage catalog repository**.

This repo is the source of truth for the Backstage catalog used by the IDP lab.
It contains:

- Catalog bootstrap and entity data under `catalog/`
- Software templates under `templates/`
- Template content files used by the Backstage Scaffolder

## How Backstage Reads This Repository

Backstage ingests this repo starting from:

```
https://github.com/ozeta/poc-idp-lab-catalog-repository/blob/main/catalog/locations.yaml
```

The bootstrap `Location` then references all catalog data and templates in this
repo.

## Quick Links

- [Repository Structure](structure.md)
- [Catalog](catalog.md)
- [Templates](templates.md)
- [Troubleshooting](troubleshooting.md)
