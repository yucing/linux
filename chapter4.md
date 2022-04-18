# chapter4

# Linux 主要目錄
## /bin
* 放可執行檔，Binary 機器碼的檔案
* Linux 不以副檔名來判斷是否可執行，而是看「屬性」
## /etc
* Linux 系統最重要的目錄之一
* /etc/放置所有系統設定檔，大多為純文字檔
* 只有系統管理員可修改
## /sbin
* 系統管理指令或工具
* 系統管理員專用的執行檔
## /dev
* 系統設備目錄
## /home
* 一般使用者的家目錄
## /root
* 系統管理者 root 的家目錄
## /boot
* 核心檔案目錄
* 放置系統開機必須使用的核心檔案
## /usr
* 安裝套件軟體大都放置在這
## /usr/bin
* 一般執行檔
* 提供一般使用者的工具或指令
## /lib
* 共用函式庫檔案
## /opt
* 非 Linux 預設安裝的外來軟體
## /var
* 變動性與系統等待處理的檔案放置
* 紀錄檔 log 放置在這
## /tmp
* 暫時性檔案
## /media
* 移動式磁碟或光碟掛載目錄
## /mnt
* 暫時性的檔案系統掛載目錄

# 目錄相關指令
## 列出所在目錄 pwd
* 顯示目前所在目錄名稱
## 列出目錄下的檔案 ls
* 列出檔案資訊
## 檔案詳細資訊


![](https://github.com/yucing/linux/blob/main/picture/file.png)

### 權限
* 此欄位共有 10 個字元，第一個字元代表該檔案的型態
類型 | 字元說明
---- | -------