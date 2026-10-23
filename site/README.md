# ぽっぽ工務店

Affinityのデザインカンプと設計方針、原稿、画像・SVG素材をもとにした静的サイトです。元資料のSVGと原稿は変更せず、サイト用コピーを `assets/` と `images/` に配置しています。

- `index.html` — トップページ
- `about.html` — 工務店の説明
- `profile.html` — 鳩居ぼたんの紹介、受付中サービス、制作環境
- `styles.css` — レイアウト、配色、レスポンシブ調整
- `script.js` — スクロール連動、無限カルーセル、作例ギャラリー
- `inner.js` — 下層ページのナビゲーション

`index.html` をブラウザで開くと表示できます。ビルド手順はありません。WebフォントはGoogle Fontsから読み込み、オフライン時は端末の明朝体・ゴシック体にフォールバックします。

色は `styles.css` 冒頭の `:root` にある `--green`、`--cream`、`--pink` から調整できます。作品リストは `script.js` の `galleries` にあります。

## フォント
見出しには「Shippori Mincho」を設定しました。和菓子屋の雰囲気を残しつつ、筆文字の印象を避けやすい候補です。もう少し丸みを出したい場合はGoogle Fontsの「Kaisei Opti」を見出し候補にできます。本文は可読性を優先して「Noto Sans JP」を設定しています。

## 位置・大きさの調整
- タイトル・見出し・本文は `styles.css` 冒頭の `:root` にある `--brand-title-size`、`--section-heading-size`、`--body-copy-size` で変更できます。
- 施工例blobの幅と各画像の見せたい位置は `--case-blob-width` と `--case-image-position-*` で調整できます。
- blob_bottomはblob_topと同じ座標で下に重ねています。サイズ・位置・回転は `--blob-bottom-*` で微調整できます。組み合わせは `assets/blob_sample.svg` を参照してください。
- トップの街並みのデスクトップ上の位置は、各SVGレイヤー用の `.town-green`、`.town-yellow`、`.town-pink` で管理しています。スマホ側はレイヤー構成を保ったまま縮尺を合わせます。
