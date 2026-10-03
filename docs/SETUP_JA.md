# Miftah セットアップ日本語早見表

## 最初の選択

| 英語 | 意味 |
| --- | --- |
| Known connector or pinned package | 既知のMCPコネクタ / 固定バージョンのパッケージ |
| Remote HTTPS endpoint | URLで公開されているリモートMCP |
| Local executable | PC内で実行するstdio MCP |
| Remote MCP with browser sign-in | ブラウザログインを使うリモートMCP |
| Existing client entry | 既存AIクライアントのMCP設定を取り込む |

## 日本語入力

- `yes`, `y`, `はい` → 続行
- `no`, `n`, `いいえ` → いいえ
- `back`, `b`, `戻る` → 前へ戻る
- `cancel`, `quit`, `q`, `中止`, `終了` → 中止

## 複数アカウント

Profile名は `work`, `personal`, `client-a` のような短い英数字名がおすすめです。

### Active profile lifetime

- `process`: 再起動時にデフォルトProfileへ戻る
- `workspace`: 最後に選択したProfileを保持する

## 詰まりやすいポイント

### GitHub
標準GitHub presetはDockerを利用します。

### macOS GUI
Claude Desktopなどは `.zshrc` の環境変数を引き継がない場合があります。OS Keychain / 1Password等のSecret Providerを検討してください。

### OAuth
Remote HTTP MCPの標準OAuth以外は、接続先MCP側のログイン手順が必要な場合があります。

### AIクライアント
upstreamの設定生成対象はClaude Desktop / Claude Code / Cursor / VS Codeです。Codex CLIは互換性試験済みですが、現時点で `--client codex` はありません。