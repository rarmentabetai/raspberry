# ラズパイメモ
raspberry pi memo

# 設定
### 画面の向き

/boot/config.txtに`display_rotate`を設定する

```
display_rotate=0 Normal
display_rotate=1 90 degrees
display_rotate=2 180 degrees
NOTE: You can rotate both the image and touch interface 180º by entering lcd_rotate=2 instead
display_rotate=3 270 degrees
display_rotate=0x10000 horizontal flip
display_rotate=0x20000 vertical flip
```

### 7インチLCDの明るさ

```
#バックライトOFF
echo 1 > /sys/class/backlight/rpi_backlight/bl_power
#バックライトON
echo 0 > /sys/class/backlight/rpi_backlight/bl_power
#明るさ 0-255
echo 80 > /sys/class/backlight/rpi_backlight/brightness
```
