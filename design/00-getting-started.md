---
depends_on:
  - ./00-index.md
  - ./00-writing-guide.md
  - ./00-format-guide.md
tags: [getting-started, usage, template]
ai_summary: "templarc-docs をプロジェクトへ導入し、最初にやることと運用の要点をまとめた手引き"
---

# はじめに（Getting Started）

> Status: Active
> 最終更新: YYYY-MM-DD

本ドキュメントは、templarc-docs をプロジェクトに導入する手順を示す。
併せて、運用の最小ルールを定義する。

---

## 対象読者

| 読者 | 目的 |
|------|------|
| 設計ドキュメントの作成者 | テンプレートを導入し、最初の下書きを作る |
| レビュワー | 設計変更の差分を追える状態にする |

---

## 導入方法

### GitHubテンプレートとして使用する

```bash
gh repo create my-project-docs --template krtw00/templarc-docs
```

### 手動でコピーする

1. 本リポジトリをクローンする。
2. `design/` を対象リポジトリへコピーする。
3. 利用者向けドキュメントが必要な場合は `docs/` もコピーする。

---

## 最初にやること（チェックリスト）

| # | 作業 | 成果 |
|---:|------|------|
| 1 | `design/00-index.md` を編集する | 目次が機能する |
| 2 | `design/01-overview/summary.md` を埋める | 1枚で全体像を説明できる |
| 3 | `design/01-overview/goals.md` と `scope.md` を埋める | 目的と境界が合意される |
| 4 | 不要なテンプレートを削除する | 読むべき対象が絞られる |
| 5 | 用語を `design/99-appendix/glossary.md` に追加する | 表記ゆれが減る |

---

## 削除してよいテンプレート

不要なテンプレートは削除してよい。
ただし、削除した事実は `design/00-index.md` に反映する。

| ドキュメント | 削除してよい条件 |
|--------------|------------------|
| `design/03-details/api.md` | APIが存在しない |
| `design/03-details/ui.md` | UIが存在しない |
| `design/03-details/data-model.md` | 永続データを持たない |

---

## 運用ルール（最小）

### 更新の順序

設計変更は、実装より先にドキュメントへ反映する。
実装が先行した場合は、同じPRでドキュメントも更新する。

### Status と最終更新

| 項目 | ルール |
|------|--------|
| Status | 合意前は Draft、合意後は Active とする |
| 最終更新 | 内容の変更を伴う更新で日付を更新する |

### 相互参照

参照リンクには、1文の要約を併記する。
詳細は[自己完結性規範](./00-writing-guide.md#参照時の要約)を参照。

---

## 関連ドキュメント

- [00-index.md](./00-index.md) - ドキュメント全体のナビゲーション
- [00-template-guide.md](./00-template-guide.md) - どこに何を書くかの対応表
- [00-user-docs-guide.md](../docs/00-user-docs-guide.md) - 利用者向けドキュメントの書き方
- [00-writing-guide.md](./00-writing-guide.md) - 文章の書き方ルール
- [00-format-guide.md](./00-format-guide.md) - 構造・メタ情報・図・命名規則
- [00-git-guide.md](./00-git-guide.md) - Git運用ルール
- [DESIGN.md](../DESIGN.md) - テンプレートの設計思想
