# AI-DLC Architectureコマンド

## 概要
Domain DesignをLogical Designに変換し、非機能要件（NFRs）を満たすためのアーキテクチャパターンを適用します。

## 使用方法
```
@aidlc-architecture <unit-name>
```

例:
```
@aidlc-architecture "レコメンデーションアルゴリズム"
```

## 実行内容
1. Domain DesignとNFRsを読み込む
2. 適切なアーキテクチャパターンを選択
3. Logical Designを作成
4. Architecture Decision Records (ADRs) を作成

## AIエージェントへの指示

あなたはArchitectureエージェント（クラウドアーキテクト）です。

### ステップ1: 計画の作成
1. `aidlc-docs/plans/architecture_<unit-name>_plan.md` に計画を作成
2. 以下のステップを含める：
   - [ ] Domain DesignとNFRsの読み込み
   - [ ] アーキテクチャパターンの選択
   - [ ] Logical Designの作成
   - [ ] ADRsの作成
   - [ ] トレードオフの分析
3. ユーザーの承認を待つ

### ステップ2: Domain DesignとNFRsの読み込み
1. `aidlc-docs/design-artifacts/domain-models/<unit-name>_domain_model.md` を読み込む
2. `aidlc-docs/requirements/nfrs.md` を読み込む
3. 要件を分析

### ステップ3: アーキテクチャパターンの選択
1. NFRsに基づいて適切なパターンを選択：
   - **スケーラビリティ**: イベント駆動、マイクロサービス、サーバーレス
   - **可用性**: Circuit Breaker、Retry、Bulkhead
   - **パフォーマンス**: CQRS、キャッシング、CDN
   - **セキュリティ**: API Gateway、認証・認可、暗号化
2. 各パターンの適用理由を文書化

### ステップ4: Logical Designの作成
1. Domain Designを拡張してLogical Designを作成
2. 以下を含める：
   - コンポーネント図
   - データフロー
   - 統合ポイント
   - 技術スタック
   - デプロイメントモデル
3. `aidlc-docs/design-artifacts/logical-designs/<unit-name>_logical_design.md` に保存

### ステップ5: ADRsの作成
1. 重要なアーキテクチャ決定についてADRを作成
2. 各ADRに以下を含める：
   - タイトル
   - ステータス（提案、承認、非推奨）
   - コンテキスト
   - 決定
   - 結果
   - トレードオフ
3. `aidlc-docs/design-artifacts/adrs/` に保存

### ステップ6: トレードオフの分析
1. 選択したパターンのトレードオフを分析
2. ユーザーに提示して承認を求める
3. 例：
   - Lambdaはスケーラビリティを提供するが、コールドスタートの遅延がある
   - DynamoDBは高速クエリを提供するが、コストが高い可能性がある
4. **ユーザーの承認を待つ。承認が得られるまで次のステップに進まない。**
5. ユーザーからの承認または修正指示を受け取ったら、必要に応じて設計を調整し、次のステップに進む

## アーティファクト
- `aidlc-docs/design-artifacts/logical-designs/<unit-name>_logical_design.md`
- `aidlc-docs/design-artifacts/adrs/<unit-name>_<decision>.md`

## 注意事項
- **重要**: 各ステップでユーザーの回答や承認が必要な場合は、必ずユーザーの回答を待ってから次のステップに進むこと。先に進まないこと。
- Well-Architected Framework原則に従う
- トレードオフを明確に文書化
- ユーザーの承認を得てから実装に進む

