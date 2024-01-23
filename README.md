[![test](https://github.com/ayamaruu/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/ayamaruu/mypkg/actions/workflows/test.yml)
* ロボットシステム学用のレポジトリ
* ros2のパッケージ
## 導入方法
1.ターミナルを起動し、自分がコピーしたいディレクトリに移動する
2.ターミナル上で以下のコマンドを入力する
```
git clone https://github.com/ayamaruu/mypkg.git
```
3.以下のコマンドを打つ
```
colcon build
```

## 必要なソフトウェア
* Python
  * テスト済み: 3.7~3.10
* ros2を実行できる環境

## テスト環境
* Ubuntu 22.04.2 LTS
## 1つ目の機能
* 以下のコマンドをターミナルに打ち込むと
```
ros2 launch mypkg talk_listen.launch.py
```
* 実行結果
```
[listener-2] [INFO] [1704897043.558577859] [listener]: Listen: 0
[listener-2] [INFO] [1704897044.030942269] [listener]: Listen: 1
[listener-2] [INFO] [1704897044.531111724] [listener]: Listen: 2
[listener-2] [INFO] [1704897045.034385792] [listener]: Listen: 3
[listener-2] [INFO] [1704897045.566017349] [listener]: Listen: 4
[listener-2] [INFO] [1704897046.066645821] [listener]: Listen: 5
```
## 2つ目の機能
* 1つのプログラムでtalker.pyを起動して、もう1つプログラムを立ち上げて使用する。
* 端末1で以下のコマンドを実行
```
ros2 run mypkg talker
```
* 端末2で以下のコマンドを実行
```
ros2 run mypkg listener
```
すると以下のように表示されます。
```
[INFO] [1704897459.825561039] [listener]: Listen: 33
[INFO] [1704897460.297147966] [listener]: Listen: 34
[INFO] [1704897460.808380251] [listener]: Listen: 35
[INFO] [1704897461.315765905] [listener]: Listen: 36
[INFO] [1704897461.805604665] [listener]: Listen: 37
[INFO] [1704897462.296451890] [listener]: Listen: 38
[INFO] [1704897462.801038988] [listener]: Listen: 39
[INFO] [1704897463.295524947] [listener]: Listen: 40
```
Ctrl Cを押せばプログラムは終了します。
## 備考
* このソフトウェアパッケージは、3条項BSDライセンスの下、再頒布および使用が許可されます.
* このパッケージのコードは下記のスライド(CC-BY-SA 4.0 by Ryuichi Ueda)のものを,本人の許可を得て自身の著作としたものです.
     * [ryuichiueda/my_slides robosys_2022](http://githb.com/ryuichiueda/my_slides/tree/master/robosys_2022)
* © 2023 Ayaka Murakoshi
