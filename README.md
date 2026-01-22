# templarc-docs

設計ドキュメントテンプレート - Design Document Template

## 概要

templarc-docs は、ソフトウェアプロジェクトの設計ドキュメントを作成するためのテンプレートである。

### 特徴

- **基本→詳細のフロー構造**: 概要から詳細へ段階的に読み進められる
- **GitHub特化**: Issue/PRテンプレート、Markdown形式
- **AI可読性**: Mermaid図、明確な構造でAIが理解しやすい
- **汎用性**: あらゆるプロジェクトで使用可能

## 構造

```
docs/
├── 00-index.md              # ナビゲーション
├── 00-writing-guide.md      # 記載規範
├── 01-overview/             # 基本（全体像）
│   ├── summary.md
│   ├── goals.md
│   └── scope.md
├── 02-architecture/         # 設計（中間）
│   ├── context.md
│   ├── structure.md
│   └── tech-stack.md
├── 03-details/              # 詳細
│   ├── data-model.md
│   ├── api.md
│   ├── ui.md
│   └── flows.md
├── 04-decisions/            # 決定記録（ADR）
│   └── 0001-template.md
└── 99-appendix/
    └── glossary.md          # 用語集
```

## 使い方

### 1. テンプレートとして使用

```bash
gh repo create my-project-docs --template krtw00/templarc-docs
```

### 2. 手動でコピー

1. このリポジトリをクローン
2. `docs/` ディレクトリを自分のプロジェクトにコピー
3. 各テンプレートの `{プレースホルダー}` を実際の内容に置き換え

## 読み方

```mermaid
flowchart LR
    A[01-overview<br/>全体像] --> B[02-architecture<br/>設計]
    B --> C[03-details<br/>詳細]
    C --> D[04-decisions<br/>決定記録]
```

| レベル | 目的 |
|--------|------|
| **01-overview** | 何を作るか、なぜ作るか |
| **02-architecture** | どう構成するか |
| **03-details** | 具体的な仕様 |
| **04-decisions** | なぜその選択をしたか |

## 記載規範

詳細は [docs/00-writing-guide.md](docs/00-writing-guide.md) を参照。

### 主なルール

- **コード禁止**: 設計ドキュメントにコードは記載しない
- **図の積極活用**: Mermaid記法で視覚化
- **What/Why優先**: 「何を・なぜ」を書く

## 参考にしたフレームワーク

| フレームワーク | 採用した要素 |
|----------------|--------------|
| arc42 | セクション構造 |
| Diátaxis | ドキュメント分類の考え方 |
| ADR | 決定記録フォーマット |
| GitHub標準 | Issue/PRテンプレート |

## ライセンス

MIT License
