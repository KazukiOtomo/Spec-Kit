# Feature Specification: 技術経歴書アプリケーション

**Feature Branch**: `001-os`
**Created**: 2025-09-06
**Status**: Draft
**Input**: User description: "技術経歴書を書くためのアプリケーションを作成したい。ユーザは、業種、業務名、担当業務内容、作業期間、担当ポジション、OS/使用ツール、言語/フレームワークなどの、経験した内容を入力できるようにします。できるだけ、入力負担を下げるために自由入力を減らしたい。"

## Execution Flow (main)

```
1. Parse user description from Input
   → If empty: ERROR "No feature description provided"
2. Extract key concepts from description
   → Identify: actors, actions, data, constraints
3. For each unclear aspect:
   → Mark with [NEEDS CLARIFICATION: specific question]
4. Fill User Scenarios & Testing section
   → If no clear user flow: ERROR "Cannot determine user scenarios"
5. Generate Functional Requirements
   → Each requirement must be testable
   → Mark ambiguous requirements
6. Identify Key Entities (if data involved)
7. Run Review Checklist
   → If any [NEEDS CLARIFICATION]: WARN "Spec has uncertainties"
   → If implementation details found: ERROR "Remove tech details"
8. Return: SUCCESS (spec ready for planning)
```

---

## 1. Feature Overview

技術経歴書（職務経歴書）を作成するための Web アプリケーション。ユーザは自身の職務経験を体系的に入力・管理できる。

## 2. Actors

- ユーザ（技術者、エンジニア）

## 3. Actions

- 経験内容の入力（業種、業務名、担当業務内容、作業期間、担当ポジション、OS/使用ツール、言語/フレームワーク等）
- 経歴の編集・削除
- 経歴の一覧表示

## 4. Data

- 業種（選択式リスト）
- 業務名（選択式リスト）
- 担当業務内容（選択式リスト＋補足自由記述）
- 作業期間（年月選択）
- 担当ポジション（選択式リスト）
- OS/使用ツール（選択式リスト＋補足自由記述）
- 言語/フレームワーク（選択式リスト＋補足自由記述）
- [NEEDS CLARIFICATION]選択肢リストの初期値はどのように決定するか？

## 5. Constraints

- 入力負担を減らすため、できるだけ選択式（プルダウンやチェックボックス）を活用
- 必須項目と任意項目の区分
- ユーザ認証は必要か？
- [NEEDS CLARIFICATION]複数経歴の管理方法方法はどうするか？

## 6. User Scenarios & Testing

- ユーザが新規経歴を追加し、必要項目を選択・入力できる
- 入力した経歴を一覧で確認・編集・削除できる
- 経歴書としてダウンロードできる
- [NEEDS CLARIFICATION]モバイル対応は必須か？

## 7. Functional Requirements

- 選択式 UI による経歴情報の入力
- 経歴情報の編集・削除
- 経歴情報の一覧表示
- [NEEDS CLARIFICATION]データ保存方法はどうするか？

## 8. Key Entities

- 経歴（Experience）
  - 業種
  - 業務名
  - 担当業務内容
  - 作業期間
  - 担当ポジション
  - OS/使用ツール
  - 言語/フレームワーク
- [NEEDS CLARIFICATION]ユーザー管理は必要か？

## 9. Review Checklist

- [x] 仕様に曖昧な点は[NEEDS CLARIFICATION]で明示
- [x] 実装方法や技術スタックは記載していない
- [x] すべての要件はテスト可能な形で記載
- [x] 必須・任意項目の区分は明示
- [x] UI/UX に関する要件は抽象的に記載

---
