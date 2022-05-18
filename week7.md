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