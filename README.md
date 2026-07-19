
[torabo-tsuki LP](https://github.com/sekigon-gonnoc/torabo-tsuki-lp)用のZMKファームウェア

* _centralがついているuf2をトラックボールがついている方に、_peripheralを反対側に書き込んでください
* キーマップはkeymap-editorおよびzmk-studioで編集できます

## オートマウスレイヤー

`feature/auto-mouse-layer` ブランチでは、トラックボールを動かすと layer 1（マウスボタン）が自動で有効になり、約1秒無操作で解除されます。

* 打鍵直後の誤発動抑制: `require-prior-idle-ms = 350`（`config/keymap.keymap`）
* 元の設定に戻す: `git checkout master`
* 調整を続ける: `git checkout feature/auto-mouse-layer`