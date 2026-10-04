# Miftah 日本語ドキュメント

通常利用は、この日本語ドキュメントだけで進められる構成を目指しています。

## まず読む

- [トップREADME](../README.md)
- [セットアップ早見表](SETUP_JA.md)
- [CLIガイド](CLI_JA.md)
- [設定ファイルガイド](CONFIG_JA.md)
- [OAuthガイド](OAUTH_JA.md)
- [セキュリティガイド](SECURITY_JA.md)

## 用語

| 用語 | 意味 |
| --- | --- |
| Profile | 同じMCPに接続するアカウント・環境単位 |
| Upstream MCP | Miftahの後ろで実際に動くMCP Server |
| Credential | API TokenやOAuth Credentialなど |
| process | 再起動時にデフォルトProfileへ戻る |
| workspace | 最後に選んだProfileを保持する |
| Secret Provider | Secretの実値を設定ファイル外で解決する仕組み |

## upstream由来の詳細資料

以下は高度な内部仕様・互換性・脅威モデルを確認するための英語原文です。通常利用では読む必要はありません。

- `architecture.md`
- `cli.md`
- `config.md`
- `console-api.md`
- `oauth-support.md`
- `security.md`
- `threat-model.md`
- `mcp-compatibility.md`

日本語版で不足する内容があればIssueで追加していく方針です。