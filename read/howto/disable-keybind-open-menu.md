---
title: 停用按鍵綁定「Super_L」開啟「Menu」
nav_order: 7022
has_children: false
parent: 如何
---


# 停用按鍵綁定「Super_L」開啟「Menu」




## 主題

* [前提](#前提)
* [調整設定指令](#調整設定指令)
* [相關議題](#相關議題)






## 前提

在「Linux Mint Mate Desktop」，預設是綁定「`Win鍵`」來觸發「開啟」或「關閉」「主要功能選單」。

可以執行下面指令，找到該設定。

``` sh
gsettings list-recursively | grep 'Super_L'
```


顯示類似如下

```
com.linuxmint.mintmenu hot-key 'Super_L'
```




## 調整設定指令

執行下面指令，停用按鍵綁定「`Super_L`」開啟「Menu」

``` sh
gsettings set com.linuxmint.mintmenu hot-key ''
```




## 恢復指令

若要恢復原本的設定，則是可以執行下面的指令

``` sh
gsettings reset com.linuxmint.mintmenu hot-key
```

或是執行下面的指令，恢復原本的設定

``` sh
gsettings set com.linuxmint.mintmenu hot-key 'Super_L'
```

執行下面的指令，則是觀看目前的設定值

``` sh
gsettings get com.linuxmint.mintmenu hot-key
```

顯示

```
'Super_L'
```




## 相關議題

| 相關議題 |
| ------- |
| [設定「Mouse Button Modifier」](https://samwhelp.github.io/note-about-linuxmint-mate/read/howto/config-mouse-button-modifier.html) |




## gschema

| gschema |
| ------- |
| `/usr/share/glib-2.0/schemas/com.linuxmint.mintmenu.gschema.xml` |


執行下面指令

``` sh
grep 'hot-key' /usr/share/glib-2.0/schemas/com.linuxmint.mintmenu.gschema.xml -A 4
```

顯示

``` xml
    <key type="s" name="hot-key">
      <default>"Super_L"</default>
      <summary></summary>
      <description></description>
    </key>
```
