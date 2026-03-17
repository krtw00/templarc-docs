# Migration

旧 `templarc-docs` から現在の構成への移行方針をまとめる。

## 主要な変更

| 旧パス | 新しい位置付け |
|--------|----------------|
| `design/` | `kits/templarc-core/design/` |
| `docs/` 利用者向けテンプレート | `legacy/user-docs-template/` |
| `design/00-git-guide.md` | `legacy/governance/00-git-guide.md` |

## 意図

- `templarc-core` は使用駆動開発のコアに絞る
- 利用者向けドキュメントテンプレートはコアから外す
- Git 規範は設計テンプレートから外す
- AI駆動開発の運用は `kits/ai-workflow/` に寄せる

## 移行時の注意

- 旧パスへの参照リンクは新しい位置に更新する
- `design/` を直接参照していた README や PR テンプレートは修正する
- 旧 `docs/` は legacy 扱いであり、新規採用は推奨しない
