# asdf
ランタイムとかのバージョン管理ツール。anyenv みたいなイメージ。

Kubernetes のCLIとか管理できるらしい

$ git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.8.0

$ source ~/.asdf/asdf.fish
$ mkdir -p ~/.config/fish/completions; and cp ~/.asdf/completions/asdf.fish ~/.config/fish/completions


各種必要になってくるだろうパッケージを入れておく。

$ sudo apt install -y automake autoconf libreadline-dev libncurses-dev libssl-dev libyaml-dev libxslt-dev libffi-dev libtool unixodbc-dev

リストはここから
https://qiita.com/kikuchi_kentaro/items/d951fa7ca7c9c29a77dc


## Python

```
$ asdf install python 3.7.4
:
WARNING: The Python bz2 extension was not compiled. Missing the bzip2 lib?
WARNING: The Python sqlite3 extension was not compiled. Missing the SQLite3 lib?
:
```

パッケージが無いせいでコンパイルしなかったものがあるらしい。

```
$ sudo apt install -y libbz2-dev libreadline-dev libsqlite3-dev
```

入れ直し。

```
$ asdf uninstall python 3.7.4
$ asdf install python 3.7.4
```


