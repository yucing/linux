# 3/1 第三週 Linux 課程

## Download
* puTTY
* WinScp

## Linux Settings Network
* Adapter1 : NAT (虛擬機可以跟本機溝通)
* Adapter2 : Host-only (本機可以跟虛擬機溝通)

## puTTy
1. Host name (IP address) : enp0s8 的 inet 
2. Connect Type : SSH
3. click "Open"
4. enter your user (user)
5. password (1234)

![](https://github.com/yucing/linux/blob/main/picture/putty1.png)

![](https://github.com/yucing/linux/blob/main/picture/putty2.png)

![](https://github.com/yucing/linux/blob/main/picture/putty3.png)

## WinSCP
1. 檔案協定 : SFTP
2. 主機名稱 : enp0s8 的 inet 
3. 輸入使用者名稱 (user)
4. 輸入密碼 (1234)

![](https://github.com/yucing/linux/blob/main/picture/putty1.png)

![](https://github.com/yucing/linux/blob/main/picture/winscp.png)

## Linux terminal 指令
* clear : 清除畫面
* 控制指令 動作指令 服務器的名稱
* cd /var/www/html : 切換至網路伺服器儲存位置
* echo "內容" : 印出 內容
* echo "內容" > 檔案 : 將要印出的內容丟到檔案裡
* cat 檔案 : 查看檔案的內容

![](https://github.com/yucing/linux/blob/main/picture/echo.png)

## 控制指令
* systemctl : 控制/管理服務器

## 動作指令
* status : 查看狀態
* stop : 停止 (重開機後恢復原來設定)
* start : 開啟 (重開機後恢復原來設定)
* disable : 永久關閉
* enable : 永久開啟

## 服務器名稱
* httpd : 網路伺服器
* firewalld : 防火牆
* sshd : 客戶端程式

## 開啟網路伺服器步驟
1. 檢查 firewalld 狀態是否是 inactive
2. 檢查 sshd 狀態是否是 running
3. 檢查 SELinux 是否關閉
4. 下載網路伺服器
5. 檢查 網路伺服器是否開啟
6. 再到本機的瀏覽器內輸入 虛擬機IP(192.168.56.101)

## 如何製作網頁
1. 開啟 word
2. 輸入內容，並使用 'htm' 格式儲存
3. 上傳到虛擬機
4. 開啟 puTTy
5. 切換成 su
6. 輸入 mv 檔案.htm /var/www/html
7. 在本機的瀏覽器輸入 虛擬機IP/檔案.htm (192.168.56.101/AAAA.htm)

## 關閉防火牆步驟
1. 切換成超級使用者 su
2. 輸入密碼 centos
3. 輸入 systemctl status firewalld 查看防火牆狀態
4. 查看 Active 是否為 inactive
5. 如果為 running 輸入 systemctl stop firewalld (如要永久關閉 stop 改成 disable)
6. 再次輸入 systemctl status firewalld

---------- sshd 步驟一樣 ----------

---------- httpd 步驟一樣 ----------

## 關閉 SELinux
1. 切換成超級使用者 su
2. 輸入密碼 centos
3. 輸入 getenforce 檢查 SELinux 狀態
4. 如果不是 Disable 請做下列動作
5. 輸入 gedit /etc/selinux/config
6. 將 SELINUX = disabled/enforceing/permissive 改為 disabled
7. click "save"
8. 重開機

## 下載網路伺服器
1. 切換成 su
2. 輸入 yum install httpd
3. click 'y'

## 參考資料
* [動作指令](https://blog.gtwang.org/linux/linux-basic-systemctl-systemd-service-unit-tutorial-examples/)

* [SELinux](https://dotblogs.com.tw/echo/2017/06/19/linux_selinux_mode)