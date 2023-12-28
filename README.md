## ros2mypkg
[![test](https://github.com/ShotaroYasunishi/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/ShotaroYasunishi/mypkg/actions/workflows/test.yml)

## talker.py
・整数の数を数えてlistener.py送信するために数えたデータをトピックにパブリッシャで送信するノードです。
数は1ずつ数えていきます。
送信されるメッセージの型は16ビットです。

## listener.py
・talker.pyから送信されたメッセージをトピックからサブスクライバーで受信するノードです。
別の端末で実行することでメッセージの表示が可能です。

## talk_listen.launch.py
・talker.pyとlistener.pyを一度に立ち上げます。
launchファイルの中にあるので複数のノードを立ち上げることが可能です。

## 実行方法
・例1

端末：$ ros2 run mypkg talker

別端末：$ ros2 run mypkg listener

結果:

[INFO] [1703739635.815743115] [listener]: Listen: 37
[INFO] [1703739636.307752007] [listener]: Listen: 38
[INFO] [1703739636.807541553] [listener]: Listen: 39
[INFO] [1703739637.307733773] [listener]: Listen: 40
[INFO] [1703739637.807700314] [listener]: Listen: 41
[INFO] [1703739638.307720779] [listener]: Listen: 42
[INFO] [1703739638.807760221] [listener]: Listen: 43
[INFO] [1703739639.307664101] [listener]: Listen: 44
[INFO] [1703739639.808635277] [listener]: Listen: 45
[INFO] [1703739640.307677835] [listener]: Listen: 46
[INFO] [1703739640.807987593] [listener]: Listen: 47
[INFO] [1703739641.307626743] [listener]: Listen: 48

例2

端末$ros2 launch mypkg talk_listen.launch.py

[INFO] [launch]: All log files can be found below /home/yasu3/.ros/log/2023-12-28-16-19-52-684406-yasu1127-1194
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [1196]
[INFO] [listener-2]: process started with pid [1198]
[listener-2] [INFO] [1703747993.725078363] [listener]: Listen: 0
[listener-2] [INFO] [1703747994.217783983] [listener]: Listen: 1
[listener-2] [INFO] [1703747994.718429566] [listener]: Listen: 2
[listener-2] [INFO] [1703747995.218335885] [listener]: Listen: 3
[listener-2] [INFO] [1703747995.718356076] [listener]: Listen: 4
[listener-2] [INFO] [1703747996.217441311] [listener]: Listen: 5
[listener-2] [INFO] [1703747996.718696597] [listener]: Listen: 6
[listener-2] [INFO] [1703747997.217488111] [listener]: Listen: 7
[listener-2] [INFO] [1703747997.718270656] [listener]: Listen: 8
[listener-2] [INFO] [1703747998.217755917] [listener]: Listen: 9
[listener-2] [INFO] [1703747998.718532638] [listener]: Listen: 10
[listener-2] [INFO] [1703747999.218214971] [listener]: Listen: 11
[listener-2] [INFO] [1703747999.718491630] [listener]: Listen: 12
[listener-2] [INFO] [1703748000.217973141] [listener]: Listen: 13
[listener-2] [INFO] [1703748000.718397767] [listener]: Listen: 14
[listener-2] [INFO] [1703748001.218143881] [listener]: Listen: 15
[listener-2] [INFO] [1703748001.717574395] [listener]: Listen: 16
[listener-2] [INFO] [1703748002.218101701] [listener]: Listen: 17
[listener-2] [INFO] [1703748002.718451304] [listener]: Listen: 18
[listener-2] [INFO] [1703748003.218125841] [listener]: Listen: 19

・両方の例はctrlとcで終了することができます。
## テスト環境
・Ubuntu 20.04
## 使用しているros2のバージョン
・Foxy 

## ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
* [ryuichiueda.github.io/my_slides/robosys_2022/lesson8](https://ryuichiueda.github.io/my_slides/robosys_2022/lesson8)
* [ryuichiueda.github.io/my_slides/robosys_2022/lesson9](https://ryuichiueda.github.io/my_slides/robosys_2022/lesson9)
* [ryuichiueda.github.io/my_slides/robosys_2022/lesson10](https://ryuichiueda.github.io/my_slides/robosys_2022/lesson10)
* © 2023　Shotaro　Yasunishi
