# 4/12 第八週 Linux 課程

## su / su - 
* 環境變量會不一樣
1. su : 使用原本
2. su - : 使用切換之使用者

![](https://github.com/yucing/linux/blob/main/picture/su -.png)

![](https://github.com/yucing/linux/blob/main/picture/su -1.png)

* [su / su -](https://registerboy.pixnet.net/blog/post/30355556)

## Liunx 指令
* uname -r : 查看系統核心

## 編譯核心
* 選擇 longterm 版本
1. 在選擇的版本 tarball 點擊右鍵
2. copy link address
3. 在虛擬機 terminal 中選擇一資料夾
4. wget 網址 : 下載
5. tar -xvf 版本 : 解壓縮
6. cd 進入資料夾
7. cp -v /boot/config-3/10/0-1160.59.1.el7.x86_64 /root