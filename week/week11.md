# 5/10 第十一週 Linux 課程

## grep 用法

[grep](https://dotblogs.com.tw/xerion30476/2021/05/21/Linux)

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
* grep -r "東西" --include="*.格式" 搜尋位置

![](https://github.com/yucing/linux/blob/main/picture/grep6.png)

### 參數五 : -A n 顯示後 n 行
* grep -A 搜尋名稱 搜尋位置

![](https://github.com/yucing/linux/blob/main/picture/grep7.png)

![](https://github.com/yucing/linux/blob/main/picture/grep9.png)

### 參數六 : -B n 顯示前 n 行
* grep -B 搜尋名稱 搜尋位置

![](https://github.com/yucing/linux/blob/main/picture/grep8.png)

### 參數七 : -C n 顯示前後 n 行
* grep -C 搜尋名稱 搜尋位置

![](https://github.com/yucing/linux/blob/main/picture/grep10.png)

## grep 正規表示法
### a 開頭
* grep "^a"

![](https://github.com/yucing/linux/blob/main/picture/grep11.png)

### a 結尾
* grep "a$"

![](https://github.com/yucing/linux/blob/main/picture/grep12.png)

### a或b 開頭
* grep "^[ab]"

![](https://github.com/yucing/linux/blob/main/picture/grep13.png)

### a或b 結尾
* grep "[ab]$"

![](https://github.com/yucing/linux/blob/main/picture/grep14.png)

### 排除空白行
* grep -v "[^$]"

![](https://github.com/yucing/linux/blob/main/picture/grep15.png)

### a開頭, b出現0次以上
* grep "^ab*"

![](https://github.com/yucing/linux/blob/main/picture/grep16.png)

### a開頭, b出現0次或1次
* egrep "^ab?"

![](https://github.com/yucing/linux/blob/main/picture/grep17.png)

### a開頭, b出現1次
* egrep "^ab+"

![](https://github.com/yucing/linux/blob/main/picture/grep18.png)

### 含有 ab 或 ac
* egrep "ab|ac"
* grep -E "ab|ac"

![](https://github.com/yucing/linux/blob/main/picture/grep19.png)

![](https://github.com/yucing/linux/blob/main/picture/grep20.png)

### 精準篩選出 xxx 字
* grep -w xxx

![](https://github.com/yucing/linux/blob/main/picture/grep21.png)

## 通配符 wildcrad
1. *: 任意字符 (0到多個)

![](https://github.com/yucing/linux/blob/main/picture/ls1.png)

![](https://github.com/yucing/linux/blob/main/picture/ls4.png)

2. ?: 代表一個字符

![](https://github.com/yucing/linux/blob/main/picture/ls2.png)

3. []: 中間為字符組合，僅匹配其中任一一個字符

![](https://github.com/yucing/linux/blob/main/picture/ls3.png)

## vim
### 操作
* 進入編輯模式 : i,o,a
* 進入命令模式 : :
* 離開 : ESC

### :
* w : write
* q : quit
* wq : write and quit
* q! : quit and give up modified 