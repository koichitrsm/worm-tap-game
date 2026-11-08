# WORM — tap and hold

スマートフォンの画面を押し続けると、黒い細いクネクネしたラインが指先へ集まり、指を離すと消えるミニゲームです。

## GitHub Pagesで公開する方法

1. GitHubにログインし、右上の **New repository** を選択。
2. Repository name を `worm-tap-game` などにする。
3. Public を選択して **Create repository**。
4. このZIPを展開し、`index.html` と `manifest.webmanifest` をリポジトリ直下にアップロード（Add file → Upload files）。
5. リポジトリの **Settings → Pages** を開く。
6. Build and deployment の Source を **Deploy from a branch** にする。
7. Branch を `main`、フォルダを `/ (root)` にして **Save**。
8. 数分後、`https://あなたのユーザー名.github.io/worm-tap-game/` で公開されます。

## スマートフォンで遊ぶ

公開URLをiPhoneまたはAndroidのブラウザで開いてください。iPhoneは共有メニューの「ホーム画面に追加」、Androidはブラウザメニューの「ホーム画面に追加」からアプリのように起動できます。

## 調整ポイント

`index.html` 内の `makeWorm()` と `loop()` で、ラインの長さ・本数・出現速度を調整できます。現在は約58〜84 CSS px（画面上で約2cmを目安）で、ラインごとに長さ・太さ・うねり方・速度に個体差をつけています。指に近づくほど振幅が大きくなり、指を離すと煙状の粒子に分散して消えます。押した瞬間から最低5本が表示され、その後は5〜20本を目安に変化します。
