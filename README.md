# COACHING-L ツール（トップページ）

コーチングスクール「COACHING-L」のツールの一覧ページです。
GitHub 組織 `coaching-l` の GitHub Pages（組織のサイト）として公開し、独自ドメイン **https://tools.coaching-l.net/** で表示します。

- HTML・CSS だけで動きます（ビルド不要、JavaScript・外部ライブラリなし）
- 配色・ロゴ・ファビコンは、各ツールとそろえています（ライト／ダークは端末の設定に合わせて自動で切り替え）

## 載せているツール

| ツール | URL | リポジトリ |
| --- | --- | --- |
| 人生の輪 | https://tools.coaching-l.net/the-wheel-of-life/ | [coaching-l/the-wheel-of-life](https://github.com/coaching-l/the-wheel-of-life) |
| 内省の問いカード | https://tools.coaching-l.net/reflection-cards/ | [coaching-l/reflection-cards](https://github.com/coaching-l/reflection-cards) |
| ポモドーロタイマー | https://tools.coaching-l.net/pomodoro/ | [coaching-l/pomodoro](https://github.com/coaching-l/pomodoro) |
| 内的土壌ノート | https://tools.coaching-l.net/inner-ground-theory/ | [coaching-l/inner-ground-theory](https://github.com/coaching-l/inner-ground-theory) |

## 独自ドメインのしくみ

- このリポジトリの `CNAME` ファイルに `tools.coaching-l.net` と書いてあり、これが組織のサイトの独自ドメインになります
- 組織のサイトに独自ドメインを設定すると、`coaching-l` の各ツールのリポジトリ（独自ドメインを設定していないもの）も、同じドメインの下で公開されます
  - 例：`https://coaching-l.github.io/pomodoro/` → `https://tools.coaching-l.net/pomodoro/`
  - 古い `coaching-l.github.io` の URL は、GitHub が自動で新しい URL に転送します
- DNS には、`tools.coaching-l.net` の CNAME レコード（向き先 `coaching-l.github.io`）が必要です

## ツールを足すとき

1. `coaching-l` 組織に、ツールのリポジトリを作って GitHub Pages で公開します（各ツールの README の「GitHub Pages での公開」と同じ手順）
2. `index.html` の `<ul class="tool-list">` の中に `<li>` を1つ足し、リンク先を `/リポジトリ名/` にします
3. この README の「載せているツール」の表にも1行足します

`style.css` を変えたときは、`index.html` と `404.html` の `style.css?v=1` の数字を1つ上げてください。

## ファイル構成

| ファイル | 内容 |
| --- | --- |
| `index.html` | ツールの一覧（トップページ） |
| `404.html` | ページが見つからないときの画面 |
| `style.css` | 見た目（スマホ優先・ライト／ダーク対応） |
| `icons/` | ロゴ・ファビコン・ホーム画面用アイコン（各ツールと同じ画像） |
| `CNAME` | 独自ドメイン（`tools.coaching-l.net`） |
