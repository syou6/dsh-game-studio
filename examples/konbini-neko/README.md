# 深夜のコンビニ猫

DSH Game Studio の `collector`（2D）テンプレートから作ったサンプルゲームです。

> 「黒猫が深夜のコンビニでおにぎりを集め、おそうじロボから逃げる」

- **遊び方**: `dist/index.html` をブラウザで開くだけ（オフライン・1ファイル）。WASD／矢印キー／ドラッグで移動、P で一時停止、M で消音。
- **ルール**: 60秒でおにぎりをできるだけ集める。ロボに3回ぶつかるとアウト。おにぎり5個ごとに「ダンボール」で4秒間無敵。
- **キャラクター**: 黒猫・おそうじロボ・おにぎり・コンビニの床はすべて `game.js` の `drawCat` / `drawRobot` / `drawOnigiri` / `drawStoreFloor` でコード描画。`game_studio_generate_asset` で生成したアートを適用すると、そのスロットだけ画像に切り替わります。
- **再ビルド**: `game.json` や `game.js` を編集したら、DSH なら `game_studio_build`、手元なら `buildProject()`（`src/build.ts`）で `dist/index.html` を作り直します。
