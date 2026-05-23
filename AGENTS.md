# Repository Agent Rules

## Project Purpose
This repository is used to collect and create personal skills for work.
Skills from this repository are copied into different work repositories when needed.

## Scope
These rules apply to the entire repository, especially all skills under `skills/`.

## Mandatory Post-Run Documentation Rule
For every skill execution under `skills/`, the agent must generate a markdown documentation file after the run.

Default output location and naming:

```txt
.documentation/
└── <current-branch-name>/
    └── <document-file-name-renegated>-<timestamp>.md
```

### Requirements
- Documentation output is required after every run.
- Base folder must default to repository root `/.documentation`.
- Files must be separated by current branch name.
- File name must include a renegated document name and a timestamp suffix.
- Output file extension must be `.md`.

### Timestamp
Recommended format:

```txt
YYYY-MM-DD_HH-mm-ss
```

## Mandatory Template For New Skills
When creating any new skill under `skills/<skill-name>/`, the skill definition file (for example `SKILL.md`) must include a dedicated rule section that enforces post-run documentation output.

Use this template block in every new skill:

```md
## Documentation Output Requirement (Mandatory)

After every skill run, always generate a markdown document.

Default output path:

```txt
.documentation/
└── <current-branch-name>/
    └── <document-file-name-renegated>-<timestamp>.md
```

Rules:
- Must generate documentation after every run.
- Must use repository-root `/.documentation` as default base folder.
- Must separate files by current branch name.
- Must include renegated document file name plus timestamp in file name.
- Must use `.md` extension.

Timestamp format:

```txt
YYYY-MM-DD_HH-mm-ss
```
```
