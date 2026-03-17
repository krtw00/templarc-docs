# ai-workflow

`ai-workflow` は、AI駆動開発の実務テンプレート群である。
設計を残す `templarc-core` とは役割を分け、作業指示、分担、検証、レビューの流れを扱う。

## 含まれるテンプレート

| ファイル | 目的 |
|----------|------|
| `PROJECT_BRIEF.md` | プロジェクト全体の前提、目的、制約を AI と共有する |
| `TASK_BRIEF.md` | 個別タスクの目的、変更範囲、受け入れ条件を固定する |
| `AGENTS.md` | AI エージェントへの恒常的な実行ルールを定義する |
| `PR_CHECKLIST.md` | 変更確認とレビュー観点を揃える |

## 基本フロー

1. `templarc-core` で安定した設計情報を残す。
2. `PROJECT_BRIEF.md` にプロジェクト全体の文脈をまとめる。
3. 個別作業ごとに `TASK_BRIEF.md` を作る。
4. AI には `AGENTS.md` と `TASK_BRIEF.md` を優先コンテキストとして渡す。
5. 変更前に受け入れ条件を確認し、変更後は `PR_CHECKLIST.md` で検証する。

## 関連ドキュメント

- [../templarc-core/README.md](../templarc-core/README.md) - 永続設計テンプレートの説明
- [../../docs/how-to-combine.md](../../docs/how-to-combine.md) - 2つのキットの組み合わせ方
