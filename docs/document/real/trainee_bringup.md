# ROS 2 トレーニーを起動しよう！

## 概要

トレーニー実機の駆動部を起動する方法を説明する。

## 目覚めよトレーニー


### odrive周りを起動
todo  
助けてBEIKE

### トレーニーのROS　2周りを起動
robot_state_publisher->urdfをload,pubするnodeの起動など  
機体の基礎的な部分を起動します
* odomなどのcontrollesのパラメータ->config/param/trainee_controllers.yaml
* urdf関連 ->trainee_description/urdf/trainee.urdf.xacro

```
ros2 launch trainee_launch trainee.launch.py
```

### joycon操作
joyconを接続してマニュアル操作を開始します．
* 最大速度などのパラメータ->config/param/logicool_f310.yaml
```
teleop_twist_joy_comfy.launch.xml
```
