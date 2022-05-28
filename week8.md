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
* sudo -l : 查看是否可以為超級使用者

![](https://github.com/yucing/linux/blob/main/picture/sudo.png)

![](https://github.com/yucing/linux/blob/main/picture/sudo2.png)

* cd - : 回到原本資料夾

![](https://github.com/yucing/linux/blob/main/picture/cd.png)

* cd ~ : 回到家目錄
* echo $? : 前面指令是否執行 ( 0 : 執行, 非 0 : 沒有執行 )

![](https://github.com/yucing/linux/blob/main/picture/echo2.png)

* cat /etc/passwd : 伺服器/使用者配置

![](https://github.com/yucing/linux/blob/main/picture/etc2.png)

![](https://github.com/yucing/linux/blob/main/picture/etc3.png)

* cat -n 位置 | sed -n "n,mp" : 取得 n 到 m 行的資料

![](https://github.com/yucing/linux/blob/main/picture/etc4.png)

* mkdir -p 名稱 : 不會報錯

![](https://github.com/yucing/linux/blob/main/picture/mkdir.png)

* mkdir -p a/b/c : 建立多個檔案

![](https://github.com/yucing/linux/blob/main/picture/mkdir2.png)

## touch
* 產生新檔案 / 改變時間

![](https://github.com/yucing/linux/blob/main/picture/touch.png)

## tail
* tail -f 檔案 : 追蹤

![](https://github.com/yucing/linux/blob/main/picture/tail.png)

## EOF
* cat <<符號 > a.txt : 產生一個 a.txt 的檔案，而且可持續輸入直到輸入 符號 

![](https://github.com/yucing/linux/blob/main/picture/cat.png)

![](https://github.com/yucing/linux/blob/main/picture/cat2.png)

## 編譯核心
* 選擇 longterm 版本
1. 在選擇的版本 tarball 點擊右鍵
2. copy link address
3. 在虛擬機 terminal 中選擇一資料夾
4. wget 網址 : 下載
5. tar -xvf 版本 : 解壓縮
6. cd 進入資料夾
7. cp -v /boot/config-3/10/0-1160.59.1.el7.x86_64 /root
8. make bzImage
9. make modules
10. make
11. make module_install
12. make install