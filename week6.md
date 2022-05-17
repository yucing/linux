# 3/23 第六週 Linux 課程

## 命令提示符號
* 使用者名稱 @ 主機名稱 目前目錄

![](https://github.com/yucing/linux/blob/main/picture/c.png)

## Linux 指令
### whoami
* 查看目前使用者

![](https://github.com/yucing/linux/blob/main/picture/whoami.png)

### w / who
* 查看使用者登入情形
* TTY : 目前使用者
* pts : putty 登入

![](https://github.com/yucing/linux/blob/main/picture/who.png)

#### w 抓取特定資料
* w | grep 資料 ( Ex: w | grep pts)

![](https://github.com/yucing/linux/blob/main/picture/w2.png)

#### w 抓取特定資料的第 n 項
* w | grep 資料 | head -n 數字 ( Ex:w | grep pts | head -n 1)

![](https://github.com/yucing/linux/blob/main/picture/w3.png)

### hostname
* 查看目前主機名稱

![](https://github.com/yucing/linux/blob/main/picture/hostname.png)

### 

## pwd v.s echo $PWD
* pwd : 一個命令
* echo $PWD : 一個系統環境變數

![](https://github.com/yucing/linux/blob/main/picture/pwd.png)

## Linux 基本觀念
### ~
* home directory

## user / superuser 家目錄位置
* user : /hone/user
* superuser : /root

![](https://github.com/yucing/linux/blob/main/picture/homedirectory.png)