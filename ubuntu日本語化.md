# MacのUbuntu日本語化（JIS配列）
GPG鍵とレポジトリインストール

https://www.ubuntulinux.jp/japanese(以下コピペ）


Ubuntu 20.04 LTSの場合:
```
wget -q https://www.ubuntulinux.jp/ubuntu-ja-archive-keyring.gpg -O- | sudo apt-key add -
wget -q https://www.ubuntulinux.jp/ubuntu-jp-ppa-keyring.gpg -O- | sudo apt-key add -
sudo wget https://www.ubuntulinux.jp/sources.list.d/focal.list -O /etc/apt/sources.list.d/ubuntu-ja.list

sudo apt update
```

Ubuntu 18.04 LTSの場合:
```
wget -q https://www.ubuntulinux.jp/ubuntu-ja-archive-keyring.gpg -O- | sudo apt-key add -
wget -q https://www.ubuntulinux.jp/ubuntu-jp-ppa-keyring.gpg -O- | sudo apt-key add -
sudo wget https://www.ubuntulinux.jp/sources.list.d/bionic.list -O /etc/apt/sources.list.d/ubuntu-ja.list

sudo apt update
```

Ubuntu 16.04 LTSの場合:
```
wget -q https://www.ubuntulinux.jp/ubuntu-ja-archive-keyring.gpg -O- | sudo apt-key add -
wget -q https://www.ubuntulinux.jp/ubuntu-jp-ppa-keyring.gpg -O- | sudo apt-key add -
sudo wget https://www.ubuntulinux.jp/sources.list.d/xenial.list -O /etc/apt/sources.list.d/ubuntu-ja.list

sudo apt update
```

その後
```
sudo apt-get upgrade
```

（コピペ終わり）


日本語（Mozc）入れる
Mozcプロパティ→キー設定→キー設定の選択の編集から
変換前入力中、変換中、直接入力、入力文字なしそれぞれで

- かなキー→IMEを有効化
- 英数キー→IMEを無効化

を設定する。

キーボードレイアウト変更

https://qiita.com/vochicong/items/6452ac54bde56b0e0bb3（以下コピペ）

コンソールで使うキーボードレイアウトの設定
```
sudo dpkg-reconfigure keyboard-configuration
```

`Generic 105-key PC (intl.)` → `Japanese` → `Japanese` → `The default for the keyboard layout` → `No compose key` → `Yes` と入力する。

X(GUI)で使うキーボードレイアウトの設定
```
gnome-session-properties
```

`Add` → コマンドに `setxkbmap jp` → `Save`
スタートアップなので名前は好きなものを

(コピペおわり）

]が入力できてればヨシ