# How To Combine

`templarc-core` と `ai-workflow` は、同じリポジトリ内で併用する前提で設計する。

## 推奨手順

1. `templarc-core` の `design/` を導入する
2. `summary`, `goals`, `scope`, `structure`, `tech-stack`, `flows` を埋める
3. `ai-workflow` の `PROJECT_BRIEF.md` を作る
4. `AGENTS.md` に共通ルールを書く
5. タスクごとに `TASK_BRIEF.md` を切る
6. AI には `AGENTS.md` と `TASK_BRIEF.md` を渡して作業させる
7. 変更後は `PR_CHECKLIST.md` で検証する

## 実務での分担

| 役割 | 主に持つもの |
|------|--------------|
| 人間 | 目的、非ゴール、受け入れ条件、最終判断 |
| AI | 実装、調査、下書き、検証結果の整理 |
| `templarc-core` | 安定した設計と意思決定 |
| `ai-workflow` | 実行ルールとタスク進行 |

## タスクの切り方

- `TASK_BRIEF.md` は 1 タスク 1 責務にする
- 受け入れ条件が 4-6 個程度で収まる粒度にする
- 変更対象ファイルが広すぎる場合はタスクを分割する
- 仕様変更と単純実装は分ける

## 実装前に最低限決めること

- 何を変えるか
- 何を変えないか
- どの文書が真実の源泉か
- 何をもって完了とするか
- どう検証するか

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
- 受け入れ条件が空のまま AI に丸投げする
