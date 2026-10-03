# Miftah 日本語ガイド

> このリポジトリは [mohanagy/miftah](https://github.com/mohanagy/miftah) の日本語向けフォークです。
> 認証・ルーティング・セキュリティのコア設計はなるべく変更せず、セットアップ時の日本語補助を中心にしています。

## Miftahとは

Miftahは、同じMCPサーバーを仕事用・個人用・顧客用など複数アカウントで使い分けるためのローカルMCP credential brokerです。

たとえばGitHubを `work` と `personal` の2アカウントで使う場合、Claude CodeやCursor側に同じMCPを複数登録する代わりに、Miftah側でProfileとして管理できます。

- ローカル動作 / クラウドサービス不要
- 複数アカウントをProfileとして管理
- CredentialをAIクライアント設定から分離
- Claude Desktop / Claude Code / Cursor / VS Code向け設定生成
- Codex CLIとの互換性もupstreamで検証済み

## 必要環境

Miftah本体は Node.js 20以上が必要です。

```bash
node --version
npm --version
```

GitHub presetはDockerを利用します。Google Search Console presetではPython/uvxなど追加要件があります。

## セットアップ

### 日本語版forkを使う

```bash
git clone https://github.com/tanakaisworking/miftah-ja.git
cd miftah-ja
npm ci
npm run build
npm install -g .
miftah setup
```

日本語補助が不要でupstreamの安定版をそのまま使う場合は `npm install -g @lubab/miftah@1.1.6` で導入できます。

このforkでは `miftah setup` の主要導線に日本語ガイドを追加し、以下の日本語入力も受け付けます。

- `はい` / `いいえ`
- `戻る` / `中止` / `終了`
- `コネクタ` / `リモート` / `ローカル` / `ブラウザログイン` / `取り込み`
- Profile保持方法として `初期値` / `デフォルト` / `保持` / `最後を保持`

英語入力と英語表示は残しているため、upstreamのドキュメントとの対応関係も維持しています。

## process と workspace

- `process`: Miftah再起動時に設定済みのデフォルトProfileへ戻る
- `workspace`: 最後に選んだProfileをこの設定用に保持する

## macOSでの注意

Claude DesktopなどGUIアプリは、ターミナルの `.zshrc` の環境変数をそのまま引き継がない場合があります。CredentialはOS Keychainや1Passwordなど、MiftahがサポートするSecret Providerの利用を推奨します。

## OAuthについて

MiftahがネイティブにOAuthを管理できるのは、標準仕様に沿ったRemote HTTP MCPです。stdio MCPや独自OAuthでは、接続先MCP側の認証手順が必要な場合があります。

## 詳細

- [日本語セットアップ早見表](docs/SETUP_JA.md)
- [upstream README](https://github.com/mohanagy/miftah)

## License

MIT License。元リポジトリの著作権表示とLICENSEを保持しています。