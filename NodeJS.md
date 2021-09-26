---
title: NodeJS Workshop for MFEE20 (1)
tags: iii-mfee20
description: NodeJS Workshop for iii MFEE20
version: 20210919
---

# NodeJS Workshop for MFEE20 (1)

Ashley (小賴)
ashleylai58@gmail.com

共筆: 
- [Git Workshop for MFEE20](https://hackmd.io/@ashleylai/S1SJk5pMt)

- [NodeJS 共筆](https://hackmd.io/@ashleylai/S1p51vEmt)


上課錄影檔: https://drive.google.com/drive/folders/1-bh6JHVJ0551ncXl6nbH4_WUb0C_uMbV?usp=sharing

作業繳交: https://docs.google.com/spreadsheets/d/1L9uniJq0n9u-PGADwk6IxV-oj92cwucqFZDwiBL-wWc/edit?usp=sharing


已經上線的同學可以寫一下測驗
- 9/26 測驗 https://forms.gle/vmnK9onhmi2aEeA16
    - 9:20 
另外，關於觀影心得，在 hello-git repo 有以 issue 的方式回覆，
同學可以去看過，看過後可以回覆或是關掉那個 issue。

---

# NodeJS

NodeJS 是什麼？

- 框架？
- JS架構下的開發工具？
以下三個是前端
- 動畫？
- 寫網頁功能？
- 互動？

NodeJS 一般來說：可以用 javascript 寫後端程式

到目前為止，你們寫的 JS 在哪裡被執行？ --> 瀏覽器
瀏覽器可以執行 JS 是因為它內建了 JS 的執行環境

==> NodeJS 讓你在瀏覽器以外執行 JS 的環境

JS 有兩種執行環境:
- 瀏覽器
- NodeJS

NodeJS 是一個程式語言？ 不是！ Javascript 才是程式語言
NodeJS 是框架嗎？ 不是！

![](https://i.imgur.com/JcXqMC2.png)

window.location ==> window object 

document.getElementById => html 

==> 瀏覽器提供

## 安裝方法

- 直接安裝 nodejs
 
LTS: long-term support 長期維護版
    - Current: 最新的、目前的
    - Active LTS: 正在積極維護跟升級中的版本
    - Maintenance LTS: 維護中的 LTS 直到生命週期結尾
    - EOL: end of life

- nvm: node version manager

「安裝路徑不可以出現中文字」

- mac:
https://github.com/nvm-sh/nvm#install--update-script

- windows:
https://github.com/coreybutler/nvm-windows/releases

```bash=

$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash


# 確認自己用的 shell 是哪一種後，修改相對應的設定檔
$ echo $0

# 根據 echo $0 的結果，下方選擇一個來確認
$ cat ~/.zshrc
$ cat ~/.bashrc

# 關掉 terminal 重新啟動
$ nvm -v
```

windows
nod nodespus

nvm-setup.zip


```bash=
# 列出可以安裝的版本
$ nvm ls-remote 14
# windows版本
$ nvm list available

# 安裝最新的 LTS
$ nvm install 14.17.6

# 切換版本
$ nvm use 14.17.6

# 確認目前 node 的版本
$ node -v

# 列出你電腦裡 node 的版本
$ nvm ls
# windows 用 list
$ nvm list

# 設定預設版本
$ nvm alias default 14.17.6
```

## 寫第一個 nodejs 程式

1. 在 github 上建立一個 hello-node 專案，勾選建立 readme

2. 找到自己這個專案的 url，在 home 目錄下 clone 這個專案

```bash=
$ cd ~
$ git clone <url>
```

3. 用 vscode 開啟這個專案，在專案內建立 practice 檔案夾

4. 在 practice 內建立 sum.js

```javascript=
console.log("hello world!");

function sum(param) {
  // TODO: 請從 1 + 2 + 3 + .... + param
}

console.log(sum(3)); // 6
console.log(sum(6)); // 21
console.log(sum(10)); // 55
```

5. 測試結果

```bash=
$ cd practice
$ node sum.js

# 如果不切換
$ node practice/sum.js
```

6. 測試OK，請 push 到 github，在 excel 打勾

期限: 16:45


==9/19==

作業

- 完成 sum.js 並且推上 github -> 如果有 issue 要解
- 觀看影片 https://www.youtube.com/watch?v=DgbSc6Ys710
    - 在 hello-git 建立一個 video.md 的檔案
    - 在這個檔案紀錄心得/筆記
    - 學習對的學習方式，事半功倍
- 這兩天上課的筆記/心得
    - hello-git 的 readme.md
- 複習 javascript 
    - map, filter, indexOf, join, map, pop, push, reduce, slice, splice, sort 這幾個函式暸解一下
https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Reference/Global_Objects/Array
    - 箭頭函式
    
星期五晚上 9:00 以前



mac --> brew
ubuntu --> apt
centOS --> yum
windows???



資料結構 & 演算法

- 資料結構 Data Structure (DS)
    資料怎麼儲存、怎麼存取、之間的關係的時候
    例如: array
- 演算法 Algorithm (algo)
    怎麼「有效率」解決一個題目
    - 時間複雜度: 通常會希望愈快愈好
    - 空間複雜度: 通常會希望用盡量少的記憶體

「用空間換取時間」


練習平台: leetcode (刷題)


梯形公式
從 1 加到 100000，重複 10000 次
SUM1: 2.289ms
從 1 加到 100，重複 10000 次
SUM1: 20.609ms
==> 在 n 很大的情況下，表現會比較好

for 迴圈的做法：
從 1 加到 100000，重複 10000 次
SUM2: 1.278s
SUM2: 4.675ms
==> 在 n 比較小的情況下，表現會比較好

- 梯形公式是 O(1) 的寫法，for-loop 是 O(n) 的寫法， O(n) 時間複雜度比較高。
- 時間複雜度跟真正的執行時間，不是一定符合的
- 時間複雜度的討論通常在 n 比較大的情況下
- 寫程式之前想一下
    - 當你學會用鐵鎚的時候，你會覺得全世界都是釘子


------

NodeJS

> node sum.js

Ryan: web 伺服器方面的問題，研究過 apache, C, Lua, Haskell 或是 Ruby

瀏覽器大戰

netscape 瀏覽器 X 
Microsoft windows, IE 6 獨佔
--> firefox
--> Chrome javascript 執行引擎 V8 --> 非常有效率的 JS 引擎

node 使用 chrome V8 來當作核心
- Chrome V8
- firefox SpiderMonkey
- Safari: Nitro (?)
- Edge: Chakra --> V8


# JS 語言的特性

- 單執行緒
- 非阻塞
- 非同步IO
- 事件循環

## 單執行緒

作業系統 Operation System (OS)

編譯式: 要事先經過「編譯」 compile -> 把程式碼轉換成機器看得懂的語言
直譯式: 在執行的當下才去做轉換

```
硬碟   記憶體   CPU裡的register
大 <---------->    小
便宜               貴
慢                 快
```

![](https://i.imgur.com/azCAxXO.png)

I/O: input/output
- 硬碟存取(開檔、讀檔)
- 網路存取
I/O 相較於 CPU 運算是非常花時間

排程 scheduling: 怎麼安排 process？什麼時候可以輪到使用 CPU?


# 補充資料

## Crash Course
https://www.youtube.com/watch?v=tpIctyqH29Q&list=PL8dPuuaLjXtNlUrzyH5r6jN9ulIgZBpdo
https://crashcourse.club/category/
