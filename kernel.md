# ハードでいろいろ問題があった

* HDMI出力ができない
* スピーカーでの出力ができない

みたいな問題があった。

結論から言えば、Kernel を 5.4.53 から 5.8.18 までアップデート。

Thinkpad T14 gen 1 ryzen 4750u ubuntu compatibility - Reddit
https://www.reddit.com/r/linuxhardware/comments/imc4o4/thinkpad_t14_gen_1_ryzen_4750u_ubuntu/

5.8にあげたらいいよって話があったけど、5.8 っていう指定だと 5.8.0-23 〜 5.8.0-29 なバージョンで試してだめだった。

apt のコマンドだと候補に出ないから、mainline

```
$ sudo add-apt-repository ppa:cappelikan/ppa
$ sudo apt update
$ sudo apt install mainline
```

再起動してHDMIを繋いだらディスプレイへの出力ができた。
同時にサウンドも解決。

