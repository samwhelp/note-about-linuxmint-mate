---
title: 設定「自訂」的「按鍵綁定」
nav_order: 7020
has_children: false
parent: 設定「按鍵綁定 (Keybind)」
grand_parent: 如何
---


# 設定「自訂」的「按鍵綁定」




## 主題

* [前提](#前提)
* [設定範例](#設定範例)
* [範例腳本](#範例腳本)
* [相關案例](#相關案例)




## 前提




## 設定範例

``` sh

##
## ## Clear Old
##

dconf reset -f /org/mate/desktop/keybindings/




##
## ## Keybind Item
##


## ### Logout
dconf write /org/mate/desktop/keybindings/system-logout/name "'System_Logout'"
dconf write /org/mate/desktop/keybindings/system-logout/action "'mate-session-save --logout-dialog'"
dconf write /org/mate/desktop/keybindings/system-logout/binding "'<Shift><Alt>x'"


## ### Shutdown
dconf write /org/mate/desktop/keybindings/system-shutdown/name "'System_Shutdown'"
dconf write /org/mate/desktop/keybindings/system-shutdown/action "'mate-session-save --shutdown-dialog'"
dconf write /org/mate/desktop/keybindings/system-shutdown/binding "'<Shift><Alt>z'"


## ### System Settings
dconf write /org/mate/desktop/keybindings/control-center/name "'Control_Center'"
dconf write /org/mate/desktop/keybindings/control-center/action "'mate-control-center'"
dconf write /org/mate/desktop/keybindings/control-center/binding "'<Shift><Alt>s'"


## ### Terminal
dconf write /org/mate/desktop/keybindings/terminal/name "'Terminal'"
dconf write /org/mate/desktop/keybindings/terminal/action "'mate-terminal'"
dconf write /org/mate/desktop/keybindings/terminal/binding "'<Alt>Return'"


## ### Terminal-1
dconf write /org/mate/desktop/keybindings/terminal-1/name "'Terminal-1'"
dconf write /org/mate/desktop/keybindings/terminal-1/action "'mate-terminal'"
dconf write /org/mate/desktop/keybindings/terminal-1/binding "'<Shift><Alt>a'"


## ### File Manager
dconf write /org/mate/desktop/keybindings/file-manager/name "'File_Manager'"
dconf write /org/mate/desktop/keybindings/file-manager/action "'caja'"
dconf write /org/mate/desktop/keybindings/file-manager/binding "'<Shift><Alt>f'"


## ### File Manager-1
dconf write /org/mate/desktop/keybindings/file-manager-1/name "'File_Manager-1'"
dconf write /org/mate/desktop/keybindings/file-manager-1/action "'thunar'"
dconf write /org/mate/desktop/keybindings/file-manager-1/binding "'<Shift><Alt>g'"


## ### Text Editor
dconf write /org/mate/desktop/keybindings/text-editor/name "'Text_Editor'"
dconf write /org/mate/desktop/keybindings/text-editor/action "'xed'"
dconf write /org/mate/desktop/keybindings/text-editor/binding "'<Shift><Alt>e'"


## ### Web Browser
dconf write /org/mate/desktop/keybindings/web-browser/name "'Web_Browser'"
dconf write /org/mate/desktop/keybindings/web-browser/action "'firefox --new-tab about:blank'"
dconf write /org/mate/desktop/keybindings/web-browser/binding "'<Shift><Alt>b'"

```

> 上面設定完後，就會綁定成功。

> 可以執行下面指令，觀看目前的設定值。

``` sh

dconf dump /org/mate/desktop/keybindings/

```

顯示

```
[control-center]
action='mate-control-center'
binding='<Shift><Alt>s'
name='Control_Center'

[file-manager-1]
action='pcmanfm-qt'
binding='<Shift><Alt>g'
name='File_Manager-1'

[file-manager]
action='caja'
binding='<Shift><Alt>f'
name='File_Manager'

[system-logout]
action='mate-session-save --logout-dialog'
binding='<Shift><Alt>x'
name='System_Logout'

[system-shutdown]
action='mate-session-save --shutdown-dialog'
binding='<Shift><Alt>z'
name='System_Shutdown'

[terminal-1]
action='mate-terminal'
binding='<Shift><Alt>a'
name='Terminal-1'

[terminal]
action='mate-terminal'
binding='<Alt>Return'
name='Terminal'

[text-editor]
action='xed'
binding='<Shift><Alt>e'
name='Text_Editor'

[web-browser]
action='firefox --new-tab about:blank'
binding='<Shift><Alt>b'
name='Web_Browser'
```

> 注意: 目前按鍵綁定觸發「`caja`」，測試結果並不會觸發，我目前也不曉得原因
，所以可以改綁定其他的「File Manager」，例如「`thunar`」或「`pcmanfm-qt`」。



## 範例腳本

* [範例腳本](https://github.com/samwhelp/note-about-linuxmint-mate/tree/gh-pages/_demo/scripts/cinnamon-keybind)




## 相關案例

* [mate-keybind-custom](https://github.com/samwhelp/note-about-ubuntu/blob/gh-pages/_demo/adjustment/de/mate/part/mate-keybind-custom/config-install.sh)
* [/etc/dconf/db/distro.d/50_mate-keybind-custom.conf](https://github.com/samwhelp/lika-live-build-respin-mate/blob/main/asset/overlay/etc/dconf/db/distro.d/50_mate-keybind-custom.conf)
