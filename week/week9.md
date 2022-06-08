# 4/26 第九週 Linux 課程

## c.sh
1. echo "echo hi" > c.sh
2. chmod +x c.sh --> 增加可讀取權利
3. ./c.sh --> ./ : 這個目錄下

![](https://github.com/yucing/linux/blob/main/picture/bash4.png)

## Linux 指令
* file 檔案 : 檔案屬性

![](https://github.com/yucing/linux/blob/main/picture/file1.png)

* which 檔案 : 檔案位置 (僅針對執行檔)

![](https://github.com/yucing/linux/blob/main/picture/which.png)

* df : 磁碟使用空間 ( 通常使用 df -h )

![](https://github.com/yucing/linux/blob/main/picture/df.png)

* ll -h ( ls -l -h )

![](https://github.com/yucing/linux/blob/main/picture/ll1.png)

![](https://github.com/yucing/linux/blob/main/picture/ll2.png)

* du : 目前目錄下的已用空間

![](https://github.com/yucing/linux/blob/main/picture/du.png)

![](https://github.com/yucing/linux/blob/main/picture/du.png)

## 腳本( 暫時 )
1. export PATH=$PATH:/檔案位置
2. 輸入執行檔

![](https://github.com/yucing/linux/blob/main/picture/export.png)

* 為暫時性的
### 建立視窗 

![](https://github.com/yucing/linux/blob/main/picture/export2.png)

### 新視窗

![](https://github.com/yucing/linux/blob/main/picture/export3.png)

## 腳本 ( 永久 )
1. gedit .bashrc
2. 最下面輸入 export PATH=$PATH:/檔案位置

![](https://github.com/yucing/linux/blob/main/picture/export4.png)

3. 重開 terminal (也可輸入 source .bashrc 或是 . .bashrc)
4. 輸入 echo $PATH

![](https://github.com/yucing/linux/blob/main/picture/echo3.png)

## 改變指令輸出
* > : 重導
* echo "" > a.txt == echo "" 1> a.txt

![](https://github.com/yucing/linux/blob/main/picture/echo4.png)

### 將錯誤訊息放入檔案
* ls /aaa 2>error.txt

![](https://github.com/yucing/linux/blob/main/picture/error.png)

### 多重指令
* ls /tmp /aaa 1>a.txt 2>&1
* &1 : 錯誤輸出跟標準輸出放在同一位置

![](https://github.com/yucing/linux/blob/main/picture/error2.png)