# OAuthガイド

## Miftahが直接管理できるOAuth

標準仕様に沿ったRemote HTTPS MCPでは、Miftahが次を管理できます。

- OAuth Discovery
- ブラウザ認証
- loopback callback
- Authorization Code交換
- Token保存
- Refresh
- 再認証
- MiftahローカルCredentialの切断

## Miftahが直接管理しないOAuth

次のケースではUpstream MCP側の認証手順に従います。

- stdio MCP
- Provider独自OAuth
- 独自Token Cacheを持つMCP
- PasswordやBrowser Cookieを使う独自認証

MiftahはProviderの非公開Token CacheやBrowser Cookieを勝手に読み取りません。

## 複数アカウント

複数アカウントを使う場合、CredentialはProfile単位で分離します。

「Tokenが有効であること」と「意図したアカウントであること」は別問題として扱われます。Upstreamが安定したIdentity Probeを提供する場合は、それを利用できます。

詳細なOAuth仕様はupstream由来の `oauth-support.md` に残しています。