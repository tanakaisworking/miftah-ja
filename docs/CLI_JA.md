# CLIガイド

## 最初に使うコマンド

### 対話セットアップ

```bash
miftah setup
```

初回利用ではこれを使うのがおすすめです。接続方法、Profile、Credential、出力先、AIクライアントの順に設定します。

### Browser Console

```bash
miftah dashboard
```

ローカルブラウザでセットアップやProfile管理を行います。

### 設定の構文確認

```bash
miftah validate --config <設定ファイル>
```

設定ファイルの形式が正しいかを確認します。

### 接続状態の診断

```bash
miftah doctor --config <設定ファイル>
```

Credential参照やUpstream MCPの起動準備を、Secretを表示せずに確認します。

### Profile単体の確認

```bash
miftah test-profile --config <設定ファイル> --profile work
```

指定Profileだけを起動・初期化して確認します。

## AIから使う管理Tool

- `miftah_list_profiles`: Profile一覧
- `miftah_current_profile`: 現在のProfile
- `miftah_use_profile`: Profile切替
- `miftah_reset_profile`: デフォルトに戻す
- `miftah_lock_profile`: 接続単位でProfileを固定（有効化時のみ）
- `miftah_unlock_profile`: 固定解除

## よく使う考え方

### process

Miftahプロセスを再起動するとデフォルトProfileへ戻ります。

### workspace

最後に切り替えたProfileを設定ごとに保持します。

## AIクライアント

upstreamが設定生成を持つのはClaude Desktop / Claude Code / Cursor / VS Codeです。

Codex CLIはupstreamで互換性試験されていますが、現時点で `--client codex` はありません。

詳細な全コマンド仕様はupstream由来の `cli.md` に残しています。