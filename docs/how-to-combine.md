# How To Combine

`templarc-core` と `ai-workflow` は、同じリポジトリ内で併用する前提で設計する。

## 推奨手順

1. `templarc-core` の `design/` を導入する
2. `summary`, `goals`, `scope`, `structure`, `tech-stack`, `flows` を埋める
3. `ai-workflow` の `PROJECT_BRIEF.md` を作る
4. タスクごとに `TASK_BRIEF.md` を切る
5. AI には `AGENTS.md` と `TASK_BRIEF.md` を渡して作業させる
6. 変更後は `PR_CHECKLIST.md` で検証する

## 使い分け

| 場面 | 使うもの |
|------|----------|
| プロジェクト全体の目的整理 | `templarc-core` |
| 個別タスクの実行指示 | `ai-workflow` |
| 重要判断の記録 | `templarc-core` の ADR |
| レビューと検証 | `ai-workflow` |

## 避けること

- 一時的な作業メモを `templarc-core` に残す
- AI への細かい運用ルールを設計テンプレートへ混ぜる
- 実装済みコードより古い仕様文書を放置する
