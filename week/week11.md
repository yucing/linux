# 5/10 第十一週 Linux 課程

## grep 用法
1. grep 尋找名稱 搜尋位置
2. cat 搜尋位置 | grep 尋找名稱

![](https://github.com/yucing/linux/blob/main/picture/grep.png)

### 參數一 : -n 顯示行號
* grep -n 搜尋名稱 搜尋位置

![](https://github.com/yucing/linux/blob/main/picture/grep2.png)

### 參數二 : -v 排除在外
* grep -v 搜尋名稱 搜尋位置

![](https://github.com/yucing/linux/blob/main/picture/grep3.png)

### 參數三 : -i 忽視大小寫
* grep -i 搜尋名稱 搜尋位置

![](https://github.com/yucing/linux/blob/main/picture/grep4.png)

### 參數四 : -r 尋找資料夾中的某個東西
* grep -r "東西" 搜尋位置

![](https://github.com/yucing/linux/blob/main/picture/grep5.png)

* 有時搭配 --include="" 使用
* 

![](https://github.com/yucing/linux/blob/main/picture/grep6.png)

### 參數五 : -A n 顯示後 n 行
* 

![](https://github.com/yucing/linux/blob/main/picture/grep7.png)

[grep](https://dotblogs.com.tw/xerion30476/2021/05/21/Linux)

## 通配符 wildcrad
1. *: 任意字符 (0到多個)

![](https://github.com/yucing/linux/blob/main/picture/ls1.png)

![](https://github.com/yucing/linux/blob/main/picture/ls4.png)

2. ?: 代表一個字符

![](https://github.com/yucing/linux/blob/main/picture/ls2.png)

3. []: 中間為字符組合，僅匹配其中任一一個字符

![](https://github.com/yucing/linux/blob/main/picture/ls3.png)