# templarc-docs

English | [日本語](README.ja.md)

Document kits for usage-driven development and AI-driven execution.

## Overview

This repository now has two primary kits.

| Kit | Purpose |
|-----|---------|
| [`kits/templarc-core/`](kits/templarc-core/README.md) | Stable design templates for usage-driven development |
| [`kits/ai-workflow/`](kits/ai-workflow/README.md) | Operational templates for AI-driven development |

The split is intentional.
`templarc-core` keeps durable design context.
`ai-workflow` keeps fast-changing execution rules, task briefs, and review checklists.

## Repository Layout

```text
repo/
├── kits/
│   ├── templarc-core/
│   └── ai-workflow/
├── docs/
│   ├── philosophy.md
│   ├── how-to-combine.md
│   └── migration.md
├── legacy/
└── examples/
```

## Start Here

If you want durable design documents, start with [`templarc-core`](kits/templarc-core/README.md).
If you want task briefs, agent rules, and PR checklists, add [`ai-workflow`](kits/ai-workflow/README.md).

Recommended reading order:

1. [`docs/philosophy.md`](docs/philosophy.md)
2. [`kits/templarc-core/README.md`](kits/templarc-core/README.md)
3. [`kits/ai-workflow/README.md`](kits/ai-workflow/README.md)
4. [`docs/how-to-combine.md`](docs/how-to-combine.md)

## Legacy

Previous user-document templates and the old Git guide were moved under [`legacy/`](legacy/README.md).
They remain as migration references, not as the default path.

## Notes

- Repositioning rationale: [`REPOSITIONING.md`](REPOSITIONING.md)
- Template philosophy: [`DESIGN.md`](DESIGN.md)
- Migration notes: [`docs/migration.md`](docs/migration.md)

## License

MIT License
