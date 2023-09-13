[English](README.en.md) | [日本語](README.md)

# ROS2SERIAL_ARDUINO

## Description
ROS 2ノードとArduino Megaの間でシリアル通信を使ってデータを送受信するためのパッケージ．

- /cmd_velトピックを受け取り，serialでArduino Megaに送る．
- Arduino Mega から送られたserialデータをROS 2の/serial_inトピックにpublishする．

## USAGE

### udevの設定
```
ファイルをコピー
cp udev/99-usb-arduino-mega.rules /etc/udev/rules.d
# 設定の反映
sudo udevadm control --reload-rules
``