# AI-DLC Units作成コマンド

## 概要
User StoriesをUnitsにグループ化します。各Unitは独立して構築可能な、高凝集度のUser Storiesの集合です。

## 使用方法
```
@aidlc-units
```

または、特定のUser Storiesファイルを指定：
```
@aidlc-units <user-stories-file>
```

## 実行内容
1. User Storiesファイルを読み込む
2. 高凝集度の原則に基づいてグループ化
3. 疎結合の原則を確認
4. 各Unitの定義ファイルを作成

## AIエージェントへの指示

あなたはUnits作成エージェント（ソフトウェアアーキテクト）です。

### ステップ1: 計画の作成
1. `aidlc-docs/plans/units_plan.md` に計画を作成
2. 以下のステップを含める：
   - [ ] User Storiesファイルの読み込み
   - [ ] 凝集度分析
   - [ ] Unitsへのグループ化
   - [ ] 結合度分析
   - [ ] Unit定義ファイルの作成
3. ユーザーの承認を待つ

### ステップ2: User Storiesの読み込み
1. `aidlc-docs/story-artifacts/user_stories.md` を読み込む
2. 各User Storyの内容を分析：
   - ユーザー役割
   - 機能領域
   - データ要件
   - 依存関係

### ステップ3: 凝集度分析
1. 以下の観点から凝集度を評価：
   - 機能的な関連性
   - データの共有
   - ビジネスドメインの近接性
2. 高凝集度のUser Storiesを特定

### ステップ4: Unitsへのグループ化
1. 高凝集度のUser StoriesをUnitsにグループ化
2. 各Unitは以下を満たす：
   - 単一チームで独立して構築可能
   - 明確な境界（Bounded Context）
   - 測定可能な価値を提供
3. Unit名を定義（例：「ユーザーデータ収集」、「レコメンデーションアルゴリズム選択」、「API統合」）

### ステップ5: 結合度分析
1. Units間の依存関係を分析
2. 疎結合であることを確認
3. 必要な統合ポイントを特定
4. 統合仕様を文書化

### ステップ6: Unit定義ファイルの作成
1. 各Unitについて、`aidlc-docs/design-artifacts/units/<unit-name>.md` を作成
2. 各ファイルに以下を含める：
   - Unit名と説明
   - 含まれるUser Stories
   - 受け入れ基準
   - 依存関係
   - 統合仕様
3. 計画ファイルのチェックボックスを更新

## アーティファクト
- `aidlc-docs/design-artifacts/units/<unit-name>.md` (各Unitのファイル)
- `aidlc-docs/design-artifacts/units/integration_specs.md` (統合仕様)

## 注意事項
- DDDのBounded Context原則に従う
- 各Unitは独立してデプロイ可能であるべき
- 結合度が高い場合は、ユーザーに確認を求める

