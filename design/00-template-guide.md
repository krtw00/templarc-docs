---
depends_on:
  - ./00-index.md
  - ./00-getting-started.md
  - ./00-writing-guide.md
  - ./00-format-guide.md
tags: [guide, template, navigation, workflow]
ai_summary: "設計の内容ごとに、どのドキュメントへ何を書くかと、変更時に更新すべきファイルを対応付けるガイド"
---

# テンプレートガイド（どこに何を書くか）

> Status: Active
> 最終更新: YYYY-MM-DD

本ドキュメントは、内容と配置先ドキュメントを対応付ける。
設計変更時に更新すべきファイルも示す。

---

## どこに何を書くか

| 書く内容 | ドキュメント | 補足 |
|----------|--------------|------|
| 1枚で分かる全体像 | [summary.md](./01-overview/summary.md) | 最初に埋める |
| 目的、課題、成功基準 | [goals.md](./01-overview/goals.md) | 非目標も明記する |
| 対象範囲、対象外、フェーズ | [scope.md](./01-overview/scope.md) | 境界の合意に使う |
| システム境界と外部連携 | [context.md](./02-architecture/context.md) | Context図を置く |
| 主要コンポーネントと責務 | [structure.md](./02-architecture/structure.md) | Container相当でまとめる |
| 技術選定と理由 | [tech-stack.md](./02-architecture/tech-stack.md) | 重要判断はADRで根拠を残す |
| データモデルと状態遷移 | [data-model.md](./03-details/data-model.md) | 永続化しないなら削除してよい |
| API仕様 | [api.md](./03-details/api.md) | APIがないなら削除してよい |
| UI仕様 | [ui.md](./03-details/ui.md) | UIがないなら削除してよい |
| 主要フローと例外 | [flows.md](./03-details/flows.md) | 実装に近い参照点になる |
| 重要な決定と理由 | [04-decisions/](./04-decisions/) | ADRとして独立させる |
| 利用者向けの使い方 | [docs/](../docs/) | 目的別（Quickstart/How-to/Reference）で分ける |
| 用語定義 | [glossary.md](./99-appendix/glossary.md) | 表記ゆれを防ぐ |

---

## 変更パターン別の更新先

| 変更 | 更新するドキュメント | 補足 |
|------|----------------------|------|
| スコープの追加/削除 | [scope.md](./01-overview/scope.md) | 目的との整合も確認する |
| 成功基準の変更 | [goals.md](./01-overview/goals.md) | 指標と目標値を更新する |
| 外部サービス追加 | [context.md](./02-architecture/context.md) | 境界と責務も更新する |
| コンポーネント分割 | [structure.md](./02-architecture/structure.md) | 依存関係の説明も更新する |
| 技術の採用/撤回 | [tech-stack.md](./02-architecture/tech-stack.md) / [04-decisions/](./04-decisions/) | 重大ならADRを書く |
| 新しいエンティティ追加 | [data-model.md](./03-details/data-model.md) | フロー・APIの影響も確認する |
| APIの追加/変更 | [api.md](./03-details/api.md) / [flows.md](./03-details/flows.md) | 主要フローに影響を書く |
| 画面追加/遷移変更 | [ui.md](./03-details/ui.md) / [flows.md](./03-details/flows.md) | 画面とフローを両方更新する |
| 用語の導入/改名 | [glossary.md](./99-appendix/glossary.md) | 既存表記を置換する |

---

## テンプレートを増やす手順

1. 新しいファイルを作成する。
2. YAML Front Matter と Status/最終更新を付与する。
3. `design/00-index.md` にリンクを追加する。
4. 関連ドキュメントを相互リンクする。

フォーマットは[フォーマット規範](./00-format-guide.md)を参照。

---

## 関連ドキュメント

- [00-getting-started.md](./00-getting-started.md) - 導入手順と運用の最小ルール
- [00-index.md](./00-index.md) - ドキュメント全体のナビゲーション
- [00-user-docs-guide.md](../docs/00-user-docs-guide.md) - ユーザードキュメントの書き方
- [00-writing-guide.md](./00-writing-guide.md) - 文章の書き方ルール
- [00-format-guide.md](./00-format-guide.md) - 構造・メタ情報・図・命名規則
