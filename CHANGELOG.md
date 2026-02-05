# Changelog

本ファイルは、templarc-docs の重要な変更を記録する。

フォーマットは [Keep a Changelog](https://keepachangelog.com/ja/1.0.0/) に基づく。

## [Unreleased]

### Added

- design/00-format-guide.md（フォーマット規範）
- design/00-getting-started.md（導入手順）
- design/00-template-guide.md（配置ガイド）
- docs/00-user-docs-guide.md（ユーザードキュメント規範）
- design/00-git-guide.md（Git規範）
- DESIGN.md（設計思想）
- docs/（利用者向けドキュメントテンプレート）
- YAML Front Matter を全テンプレートファイルに導入
- 記載規範に分量ガイドライン・文章品質規範・自己完結性規範・冗長性規範を追加
- コミットメッセージ規範・ブランチ命名規則を追加

### Changed

- design/00-writing-guide.md を記載規範（テキスト品質）とフォーマット規範（構造）に分割
- 設計（`design/`）と利用者向け（`docs/`）のドキュメントを分離

### Removed

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
