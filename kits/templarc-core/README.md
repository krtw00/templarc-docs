# templarc-core

`templarc-core` は、使用駆動開発のための軽量設計テンプレートである。
合意、設計、判断根拠として残す価値がある文書だけを中核に置く。

## 標準構成

以下を標準セットとする。

- `design/01-overview/summary.md`
- `design/01-overview/goals.md`
- `design/01-overview/scope.md`
- `design/02-architecture/structure.md`
- `design/02-architecture/tech-stack.md`
- `design/03-details/flows.md`
- `design/99-appendix/glossary.md`
- `design/04-decisions/`

## オプション拡張

以下は必要な場合のみ残す。

- `design/02-architecture/context.md`
- `design/03-details/data-model.md`
- `design/03-details/api.md`
- `design/03-details/ui.md`

## コアに含めないもの

以下は `templarc-core` の責務から外した。

- 利用者向けドキュメントテンプレート
- Git運用規範
- AI駆動開発の運用テンプレート

利用者向けドキュメントテンプレートと Git 規範は `legacy/` に残している。
AI駆動開発の運用テンプレートは [`../ai-workflow/README.md`](../ai-workflow/README.md) を参照。

## 使い方

1. `design/` ディレクトリを対象リポジトリへコピーする。
2. `design/00-index.md` と `design/00-getting-started.md` を読む。
3. `summary`, `goals`, `scope`, `structure`, `tech-stack`, `flows` を埋める。
4. 不要なオプション拡張テンプレートを削除する。
5. 重要な判断は `04-decisions/` に ADR として残す。

## 関連ドキュメント

- [design/00-index.md](design/00-index.md) - 設計テンプレート全体の目次
- [design/00-getting-started.md](design/00-getting-started.md) - 導入と最初の運用ルール
- [design/00-template-guide.md](design/00-template-guide.md) - どこに何を書くかの対応表
