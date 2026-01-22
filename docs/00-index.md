# ドキュメントインデックス

> Status: Active
> 最終更新: YYYY-MM-DD

本ドキュメントは、設計ドキュメント全体のナビゲーションを提供する。

---

## ドキュメント構造

```mermaid
flowchart LR
    A[01-overview<br/>全体像] --> B[02-architecture<br/>設計]
    B --> C[03-details<br/>詳細]
    C --> D[04-decisions<br/>決定記録]
```

| レベル | 目的 | 対象読者 |
|--------|------|----------|
| **01-overview** | 何を作るか、なぜ作るか | 初見・思い出し用 |
| **02-architecture** | どう構成するか | 設計理解 |
| **03-details** | 具体的な仕様 | 実装時参照 |
| **04-decisions** | なぜその選択をしたか | 判断根拠 |

---

## ドキュメント一覧

### 00 - メタドキュメント

| ドキュメント | 説明 |
|--------------|------|
| [00-index.md](./00-index.md) | 本ドキュメント。全体ナビゲーション |
| [00-writing-guide.md](./00-writing-guide.md) | 記載規範 |

### 01 - Overview（全体像）

| ドキュメント | 説明 |
|--------------|------|
| [summary.md](./01-overview/summary.md) | プロジェクト概要（1枚で全体把握） |
| [goals.md](./01-overview/goals.md) | 目的・解決する課題 |
| [scope.md](./01-overview/scope.md) | スコープ・対象外 |

### 02 - Architecture（設計）

| ドキュメント | 説明 |
|--------------|------|
| [context.md](./02-architecture/context.md) | システム境界・外部連携 |
| [structure.md](./02-architecture/structure.md) | 主要コンポーネント構成 |
| [tech-stack.md](./02-architecture/tech-stack.md) | 技術スタック |

### 03 - Details（詳細）

| ドキュメント | 説明 |
|--------------|------|
| [data-model.md](./03-details/data-model.md) | データモデル・ER図 |
| [api.md](./03-details/api.md) | API設計（オプション） |
| [ui.md](./03-details/ui.md) | UI設計（オプション） |
| [flows.md](./03-details/flows.md) | 主要フロー・シーケンス |

### 04 - Decisions（決定記録）

| ドキュメント | 説明 |
|--------------|------|
| [0001-template.md](./04-decisions/0001-template.md) | ADRテンプレート |

### 99 - Appendix（付録）

| ドキュメント | 説明 |
|--------------|------|
| [glossary.md](./99-appendix/glossary.md) | 用語集 |

---

## 読み方ガイド

### 初めて読む場合

1. [summary.md](./01-overview/summary.md) - プロジェクト概要を把握
2. [goals.md](./01-overview/goals.md) - 目的を理解
3. [context.md](./02-architecture/context.md) - システム境界を確認

### 設計を理解したい場合

1. [structure.md](./02-architecture/structure.md) - コンポーネント構成
2. [tech-stack.md](./02-architecture/tech-stack.md) - 技術選定理由
3. [04-decisions/](./04-decisions/) - 設計判断の根拠

### 実装時に参照する場合

1. [data-model.md](./03-details/data-model.md) - データ構造
2. [flows.md](./03-details/flows.md) - 処理フロー
3. [glossary.md](./99-appendix/glossary.md) - 用語確認

---

## 関連ドキュメント

- [00-writing-guide.md](./00-writing-guide.md) - 記載規範
