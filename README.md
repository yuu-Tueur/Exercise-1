# Exercise-1
これはロボットシステム学の課題１です

# 内容
このデバイスドライバーは講義内で作成したものに変更を加えて作成したものです

実行するとモールス信号で”SOS”と点滅します

# 動作環境
・Raspberry Pi 4

・Ubuntu 20.04.1

# 準備物
・Raspberry Pi 4

・ブレッドボード

・LED(今回は白を使用)

・ジャンパー線 オス−メス ×２

# 回路
LEDのアノードをGPIO25に接続しカソードをGNDに接続

# 実行方法
実行は下記の通りに行います
```
git clone https://github.com/yuu-Tueur/Exercise-1.git
cd Exercise-1/myled
make
sudo rmmod myled
sudo insmod myled.ko
sudo chmod 666 /dev/myled0
echo 0 > /dev/myled0 
```

# makeでエラーが出る場合
makeをした後に
```
Makefile:8: *** 分離記号を欠いています (8 個の空白でしたが, TAB のつもりでしたか?).  中止.
```
とエラーが出る場合があります

その場合は8,11行目の先頭の空白をTABに変更してください

# 実行動画
下記のURLからご覧になれます

<https://youtu.be/XVD8Ys5L_7Q>

# ライセンス
GNU General Public License v3.0
