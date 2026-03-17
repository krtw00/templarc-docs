# Changelog

本ファイルは、templarc-docs の重要な変更を記録する。

フォーマットは [Keep a Changelog](https://keepachangelog.com/ja/1.0.0/) に基づく。

## [Unreleased]

### Added

- REPOSITIONING.md（再配置方針と移行段階）
- kits/templarc-core/README.md（コアキット概要）
- kits/ai-workflow/README.md（AIワークフローキット概要）
- kits/ai-workflow/PROJECT_BRIEF.md（プロジェクト前提共有テンプレート）
- kits/ai-workflow/TASK_BRIEF.md（個別タスク共有テンプレート）
- kits/ai-workflow/AGENTS.md（AIエージェント向けルールテンプレート）
- kits/ai-workflow/PR_CHECKLIST.md（PR確認テンプレート）
- docs/philosophy.md（キット分離の思想）
- docs/how-to-combine.md（templarc-core と ai-workflow の併用方法）
- docs/migration.md（旧構成からの移行ノート）
- legacy/README.md（legacy 配下の説明）
- examples/ai-workflow/*.example.md（ai-workflow の記入例）
- design/00-format-guide.md（フォーマット規範）
- design/00-getting-started.md（導入手順）
- design/00-template-guide.md（配置ガイド）
- docs/00-user-docs-guide.md（ユーザードキュメント規範）
- DESIGN.md（設計思想）
- docs/（利用者向けドキュメントテンプレート）
- YAML Front Matter を全テンプレートファイルに導入
- 記載規範に分量ガイドライン・文章品質規範・自己完結性規範・冗長性規範を追加
- コミットメッセージ規範・ブランチ命名規則を追加

### Changed

- README.md と README.ja.md に再整理方針を追加
- リポジトリ構成を `kits/`, `docs/`, `legacy/`, `examples/` に再編
- `ai-workflow` のテンプレートを実運用向けに具体化
- design/00-writing-guide.md を記載規範（テキスト品質）とフォーマット規範（構造）に分割
- 設計（`design/`）と利用者向け（`docs/`）のドキュメントを分離

### Removed

- `templarc-core` から Git規範を分離
- `templarc-core` から利用者向けドキュメントテンプレートを分離
- README.md から参考フレームワークセクションを削除

## [1.0.0] - YYYY-MM-DD

### Added

- 初期テンプレート構造
  - 00-index.md（ナビゲーション）
  - 00-writing-guide.md（記載規範）
  - 01-overview/（概要セクション）
  - 02-architecture/（設計セクション）
  - 03-details/（詳細セクション）
  - 04-decisions/（ADRセクション）
  - 99-appendix/（付録）
- GitHub関連ファイル
  - Issue テンプレート（バグ報告、機能リクエスト）
  - PR テンプレート
- README.md
- LICENSE（MIT）
