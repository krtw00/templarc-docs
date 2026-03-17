# templarc-docs

日本語 | [English](README.md)

設計ドキュメントテンプレート - Design Document Template

## 概要

templarc-docs は、使用駆動開発のための設計テンプレートと、
AI駆動開発のための運用テンプレートを分けて提供するリポジトリである。

## キット構成

| キット | 役割 |
|--------|------|
| [`kits/templarc-core/`](kits/templarc-core/README.md) | 使用駆動開発向けの永続設計テンプレート |
| [`kits/ai-workflow/`](kits/ai-workflow/README.md) | AI駆動開発向けの task brief、agent rule、PR checklist |

## リポジトリ構成

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

## 読み始める順番

1. [docs/philosophy.md](docs/philosophy.md) - なぜ分けたか
2. [kits/templarc-core/README.md](kits/templarc-core/README.md) - コア設計テンプレートの説明
3. [kits/ai-workflow/README.md](kits/ai-workflow/README.md) - AI運用テンプレートの説明
4. [docs/how-to-combine.md](docs/how-to-combine.md) - 併用方法

## legacy

旧 利用者向けドキュメントテンプレートと Git 規範は
[legacy/](legacy/README.md) に退避した。
移行参照用として残すが、新規採用の標準とはしない。

## 補足

- 再配置方針: [REPOSITIONING.md](REPOSITIONING.md)
- テンプレート思想: [DESIGN.md](DESIGN.md)
- 移行ノート: [docs/migration.md](docs/migration.md)

## ライセンス

MIT License
