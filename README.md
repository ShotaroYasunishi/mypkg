## ros2mypkg
mypkg外のサービスが呼び出された時処理です。mypkg外のサービスをQuery.srvと置いています。
## talker.py
・リクエストした名前によって返すデータが違うノードです。
1回サービスを呼び出したら終了です。
送信されるメッセージの型Query.srvは
```bash
string name
---
uint8 age
```
となっています。

## listener.py
・talker.pyから送信されたメッセージをトピックからサブスクライバーで受信するノードです。
別の端末で実行することでメッセージの表示が可能です。

## talk_listen.launch.py
・talker.pyとlistener.pyを一度に立ち上げます。
launchファイルの中にあるので複数のノードを立ち上げることが可能です。

## 実行方法
・例1

端末：
```bash
$ ros2 run mypkg talker
```

別端末：
```bash
$ ros2 run mypkg listener
```

結果:
```bash
[INFO] [1703751431.128828517] [listener]: age: 19
```

・例2

例1の順番を入れ替えて行う

別端末：
```bash
$ ros2 run mypkg listener
```

端末：
```bash
$ ros2 run mypkg talker
```

結果：
```bash
[INFO] [1703752117.598256795] [listener]: 待機中
[INFO] [1703752118.601192775] [listener]: 待機中
[INFO] [1703752119.605290182] [listener]: 待機中
[INFO] [1703752120.608192807] [listener]: 待機中
[INFO] [1703752121.612646691] [listener]: 待機中
[INFO] [1703752122.615631679] [listener]: 待機中
[INFO] [1703752123.619979028] [listener]: age: 19
```

## テスト環境
・Ubuntu 20.04
## 使用しているros2のバージョン
・Foxy 

## ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
* [ryuichiueda.github.io/my_slides/robosys_2022/lesson8](https://ryuichiueda.github.io/my_slides/robosys_2022/lesson8)
* [ryuichiueda.github.io/my_slides/robosys_2022/lesson9](https://ryuichiueda.github.io/my_slides/robosys_2022/lesson9)
* © 2023　Shotaro　Yasunishi
