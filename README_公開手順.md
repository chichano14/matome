# web公開用フォルダ｜GitHub Pages 公開手順

このフォルダのHTMLは、**画像をすべて埋め込んだ単一HTML**です。
画像フォルダを一緒にアップする必要はなく、これらのファイルだけで動きます（オフラインでもOK）。

## ファイル構成

| ファイル | 内容 | サイズ |
|---|---|---|
| `index.html` | 入口（4ツールへのリンク集） | 軽量 |
| `conbini.html` | コンビニ痩せ商品150選 | 約3.5MB |
| `super.html` | スーパー痩せリスト250選 | 約3.3MB |
| `gaishoku.html` | 外食チェーン痩せメニュー54品 | 約1.0MB |
| `tool.html` | 自走式ダイエット管理ツール | 軽量 |

※ `index.html` を開くと4ツールを選べます。個別リンクを配りたい場合は各htmlのURLを直接どうぞ。
※ `tool.html` は記録データをその端末のブラウザ内（localStorage）に保存します。サーバーには何も送信しません。

## GitHub Pages で公開する手順

1. GitHubで新しいリポジトリを作成（例：`diet-list`）。Public。
2. このフォルダのHTML（index / conbini / super / gaishoku / tool）をリポジトリにアップロード
   （画面右上「Add file」→「Upload files」でドラッグ＆ドロップ）。
3. リポジトリの **Settings → Pages** を開く。
4. 「Build and deployment」→ Source を **Deploy from a branch**、
   Branch を **main / (root)** にして Save。
5. 数分待つと `https://<ユーザー名>.github.io/diet-list/` で公開されます。
   - 入口：`.../diet-list/`（index.html）
   - コンビニ：`.../diet-list/conbini.html`
   - スーパー：`.../diet-list/super.html`
   - 外食：`.../diet-list/gaishoku.html`
   - 管理ツール：`.../diet-list/tool.html`

## 更新したいとき

元ファイル（1つ上のフォルダの `コンビニ痩せ商品検索アプリ.html` など）を編集したあと、
埋め込み版を作り直して、この4ファイルを差し替えてアップロードし直せばOKです。
（埋め込み生成はAIに「公開用を作り直して」と頼めば再生成します）

## 注意
- 画像は各コンビニ・各メーカー・各チェーン公式の商品情報を参照しています。商用の大規模再配布などは各社の権利にご留意ください。
- 栄養値は参考値です（フッターにも注記あり）。
