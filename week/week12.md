# 5/17 第十二週 Linux 課程

## USB
* 先在 virtualbox 的 settings 裡面選擇 USB 勾選需要的 USB 類型
* 進入虛擬機，在虛擬機上方的 Devices 選擇 USB 看到有打勾就成功了
* lsblk -f : 查看類型
* cd /
*  yum -y install epel-release http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-5.el7.nux.noarch.rpm
* yum -y install fuse-exfat exfat-utils
* mount -t exfat /dev/類型 /media
* cd /media : 就可查看 USB 的內容
* umount /media : 卸載

## Linux 指令
* lsblk : 虛擬機磁碟情況

![](https://github.com/yucing/linux/blob/main/picture/lsblk.png)

* lsblk -f : 可察看檔案系統

![](https://github.com/yucing/linux/blob/main/picture/lsblk2.png)

* ~+ : pwd ( Ex: echo ~+ == echo pwd)

![](https://github.com/yucing/linux/blob/main/picture/pwd2.png)

* ~- : previous directory

![](https://github.com/yucing/linux/blob/main/picture/pwd3.png)

* 標準輸入 xargs

![](https://github.com/yucing/linux/blob/main/picture/echo6.png)

## 掛載常用的地方
1. /mnt
2. /media
3. /run

![](https://github.com/yucing/linux/blob/main/picture/111.png)

## 新增硬碟
* settings -> storage -> adds hard disk

![](https://github.com/yucing/linux/blob/main/picture/st.png)

* 選擇 create
* 選擇大小
* clike "ok"

### 建立分割區
* 進入treminal
* lsblk -f 或是 dmesg | grep sd : 查看是否新增
* fdisk /dev/新硬碟名稱
* n : 新增分割區
* p : 選擇主分割區
* 1
* 按下 enter，預設使用空間
* w : 儲存並離開

### 安裝新磁碟
* mkfs -t 格式 /dev/新硬碟名稱 : 格式化磁碟分割區
* mount -t 格式 /dev/新硬碟名稱 /media : 掛載

## fdisk 常用指令
* p : 印出硬碟裡分割區資訊
* n : 在硬碟中新增分割區
* d : 刪除分割區
* m : help
* t : 變更分割區檔案類型
* w : 儲存並離開
* q : 離開

## user
* id user : 使用者資訊
* wheel : 可切換成 root

![](https://github.com/yucing/linux/blob/main/picture/user.png)