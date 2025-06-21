# my-repo
GitHub Actionsの練習用

## hello.yml ワークフローについて

`hello.yml`は、GitHub Actionsを使用したシンプルなワークフローファイルです。リポジトリにプッシュが行われた際に自動実行されます。

### 処理の流れ

```mermaid
graph TD
    A["Git Pushイベント発生"] --> B["ワークフロー開始<br/>名前: Hello"]
    B --> C["ジョブ: hello<br/>ランナー: ubuntu-latest"]
    C --> D["ステップ1: シェルコマンド実行<br/>echo 'Hello, world'"]
    D --> E["ステップ2: アクション実行<br/>actions/checkout@v4"]
    E --> F["ワークフロー完了"]
    
    style A fill:#e1f5fe
    style B fill:#f3e5f5
    style C fill:#e8f5e8
    style D fill:#fff3e0
    style E fill:#fff3e0
    style F fill:#ffebee
```

### 詳細説明

1. **トリガー**: `on: push` により、リポジトリへのプッシュ時にワークフローが起動
2. **実行環境**: Ubuntu最新版のランナーで実行
3. **実行ステップ**:
   - `echo "Hello, world"`: コンソールに挨拶メッセージを出力
   - `actions/checkout@v4`: リポジトリのソースコードをチェックアウト

このワークフローは、GitHub Actionsの基本的な動作を学習するためのサンプルです。