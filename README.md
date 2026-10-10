# 排水勾配計算 Webアプリ

## 内容
- 必要落差計算（管長＋勾配 1/N）
- 実測判定（水平距離、起点・終点標高）
- 長距離の等分割計算（最大20区間）
- 計算結果コピー
- 履歴保存（ブラウザーのローカルストレージ、最大30件）
- iPhoneホーム画面追加用 manifest / アイコン
- Service Workerによるキャッシュ

## 公開方法（GitHub Pages）
1. GitHubにログインし、New repositoryを作成。例：`haisui-slope`
2. リポジトリを Public にする（GitHub FreeでPagesを使う場合）。
3. このZIPを展開し、中の5ファイル（`index.html`, `manifest.webmanifest`, `sw.js`, `icon.svg`, `README.md`）をリポジトリ直下にアップロードする。
4. リポジトリの Settings → Pages を開く。
5. Build and deployment の Source を `Deploy from a branch` にし、Branch を `main`、フォルダーを `/(root)` にして Save。
6. 公開が完了すると `https://ユーザー名.github.io/haisui-slope/` のようなURLが表示される。URLをSafariで開く。
7. GitHub PagesはHTTPSで配信される。公開サイトはインターネット上で誰でも見られるので、個人情報を入れないこと。

## iPhoneホーム画面への追加
1. iPhoneのSafariで公開URLを開く（アプリ内ブラウザーではなくSafari）。
2. 共有ボタンをタップ。
3. 「ホーム画面に追加」を選択。
4. 「Webアプリとして開く」が表示されたらオンにし、「追加」。
5. ホーム画面の「排水勾配」アイコンから起動。

## 注意
- 公開作業は利用者のGitHubアカウントで行う必要があります。このZIPを作成しただけでは、Web上にはまだ公開されていません。
- 適用勾配は管径・管種・用途・設計図書・現場条件で異なります。計算結果は理論値であり、法定・設計適合の判定を保証しません。
