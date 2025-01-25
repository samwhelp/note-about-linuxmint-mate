---
title: 設定「按鍵綁定 (Keybind)」
nav_order: 7030
has_children: true
parent: 如何
---


# 設定「按鍵綁定 (Keybind)」




## 主題

* [前提](#前提)
* [設定方式](#設定方式)
* [相關議題](#相關議題)




## 前提

> 執行下面指令，探索關於「`keybind`」的設定。

``` sh
gsettings list-recursively | grep 'keybind'
```

顯示如下 (有很多，就不列了在此，請參考我放在「GitHub」上的[紀錄](https://github.com/samwhelp/linuxmint-mate-adjustment/blob/main/sample/22.1/dump/keybind/keybind.txt))


> 執行下面指令，進一步篩選出顯示結果

``` sh
gsettings list-recursively | grep keybind | grep mate
```

顯示

```
org.mate.Marco.global-keybindings cycle-group '<Alt>F6'
org.mate.Marco.global-keybindings cycle-group-backward 'disabled'
org.mate.Marco.global-keybindings cycle-panels '<Control><Alt>Escape'
org.mate.Marco.global-keybindings cycle-panels-backward 'disabled'
org.mate.Marco.global-keybindings cycle-windows '<Alt>Escape'
org.mate.Marco.global-keybindings cycle-windows-backward 'disabled'
org.mate.Marco.global-keybindings panel-main-menu '<Alt>F1'
org.mate.Marco.global-keybindings panel-run-dialog '<Alt>F2'
org.mate.Marco.global-keybindings rename-workspace 'disabled'
org.mate.Marco.global-keybindings run-command-1 'disabled'
org.mate.Marco.global-keybindings run-command-10 'disabled'
org.mate.Marco.global-keybindings run-command-11 'disabled'
org.mate.Marco.global-keybindings run-command-12 'disabled'
org.mate.Marco.global-keybindings run-command-2 'disabled'
org.mate.Marco.global-keybindings run-command-3 'disabled'
org.mate.Marco.global-keybindings run-command-4 'disabled'
org.mate.Marco.global-keybindings run-command-5 'disabled'
org.mate.Marco.global-keybindings run-command-6 'disabled'
org.mate.Marco.global-keybindings run-command-7 'disabled'
org.mate.Marco.global-keybindings run-command-8 'disabled'
org.mate.Marco.global-keybindings run-command-9 'disabled'
org.mate.Marco.global-keybindings run-command-screenshot 'Print'
org.mate.Marco.global-keybindings run-command-terminal '<Primary><Alt>t'
org.mate.Marco.global-keybindings run-command-window-screenshot '<Alt>Print'
org.mate.Marco.global-keybindings show-desktop '<Control><Alt>d'
org.mate.Marco.global-keybindings switch-group '<Alt>grave'
org.mate.Marco.global-keybindings switch-group-backward 'disabled'
org.mate.Marco.global-keybindings switch-panels '<Control><Alt>Tab'
org.mate.Marco.global-keybindings switch-panels-backward 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-1 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-10 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-11 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-12 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-2 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-3 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-4 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-5 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-6 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-7 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-8 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-9 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-down '<Control><Alt>Down'
org.mate.Marco.global-keybindings switch-to-workspace-left '<Control><Alt>Left'
org.mate.Marco.global-keybindings switch-to-workspace-prev 'disabled'
org.mate.Marco.global-keybindings switch-to-workspace-right '<Control><Alt>Right'
org.mate.Marco.global-keybindings switch-to-workspace-up '<Control><Alt>Up'
org.mate.Marco.global-keybindings switch-windows '<Alt>Tab'
org.mate.Marco.global-keybindings switch-windows-all 'disabled'
org.mate.Marco.global-keybindings switch-windows-all-backward 'disabled'
org.mate.Marco.global-keybindings switch-windows-backward 'disabled'
org.mate.Marco.keybinding-commands command-1 ' '
org.mate.Marco.keybinding-commands command-10 ' '
org.mate.Marco.keybinding-commands command-11 ' '
org.mate.Marco.keybinding-commands command-12 ' '
org.mate.Marco.keybinding-commands command-2 ' '
org.mate.Marco.keybinding-commands command-3 ' '
org.mate.Marco.keybinding-commands command-4 ' '
org.mate.Marco.keybinding-commands command-5 ' '
org.mate.Marco.keybinding-commands command-6 ' '
org.mate.Marco.keybinding-commands command-7 ' '
org.mate.Marco.keybinding-commands command-8 ' '
org.mate.Marco.keybinding-commands command-9 ' '
org.mate.Marco.keybinding-commands command-screenshot 'mate-screenshot'
org.mate.Marco.keybinding-commands command-window-screenshot 'mate-screenshot --window'
org.mate.Marco.window-keybindings activate-window-menu '<Alt>space'
org.mate.Marco.window-keybindings begin-move '<Alt>F7'
org.mate.Marco.window-keybindings begin-resize '<Alt>F8'
org.mate.Marco.window-keybindings close '<Alt>F4'
org.mate.Marco.window-keybindings lower 'disabled'
org.mate.Marco.window-keybindings maximize 'disabled'
org.mate.Marco.window-keybindings maximize-horizontally 'disabled'
org.mate.Marco.window-keybindings maximize-vertically 'disabled'
org.mate.Marco.window-keybindings minimize '<Alt>F9'
org.mate.Marco.window-keybindings move-to-center 'disabled'
org.mate.Marco.window-keybindings move-to-corner-ne 'disabled'
org.mate.Marco.window-keybindings move-to-corner-nw 'disabled'
org.mate.Marco.window-keybindings move-to-corner-se 'disabled'
org.mate.Marco.window-keybindings move-to-corner-sw 'disabled'
org.mate.Marco.window-keybindings move-to-monitor-e 'disabled'
org.mate.Marco.window-keybindings move-to-monitor-n 'disabled'
org.mate.Marco.window-keybindings move-to-monitor-s 'disabled'
org.mate.Marco.window-keybindings move-to-monitor-w 'disabled'
org.mate.Marco.window-keybindings move-to-side-e 'disabled'
org.mate.Marco.window-keybindings move-to-side-n 'disabled'
org.mate.Marco.window-keybindings move-to-side-s 'disabled'
org.mate.Marco.window-keybindings move-to-side-w 'disabled'
org.mate.Marco.window-keybindings move-to-workspace-1 'disabled'
org.mate.Marco.window-keybindings move-to-workspace-10 'disabled'
org.mate.Marco.window-keybindings move-to-workspace-11 'disabled'
org.mate.Marco.window-keybindings move-to-workspace-12 'disabled'
org.mate.Marco.window-keybindings move-to-workspace-2 'disabled'
org.mate.Marco.window-keybindings move-to-workspace-3 'disabled'
org.mate.Marco.window-keybindings move-to-workspace-4 'disabled'
org.mate.Marco.window-keybindings move-to-workspace-5 'disabled'
org.mate.Marco.window-keybindings move-to-workspace-6 'disabled'
org.mate.Marco.window-keybindings move-to-workspace-7 'disabled'
org.mate.Marco.window-keybindings move-to-workspace-8 'disabled'
org.mate.Marco.window-keybindings move-to-workspace-9 'disabled'
org.mate.Marco.window-keybindings move-to-workspace-down '<Control><Shift><Alt>Down'
org.mate.Marco.window-keybindings move-to-workspace-left '<Control><Shift><Alt>Left'
org.mate.Marco.window-keybindings move-to-workspace-right '<Control><Shift><Alt>Right'
org.mate.Marco.window-keybindings move-to-workspace-up '<Control><Shift><Alt>Up'
org.mate.Marco.window-keybindings raise 'disabled'
org.mate.Marco.window-keybindings raise-or-lower 'disabled'
org.mate.Marco.window-keybindings tile-to-corner-ne 'disabled'
org.mate.Marco.window-keybindings tile-to-corner-nw 'disabled'
org.mate.Marco.window-keybindings tile-to-corner-se 'disabled'
org.mate.Marco.window-keybindings tile-to-corner-sw 'disabled'
org.mate.Marco.window-keybindings tile-to-side-e 'disabled'
org.mate.Marco.window-keybindings tile-to-side-w 'disabled'
org.mate.Marco.window-keybindings toggle-above 'disabled'
org.mate.Marco.window-keybindings toggle-fullscreen 'disabled'
org.mate.Marco.window-keybindings toggle-maximized '<Alt>F10'
org.mate.Marco.window-keybindings toggle-on-all-workspaces 'disabled'
org.mate.Marco.window-keybindings toggle-shaded 'disabled'
org.mate.Marco.window-keybindings unmaximize '<Alt>F5'
org.mate.SettingsDaemon.plugins.keybindings active true
org.mate.SettingsDaemon.plugins.keybindings priority 6
org.mate.terminal.keybindings close-tab '<Ctrl><Shift>w'
org.mate.terminal.keybindings close-window '<Ctrl><Shift>q'
org.mate.terminal.keybindings copy '<Ctrl><Shift>c'
org.mate.terminal.keybindings detach-tab 'disabled'
org.mate.terminal.keybindings full-screen 'F11'
org.mate.terminal.keybindings help 'F1'
org.mate.terminal.keybindings move-tab-left '<Ctrl><Shift>Page_Up'
org.mate.terminal.keybindings move-tab-right '<Ctrl><Shift>Page_Down'
org.mate.terminal.keybindings new-profile 'disabled'
org.mate.terminal.keybindings new-tab '<Ctrl><Shift>t'
org.mate.terminal.keybindings new-window '<Ctrl><Shift>n'
org.mate.terminal.keybindings next-profile '<Alt>Page_Down'
org.mate.terminal.keybindings next-tab '<Control>Page_Down'
org.mate.terminal.keybindings paste '<Ctrl><Shift>v'
org.mate.terminal.keybindings prev-profile '<Alt>Page_Up'
org.mate.terminal.keybindings prev-tab '<Control>Page_Up'
org.mate.terminal.keybindings reset 'disabled'
org.mate.terminal.keybindings reset-and-clear 'disabled'
org.mate.terminal.keybindings save-contents 'disabled'
org.mate.terminal.keybindings search-find '<Ctrl><Shift>f'
org.mate.terminal.keybindings search-find-next '<Ctrl><Shift>h'
org.mate.terminal.keybindings search-find-previous '<Ctrl><Shift>g'
org.mate.terminal.keybindings select-all '<Ctrl><Shift>a'
org.mate.terminal.keybindings set-terminal-title 'disabled'
org.mate.terminal.keybindings switch-to-tab-1 '<Alt>1'
org.mate.terminal.keybindings switch-to-tab-10 '<Alt>0'
org.mate.terminal.keybindings switch-to-tab-11 'disabled'
org.mate.terminal.keybindings switch-to-tab-12 'disabled'
org.mate.terminal.keybindings switch-to-tab-2 '<Alt>2'
org.mate.terminal.keybindings switch-to-tab-3 '<Alt>3'
org.mate.terminal.keybindings switch-to-tab-4 '<Alt>4'
org.mate.terminal.keybindings switch-to-tab-5 '<Alt>5'
org.mate.terminal.keybindings switch-to-tab-6 '<Alt>6'
org.mate.terminal.keybindings switch-to-tab-7 '<Alt>7'
org.mate.terminal.keybindings switch-to-tab-8 '<Alt>8'
org.mate.terminal.keybindings switch-to-tab-9 '<Alt>9'
org.mate.terminal.keybindings toggle-menubar 'disabled'
org.mate.terminal.keybindings zoom-in '<Ctrl>plus'
org.mate.terminal.keybindings zoom-normal '<Ctrl>0'
org.mate.terminal.keybindings zoom-out '<Ctrl>minus'
```


> 也可以執行下面指令，進一步篩選出顯示結果

``` sh
gsettings list-recursively | grep org.mate.Marco.global-keybindings
```

> 也可以執行下面指令，進一步篩選出顯示結果

``` sh
gsettings list-recursively | grep org.mate.Marco.keybinding-command
```

> 也可以執行下面指令，進一步篩選出顯示結果

``` sh
gsettings list-recursively | grep org.mate.Marco.window-keybindings
```

> 相關的指令和顯示結果，我有放在「[GitHub](https://github.com/samwhelp/linuxmint-mate-adjustment/tree/main/sample/22.1/dump/keybind)」上。




## 設定方式

> 接著我們在『[設定「主要」的「按鍵綁定」](https://samwhelp.github.io/note-about-linuxmint-mate/read/howto/config-keybind/config-keybind-main.html)』這篇來說明如何修改設定。




## 相關議題

* [設定「主要」的「按鍵綁定」](https://samwhelp.github.io/note-about-linuxmint-mate/read/howto/config-keybind/config-keybind-main.html)
* [設定「自訂」的「按鍵綁定」](https://samwhelp.github.io/note-about-linuxmint-mate/read/howto/config-keybind/config-keybind-custom.html)
