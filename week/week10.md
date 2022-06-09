# 5/3 第十週 Linux 課程

## 改變指令輸出
* ls /tmp 1>/dev/null : 將資訊丟到 null 裡面

![](https://github.com/yucing/linux/blob/main/picture/null.png)

## Linux 指令
* id 使用者 : 查看是否有此使用者存在

![](https://github.com/yucing/linux/blob/main/picture/id.png)

![](https://github.com/yucing/linux/blob/main/picture/id2.png)

* touch {}.txt : 建立多個檔案 ( Ex: touch {a..z}.txt )

![](https://github.com/yucing/linux/blob/main/picture/touch2.png)

## 腳本
1. which bash : 查看 bash 所在位置

![](https://github.com/yucing/linux/blob/main/picture/bash5.png)

2. gedit xx.sh &
3. 第一行輸入 #!bash位置 ( Ex: #!/usr/bin/bash)
4. 輸入程式，並儲存
5. chmod +x xx.sh
6. ./xx.sh
### checkuser.sh
```
#!/usr/bin/bash

id $1 1>dev/null 2>&!
result=`echo $?`

if [ $result -eq 0 ]
then
    echo "$1 exists"
else
    echo "$1 doesn't exist"
fi
```
* $1 : 輸入的變數 ( Ex: ./checkuser.sh abc ) $1 == abc

![](https://github.com/yucing/linux/blob/main/picture/bash6.png)

![](https://github.com/yucing/linux/blob/main/picture/bash7.png)

### getip.sh
```
#!/usr/bin/bash

ip=`ifconfig $1 | grep inet | grep -v inet6 | awk '{print $2}'`

echo "ip: $ip"
```

![](https://github.com/yucing/linux/blob/main/picture/getip2.png)

![](https://github.com/yucing/linux/blob/main/picture/getip.png)

## pipe
* 輸入 | 輸出

* echo "密碼" | passwd tom --> 失敗
* echo "密碼" | passwd --stdin tom --> 成功

![](https://github.com/yucing/linux/blob/main/picture/echo5.png)

## 尋找檔案
### which
* 尋找環境變數PATH中所有目錄是否有特定執行檔

![](https://github.com/yucing/linux/blob/main/picture/which.png)

### whereis
* 找到完整檔名

![](https://github.com/yucing/linux/blob/main/picture/where.png)

### locate
* 可尋找所有檔案
* 在 database 尋找，需先使用 updatedb

### find
* 可尋找所有檔案
* 在磁碟裡一個一個找
* 最花時間
* 可做條件式的功能

![](https://github.com/yucing/linux/blob/main/picture/find.png)

* 找出特定格式檔案 ★ 一定要用"" ★

![](https://github.com/yucing/linux/blob/main/picture/f2.png)

* -perm : 特殊權限

![](https://github.com/yucing/linux/blob/main/picture/perm.png)

* -exec rm -f {} \; : 刪除所有檔案

![](https://github.com/yucing/linux/blob/main/picture/exec.png)

* -exec chmod 644 () \; : 更改所有檔案權限

![](https://github.com/yucing/linux/blob/main/picture/exec2.png)

* -empty -exec rm -f {} \; : 刪除所有空資料夾

![](https://github.com/yucing/linux/blob/main/picture/exec3.png)

### 補充一 : -i
* 可利用 -i 不分大小寫找到資料

![](https://github.com/yucing/linux/blob/main/picture/-i.png)

### 補充二 : -type
1. d : 目錄

![](https://github.com/yucing/linux/blob/main/picture/d.png)

2. f : 一般檔案

![](https://github.com/yucing/linux/blob/main/picture/f.png)

3. l : 連結檔

![](https://github.com/yucing/linux/blob/main/picture/l.png)

### 補充三 : 修改時間
1. -atime n : 最後存取時間
2. -mtime n : 最後修改時間
3. -ctime n : 最後修改時間

#### 天數
1. -?time n : n天前有被修改的檔案 ( n=7, 今天是 9/17, 7天前是 9/11 )
2. -?time -n : n 天內有被修改的檔案 ( n=-7, 今天是 9/17, 7天內是 9/11~9/17)
3. -?time +n : n 天以上有被修改的檔案 ( n=+7, 今天是 9/17 , 7天以上是 9/11以前)

[尋找檔案](https://blog.gtwang.org/linux/unix-linux-find-command-examples/)

## 檔案權限 rwx
* r : 4, w : 2, x : 1
* rwx : 4+2+1=7, rw- : 4+2=6, r-- : 4
* rwx rwx rwx (777)

## stat
* 可察看檔案修改時間
1. access : 有讀取

![](https://github.com/yucing/linux/blob/main/picture/stat3.png)

2. modify : 修改內容 

![](https://github.com/yucing/linux/blob/main/picture/stat2.png)

3. change : 修改內容或權限

![](https://github.com/yucing/linux/blob/main/picture/stat4.png)

## 備份
### 初次備份
1. tar cvfz xxx.tar.gz 檔案
2. touch timebase

### 增量備份
1. tar cvfz xxx.tar.gz `find . -cnewer ./timebase -type f`

### 解壓縮
* tar xvfz xxx.tar.gz