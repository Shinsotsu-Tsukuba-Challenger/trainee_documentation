
## 事前準備

準備するものは、こちらです！  
全部そろってますか！？
<center><a href="../../../images/trainee_preparation.png"><img src="../../../images/trainee_preparation.png" width="600"/></a>
</center>

## 電源の立ち上げ

### トレーニー本体用バッテリーの接続
`トレーニー用の電源プラグ`と`トレーニー本体用バッテリー`を接続しましょう
<center><a href="../../../images/lithium-ion_battery_connection.png"><img src="../../../images/lithium-ion_battery_connection.png" width="600"/></a>
</center>

### LiDAR用バッテリーの接続
`LiDAR用の電源アダプタ`と`LiDAR用バッテリー`を接続しましょう

* 電源ボタンを押す（長押し）
<center><a href="../../../images/LiDAR-battery-on.jpg"><img src="../../../images/LiDAR-battery-on.jpg" width="600"/></a>
</center>

* DC用のボタンを押す（一瞬押すだけ）
<center><a href="../../../images/LiDAR-battery-dc-on.jpg"><img src="../../../images/LiDAR-battery-dc-on.jpg" width="600"/></a>
</center>

* 接続タイム（一番右下はInput用となっておりますので、気をつけなはれや）
<center><a href="../../../images/LiDAR-battery-dc-connection.jpg"><img src="../../../images/LiDAR-battery-dc-connection.jpg" width="600"/></a>
</center>

### 有線LANアダプターの接続
LiDAR用の有線と有線LANアダプターを接続しましょう
<center><a href="../../../images/wired_LAN_adapter_connection.jpg"><img src="../../../images/wired_LAN_adapter_connection.jpg" width="600"/></a>
</center>

### お守りを置きましょう？
あれ？`お守り`は、置きましたか？  
まだ置いてないんですね！  
では、`お守り`を優しく置きましょう。
<center><a href="../../../images/set_omamori.gif"><img src="../../../images/set_omamori.gif" width="600"/></a>
</center>

### 電源ボタン ONするのです
よろしくおねがいしまぁぁぁぁぁぁす！（ポチッ）
<center><a href="../../../images/trainee_power_on.gif"><img src="../../../images/trainee_power_on.gif" width="600"/></a>
</center>

## システムの立ち上げ

### ネットワーク接続

* LiDARと接続

LiDARとPCを接続しましょう
<center><a href="../../../images/lidar_and_pc_conection.png"><img src="../../../images/lidar_and_pc_conection.png" width="600"/></a>
</center>

* Raspiと接続

Raspiからは`trainee`というホットスポットが立ち上がっているので、接続することでRaspiとノートPCが接続されます
<center><a href="../../../images/trainee_wifi_select.png"><img src="../../../images/trainee_wifi_select.png" width="600"/></a>
</center>

### ssh接続
ノートPCからRaspiにアクセスしましょう


* ノートPC上で実行
```
ssh ubuntu@192.168.12.1
```

### 時刻同期
Raspiの時刻をPCと同期させます

* ssh越しでRaspi上で実行
```
sudo systemctl restart chrony.service
```

### trainee.launchの実行

* ノートPC上で実行
```
ros2 launch trainee_launch trainee.launch.py
```