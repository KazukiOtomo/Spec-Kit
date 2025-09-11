# Tasks: プログラミング言語・フレームワーク習熟度入力機能

**Input**: Design documents from `/specs/002-force/`
**Prerequisites**: plan.md (required)

## Execution Flow (main)

// ...existing code...

## Phase 3.1: Setup

- [ ] T001 backend/・frontend/・Dockerfile・nginx.conf など、プロジェクト構造を作成
- [ ] T002 backend: Laravel プロジェクト初期化・必要パッケージ追加
- [ ] T003 frontend: Vue.js プロジェクト初期化・必要パッケージ追加
- [ ] T004 [P] Docker 環境構築（MySQL・Nginx 含む）
- [ ] T005 [P] Lint・フォーマットツール設定（PHP, JS）

## Phase 3.2: Tests First (TDD)

- [ ] T006 backend/tests: 習熟度モデルのテスト作成
- [ ] T007 backend/tests: API コントラクトテスト（習熟度登録・取得・編集・削除）
- [ ] T008 frontend/tests: 習熟度入力 UI のテスト作成
- [ ] T009 frontend/tests: チェックボックス選択 UI のテスト作成

## Phase 3.3: Core Implementation

- [ ] T010 backend/src: 習熟度モデル・マイグレーション作成
- [ ] T011 backend/src: 習熟度 API コントローラ・ルート作成
- [ ] T012 frontend/src: 習熟度入力 UI（チェックボックス選択式）作成
- [ ] T013 frontend/src: 実績記述 UI 作成

## Phase 3.4: Integration

- [ ] T014 backend/src: MySQL 接続・データ保存実装
- [ ] T015 backend/src: Nginx 設定（API/フロント分離）
- [ ] T016 frontend/src: API 連携（習熟度データ取得・送信）

## Phase 3.5: Polish

- [ ] T017 backend/tests: 単体テスト追加
- [ ] T018 frontend/tests: 単体テスト追加
- [ ] T019 ドキュメント作成（セットアップ・利用方法）

## Parallel Execution Examples

- T004, T005 は同時実行可能 [P]
- T006, T007, T008, T009 はテストファイルが分かれていれば同時実行可能 [P]

## Dependency Notes

- T001→T002,T003→T004,T005
- T006,T007,T008,T009→T010,T011,T012,T013
- T010→T014,T015
- T012→T016
- T017,T018,T019 は最終仕上げ

---
