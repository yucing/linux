# 6/1 第十四週 Linux 課程

## Linux 指令
* pstree : 查看Linux開機第一個行程

![](https://github.com/yucing/linux/blob/main/picture/pstree.png)

* top : 查看為什麼是第一個執行的程式

![](https://github.com/yucing/linux/blob/main/picture/top.png)

* free -m : 了解系統使用情形

![](https://github.com/yucing/linux/blob/main/picture/free.png)

* ps : 使用者正在使用的bash

![](https://github.com/yucing/linux/blob/main/picture/ps.png)

* ps -f : 查看更詳細的資料

![](https://github.com/yucing/linux/blob/main/picture/ps1.png)

* ps aux / ps -ef : 系統背景執行服務

![](https://github.com/yucing/linux/blob/main/picture/ps2.png)

* echo $$ : 顯示 bash 的 PID

![](https://github.com/yucing/linux/blob/main/picture/ps5.png)

* & : 在背景執行

## ps aux / ps -ef 欄位意義
* USER : 該行程的擁有者
* PID : 該行程的PID
* %CPU : CPU 使用率
* %MEM : 記憶體使用率
* VSZ : 虛擬記憶體的使用量
* RSS : 固定占用的記憶體
* TTY : 哪一個終端機編號所產生, 系統服務顯示為 ?
* STAT : 形成目前狀態,  S : 睡眠中, R : 執行中
* START :行程被啟動時間
* TIME : 實際CPU使用時間
* COMMAND : 該行程的指令

![](https://github.com/yucing/linux/blob/main/picture/ps3.png)

### 針對服務
* ps aux | grep cron

![](https://github.com/yucing/linux/blob/main/picture/ps4.png)

## sleep : 在背景執行
* sleep 數

![](https://github.com/yucing/linux/blob/main/picture/sleep.png)

### 查看工作
* jobs

![](https://github.com/yucing/linux/blob/main/picture/sleep1.png)

### 移到前景
* fg 數

![](https://github.com/yucing/linux/blob/main/picture/sleep2.png)

## nice : 指定優先權
* -20 ~ 19 表示, 數值愈低, 優先權愈大
* -n 數字 : 指定優先權

![](https://github.com/yucing/linux/blob/main/picture/nice.png)

## kill : 刪除行程
* kill -9 PID : 強制刪除

![](https://github.com/yucing/linux/blob/main/picture/kill.png)

* kill -1 PID : 重新加載
* pkill PID / 名稱