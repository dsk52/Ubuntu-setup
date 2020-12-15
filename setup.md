$ sudo apt update && sudo apt upgrade


## Setting

* タッチバー無効化
設定 > 「マウスとタッチパッド」からタッチパッドを無効化

* CapsLock to Ctrl

$ sudo nano /etc/default/keyboard

:
XKBVARIANT=""
XKBOPTIONS=""
↓
KBVARIANT=""
XKBOPTIONS="ctrl:nocaps"

保存

$ reboot

https://linux.just4fun.biz/?Ubuntu/Caps-Lock%E3%82%AD%E3%83%BC%E3%82%92Ctrl%E3%82%AD%E3%83%BC%E3%81%AB%E3%81%99%E3%82%8B%E6%96%B9%E6%B3%95


マウス
https://www.yokoweb.net/2020/05/15/ubuntu-desktop-solaar-install/

$ sudo apt install solaar

ドングル挿してマウスを動かしたらペアリングできた


## 入力

$ sudo apt install fcitx fcitx-mozc -y
「言語サポート」のキーボードの入力に使うIMシステムからfcitxを選択

## Terminal

$ sudo apt-add-repository ppa:fish-shell/release-3
$ sudo apt-get update
$ sudo apt-get install fish

$ chsh -s /usr/bin/fish 

reboot しないと有効にならない

$ curl https://git.io/fisher --create-dirs -sLo ~/.config/fish/functions/fisher.fish


### ホームディレクトリ以下のディレクトリ名を日本語から英語に変える

$ LANG=C xdg-user-dirs-gtk-update

出てきたポップアップの内容を確認してUpdateなボタンをクリック

https://www.rough-and-cheap.jp/linux/ubuntu-change-xdg-directory-name/

