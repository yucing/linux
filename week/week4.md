# 3/08 第四週 Linux 課程

## Linux terminal 指令
* uname -r : 查看現在Linux使用版本
* uname -a : 查看更多版本資訊
* ls 尋找資料* : 列出尋找的資料 ( Ex. ls vmlinuz* : 列出所有 vmlinuz 開頭的資料 )
* *: 萬用字元 
* ls 尋找資料* -l : 列出尋找資料長格式 ( Ex. ls vmlinuz* -l )
* echo $SHELL : 顯示所使用的SHELL
* echo $USER : 登入的使用者
* echo $PWD : 現在的路徑
* $ : 取出變數
* gedit 檔案 & : 編輯檔案
* & : 在背景執行
* chmod +x 檔案 : 改變檔案存取權限
* passwd : 改變使用者密碼
* passwd 使用者 : 改變指定使用者密碼 ( 需在超級使用者模式下 )
* adduser 使用者 : 增加一個使用者
* ssh 使用者@本機 : 切換成另一個使用者

![](https://github.com/yucing/linux/blob/main/picture/vm.png)

![](https://github.com/yucing/linux/blob/main/picture/-l.png)

![](https://github.com/yucing/linux/blob/main/picture/echo1.png)

## kernel位置
1. 切換成超級使用者 su
2. cd /usr/lib64/
3. cd /boot

![](https://github.com/yucing/linux/blob/main/picture/kernel.png)

## 執行.sh檔
1. bash 檔案.sh
2. ./檔案.sh

----------------- 注意 -----------------

* 使用方法二，需要注意執行權限

![](https://github.com/yucing/linux/blob/main/picture/bash1.png)

![](https://github.com/yucing/linux/blob/main/picture/bash2.png)

![](https://github.com/yucing/linux/blob/main/picture/bash3.png)

## 檔案名稱
1. 開頭為 - : 為一個檔案
2. 開頭為 d : 為一個資料夾

![](https://github.com/yucing/linux/blob/main/picture/filename.png)