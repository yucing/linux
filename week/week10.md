# 5/3 第十週 Linux 課程

## 改變指令輸出
* ls /tmp 1>/dev/null : 將資訊丟到 null 裡面

![](https://github.com/yucing/linux/blob/main/picture/null.png)

## Linux 指令
* id 使用者 : 查看是否有此使用者存在

![](https://github.com/yucing/linux/blob/main/picture/id.png)

![](https://github.com/yucing/linux/blob/main/picture/id2.png)

## 腳本
### checkuser.sh
1. which bash : 查看 bash 所在位置

![](https://github.com/yucing/linux/blob/main/picture/bash5.png)

2. gedit xx.sh &
3. 第一行輸入 #!bash位置 ( Ex: #!/usr/bin/bash)
4. 輸入程式，並儲存

![](https://github.com/yucing/linux/blob/main/picture/bash6.png)

5. chmod +x xx.sh
6. ./xx.sh

![](https://github.com/yucing/linux/blob/main/picture/bash7.png)

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

## 貼照片
* 寫一個回應 ip/ether 的腳本

## pipe
* 輸入 | 輸出

* echo "密碼" | passwd tom --> 失敗
* echo "密碼" | passwd --stdin tom --> 成功