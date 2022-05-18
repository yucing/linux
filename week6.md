# 3/23 第六週 Linux 課程

## 命令提示符號
* 使用者名稱 @ 主機名稱 目前目錄

![](https://github.com/yucing/linux/blob/main/picture/c.png)

## Linux 指令
### whoami
* 查看目前使用者

![](https://github.com/yucing/linux/blob/main/picture/whoami.png)

### w / who
* 查看使用者登入情形
* TTY : 目前使用者
* pts : putty 登入

![](https://github.com/yucing/linux/blob/main/picture/who.png)

#### w 抓取特定資料
* w | grep 資料 ( Ex: w | grep pts)

![](https://github.com/yucing/linux/blob/main/picture/w2.png)

#### w 抓取特定資料的第 n 項
* w | grep 資料 | head -n 數字 ( Ex:w | grep pts | head -n 1)

![](https://github.com/yucing/linux/blob/main/picture/w3.png)

### hostname
* 查看目前主機名稱

### man 指令
* 得到指令的完整用法
* Ex: man ls

![](https://github.com/yucing/linux/blob/main/picture/man1.png)

![](https://github.com/yucing/linux/blob/main/picture/man2.png)

![](https://github.com/yucing/linux/blob/main/picture/hostname.png)

## pwd v.s echo $PWD
* pwd : 一個命令
* echo $PWD : 一個系統環境變數

![](https://github.com/yucing/linux/blob/main/picture/pwd.png)

## Linux 基本觀念
### ~
* home directory

## user / superuser 家目錄位置
* user : /hone/user
* superuser : /root

![](https://github.com/yucing/linux/blob/main/picture/homedirectory.png)

## shell 按鍵
### TAB
* 快速完成現在輸入的工作

### Ctrl+C
* 中斷目前的工作

### Ctrl+Z
* 暫停目前的工作，利用fg可取得暫停的工作

![](https://github.com/yucing/linux/blob/main/picture/shell.png)

### Ctrl+A
* 游標移到最前面

### Ctrl+E
* 游標移到最後面

## 指令 [選項] [參數]
### ls
* 列出目前所在目錄的檔案

![](https://github.com/yucing/linux/blob/main/picture/c3.png)

### ls -l -h ( ls -lh )
* 列出所在目錄的檔案，並顯示出檔案的大小 (用符號表示)

![](https://github.com/yucing/linux/blob/main/picture/c4.png)

### ls -a
* 列出隱藏的檔案

![](https://github.com/yucing/linux/blob/main/picture/c5.png)

### ls -l /tmp
* 列出 /tmp 的詳細檔案

![](https://github.com/yucing/linux/blob/main/picture/c2.png)

## 新增使用者
* su 模式下使用
* cd /home : 可察看使用者
1. adduser 名稱
2. 照著步驟做

## 切換使用者
* su - 使用者

## 變更密碼
### 一般使用者
* passwd --> 僅能更改自己的密碼

### 超級使用者
* 方法一 : passwd 使用者 --> 可更改任意使用者
* 方法二 : echo "密碼" | passwd --stdin 使用者 --> 可直接更改密碼

## shutdown 指令
* shutdown -h now : 關機
* shutdown -h +分鐘 : 幾分鐘後關機
* shutdown -r now : 重新啟動