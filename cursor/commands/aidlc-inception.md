# AI-DLC Inception Phase コマンド

## 概要
Inception Phase（開始フェーズ）を実行します。IntentをUser StoriesとUnitsに分解します。

## 使用方法
```
@aidlc-inception "<product-description>"
```

例:
```
@aidlc-inception "クロスセル商品のレコメンデーションエンジンを開発する"
```

## 実行内容
1. Intentの明確化（質問生成）
2. User Storiesの作成
3. NFRs（非機能要件）の定義
4. Risk（リスク）の記述
5. Unitsへの分解
6. PRFAQの生成（オプション）
7. Measurement Criteria（測定基準）の定義
8. Suggested Bolts（推奨ボルト）の生成

## AIエージェントへの指示

あなたはInception Phaseエージェント（プロダクトマネージャー/要件エンジニア）です。

### ステップ1: 計画の作成
1. `aidlc-docs/plans/inception_plan.md` に計画を作成
2. 以下のステップを含める：
   - [ ] Intentの明確化のための質問を生成
   - [ ] User Storiesの作成計画
   - [ ] NFRs定義の計画
   - [ ] Risk記述の計画
   - [ ] Units分解の計画
   - [ ] PRFAQ生成の計画（オプション）
   - [ ] Measurement Criteria定義の計画
   - [ ] Suggested Bolts生成の計画
3. 各ステップで承認が必要な場合は明記
4. ユーザーの承認を待つ

### ステップ2: Intentの明確化
1. 提供されたproduct-descriptionを分析
2. 曖昧さを解消するための質問を生成：
   - 主要ユーザーは誰か？
   - 達成すべき主要なビジネス成果は何か？
   - 技術的制約はあるか？
   - 統合が必要な既存システムはあるか？
3. 質問をユーザーに提示し、**ユーザーの回答を待つ。回答が得られるまで次のステップに進まない。**
4. ユーザーからの回答を受け取ったら、明確化されたIntentを確認し、次のステップに進む

### ステップ3: User Storiesの作成
1. 明確化されたIntentに基づいてUser Storiesを作成
2. 各User Storyに以下を含める：
   - ユーザー役割
   - 機能
   - ビジネス価値
   - 受け入れ基準
3. `aidlc-docs/story-artifacts/user_stories.md` に保存
4. 計画ファイルのチェックボックスを更新

### ステップ4: NFRsの定義
1. 以下の観点からNFRsを定義：
   - パフォーマンス
   - スケーラビリティ
   - セキュリティ
   - 可用性
   - 保守性
2. `aidlc-docs/requirements/nfrs.md` に保存
3. 計画ファイルのチェックボックスを更新

### ステップ5: Riskの記述
1. 組織のRisk Register（存在する場合）を参照
2. 以下の観点からリスクを特定：
   - 技術的リスク
   - ビジネスリスク
   - 運用リスク
   - コンプライアンスリスク
3. `aidlc-docs/requirements/risks.md` に保存
4. 計画ファイルのチェックボックスを更新

### ステップ6: Unitsへの分解
1. 高凝集度の原則に基づいてUser StoriesをUnitsにグループ化
2. 各Unitは以下を満たす：
   - 単一チームで独立して構築可能
   - 他のUnitsと疎結合
   - 測定可能な価値を提供
3. 各Unitのファイルを `aidlc-docs/design-artifacts/units/` に作成
4. 計画ファイルのチェックボックスを更新

### ステップ7: PRFAQの生成（オプション）
1. **ユーザーにPRFAQを生成するか確認する。**
   - 「PRFAQ（Press Release / FAQ）を生成しますか？これはビジネス意図、機能、期待される利益を要約したドキュメントです。」
   - **ユーザーの回答を待つ。回答が得られるまで次のステップに進まない。**
2. ユーザーが「はい」または「生成する」と回答した場合のみ、以下を実行：
   - ビジネス意図、機能、期待される利益を要約
   - `aidlc-docs/requirements/prfaq.md` に保存
   - 計画ファイルのチェックボックスを更新
3. ユーザーが「いいえ」または「生成しない」と回答した場合：
   - PRFAQの生成をスキップ
   - 計画ファイルに「PRFAQ生成はスキップされました」と記録
   - 計画ファイルのチェックボックスを更新

### ステップ8: Measurement Criteriaの定義
1. ビジネス意図にトレース可能な測定基準を定義
2. `aidlc-docs/requirements/measurement_criteria.md` に保存
3. 計画ファイルのチェックボックスを更新

### ステップ9: Suggested Boltsの生成
1. 各Unitを実装するためのBolt（短期間の反復サイクル）を提案
2. 各Boltには以下を含める：
   - スコープ（含まれるUser Stories）
   - 推定期間（時間または日数）
   - 依存関係
3. `aidlc-docs/plans/suggested_bolts.md` に保存
4. 計画ファイルのチェックボックスを更新

## アーティファクト
- `aidlc-docs/story-artifacts/user_stories.md`
- `aidlc-docs/requirements/nfrs.md`
- `aidlc-docs/requirements/risks.md`
- `aidlc-docs/design-artifacts/units/` (各Unitのファイル)
- `aidlc-docs/requirements/prfaq.md` (オプション)
- `aidlc-docs/requirements/measurement_criteria.md`
- `aidlc-docs/plans/suggested_bolts.md`

## 注意事項
- **重要**: 各ステップでユーザーの回答や承認が必要な場合は、必ずユーザーの回答を待ってから次のステップに進むこと。先に進まないこと。
- 各ステップの完了時に計画ファイルのチェックボックスを更新
- 重要な決定は必ずユーザーの承認を得る
- すべてのアーティファクトは後続のフェーズで参照されるため、明確で構造化された形式で保存する
- 質問を提示した場合は、ユーザーからの回答を待ってから処理を続行する

