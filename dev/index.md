## 開発用
$ sudo apt install vim

$ sudo apt install git


$ sudo apt install docker


VSCode
公式の .deb ファイルを落としてみたけどうまく入れられなかったので以下の記事を実行。インストールされた
https://mebee.info/2020/03/18/post-7546/



## Node.js setup

nvm install

```
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.0/install.sh | bash
```

fish setting

```
$ fisher install jorgebucaran/nvm.fish


$ nvm use lts
```

ex.
$ node -v > .nvmrc
$ nvm

$ node -v
14.15.0


Uninstall  
asdf に移行。

```
$ fisher uninstall jorgebucaran/nvm.fish
$ rm ~/.nvm 
```

## gibo

```
$ curl -L https://raw.github.com/simonwhitaker/gibo/master/gibo \
    -so ~/bin/gibo && chmod +x ~/bin/gibo && gibo update
```
