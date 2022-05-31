# 2/22 第二週 Linux 課程

## 遠端桌面連線
1. 在搜尋輸入 mstsc
2. 在 VirtualBox 選擇 centos7-1 / settings / display / Remote display
3. Enable Server 打開 / 輸入 Server port
4. 到 遠端桌面連線 輸入 127.0.0.1:Server port

## 圖形化關機
* 點擊右上角 / 按下 關機鍵 / poweroff

## 關機指令
1. 打開 terminal
2. 輸入 halt -p / poweroff / shutdown

----------選擇 shutdown----------

3. su (change to SuperUcer)
4. centos
5. shutdown

## Network Adapter

### Bridge Adapter
1. 機器地位平等
2. 機器間可互相看到對方
3. 機器皆可存取Internet
4. 適合架設伺服器

![](https://github.com/yucing/linux/blob/main/picture/Bridge.png)

![](https://github.com/yucing/linux/blob/main/picture/BridgeTest.jpg)

### NAT
1. 虛擬機可以看到物理機
2. 物理機不能看到虛擬機
3. 虛擬機可連到網路，但無法存取
4. 有 virtual DHCP server

![](https://github.com/yucing/linux/blob/main/picture/NAT.png)

![](https://github.com/yucing/linux/blob/main/picture/NATTest.jpg)

### NAT Network
1. 虛擬機可以互相溝通
2. 虛擬機可以看到物理機
3. 物理機不能看到虛擬機

![](https://github.com/yucing/linux/blob/main/picture/NATNetwork.png)

### Host-Only
1. 產生一個內部網路
2. 虛擬機可以跟物理機溝通
3. 虛擬機可以互相溝通
4. 無法連到 Internet

![](https://github.com/yucing/linux/blob/main/picture/Hostonly.png)

### Internal Network
1. 只有在同網路虛擬機才能互相通訊
2. 不能連到其他網路

![](https://github.com/yucing/linux/blob/main/picture/InternalNetwork.png)

## 複製虛擬機
1. 右鍵選擇要複製的虛擬機
2. click 'clone'
3. 取另一個名字
4. MAC Address Policy : Generate new MAC address ( 產生新的網路卡卡號 )
5. click 'next'
6. 硬碟空間夠 : Full clone ，不夠 : Limit clone
7. click 'clone'

## 保護虛擬機
1. 在 VirtualBox 點選 Take
2. 建立一個 Snapshot

---------- 還原 ----------

3. 點選要還原的 Snapshot
4. 點擊 Restore

## 備份虛擬機
1. 在 VirtualBox 點擊左上角 File
2. 選擇 Export Application
3. 選擇要打包的虛擬機
4. 選擇檔案位置
5. 匯出

---------- 匯入 ----------

1. 在 VirtualBox 點擊左上角 File
2. 選擇 Import Application
3. 找到備份的虛擬機
4. 匯入

## 補充資料
[Network mode](https://segmentfault.com/a/1190000018641361)