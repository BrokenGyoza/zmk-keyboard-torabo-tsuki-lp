
[torabo-tsuki LP](https://github.com/sekigon-gonnoc/torabo-tsuki-lp)用のZMKファームウェア

* _centralがついているuf2をトラックボールがついている方に、_peripheralを反対側に書き込んでください
* キーマップはkeymap-editorおよびzmk-studioで編集できます

## オートマウスレイヤー

`feature/auto-mouse-layer` ブランチでは、BrokenGyoza の `master` キーマップをベースに、トラックボール移動で layer 1（マウスパッド層）が自動有効になり、約1秒無操作で解除されます。

* 打鍵直後の誤発動抑制: `require-prior-idle-ms = 350`（`config/keymap.keymap`）
* 元のキーマップのみに戻す: GitHub の `master` ブランチ
* AML 付きで使う: `feature/auto-mouse-layer`

## ホールドスクロール

`feature/hold-to-scroll` ブランチでは、上記の AML に加えて、layer 1 の左クリックの一つ下のキー（position 47）を押している間だけ layer 4 に入り、ボールの移動がスクロールになります。

* 離せばすぐカーソル移動に戻ります
* スクロールの向きが逆なら `config/keymap.keymap` の `scroller` 内の `INPUT_TRANSFORM_X_INVERT` / `INPUT_TRANSFORM_Y_INVERT` を調整してください
* AML のみで使う: `feature/auto-mouse-layer`