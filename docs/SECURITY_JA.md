# セキュリティガイド

MiftahはCredentialを扱うため、便利さより安全側に倒した制約があります。

## 重要な原則

- 生のSecretを共有設定へ保存しない
- OAuth CredentialやProvider Cacheを不用意に共有しない
- Provider Credential自体は最小権限で発行する
- Profile名だけで正しいアカウントだと決めつけない
- MiftahのLocal PolicyはProvider側の権限そのものを縮小するものではない

## Profile切替

Profile切替には確認を要求する設定ができます。仕事用と個人用を混同したくない場合に有効です。

## 監査ログ

監査情報はローカルに保存され、SecretはRedactされます。

## Remote OAuth

MiftahはDiscovery結果、Issuer、Resourceなどを厳密に確認し、想定外のOAuth先へCredentialを送らないようにします。

## 注意

Credentialが正しく解決できても、Provider側で付与済みの権限が強すぎればMiftahだけでは縮小できません。Token/API Key自体を最小権限で発行してください。

詳細な脅威モデル・セキュリティ境界はupstream由来の `security.md` / `threat-model.md` に残しています。