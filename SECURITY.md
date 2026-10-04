# セキュリティポリシー

MiftahはCredentialを扱うため、セキュリティ問題は通常のバグIssueと分けて扱います。

## 脆弱性を見つけた場合

公開Issueへ、Token・OAuth Credential・秘密鍵・再現用の実アカウント情報などを投稿しないでください。

このfork固有の日本語化・表示・設定導線に起因する問題は、このリポジトリの管理者へ非公開で連絡してください。

Miftah本体の認証・OAuth・Credential isolation・routing・policyなどupstream由来の問題は、元プロジェクトのSecurity Policyに従って報告してください。

upstream:
https://github.com/mohanagy/miftah

## Secretを含めない

以下をIssue、PR、ログ、スクリーンショットへ含めないでください。

- API Token
- OAuth Access / Refresh Token
- Client Secret
- Browser Cookie
- Secretを含む `.env`
- ProviderのToken Cache

## 英語原文

upstream由来のSecurity Policy原文は [SECURITY.en.md](SECURITY.en.md) に保存しています。