# 3/29 第七週 Linux 課程

## 網路連不上
* cat /etc/resolv.conf
* 新增 8.8.8.8

![](https://github.com/yucing/linux/blob/main/picture/etc.png)

## 網頁伺服器改變 port
1. cd /etc/httpd/conf
2. gedit httpd.conf
3. 找到 Listen
4. 更改 Listen 後面的號碼
5. 儲存
6. systemctl restart httpd.service
7. 在本機輸入 虛擬機ip:更改號碼 ( Ex: 192.168.56.112:8080 )
8. 可在虛擬機輸入 netstat -tunlp | grep 80 查看網路狀況

![](https://github.com/yucing/linux/blob/main/picture/httpd.png)

![](https://github.com/yucing/linux/blob/main/picture/httpd2.png)

![](https://github.com/yucing/linux/blob/main/picture/httpd3.png)

## 查看 arp 表格
* Linux : arp -n
* Windows : arp -a

![](https://github.com/yucing/linux/blob/main/picture/arp.png)

## tree
* yum install tree
* tree 目錄 : 可以查看目錄下的所有東西

![](https://github.com/yucing/linux/blob/main/picture/tree.png)

## Linux 指令
* ls -l 資料夾 -d : 查看資料夾的權限
* ls -l -d 資料夾 : 查看資料夾的權限
* stat 檔案 : 查看檔案時間

![](https://github.com/yucing/linux/blob/main/picture/stat.png)

* cp 檔案名稱 複製檔案 : 複製檔案
* rm 檔案名稱 另一個檔案名稱 : 複製檔案
* rm 檔案 : 刪除檔案

## 更改存取權限

![](https://github.com/yucing/linux/blob/main/picture/chmod1.png)

* chmod 400 目錄 : 只可讀取裡面含有多少物件

![](https://github.com/yucing/linux/blob/main/picture/chmod2.png)

* chmod 500 目錄 : 可進入資料夾，不可修改檔案

![](https://github.com/yucing/linux/blob/main/picture/chmod3.png)

* chmod 700 目錄 : 可修改檔案

![](https://github.com/yucing/linux/blob/main/picture/chmod4.png)

## link
### 硬連結
* ln 檔案名稱 連結名稱
* 修改檔案的同時，連結也會修改

![](https://github.com/yucing/linux/blob/main/picture/link.png)

### 符號連結
* ln -s 檔案名稱 連結名稱

![](https://github.com/yucing/linux/blob/main/picture/link2.png)

## man
* 空白鍵 : 往下翻頁
* PageDown : 往下翻頁，與空白鍵相同
* PageUp : 往上翻頁
* /字串 : 搜尋字串
* N : 往下尋找下一個
* n : 往上尋找上一個
* q : 結束