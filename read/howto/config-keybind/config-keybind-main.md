---
title: 設定「主要」的「按鍵綁定」
nav_order: 7010
has_children: false
parent: 設定「按鍵綁定 (Keybind)」
grand_parent: 如何
---


# 設定「主要」的「按鍵綁定」




## 主題

* [前提](#前提)
* [設定範例](#設定範例)
* [統整](#統整)
* [範例腳本](#範例腳本)
* [相關案例](#相關案例)




## 前提

延續「[設定「按鍵綁定 (Keybind)」](https://samwhelp.github.io/note-about-linuxmint-mate/read/howto/config-keybind.html)」這篇找到的設定，

以下紀錄我常用的「視窗操作按鍵綁定」來當作「[設定範例](#設定範例)」說明。

> 要注意的是，以下只是單就個別項目做說明，有些綁定可能會跟目前既有的綁定衝突，所以要設定完整，還是要做統整的設定
以下紀錄並不完全。




## 設定範例

* [Application / Main Menu](#application--main-menu)
* [Application / Runner](#application--runner)
* [Application / Launcher](#application--launcher)
* [Window / Close](#window--close)
* [Window / Toggle Maximized](#window--toggle-maximized)
* [Window / Toggle Fullscreen](#window--toggle-fullscreen)
* [Window / Show Desktop](#window--show-desktop)
* [Window / Begin Move](#window--begin-move)
* [Window / Begin Resize](#window--begin-resize)
* [Alt-Tab Switcher](#alt-tab-switcher)
* [Window / Previous](#window--previous)
* [Window / Next](#window--next)
* [Workspace / Previous](#workspace--previous)
* [Workspace / Next](#workspace--next)
* [Window / Tiling Move](#window--tiling-move)
* [Screenshot](#screenshot)
* [統整](#統整)




## Application / Main Menu

> 請參考另一篇『[停用按鍵綁定「Super_L」開啟「Main Menu」](https://samwhelp.github.io/note-about-linuxmint-mate/read/howto/disable-keybind-open-main-menu.html)』的「設定說明」。

除了上面的「Menu」綁定，在「Mate Desktop」還有另一個「 Menu」綁定，設定如下。

> 執行下面指令，綁定「`Alt + F1`」來顯示「Application Menu」。

``` sh
gsettings set org.mate.Marco.global-keybindings panel-main-menu "'<Alt>F1'"
```




## Application / Runner

> 執行下面指令，綁定「`Alt + F2`」來顯示「Application Runner」。

``` sh
gsettings set org.mate.Marco.global-keybindings panel-run-dialog "'<Alt>F2'"
```




## Application / Launcher

> 便捷開啟「常用的應用程式」，請參考『[設定「自訂」的「按鍵綁定」](https://samwhelp.github.io/note-about-linuxmint-mate/read/howto/config-keybind/config-keybind-custom.html)』這篇的設定說明。




## Window / Close

大部份的桌面環境，預設是綁定「`Alt + F4`」來「關閉視窗」。

```
org.mate.Marco.window-keybindings close '<Alt>F4'
```

我個人慣用的是綁定「`Win + q`」來「關閉視窗」。


> 執行下面指令，綁定「`Win + q`」來「關閉視窗」。

``` sh
gsettings set org.mate.Marco.window-keybindings close "'<Super>q'"
```




## Window / Toggle Maximized

> 執行下面指令，綁定「`Win + w`」來「切換視窗最大化」。

``` sh
gsettings set org.mate.Marco.window-keybindings toggle-maximized "'<Super>w'"
```




## Window / Toggle Fullscreen

> 執行下面指令，綁定「`Win + f`」來「切換視窗全螢幕」。

``` sh
gsettings set org.mate.Marco.window-keybindings toggle-fullscreen "'<Super>f'"
```




## Window / Show Desktop

> 執行下面指令，綁定「`Win + d`」來「切換顯示桌面」。

``` sh
gsettings set org.mate.Marco.global-keybindings show-desktop "'<Super>d'"
```




## Window / Begin Move

> 執行下面指令，綁定「`Win + e`」來切換到「視窗開始移動」狀態。

``` sh
gsettings set org.mate.Marco.window-keybindings begin-move "'<Super>e'"
```




## Window / Begin Resize

> 執行下面指令，綁定「`Win + r`」來切換到「視窗開始更改大小」狀態。

``` sh
gsettings set org.mate.Marco.window-keybindings begin-resize "'<Super>r'"
```


> 關於「[begin-move](#window--begin-move)」和「[begin-resize](#window--begin-resize)」，可以對照另一篇『[設定「Mouse Button Modifier」](https://samwhelp.github.io/note-about-linuxmint-mate/read/howto/config-mouse-button-modifier.html)』提到的用法。




## Alt-Tab Switcher


## Window / Previous

> 執行下面指令，綁定「`Win + a`」來切換聚焦到「`上一個視窗`」。

``` sh
gsettings set org.mate.Marco.global-keybindings switch-windows-backward "'<Super>a'"
```




## Window / Next

> 執行下面指令，綁定「`Win + s`」來切換聚焦到「`下一個視窗`」。

``` sh
gsettings set org.mate.Marco.global-keybindings switch-windows "'<Super>s'"
```




## Workspace / Previous

> 執行下面指令，綁定「`Alt + a`」來切換到「`上一個工作空間`」。

``` sh
gsettings set org.mate.Marco.global-keybindings switch-to-workspace-left  "'<Alt>a'"
```




## Workspace / Next

> 執行下面指令，綁定「`Alt + s`」來切換到「`下一個工作空間`」。

``` sh
gsettings set org.mate.Marco.global-keybindings switch-to-workspace-right  "'<Alt>s'"
```


| 方位        | 按鍵           | 功能                    |
| ----------- | -------------- | ----------------------- |
| 左 (Left)   | `Win + a`      | `Window / Previous`     |
| 右 (Right)  | `Win + s`      | `Window / Next`         |
| 左 (Left)   | `Alt + a`      | `Workspace / Previous`  |
| 右 (Right)  | `Alt + s`      | `Workspace / Next`      |

> 關於「grave」指是「`」，在「Tab鍵」上方的那個「鍵盤按鍵」。

> `Super` for `Window`

> `Alt` for `Workspace`




## Window / Tiling Move

> 設定參考指令如下

``` sh

##
## ## Window / Tiling Move
##

gsettings set org.mate.Marco.window-keybindings tile-to-corner-ne "'<Super><Shift>Down'"

gsettings set org.mate.Marco.window-keybindings tile-to-corner-nw "'<Super><Shift>Up'"

gsettings set org.mate.Marco.window-keybindings tile-to-corner-se "'<Super><Shift>Right'"

gsettings set org.mate.Marco.window-keybindings tile-to-corner-sw "'<Super><Shift>Left'"

gsettings set org.mate.Marco.window-keybindings tile-to-side-e "'<Super>Right'"

gsettings set org.mate.Marco.window-keybindings tile-to-side-w "'<Super>Left'"

```


## Screenshot

> 執行下面指令，探索關於「`screenshot`」的「按鍵綁定」設定

``` sh
gsettings list-recursively | grep screenshot | grep mate
```

顯示

```
org.mate.Marco.global-keybindings run-command-screenshot 'Print'
org.mate.Marco.global-keybindings run-command-window-screenshot '<Alt>Print'
org.mate.Marco.keybinding-commands command-screenshot 'mate-screenshot'
org.mate.Marco.keybinding-commands command-window-screenshot 'mate-screenshot --window'
org.mate.screenshot border-effect 'none'
org.mate.screenshot delay 0
org.mate.screenshot include-border true
org.mate.screenshot include-pointer true
org.mate.screenshot last-save-directory ''
```


> 執行下面指令，修改關於「`screenshot`」的「按鍵綁定」設定

``` sh

##
## ## Screenshot
##

gsettings set org.mate.Marco.global-keybindings run-command-screenshot "'Print'"

gsettings set org.mate.Marco.keybinding-commands command-screenshot "'mate-screenshot'"


##
## ## Screenshot / Window
##

gsettings set org.mate.Marco.global-keybindings run-command-window-screenshot "'<Super>Print'"

gsettings set org.mate.Marco.keybinding-commands command-window-screenshot "'mate-screenshot --window'"


##
## ## Screenshot / Area
##

gsettings set org.mate.Marco.global-keybindings run-command-2 "'<Control>Print'"

gsettings set org.mate.Marco.keybinding-commands command-2 '/bin/sh -c "sleep 0.1; mate-screenshot --area"'

```

> `Super` for `Window`

> `Control` for `Area`




## 統整

> 統整以上提到的綁定

``` sh

##
##  ## Application / Launcher
##

gsettings set org.mate.Marco.global-keybindings panel-main-menu "'<Alt>F1'"

gsettings set org.mate.Marco.global-keybindings panel-run-dialog "'<Alt>F2'"


##
## ## Window
##

gsettings set org.mate.Marco.window-keybindings close "'<Super>q'"

gsettings set org.mate.Marco.window-keybindings toggle-maximized "'<Super>w'"

gsettings set org.mate.Marco.window-keybindings toggle-fullscreen "'<Super>f'"

gsettings set org.mate.Marco.global-keybindings show-desktop "'<Super>d'"

gsettings set org.mate.Marco.window-keybindings begin-move "'<Super>e'"

gsettings set org.mate.Marco.window-keybindings begin-resize "'<Super>r'"


##
## ## Window / Switch
##

gsettings set org.mate.Marco.global-keybindings switch-windows-backward "'<Super>a'"

gsettings set org.mate.Marco.global-keybindings switch-windows "'<Super>s'"


##
## ## Workspace / Switch
##

gsettings set org.mate.Marco.global-keybindings switch-to-workspace-left  "'<Alt>a'"

gsettings set org.mate.Marco.global-keybindings switch-to-workspace-right  "'<Alt>s'"

gsettings set org.mate.Marco.global-keybindings switch-to-workspace-prev  "'<Alt>z'"


##
## ## Window / Tiling Move
##

gsettings set org.mate.Marco.window-keybindings tile-to-corner-ne "'<Super><Shift>Down'"

gsettings set org.mate.Marco.window-keybindings tile-to-corner-nw "'<Super><Shift>Up'"

gsettings set org.mate.Marco.window-keybindings tile-to-corner-se "'<Super><Shift>Right'"

gsettings set org.mate.Marco.window-keybindings tile-to-corner-sw "'<Super><Shift>Left'"

gsettings set org.mate.Marco.window-keybindings tile-to-side-e "'<Super>Right'"

gsettings set org.mate.Marco.window-keybindings tile-to-side-w "'<Super>Left'"


##
## ## Screenshot
##

gsettings set org.mate.Marco.global-keybindings run-command-screenshot "'Print'"

gsettings set org.mate.Marco.keybinding-commands command-screenshot "'mate-screenshot'"


##
## ## Screenshot / Window
##

gsettings set org.mate.Marco.global-keybindings run-command-window-screenshot "'<Super>Print'"

gsettings set org.mate.Marco.keybinding-commands command-window-screenshot "'mate-screenshot --window'"


##
## ## Screenshot / Area
##

gsettings set org.mate.Marco.global-keybindings run-command-2 "'<Control>Print'"

gsettings set org.mate.Marco.keybinding-commands command-2 '/bin/sh -c "sleep 0.1; mate-screenshot --area"'

```


> 另外關於「Workspace」，我會做如下的額外設定


``` sh

gsettings set org.mate.Marco.general num-workspaces 5


gsettings set org.mate.Marco.workspace-names name-1 'File'

gsettings set org.mate.Marco.workspace-names name-2 'Edit'

gsettings set org.mate.Marco.workspace-names name-3 'Web'

gsettings set org.mate.Marco.workspace-names name-4 'Term'

gsettings set org.mate.Marco.workspace-names name-5 'Misc'

```




## 範例腳本

* [範例腳本](https://github.com/samwhelp/note-about-linuxmint-mate/tree/gh-pages/_demo/scripts/mate-keybind)




## 相關案例

* [mate-keybind-main](https://github.com/samwhelp/note-about-ubuntu/blob/gh-pages/_demo/adjustment/de/mate/part/mate-keybind-main/config-install.sh)
* [/usr/share/glib-2.0/schemas/50_mate-keybind-main.gschema.override](https://github.com/samwhelp/lika-live-build-respin-mate/blob/main/asset/overlay/usr/share/glib-2.0/schemas/50_mate-keybind-main.gschema.override)
