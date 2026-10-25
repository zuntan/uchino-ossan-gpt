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
- `stories/001-ksl.html`：第1話の仮原稿・レイアウト試作
- `assets/css/style.css`：共通スタイル
- `assets/images/`：人物の仮イラスト（SVG）
- [初期構想・制作方針](docs/initial-concept.md)

## 試作の状態

生成りの紙と線画を組み合わせたデザインの初案です。人物イラストと紹介文は仮案、第1話はレイアウト確認用の創作文で、本原稿や実際の会話の引用ではありません。第2〜4話は構想中です。CSSはスマートフォン向けの配置にも対応させていますが、実際のブラウザー表示確認はまだできていません。

HTML内のローカルリンク、アンカー、画像・CSS参照先、SVGのXML構文は検査済みです。制作環境のサーバー待受け制限とブラウザー接続の問題により、目視確認は未完了です。

## GitHub Pagesへの公開

`.github/workflows/pages.yml` で、mainへのpushまたは手動実行をきっかけに公開します。ビルドは不要です。HTML、assets、storiesだけを公開用に配置し、READMEや企画文書は配信対象に含めません。

初回はGitHubのリポジトリで Settings → Pages → Build and deployment → Source を **GitHub Actions** に設定してください。続いてmainにpushし、Actionsの「Deploy to GitHub Pages」が成功することを確認します。

公開予定URL：https://zuntan.github.io/uchino-ossan-gpt/

2026-10-25：ずんたんより、試作のpushとPages公開を依頼済み。公開完了はActionsとURLで別途確認します。
