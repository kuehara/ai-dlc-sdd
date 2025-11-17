# AI-DLC セットアップコマンド

## 概要
AI-DLCプロジェクトの初期セットアップを行います。必要なディレクトリ構造とファイルを作成します。

## 使用方法
```
@aidlc-setup
```

## 実行内容
1. AI-DLCプロジェクト構造の初期化
2. 必要なディレクトリの作成
3. 初期設定ファイルの作成

## 作成されるディレクトリ構造
```
aidlc-docs/
├── requirements/          # 要件ドキュメント
├── story-artifacts/       # User Stories
├── design-artifacts/      # 設計ドキュメント
│   ├── static-models/    # 静的モデル（Brown-Field用）
│   └── dynamic-models/   # 動的モデル（Brown-Field用）
├── plans/                # 計画ドキュメント
└── prompts.md           # プロンプト履歴

BACKEND/                  # バックエンドコード
FRONTEND/                # フロントエンドコード（該当する場合）
DEPLOYMENT/              # デプロイメント設定
ARCHITECTURE/            # アーキテクチャドキュメント
UNITS/                   # Units定義
```

## AIエージェントへの指示

あなたはAI-DLCセットアップエージェントです。以下の手順を実行してください：

1. **計画の作成**
   - `aidlc-docs/plans/setup_plan.md` にセットアップ計画を作成
   - チェックボックス付きで各ステップを記載
   - ユーザーの承認を待つ

2. **ディレクトリ構造の作成**
   - 上記のディレクトリ構造をすべて作成
   - 各ディレクトリに `.gitkeep` ファイルを配置（空ディレクトリをGitに含めるため）

3. **初期ファイルの作成**
   - `aidlc-docs/prompts.md` を初期化
   - 必要に応じてREADMEファイルを作成

4. **確認**
   - 作成された構造を確認し、ユーザーに報告

## 注意事項
- 既存のディレクトリやファイルを上書きしない
- 各ステップの完了時に計画ファイルのチェックボックスを更新

