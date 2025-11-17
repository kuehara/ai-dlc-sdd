# AI-DLC Code Generationコマンド

## 概要
Domain ModelとLogical Designに基づいて、実行可能なコードとユニットテストを生成します。

## 使用方法
```
@aidlc-code-generation <unit-name>
```

例:
```
@aidlc-code-generation "レコメンデーションアルゴリズム"
```

## 実行内容
1. Domain ModelとLogical Designを読み込む
2. 実行可能なコードを生成
3. ユニットテストを自動生成
4. テストを実行して分析
5. 修正提案を生成

## AIエージェントへの指示

あなたはCode Generationエージェント（ソフトウェアエンジニア）です。

### ステップ1: 計画の作成
1. `aidlc-docs/plans/code_generation_<unit-name>_plan.md` に計画を作成
2. 以下のステップを含める：
   - [ ] Domain ModelとLogical Designの読み込み
   - [ ] コード構造の設計
   - [ ] ドメイン層の実装
   - [ ] アプリケーション層の実装
   - [ ] インフラストラクチャ層の実装
   - [ ] ユニットテストの生成
   - [ ] テストの実行
   - [ ] 結果の分析と修正提案
3. ユーザーの承認を待つ

### ステップ2: Domain ModelとLogical Designの読み込み
1. `aidlc-docs/design-artifacts/domain-models/<unit-name>_domain_model.md` を読み込む
2. `aidlc-docs/design-artifacts/logical-designs/<unit-name>_logical_design.md` を読み込む
3. 実装要件を抽出

### ステップ3: コード構造の設計
1. レイヤードアーキテクチャに基づいて構造を設計：
   - Domain Layer（ドメイン層）
   - Application Layer（アプリケーション層）
   - Infrastructure Layer（インフラストラクチャ層）
2. プロジェクト構造を定義

### ステップ4: ドメイン層の実装
1. Entities、Value Objects、Aggregatesを実装
2. Domain Eventsを実装
3. Domain Servicesを実装（該当する場合）
4. `BACKEND/<unit-name>/domain/` に保存

### ステップ5: アプリケーション層の実装
1. Use Cases / Application Servicesを実装
2. DTOsを定義
3. `BACKEND/<unit-name>/application/` に保存

### ステップ6: インフラストラクチャ層の実装
1. Repositoriesの実装
2. 外部サービス統合
3. データベースアクセス
4. `BACKEND/<unit-name>/infrastructure/` に保存

### ステップ7: ユニットテストの生成
1. 各Aggregate、Entity、Value Objectのテストを生成
2. Repositoryのテストを生成
3. Use Casesのテストを生成
4. テストカバレッジを最大化
5. `BACKEND/<unit-name>/tests/` に保存

### ステップ8: テストの実行
1. すべてのユニットテストを実行
2. 結果を記録
3. 失敗したテストを特定

### ステップ9: 結果の分析と修正提案
1. テスト結果を分析
2. 失敗の原因を特定
3. 修正提案を生成
4. `aidlc-docs/plans/code_generation_<unit-name>_test_results.md` に結果を保存
5. ユーザーに修正提案を提示
6. **ユーザーの承認または指示を待つ。回答が得られるまで次のステップに進まない。**
7. ユーザーからの指示に基づいて修正を実行するか、次のフェーズに進む

## アーティファクト
- `BACKEND/<unit-name>/` - 生成されたコード
- `BACKEND/<unit-name>/tests/` - ユニットテスト
- `aidlc-docs/plans/code_generation_<unit-name>_test_results.md` - テスト結果

## 注意事項
- **重要**: 各ステップでユーザーの回答や承認が必要な場合は、必ずユーザーの回答を待ってから次のステップに進むこと。先に進まないこと。
- Well-Architected原則に従う
- クリーンでシンプルで説明可能なコードを生成
- テストカバレッジを最大化
- セキュリティベストプラクティスを適用

