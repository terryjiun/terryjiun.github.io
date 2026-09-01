---
title: 泰瑞版小小輸入法─相關字詞篇
date: 2011-01-08 10:10:00 +0800
categories: [泰瑞版小小輸入法]
tags: [Terry_Yong, 倉頡, 注音, 碼表]
---

使用小小輸入法搭配倉頡碼表的情況下，<br>
小小雖然有「反查組字字根時只會列出英數碼而不會列出倉頡碼」的問題，<br>
但是畢竟小小是大陸網友製作的，服務對象也以大陸民眾為優先，<br>
大陸民眾用的中文輸入法大多都是英數碼，<br>
沒有台灣民眾有注音碼、倉頡碼、大易碼這些問題，<br>
所以小小忽略這一部分倒也無可厚非。<br>
（<br>
2011.01.15 補註：<br>
關於「反查組字字根時只會列出英數碼而不會列出倉頡碼」這個問題，<br>
在 2011.01.09 發佈的小小輸入法裡已經被解決了！<br>
但是反查時仍然只能用手動的方式反查，暫時無法設定自動反查！<br>
）<br>
<br>
所幸！小小有「相關字詞」（即「聯想詞」）的功能，<br>
我們可以用它來實現自動反查組字字根。<br>
我最近整理的「泰瑞版小小輸入法」（[按此下載](https://terryjiun.github.io/posts/Terry-Yong-Guide/){:target="_blank"}）<br>
把相關字詞的相關檔案放在「LC」資料夾下了！<br>
為了避免檔案太大而浪費網友的下載時間，<br>
我在「LC」資料夾裡只放了「LC.txt」、「LC&#95;Phon.txt」這兩個檔案。<br>
前者是取自「Windows XP 繁體中文版」的相關字詞，<br>
雖然有點老舊，相關字詞的數目也不多，<br>
但足以應付一般所需了！<br>
<br>
我又整理了注音、倉頡、嘸蝦米的相關字詞，<br>
需要的網友可以到這裡下載：<br>
[https://www.mediafire.com/file/xs15uradyaj9rtt/Terry_LC.zip](https://www.mediafire.com/file/xs15uradyaj9rtt/Terry_LC.zip){:target="_blank"}<br>
這個壓縮檔裡有 6 個檔案，它們的用途是：<br>
2Boshiamy.txt：以嘸蝦米碼為相關字詞。<br>
（依碼數排列，以方便查詢「最簡碼」；<br>
因為我整理的碼表裡有 VRSF 選字，所以這裡列出的嘸蝦米碼末尾也會帶有 VRSF）<br>
2Chajei.txt：以倉頡碼為相關字詞。<br>
2Phon.txt：以注音碼為相關字詞。<br>
LC&#95;Boshiamy.txt：以嘸蝦米碼為相關字詞，並結合常用相關字詞。<br>
LC&#95;Chajei.txt：以倉頡碼為相關字詞，並結合常用相關字詞。<br>
LC&#95;Phon.txt：以注音碼為相關字詞，並結合常用相關字詞。<br>
有需要的人可以將上述檔案放到「LC」資料夾下，<br>
然後再編輯 yong.ini 的相關字詞檔案來源路徑，<br>
最後再重新執行小小就可以了！<br>
<br>
不過，用這樣的相關字詞有兩個缺點：<br>
一是：比如我在聊天室裡打到「吧」字結尾，<br>
按 Enter 送出時，它只會先清除相關字詞視窗，<br>
要再按一次 Enter 才會真的送出我打的句子；<br>
二是：比如打「99年12月25日」時，<br>
打完「年」後要先按 ESC 將相關字詞視窗關閉，<br>
不然接下來按「12」時會選到第一個相關字詞。<br>
<br>
有興趣的人下載回去用看看吧！<br>
以<span style="color: purple">倉頡</span>反查<span style="color: red">注音</span>為例，我建議將 yong.ini 改成：<br>
一、在「&#35;輸入法模式」末尾加上「<span style="color: blue">9=</span><span style="color: purple">Chajei2</span>」<br>
二、在「&#35;輸入法模式快速切換」末尾加上「<span style="color: blue">switch&#95;9=CTRL&#95;9</span>」<br>
三、在 yong.ini 的最末尾加上這段：<br>
<span style="color: blue">&#91;<span style="color: purple">Chajei2</span><span style="color: blue">&#93;</span><br>
<span style="color: blue">name=</span><span style="color: purple">倉頡聯想</span><br>
<span style="color: blue">engine=libmb.so<br>
arg=mb/</span><span style="color: purple">Chajei.txt</span><br>
<span style="color: blue">trad=1<br>
overlay=mb/</span><span style="color: purple">Chajei.ini</span><br>
<span style="color: blue">legend=LC/LC&#95;</span><span style="color: red">Phon.txt</span><br>
然後，真的需要用到自動反查注音或相關字詞時，<br>
再按 Ctrl+9 切換到「倉頡聯想」模式去打字，<br>
用完後再按 Ctrl+0 切回「泰瑞倉頡」模式來打字。<br>
