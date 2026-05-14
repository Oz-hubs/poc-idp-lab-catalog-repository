# Repository Structure

```text
catalog/
  locations.yaml      # Bootstrap Location entity
  entities.yaml       # Systems, Components, APIs, Resources
  org.yaml            # Users and Groups
templates/
  repo-template/
    template.yaml
    content/          # Files scaffolded into new repos
  csharp-repo-template/
    template.yaml
    content/
  python-repo-template/
    template.yaml
    content/
catalog-info.yaml     # This repository registered as a Component
mkdocs.yml            # TechDocs configuration
docs/                 # TechDocs sources
```

## Key Files

- `catalog/locations.yaml` — entry point Backstage points at.
- `catalog-info.yaml` — registers this repo itself as a Component with TechDocs.
- `mkdocs.yml` — TechDocs site configuration.
