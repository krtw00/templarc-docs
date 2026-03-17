# ai-workflow

`ai-workflow` は、AI駆動開発の実務テンプレート群である。
設計を残す `templarc-core` とは役割を分け、作業指示、分担、検証、レビューの流れを扱う。

## 想定する運用

`ai-workflow` は、以下のような現場を想定する。

- 安定した設計は `templarc-core` に残す
- 実装作業は issue やタスク単位で進める
- AI には毎回必要最小限のコンテキストを渡す
- 人間は受け入れ条件、仕様解釈、最終レビューを握る

## 推奨配置

テンプレートは、対象リポジトリのルートまたは `.project/` 配下に置く。
最小構成は以下である。

```text
repo/
├── AGENTS.md
├── PROJECT_BRIEF.md
├── work/
│   └── TASK_BRIEF-<task>.md
└── docs/ or design/
```

## 含まれるテンプレート

| ファイル | 目的 |
|----------|------|
| `PROJECT_BRIEF.md` | プロジェクト全体の前提、目的、制約を AI と共有する |
| `TASK_BRIEF.md` | 個別タスクの目的、変更範囲、受け入れ条件を固定する |
| `AGENTS.md` | AI エージェントへの恒常的な実行ルールを定義する |
| `PR_CHECKLIST.md` | 変更確認とレビュー観点を揃える |

## いつ使うか

| タイミング | 使うファイル |
|------------|--------------|
| プロジェクト開始時 | `PROJECT_BRIEF.md` |
| AI への共通ルールを決める時 | `AGENTS.md` |
| 実装タスクを切る時 | `TASK_BRIEF.md` |
| レビュー前の最終確認 | `PR_CHECKLIST.md` |

## 基本フロー

1. `templarc-core` で安定した設計情報を残す。
2. `PROJECT_BRIEF.md` にプロジェクト全体の文脈をまとめる。
3. `AGENTS.md` に AI が毎回守るルールを書く。
4. 個別作業ごとに `TASK_BRIEF.md` を作る。
5. AI には `AGENTS.md` と `TASK_BRIEF.md` を優先コンテキストとして渡す。
6. 変更前に受け入れ条件を確認し、変更後は `PR_CHECKLIST.md` で検証する。

## 最小運用ルール

- `PROJECT_BRIEF.md` はプロジェクト単位で 1 つに保つ
- `TASK_BRIEF.md` は 1 タスク 1 ファイルにする
- `受け入れ条件` が書けないタスクは AI に渡さない
- `実行コマンド` がない変更は、理由を明示する
- 仕様変更がある場合は、コードと同じ変更セットで文書も更新する

## よくある失敗

| 失敗 | 回避方法 |
|------|----------|
| `TASK_BRIEF.md` が大きすぎる | 1タスク1責務に分ける |
| `AGENTS.md` が抽象的すぎる | 禁止事項、優先順位、報告形式を書く |
| AI に全ファイルを読ませる | `PROJECT_BRIEF.md` と必要な設計資料に絞る |
| PR で仕様変更が説明されない | `PR_CHECKLIST.md` の確認項目に含める |

## 記入例

サンプルは [`../../examples/ai-workflow/`](../../examples/ai-workflow/) を参照。

## 関連ドキュメント

- [../templarc-core/README.md](../templarc-core/README.md) - 永続設計テンプレートの説明
- [../../docs/how-to-combine.md](../../docs/how-to-combine.md) - 2つのキットの組み合わせ方
