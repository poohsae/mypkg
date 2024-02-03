# mypkg
ロボットシステム学2023の授業内で制作したROS2のパッケージです。

[![test](https://github.com/poohsae/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/poohsae/mypkg/actions/workflows/test.yml)

## talker.py

数字をカウントしてトピック/countupを通じて送信する。

### 実行例

```
$ ros2 run mypkg talker
```

```
（なにも表示されない）
```

## listener.py

トピック/countupからメッセージを貰って表示する。

talker.pyを実行しながら、別の端末でlistener.pyを実行する。

### 実行例

```
$ ros2 run mypkg listener
```

```
[INFO] [1706931888.376836566] [listener]: Listen: 19
[INFO] [1706931888.867769701] [listener]: Listen: 20
[INFO] [1706931889.367992023] [listener]: Listen: 21
[INFO] [1706931889.866830516] [listener]: Listen: 22
...
```

## launch

talker.pyとlistener.pyを一度に立ち上げる。

### 実行例

```
$ ros2 launch mypkg talk_listen.launch.py
```

```
[INFO] [launch]: All log files can be found below /home/sae_1125/.ros/log/2024-02-03-01-16-57-667474-DESKTOP-MOSMVA-106
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [108]
[INFO] [listener-2]: process started with pid [110]
[listener-2] [INFO] [1706890618.673757450] [listener]: Listen: 0
[listener-2] [INFO] [1706890619.143728829] [listener]: Listen: 1
[listener-2] [INFO] [1706890619.643828809] [listener]: Listen: 2
[listener-2] [INFO] [1706890620.144499639] [listener]: Listen: 3
...
```

## テスト環境
* Ubuntu 20.04

## ライセンス
* このソフトウェアパッケージは、3条項BSDライセンスの下、再配布および使用が許可されます。
* このパッケージのコードは、下記のスライド(CC-BY-SA 4.0 by Ryuichi Ueda)のものを、本人の許可を得て自身の著作としたものです。
[ryuichiueda/robosys_2023](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)

© 2023 Sae Sasaki





