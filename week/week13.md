# 5/24 第十三週 Linux 課程

## 系統帳戶
* grep nologin /etc/passwd | wc -l : 統計多少行

![](https://github.com/yucing/linux/blob/main/picture/user.png)

* who | awk '{print $1}' | sort | uniq | wc -l : 顯示有幾位使用者
* sort : 分類, uniq : 獨一無二

![](https://github.com/yucing/linux/blob/main/picture/who1.png)

* grep /bin/bash /etc/passwd | grep -v root | wc -l : 顯示有幾位使用者

![](https://github.com/yucing/linux/blob/main/picture/grep23.png)

## user
### useradd [選項] 使用者 : 新增使用者, 可客製化選項
* -g 群組名稱 : 新增群組 (主要群組)
* -G 群組名稱 : 新增群組 (其他群組)
* -c 註解 : 註解
* -d 目錄 : 指定家目錄

### userdel 使用者 : 刪除使用者
* -r : 刪除家目錄

### 帳號停權
* gedit /etc/passwd
* 在帳號前面加入 !

![](https://github.com/yucing/linux/blob/main/picture/user2.png)

![](https://github.com/yucing/linux/blob/main/picture/user3.png)

### usermod : 修改群組

## cat
* cat 檔案 | awk -F, '{print $?}' : 以,分開

![](https://github.com/yucing/linux/blob/main/picture/cat3.png)

* cat 檔案 | awk -F[符號] '{print $?}' : 以符號分開 (可多個)

![](https://github.com/yucing/linux/blob/main/picture/cat4.png)

## chmod : 變更存取權限
* r : 可列出
* w : 可修改
* x : 可進入該目錄中
### 數字
* r : 4, w : 2, x : 

### 符號
* u : user, g : root, o : other, a : all
* -: 拿掉
* +: 加回去

![](https://github.com/yucing/linux/blob/main/picture/ll3.png)

![](https://github.com/yucing/linux/blob/main/picture/ll4.png)

## chown : 變更檔案擁有者
* chown 使用者帳號 檔案

![](https://github.com/yucing/linux/blob/main/picture/chown.png)

* chown -R 使用者帳號 檔案 : 多重修改

![](https://github.com/yucing/linux/blob/main/picture/chown2.png)