# 3/15 第五週 Linux 課程

## 取出特定資料
### 特定資料所有資訊
* ifconfig 特定資料 ( Ex: ifconfig enp0s3 )

![](https://github.com/yucing/linux/blob/main/picture/ifconfig1.png)

### 特定資料某一行資訊
* ifconfig 特定資料 | grep 資訊 ( Ex: ifconfig enp0s3 | grep netmask )

![](https://github.com/yucing/linux/blob/main/picture/ifconfig2.png)

### 特定資料某一項資訊
* ifconfig 特定資料 | grep 資訊 | awk '{print $位置}'

![](https://github.com/yucing/linux/blob/main/picture/ifconfig3.png)

* | : 管道