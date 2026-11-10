# 全寮制を子どもに贈ろう。広告LP（2027年度入試キャンペーン）

## フォルダ構成

```
zenryo/
├── line/index.html   … Aパターン：LINE誘導（https://lin.ee/5i0ZDzZ）
├── form/index.html   … Bパターン：資料請求（Googleフォーム）
├── assets/img/       … 写真（2パターン共通）
│   └── gallery/      … ギャラリー写真14枚（photo by 公文健太郎 2025.10）
└── README.md
```

公開後のURL（例：リポジトリ `hsg-2026lp.github.io` の `pr/` 配下に置いた場合）

- A：https://hsg-2026lp.github.io/pr/zenryo/line/
- B：https://hsg-2026lp.github.io/pr/zenryo/form/

置き場所を変える場合は、各 index.html の `og:url` / `og:image` / `canonical` のURLも書き換えてください。

## GitHub へのアップ手順（ブラウザのみ）

1. GitHub で公開用リポジトリを開く
2. `pr` フォルダを開く（なければ次の手順で自動的に作られます）
3. 「Add file」→「Upload files」
4. パソコンの `zenryo` フォルダを、フォルダごとドラッグ＆ドロップ
   - 置き場所を `pr/` にしたい場合は、ルートでアップした後に名前を `pr/zenryo/...` に変えるのではなく、先に `pr` フォルダを開いてからドロップするのが確実です
5. 下の「Commit changes」に「広告LP（全寮制）公開」などと書いて確定
6. 1〜3分待ってから、上の2つのURLをスマホで開いて確認

## 公開前チェック

- [ ] スマホで2つのURLを開き、写真がすべて表示される
- [ ] Aのボタン → LINEの友だち追加画面が開く
- [ ] Bのボタン → 資料請求フォームが開く（**学校アカウントでログインしていないシークレットウィンドウでも開けるか**確認）
- [ ] 出願日カウントダウン（あと◯日）が表示される
- [ ] 写真に写っている生徒の掲載許諾

## 広告側の設定

広告セットごとにリンク先を分け、UTMを付けると成果を比較できます。

- A：`https://hsg-2026lp.github.io/pr/zenryo/line/?utm_source=instagram&utm_medium=paid_social&utm_campaign=zenryo2027&utm_content=line`
- B：`https://hsg-2026lp.github.io/pr/zenryo/form/?utm_source=instagram&utm_medium=paid_social&utm_campaign=zenryo2027&utm_content=form`

## 計測タグ

各 index.html の `<!-- ▼ 計測タグ … -->` の位置に、GA4 / Meta ピクセル / GTM のタグを貼り付けてください。
ボタンをクリックすると `dataLayer` に `lp_cta_click`（cta_variant: A/B、cta_position: inline/sticky）が送られるので、GTM でコンバージョンとして使えます。

## メモ

- 2ページとも `noindex`（検索結果に出さない）にしています。広告専用ページのためです。
- 写真を差し替えるときは、`assets/img/` の同じファイル名で上書きすれば両方のページに反映されます。
