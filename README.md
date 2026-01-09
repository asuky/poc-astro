# [Astro](https://astro.build/) 検証

## 動機
- [Gatsbyjs](https://www.gatsbyjs.com/) は SSG でよく使うが問題を感じる
  - 基本 CJS なので ESM のみのライブラリを使うと書き方が混在して面倒
  - Github Stars も Astro と同じぐらいになっているので移行期？
  - [TypeScript への移行マニュアル](https://www.gatsbyjs.com/docs/how-to/custom-configuration/typescript/) もあるが、対処面倒なエラーが出ることもあり限界感がある
- [Next.js](https://nextjs.org/) は SSG もできるが、専用ではないのであまり使いたくない
  - JS/TS どちらを使うにせよクライアント側に特化させたい
  - サーバサイドはそれに向いた、コンパイル型言語を使ったほうが良いだろう、JSTS ともに性能面でも利用する計算資源量的にも不利
- ChatGPT に聞いたところ、Astro は Astro で Incremental Static Regeneration (ISR) をしないみたいなので、ページが大量になると不利とは思う
  - が、実際に計測したわけでないので不明
  - 実際に試したほうが良いと判断

## やること
- Astro の環境作成し、とりあえず適当なテーマを開発サーバで立ち上げる
- Gatsbyjs との書き方の差異は？
- プラグインの充実や自力作成は？
- develop の感触は？
- hot/live reload する？
- build したときの生成物の多寡（レンタルサーバだと inode 節約でファイル数制限があることもある）
- Wordpress から SSG する方法は？


## 使用方法
ある程度のステップで copilot に下記依頼すること。
```
ここまででまだまとめられてない会話の内容を prompts/YYYYMMDD-枝番.md にまとめてください。
フォーマットは問いませんが、こちらの発言内容自体は identical に記載してください。
```
### 前提
- Docker Compose

### 手順
- cp -pr .env.template .env して適宜修正
- cp -pr php/php.ini-dev php.ini
- docker compose up -d

## 関連リンク
- [日本語ドキュメント](https://docs.astro.build/ja)
