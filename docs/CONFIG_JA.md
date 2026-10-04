# 設定ファイルガイド

Miftahの設定は、MCP本体の起動方法と複数ProfileのCredential参照をまとめたものです。

## 基本方針

- 生のTokenやPasswordを共有設定へ直接書かない
- ProfileごとにCredentialを分離する
- Secret Provider経由で実値を解決する
- Upstream MCPの権限は最小権限にする

## Profile

同じMCPを複数アカウントで使う場合、Profileを分けます。

例:

```text
GitHub
├─ work
└─ personal
```

Profile名は `work`, `personal`, `client-a` のような短い英数字を推奨します。

## Secret Provider

Miftahは設定ファイルにSecretの実値を直接置く代わりに、参照を使えます。

代表例:

- OS Keychain
- 1Password
- 環境変数

macOSのGUIアプリは `.zshrc` の環境変数を引き継がない場合があるため、Keychainや1Passwordの方が安定しやすいです。

## Local stdio MCP

ローカルMCPを登録するとき、Miftahはshell文字列ではなく実行ファイルと引数配列として保存します。

危険なshell展開やCredentialの埋め込みを避けるための設計です。

## Remote MCP

新しいRemote MCPはStreamable HTTPを利用します。URLへCredentialを埋め込まず、HeaderまたはOAuthを利用してください。

詳細なスキーマや全項目はupstream由来の `config.md` に残しています。