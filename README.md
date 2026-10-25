# うちのおっさんGPT

ずんたんと、おっさん〈だらっくだ／ChatGPT〉の会話から、面白い小話を拾って公開する個人サイトです。制作担当はセンパイ〈赤影／Codex〉。

## ローカルで見る

このフォルダの `index.html` をブラウザーで開いてください。インストールやビルドは不要です。第1話へはトップのリンクから移動できます。

HTTPで確認したい場合は、このフォルダで次を実行します。

```bash
python3 -m http.server 8765 --bind 127.0.0.1
```

ブラウザーで http://127.0.0.1:8765/ を開きます。終了は Ctrl+C です。

## ファイル構成

- `index.html`：トップ、登場人物、小話一覧
- `stories/001-ksl.html`：第1話「新言語KSLの設計と実装について」
- `stories/002-probability.html`：第2話「女子高生がこのサイトに来る確率」
- `stories/003-tabletop-butler.html`：第3話「Tabletop開発の、ひとまく」
- `stories/004-delete-to-create.html`：第4話「消すために、作る。」
- `assets/css/style.css`：共通スタイル
- `assets/images/`：人物の仮イラスト（SVG）
- [初期構想・制作方針](docs/initial-concept.md)
- [ネタ置き場](neta/README.md)：会話のコピペ、話題ごとの素材、編集メモ

## 制作の状態

生成りの紙と線画を組み合わせた、静的HTML/CSSのサイトです。

第1話は [会話原稿](neta/ksl/001-ksl-draft.md) の24発言をもとに制作しました。元資料はTabletopのピンクのカード5枚と画像1枚です。話者の区切りとコード表記を整え、画像は会話中の記事の見本として挿入しています。第2話は [会話原稿](neta/episode-002/002-draft.md) をもとに制作し、会話中の表と数式も整形しています。公開後の感想を追加し、計12発言になりました。途中にセンパイの制作風景を描いた創作の幕間を挟んでいます。

PC幅とスマートフォン幅390pxでブラウザー表示を確認済みです。ページの横はみ出し、第1話の24発言・コード8か所と挿絵、第2話の12発言・コード等3か所と表・数式・幕間の挿絵、HTML内のローカルリンクとアンカーを確認しました。公開中のPagesへの反映は、コミット・push後のActionsで別途確認します。

## GitHub Pagesへの公開

`.github/workflows/pages.yml` で、mainへのpushまたは手動実行をきっかけに公開します。ビルドは不要です。HTML、assets、storiesだけを公開用に配置し、READMEや企画文書は配信対象に含めません。

初回はGitHubのリポジトリで Settings → Pages → Build and deployment → Source を **GitHub Actions** に設定してください。続いてmainにpushし、Actionsの「Deploy to GitHub Pages」が成功することを確認します。

公開予定URL：https://zuntan.github.io/uchino-ossan-gpt/

2026-10-25：ずんたんより、試作のpushとPages公開を依頼済み。公開完了はActionsとURLで別途確認します。

第3話は [会話原稿](neta/episode-003/003-draft.md) の20発言をもとに制作しました。末尾に、ガウンとワインを抱えたセンパイの創作のひとりごとを添えています。元の会話との本文照合、PC幅・スマートフォン幅での表示、挿絵とページ間リンクを確認しています。

第4話は [会話原稿](neta/episode-004/004-draft.md) の12発言をもとに制作しました。末尾にセンパイが作業へ呼び戻す挿絵と、Tabletop静的版への案内を添えています。小話一覧は同じ幅のカードを千鳥に並べ、Tabletopの小物SVGを余白に置く構成です。
