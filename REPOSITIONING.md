# Repositioning Plan

templarc-docs を、AI向け万能ドキュメント一式ではなく、
使用駆動開発のための軽量テンプレート群へ再定義する。
併せて、AI駆動開発向けの運用テンプレートを別レイヤーで扱う。

## 概要

- `Templarc` はブランド名として維持する
- コア成果物は `templarc-core` として定義する
- AI駆動開発の運用テンプレートは `ai-workflow` として分離する
- 当面は単一リポジトリで管理する
- 配布は package ではなく scaffold 前提で設計する
- 旧テンプレートは移行参照用に `legacy/` へ退避する

## 目的

- 設計テンプレートの責務を絞り、ドキュメント負債を減らす
- AI駆動開発の変化しやすい運用知識を、コアテンプレートから切り離す
- 将来の CLI 化や init コマンド追加に耐える配布単位を作る

## 決定事項

### 1. templarc-core の役割

`templarc-core` は、使用駆動開発のための永続ドキュメントを扱う。
対象は、合意・設計・判断根拠として残す価値があるファイルに限定する。

想定内容:

- `summary`
- `goals`
- `scope`
- `structure`
- `tech-stack`
- `flows`
- `glossary`
- `ADR`

### 2. ai-workflow の役割

`ai-workflow` は、AI駆動開発の実務テンプレートを扱う。
対象は、実際にリポジトリへ展開して使う運用テンプレートである。

想定内容:

- `PROJECT_BRIEF.md`
- `TASK_BRIEF.md`
- `AGENTS.md`
- `PR_CHECKLIST.md`

### 3. コアから外すもの

以下は `templarc-core` の責務から外す。

- 利用者向けドキュメントテンプレート
- Git運用規範
- AIへの依頼方法やレビュー運用の詳細
- 変化の速い作業手順

### 4. リポジトリ方針

現時点では別リポジトリに分割しない。
思想の違いではなく、配布・版管理・利用者の分離が必要になった時点で、
別リポジトリ化を検討する。

## 目標構成

```text
repo/
├── README.md
├── README.ja.md
├── REPOSITIONING.md
├── kits/
│   ├── templarc-core/
│   │   ├── design/
│   │   └── README.md
│   └── ai-workflow/
│       ├── PROJECT_BRIEF.md
│       ├── TASK_BRIEF.md
│       ├── AGENTS.md
│       ├── PR_CHECKLIST.md
│       └── README.md
├── docs/
│   ├── philosophy.md
│   ├── how-to-combine.md
│   └── migration.md
├── legacy/
└── examples/
```

## 現行構成からの対応

| 現行 | 目標 |
|------|------|
| `design/` | `kits/templarc-core/design/` |
| `docs/` の利用者向けテンプレート | `legacy/user-docs-template/` へ退避 |
| `design/00-git-guide.md` | `legacy/governance/00-git-guide.md` へ退避 |
| `README.md` | リポジトリ全体の案内に再編 |
| `DESIGN.md` | テンプレート思想の説明として維持 |

## 段階的移行

### Phase 1: 方針固定

- 本ドキュメントを追加する
- README に新しい方向性を反映する
- 現行構成を即時には壊さない

### Phase 2: 配布単位の分離

- `kits/templarc-core/` を作成する
- `design/` を `templarc-core` 配下へ移す
- `ai-workflow` の初期テンプレートを追加する
- `docs/` をリポジトリ説明用に再編する
- 旧テンプレートを `legacy/` に退避する

### Phase 3: 旧構成の整理

- 旧 `docs/` の位置付けを見直す
- コアと無関係な規範を削除または移動する
- README と導入手順を新構成に合わせる

### Phase 4: scaffold 化

- `init` を意識したテンプレート配置へ整理する
- 必要なら CLI またはスクリプトを追加する

## リスク

- `design/` の規範の一部は、今後 `templarc-core` から削る必要がある
- 旧 `docs/` の扱いを曖昧にしたまま移行すると、再び責務が混ざる
- CLI 化を急ぐと、テンプレート自体の再定義が中途半端になる

## 未決事項

- `00-format-guide.md` と `00-writing-guide.md` のどこまでをコア規範とするか
- `ai-workflow` にレビュー規約まで含めるか、最小テンプレのみに留めるか
