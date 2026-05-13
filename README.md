# poc-idp-lab-catalog-repository

Source of truth for the Backstage catalog in the IDP lab.

This repository contains:

- Catalog bootstrap and entity data under `catalog/`
- Software templates under `templates/`
- Template content files used by Backstage Scaffolder

Backstage is configured to ingest this repo starting from:

- `catalog/locations.yaml`

## How Backstage Reads This Repository

Backstage points to this URL:

- `https://github.com/Oz-hubs/poc-idp-lab-catalog-repository/blob/oz-hubs/catalog/locations.yaml`

The bootstrap location then references all catalog data and templates in this repo.

## Repository Structure

```text
catalog/
	locations.yaml
	entities.yaml
	org.yaml
templates/
	repo-template/
		template.yaml
		content/
			catalog-info.yaml
			CODEOWNERS
			README.md
	csharp-repo-template/
		template.yaml
		content/
			catalog-info.yaml
			CODEOWNERS
			readme.md
```

## Catalog Bootstrap

Current bootstrap file:

- `catalog/locations.yaml`

It references:

- `./entities.yaml`
- `./org.yaml`
- `../templates/repo-template/template.yaml`
- `../templates/csharp-repo-template/template.yaml`

Important: paths in `catalog/locations.yaml` are relative to `catalog/`, so do not prefix with `catalog/` again.

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

If `User`, `Group`, or `Template` are not allowed, ingestion warnings will appear and those entities will be skipped.

## Branching and Target Branch

The catalog branch is selected in the Backstage location URL itself.

The POC currently reads from the `oz-hubs` branch.

Example:

- oz-hubs branch: `.../blob/oz-hubs/catalog/locations.yaml`
- Main branch: `.../blob/main/catalog/locations.yaml`
- Feature branch: `.../blob/feature/my-branch/catalog/locations.yaml`

`catalog.import.pullRequestBranchName` is unrelated to ingestion target branch. It is only used when Backstage creates import PRs.

## Templates Included

### 1) New Repository with README

- Template file: `templates/repo-template/template.yaml`
- Creates a GitHub repository under the **Oz-hubs** organization
- Adds `README.md`, `CODEOWNERS`, and `catalog-info.yaml`
- Registers the new component in Backstage via `catalog:register`

### 2) New C# Repository Foundation

- Template file: `templates/csharp-repo-template/template.yaml`
- Creates a GitHub repository under the **Oz-hubs** organization for C# projects
- Adds governance and starter files
- Registers the new component in Backstage via `catalog:register`

## Updating Catalog Data

1. Edit files under `catalog/` and/or `templates/`.
2. Open a pull request.
3. Merge to the branch used by Backstage.
4. Backstage refreshes and ingests updated entities.

## Troubleshooting

### Warning: no matching files found with duplicated path

Example:

- `.../catalog/catalog/entities.yaml`

Cause:

- Wrong relative target in `catalog/locations.yaml`.

Fix:

- Use `./entities.yaml`, not `./catalog/entities.yaml`.

### Warning: entity is not of an allowed kind

Example:

- `Entity user:default/guest ... is not of an allowed kind`

Cause:

- Backstage `catalog.rules` does not include `User`/`Group`/`Template`.

Fix:

- Add missing kinds in Backstage config rules.

## Notes

- Keep entity references consistent (`owner`, `system`, etc.).
- Prefer small and reviewable PRs for catalog changes.
- Treat this repo as platform-critical configuration.
