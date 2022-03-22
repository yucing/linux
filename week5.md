# 3/15 第五週 Linux 課程

## 取出特定資料
### 特定資料所有資訊
* ifconfig 特定資料 ( Ex: ifconfig enp0s3 )

![](https://github.com/yucing/linux/blob/main/picture/ifconfig1.png)

### 特定資料某一行資訊
* ifconfig 特定資料 | grep 資訊 ( Ex: ifconfig enp0s3 | grep netmask )

![](https://github.com/yucing/linux/blob/main/picture/ifconfig2.png)

### 特定資料某一項資訊
* ifconfig 特定資料 | grep 資訊 | awk '{print $位置}' ( Ex: ifconfig enp0s3 | grep netmask | awk '{print $2}' )

![](https://github.com/yucing/linux/blob/main/picture/ifconfig3.png)

* | : 管道

### 去除不要的資料
1. ifconfig | grep inet
2. ifconfig | grep inet | grep -v inet6

![](https://github.com/yucing/linux/blob/main/picture/inet1.png)

![](https://github.com/yucing/linux/blob/main/picture/inet2.png)

## 清除所有設定
1. 進入超級使用者 su
2. 輸入密碼 (centos)
3. ifconfig enp0s3 0
4. ifconfig enp0s3 輸入原本的資料
5. 此時不能ping 8.8.8.8，無法連上網路
6. ip route add default via 10.0.2.2
7. route -n
8. 重新連上網路

![](https://github.com/yucing/linux/blob/main/picture/clear1.png)

![](https://github.com/yucing/linux/blob/main/picture/clear2.png)

![](https://github.com/yucing/linux/blob/main/picture/clear3.png)

## 更改網路卡卡號 (暫時)
1. 切換成超級使用者 su
2. ifconfig enp0s3
3. ifconfig enp0s3 hw ether 更改的卡號 ( Ex: 00:00:00:00:00:01)
4. ifconfig enp0s3

![](https://github.com/yucing/linux/blob/main/picture/ether.png)

## Linux terminal 指令
* df -h : 顯示資料大小
* history : 查看歷史指令
* 進入 history 後，輸入 !時間\指令 : 執行先前指令 ( 不用打全名，會從下到上比對指令 )

![](https://github.com/yucing/linux/blob/main/picture/history.png)

![](https://github.com/yucing/linux/blob/main/picture/history2.png)

## 更改主機名稱
1. 進入超級使用者模式 su
2. hostnamectl set-hostname 名稱
3. bash

## nmap
1. 進入超級使用者模式 su
2. yum install nmap

## Hydra
1. 進入超級使用者模式 su
2. yum install epel-release
3. yum install hydra

## 資料
[Hydra](https://itw01.com/89YGETJ.html)

[Hydra](https://www.twblogs.net/a/5cad5d1dbd9eee7fd992ab12)