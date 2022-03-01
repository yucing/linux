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

## 控制指令
* systemctl : 控制/管理服務器

## 動作指令
* status : 查看狀態
* stop : 停止 (重開機後恢復原來設定)
* start : 開啟 (重開機後恢復原來設定)
* disable : 關閉
* enable : 開啟

## 服務器名稱
* httpd : 網路伺服器
* firewalld : 防火牆
* sshd : 客戶端程式

## 開啟網路伺服器步驟
1. 檢查 firewalld 狀態是否是 inactive
2. 檢查 sshd 狀態是否是 running
3. 檢查 SELinux 是否關閉

## 關閉防火牆步驟
1. 切換成超級使用者 su
2. 輸入密碼 centos
3. 輸入 systemctl status firewalld 查看防火牆狀態
4. 查看 Active 是否為 inactive
5. 如果為 running 輸入 systemctl stop firewalld (如要永久關閉 stop 改成 disable)
6. 再次輸入 systemctl status firewalld

---------- sshd 步驟一樣 ----------

5. 查看 Active 是否為 running

## 關閉 SELinux
1. 切換成超級使用者 su
2. 輸入密碼 centos
3. 輸入 getenforce 檢查 SELinux 狀態
4. 如果不是 Disable 請做下列動作
5. 輸入 gedit /etc/selinux/config

## 參考資料
* [動作指令](https://blog.gtwang.org/linux/linux-basic-systemctl-systemd-service-unit-tutorial-examples/)
