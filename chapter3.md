# chapter3
# 命令提示符號
* '#' : 最高權限管理者
* '$' : 一般使用者

![](https://github.com/yucing/linux/blob/main/picture/command.pnd)

## 資訊
* 命令提示符號前的中括號提供了三個資訊

![](https://github.com/yucing/linux/blob/main/picture/name.pnd)

# 輸入指令
## w
* 列出 Linux 目前登入的使用者帳號資訊

![](https://github.com/yucing/linux/blob/main/picture/w.pnd)

## ls
* 顯示檔名

![](https://github.com/yucing/linux/blob/main/picture/ls.pnd)

### ls -l
* 顯示詳細格式

![](https://github.com/yucing/linux/blob/main/picture/ls-l.pnd)

### ls -a
* 列出隱藏的所有檔案

![](https://github.com/yucing/linux/blob/main/picture/ls-a.pnd)

### 可寫成 ls -al

# 使用者帳號
## 家目錄
* 「~」
* cd ~ 可快速切換至家目錄
## 變更密碼
* passwd
## whoami
* 顯示目前登入的使用者

# 主控台
* Linux 提供虛擬主機台
* 共有 6 個主控台
* 用 CTRL + ALT 加上 F1.F2.F3...F6

# 關機/重啟指令
## 關機 shutdown
### 立即關機
* shutdown -h now
### 等待一段時間關機
* shutdown -h 分鐘
### 取消
* shutdown -c
### 傳送公告訊息給線上使用者
* shutdown -h 分鐘 '訊息'
## 重新啟動 reboot
* reboot
* shutdown -r now