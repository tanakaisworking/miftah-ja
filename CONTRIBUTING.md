# コントリビューションガイド

このリポジトリは [mohanagy/miftah](https://github.com/mohanagy/miftah) の日本向けフォークです。

日本語化・日本向けセットアップ改善・日本のAIクライアント利用時の詰まりどころの改善を歓迎します。

## 変更方針

- Miftah本体の認証・ルーティング・セキュリティ設計はできるだけupstreamへ追従する
- 日本語化だけのためにコアロジックを大きく分岐させない
- 英語入力やupstream互換性を壊さない
- Secretや実CredentialをIssue・PR・テストデータへ含めない

## 開発

```bash
git clone https://github.com/tanakaisworking/miftah-ja.git
cd miftah-ja
npm ci
npm run typecheck
npm test
npm run build
```

## Pull Request

PRには次を簡潔に書いてください。

- 何を変えたか
- なぜ必要か
- どの操作を確認したか
- upstreamとの差分が増える変更の場合、その理由

## upstreamへ出すべき変更

日本固有ではないバグ修正やMiftah本体の改善は、可能であればupstreamへ先に提案する方針です。

英語のupstream原文は [CONTRIBUTING.en.md](CONTRIBUTING.en.md) に残しています。