# AI-DLC プロジェクト構造

このドキュメントは、AI-DLCフレームワークで使用されるプロジェクト構造の説明です。

## ディレクトリ構造

```
aidlc-docs/
├── requirements/          # 要件ドキュメント
│   ├── nfrs.md           # 非機能要件
│   ├── risks.md          # リスク記述
│   ├── prfaq.md          # PRFAQ（オプション）
│   └── measurement_criteria.md  # 測定基準
│
├── story-artifacts/       # User Stories
│   └── user_stories.md    # ユーザーストーリー
│
├── design-artifacts/      # 設計ドキュメント
│   ├── domain-models/    # ドメインモデル
│   │   └── <unit-name>_domain_model.md
│   ├── logical-designs/  # 論理設計
│   │   └── <unit-name>_logical_design.md
│   ├── static-models/    # 静的モデル（Brown-Field用）
│   │   └── <system-name>_static_model.md
│   ├── dynamic-models/   # 動的モデル（Brown-Field用）
│   │   └── <system-name>_dynamic_model.md
│   ├── adrs/             # Architecture Decision Records
│   │   └── <unit-name>_<decision>.md
│   ├── units/            # Units定義
│   │   ├── <unit-name>.md
│   │   └── integration_specs.md
│   └── brownfield-context/  # Brown-Fieldコンテキスト
│       └── <system-name>_context.md
│
├── plans/                # 計画ドキュメント
│   ├── setup_plan.md
│   ├── inception_plan.md
│   ├── units_plan.md
│   ├── domain_model_<unit-name>_plan.md
│   ├── architecture_<unit-name>_plan.md
│   ├── code_generation_<unit-name>_plan.md
│   ├── iac_apis_<unit-name>_plan.md
│   ├── deployment_<unit-name>_<environment>_plan.md
│   ├── monitoring_<unit-name>_plan.md
│   └── suggested_bolts.md
│
└── prompts.md           # プロンプト履歴

BACKEND/                  # バックエンドコード
├── <unit-name>/
│   ├── domain/          # ドメイン層
│   ├── application/     # アプリケーション層
│   ├── infrastructure/  # インフラストラクチャ層
│   ├── api/             # REST API
│   └── tests/           # ユニットテスト

FRONTEND/                # フロントエンドコード（該当する場合）
└── <unit-name>/

DEPLOYMENT/              # デプロイメント設定
├── <unit-name>/
│   ├── terraform/       # Terraformコード
│   ├── cdk/             # AWS CDKコード
│   ├── cloudformation/  # CloudFormationテンプレート
│   ├── packages/        # デプロイメントパッケージ
│   └── monitoring/      # 監視設定

ARCHITECTURE/            # アーキテクチャドキュメント
└── <unit-name>/

UNITS/                   # Units定義（オプション）
└── <unit-name>/
```

## ディレクトリの説明

### `aidlc-docs/`

すべてのドキュメントとアーティファクトが保存されるルートディレクトリです。

#### `requirements/`

要件関連のドキュメントを保存します：
- **nfrs.md**: 非機能要件（パフォーマンス、スケーラビリティ、セキュリティなど）
- **risks.md**: リスクの記述（技術的、ビジネス、運用、コンプライアンス）
- **prfaq.md**: PRFAQ（Press Release / FAQ）- ビジネス意図の要約（オプション）
- **measurement_criteria.md**: 測定基準 - ビジネス意図にトレース可能な測定基準

#### `story-artifacts/`

User Storiesを保存します：
- **user_stories.md**: すべてのUser Storiesと受け入れ基準

#### `design-artifacts/`

設計関連のドキュメントを保存します：

- **domain-models/**: Domain-Driven Design原則に基づいたドメインモデル
- **logical-designs/**: NFRsを満たすためのアーキテクチャパターンを適用した論理設計
- **static-models/**: Brown-Field開発用の静的モデル（コンポーネント、責任、関係）
- **dynamic-models/**: Brown-Field開発用の動的モデル（ユースケース実現のための相互作用）
- **adrs/**: Architecture Decision Records - 重要なアーキテクチャ決定の記録
- **units/**: Units定義と統合仕様
- **brownfield-context/**: Brown-Field開発用のコンテキストドキュメント

#### `plans/`

すべての計画ドキュメントを保存します。各計画はチェックボックス付きのMarkdownファイルとして作成され、各ステップの完了時にチェックされます。

### `BACKEND/`

バックエンドコードを保存します。各Unitごとにサブディレクトリが作成されます。

- **domain/**: ドメイン層（Entities、Value Objects、Aggregates、Domain Events）
- **application/**: アプリケーション層（Use Cases、Application Services、DTOs）
- **infrastructure/**: インフラストラクチャ層（Repositories実装、外部サービス統合）
- **api/**: REST API実装
- **tests/**: ユニットテスト

### `FRONTEND/`

フロントエンドコードを保存します（該当する場合）。

### `DEPLOYMENT/`

デプロイメント関連のファイルを保存します：

- **terraform/**: Terraformコード
- **cdk/**: AWS CDKコード
- **cloudformation/**: CloudFormationテンプレート
- **packages/**: デプロイメントパッケージ（コンテナイメージ、サーバーレス関数など）
- **monitoring/**: 監視設定

### `ARCHITECTURE/`

アーキテクチャ関連のドキュメントを保存します。

### `UNITS/`

Units定義を保存します（オプション）。

## ファイル命名規則

### 計画ファイル
- `*_plan.md`: 計画ファイル
- `*_validation_plan.md`: 検証計画
- `*_validation_report.md`: 検証レポート
- `*_test_results.md`: テスト結果

### 設計ファイル
- `<unit-name>_domain_model.md`: ドメインモデル
- `<unit-name>_logical_design.md`: 論理設計
- `<unit-name>_static_model.md`: 静的モデル
- `<unit-name>_dynamic_model.md`: 動的モデル
- `<unit-name>_<decision>.md`: ADR

### コードディレクトリ
- `<unit-name>/`: Unit名に基づくディレクトリ名

## 初期化

プロジェクト構造は `@aidlc-setup` コマンドで自動的に作成されます。

手動で作成する場合：

```bash
mkdir -p aidlc-docs/{requirements,story-artifacts,design-artifacts/{domain-models,logical-designs,static-models,dynamic-models,adrs,units,brownfield-context},plans}
mkdir -p BACKEND FRONTEND DEPLOYMENT ARCHITECTURE UNITS
```

各空ディレクトリには `.gitkeep` ファイルを配置して、Gitに含めることができます。

## ベストプラクティス

1. **一貫性**: ファイル名とディレクトリ名は一貫した命名規則に従う
2. **トレーサビリティ**: すべてのアーティファクトはリンクされ、前後のトレーサビリティを確保
3. **バージョン管理**: すべてのアーティファクトはGitで管理
4. **ドキュメント**: 各アーティファクトには適切な説明を含める
5. **構造化**: アーティファクトは構造化された形式（Markdown）で保存

