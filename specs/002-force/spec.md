# Feature Specification: プログラミング言語・フレームワーク習熟度入力機能

**Feature Branch**: `002-force`
**Created**: 2025-09-09
**Status**: Draft
**Input**: User description: "各プログラミング言語やフレームワークの習熟度は経験年数だけでは分かりにくい。自己評価や具体的な実績、レベル選択などで入力できるようにしたい。"

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

各プログラミング言語やフレームワークの習熟度を、経験年数以外の指標（自己評価、レベル選択、具体的な実績記述等）で入力できる機能を追加する。

## 2. Actors

- ユーザ（技術者、エンジニア）

## 3. Actions

- 習熟度の入力（自己評価、レベル選択、実績記述）
- 習熟度の編集・削除
- 習熟度の一覧表示

## 4. Data

- プログラミング言語・フレームワーク名（選択式リスト）
- 習熟度（例：5 段階評価、自己記述、実績 URL 等）
- 経験年数
- 実績記述例（例：Node.js の場合 → nodenv/nodenv などのバージョン管理ツール利用経験、npm scripts の理解、gulp.js 利用経験、gulpfile.js を一から作成した経験など）
- 習熟度・実績の入力は、チェックボックスで選択できる項目として各言語・フレームワークごとに用意する
- [NEEDS CLARIFICATION: 習熟度の評価基準はどうするか？（例：初心者〜エキスパート、自己記述、実績 URL 添付など）]

## 5. Constraints

- 習熟度の入力方法は選択式＋自由記述を併用
- 習熟度・実績の入力はチェックボックス選択式で、各言語・フレームワークごとに用意する
- 必須項目と任意項目の区分
- [NEEDS CLARIFICATION: 習熟度の自己評価はどのような UI で実現するか？]
- [NEEDS CLARIFICATION: 習熟度の公開範囲（全体/限定/非公開）は？]

## 6. User Scenarios & Testing

- ユーザが自身の言語・フレームワークごとに習熟度を入力できる
- Node.js の習熟度入力例：nodenv 利用経験、npm scripts 理解、gulp.js 利用経験、gulpfile.js 作成経験などを記述できる
- 入力した習熟度を一覧で確認・編集・削除できる
- [NEEDS CLARIFICATION: 習熟度情報のエクスポート・共有機能は必要か？]

## 7. Functional Requirements

- 習熟度入力 UI（選択式＋自由記述）
- 習熟度情報の編集・削除
- 習熟度情報の一覧表示
- [NEEDS CLARIFICATION: 習熟度情報の保存方法（ローカル/クラウド/ファイル出力のみ等）]

## 8. Key Entities

- 習熟度（Proficiency）
  - プログラミング言語・フレームワーク名
  - 習熟度
  - 経験年数
  - 実績 URL 等
- ユーザ（[NEEDS CLARIFICATION: ユーザ管理の有無]）

## 9. Review Checklist

- [x] 仕様に曖昧な点は[NEEDS CLARIFICATION]で明示
- [x] 実装方法や技術スタックは記載していない
- [x] すべての要件はテスト可能な形で記載
- [x] 必須・任意項目の区分は明示
- [x] UI/UX に関する要件は抽象的に記載

---
