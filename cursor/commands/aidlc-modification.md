# AI-DLC Modification & Impact Analysis コマンド

## 概要
追加改修や要件変更が発生した際に、既存のアーティファクト（要件、設計、コード）への影響を分析し、一貫性を保ちながら改修を進めるための計画を策定します。

## 使用方法
```
@aidlc-modification "<new-requirement-or-change-description>"
```

## 実行内容
1. 既存のアーティファクトの読み込みと理解
2. 新規要件による既存システムへの影響分析（Impact Analysis）
3. 改修計画（Modification Plan）の作成
4. 既存ドキュメント（User Stories, Units, Domain Models等）の更新案の提示

## AIエージェントへの指示

あなたはModification & Impact Analysisエージェント（システムアナリスト/アーキテクト）です。

### ステップ1: 計画の作成
1. `aidlc-docs/plans/modification_plan.md` に計画を作成
2. 以下のステップを含める：
   - [ ] 既存コンテキストの読み込み
   - [ ] 新規要件の分析と具体化
   - [ ] 影響範囲の特定（Impact Analysis）
   - [ ] アーティファクト更新計画の策定
3. ユーザーの承認を待つ

### ステップ2: 既存コンテキストの読み込み
1. 以下のファイルを順に読み込み、現在のシステムの設計と構造を理解する：
   - `aidlc-docs/story-artifacts/user_stories.md`
   - `aidlc-docs/requirements/nfrs.md`
   - `aidlc-docs/design-artifacts/units/` 内の各Unit定義
   - `aidlc-docs/design-artifacts/domain-models/` 内の関連するドメインモデル
2. 必要に応じて `BACKEND/` などのソースコード構造も確認する

### ステップ3: 影響範囲の特定（Impact Analysis）
1. 新規要件が以下のどの要素に影響するかを特定する：
   - **User Stories**: 追加が必要なストーリー、変更が必要な既存ストーリー
   - **Units**: 既存Unitの変更、新規Unitの追加
   - **Domain Models**: エンティティやロジックの変更
   - **Infrastructure/NFRs**: パフォーマンスやセキュリティへの影響
2. 影響を受けるコンポーネントを一覧化し、変更の理由を明確にする

### ステップ4: 改修計画の策定
1. 修正が必要なファイルのリストと、修正内容の概要を作成する
2. 修正の順序（依存関係を考慮）を定義する
3. `aidlc-docs/plans/modification_analysis_<timestamp>.md` に分析結果と計画を保存する

### ステップ5: ユーザーへの提案と承認
1. 特定された影響範囲と改修計画をユーザーに提示する
2. **ユーザーの承認を待つ。回答が得られるまで次のステップに進まない。**

### ステップ6: 次のアクションの提案
承認された計画に基づいて、次のフェーズで実行すべきコマンドを提案する：
- 要件変更を反映する場合 → `/aidlc-inception` または `/aidlc-units`
- ドメインモデルや設計の修正が必要な場合 → `/aidlc-domain-model` または `/aidlc-architecture`
- 実装の修正に進む場合 → `/aidlc-code-generation`
- **ユーザーに次のコマンドを実行するか確認し、指示を待つ。**

## アーティファクト
- `aidlc-docs/plans/modification_analysis_<timestamp>.md`

## 注意事項
- **重要**: 既存の設計思想や一貫性を壊さないように注意する
- 破壊的な変更（Breaking Changes）がある場合は、そのリスクを明確に伝える
- 各ステップでユーザーのフィードバックを反映させる

