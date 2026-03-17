---
depends_on:
  - ../02-architecture/structure.md
  - ./data-model.md
tags: [details, api, endpoints, rest]
ai_summary: "APIエンドポイント一覧・リクエスト/レスポンス仕様・認証・エラー形式を定義"
---

# API設計

> Status: Draft
> 最終更新: YYYY-MM-DD

本ドキュメントは、システムのAPI設計を定義する。

※ APIを持たないプロジェクトの場合、本ドキュメントは削除可。

---

## API概要

| 項目 | 内容 |
|------|------|
| ベースURL | `https://api.example.com/v1` |
| 認証方式 | {Bearer Token / API Key / etc} |
| レスポンス形式 | JSON |

---

## エンドポイント一覧

| メソッド | パス | 説明 |
|----------|------|------|
| GET | `/resources` | リソース一覧取得 |
| GET | `/resources/:id` | リソース詳細取得 |
| POST | `/resources` | リソース作成 |
| PUT | `/resources/:id` | リソース更新 |
| DELETE | `/resources/:id` | リソース削除 |

---

## エンドポイント詳細

### GET /resources

リソースの一覧を取得する。

#### リクエスト

| パラメータ | 位置 | 型 | 必須 | 説明 |
|------------|------|-----|------|------|
| page | query | number | - | ページ番号（デフォルト: 1） |
| limit | query | number | - | 取得件数（デフォルト: 20） |
| status | query | string | - | ステータスでフィルタ |

#### レスポンス

| ステータス | 説明 |
|------------|------|
| 200 | 成功 |
| 401 | 認証エラー |
| 500 | サーバーエラー |

### POST /resources

リソースを作成する。

#### リクエスト

| パラメータ | 位置 | 型 | 必須 | 説明 |
|------------|------|-----|------|------|
| name | body | string | ○ | リソース名 |
| description | body | string | - | 説明 |

#### レスポンス

| ステータス | 説明 |
|------------|------|
| 201 | 作成成功 |
| 400 | バリデーションエラー |
| 401 | 認証エラー |
| 500 | サーバーエラー |

---

## 共通仕様

### 認証

<!-- 認証方式の説明 -->

| 項目 | 内容 |
|------|------|
| 認証ヘッダー | `Authorization: Bearer {token}` |
| トークン取得 | {取得方法} |
| 有効期限 | {期限} |

### エラーレスポンス

<!-- 共通エラーフォーマット -->

| フィールド | 型 | 説明 |
|------------|-----|------|
| error.code | string | エラーコード |
| error.message | string | エラーメッセージ |

### ページネーション

<!-- ページネーションの仕様 -->

| フィールド | 型 | 説明 |
|------------|-----|------|
| data | array | データ配列 |
| meta.total | number | 総件数 |
| meta.page | number | 現在ページ |
| meta.limit | number | 1ページの件数 |

---

## 関連ドキュメント

- [data-model.md](./data-model.md) - データモデル
- [flows.md](./flows.md) - 主要フロー
