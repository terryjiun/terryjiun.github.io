---
title: 新細明體更新套件（三）：輸入法篇
date: 2008-11-09 10:30:00 +0800
categories: [字碼與字型]
tags: [Windows, 新細明體, 字型下載]
---

一般情況下，<br>
除非使用的作業系統是 Windows Vista 或 Server 2008，<br>
不然造訪我所寫的這篇文章─<br>
《測試無名小站的資料庫能否儲存 CNS11643 的怪字》，<br>
應該會出現以下的畫面：<br>
![XP-IE-PMingLiU](/assets/img/font/PMingLiU-Update-Pack-0A.jpg)
<br>
也就是紅色框線內應該顯示的文字並不會正確的顯示出來！<br>
<br>
如果使用的是 Windows Vista、Server 2008 的話，<br>
則可以正常顯示：<br>
![XP-IE-PMingLiU-Update](/assets/img/font/PMingLiU-Update-Pack-0B.jpg)
<br>
Windows XP/Server 2003 在安裝「新細明體更新套件」後，<br>
就能和 Vista/Server 2008 一樣正常顯示那些罕見的 CJK Ext-A、CJK Ext-B 的字元了！<br>
<br>
解決了顯示的問題後，<br>
來談談如何打出這些字的問題，<br>
也就是輸入法的問題。<br>
<br>
如果你不會倉頡、大易、行列、嘸蝦米…這類的輸入法，<br>
就必須先知道這些字的注音。<br>
因為這些罕見字通常不容易猜出它的讀音<br>
所以必須去查康熙字典、[教育部的異體字字典](https://dict.variants.moe.edu.tw/){:target="_blank"}，<br>
或行政院主計處建置的「[CNS11643中文標準交換碼全字庫](https://www.cns11643.gov.tw/){:target="_blank"}」（建議用這個）。<br>
<br>
例如要找「𡴭」（左山右乙）和「𡴯」（上山下乙）的讀音，<br>
可以連上「[CNS11643中文標準交換碼全字庫](https://www.cns11643.gov.tw/){:target="_blank"}」後，<br>
點選「字碼查詢&下載」，然後用「複合查詢」<br>
（不建議使用筆劃、部首查詢，因為查出來的字會很多，不好找；<br>
　更不要用筆順序查詢，因為如果字體太複製的話，會浪費太多時間），<br>
【型態一：請選擇筆畫數】拉選「4」（本例字元的總筆劃），<br>
接著，點選【型態二：請輸入部首】右邊的「進入部首代表號表」，<br>
找到〝三畫〞的「山」，記下它的代號是「46」，<br>
然後將它輸入【型態二：請輸入部首】下方的欄位，<br>
最後按頁面上方的「開始搜尋」，<br>
就可以找到這兩個字了，<br>
「𡴭」（左山右乙）唸「ㄧㄚˋ」，會倉頡的人一看就知道它的倉頡碼是「山弓」；<br>
「𡴯」（上山下乙）唸「ㄜˋ」，會倉頡的人一看就知道它的倉頡碼也是「山弓」。<br>
<br>
知道了它的讀音或倉頡碼，<br>
就可以來輸入這些文字了！<br>
（但即使用全字庫網站的字碼查詢功能，<br>
也未必查得到注音，因為 CJK Ext-A/B 區的很多字元都是沒有注音的，<br>
所以建議常常有罕見字需求的人一定要去學倉頡輸入法）<br>
在 Vista/Server 2008 裡，<br>
預設只能輸入 20,902 個 CJK 的漢字，<br>
但開啟輸入法設定的畫面後，<br>
按照下圖進行設定，就可以輸入上面說的那兩個字了！<br>
<br>
圖1：<br>
![PMingLiU-Update-Pack-01](/assets/img/font/PMingLiU-Update-Pack-01.jpg)
<br>
圖2：<br>
![PMingLiU-Update-Pack-02](/assets/img/font/PMingLiU-Update-Pack-02.jpg)
<br>
圖3：<br>
![PMingLiU-Update-Pack-03](/assets/img/font/PMingLiU-Update-Pack-03.jpg)
<br>
圖4：<br>
![PMingLiU-Update-Pack-04](/assets/img/font/PMingLiU-Update-Pack-04.jpg)
<br>
圖5：<br>
![PMingLiU-Update-Pack-05](/assets/img/font/PMingLiU-Update-Pack-05.jpg)
<br>
在圖5中，<br>
各位會看到三種顏色的字元，<br>
其中黑色字是 20,902 個屬於 CJK 的字元，<br>
綠色字是 6,582 個屬於擴展 A 區的字元，<br>
紅色字是 42,711 個屬於擴展 B 區的字元。<br>
我不確定是否可以打出「香港增補字符集（HKSCS）」的字元，<br>
其實它們大多數都已經被納入 CJK 及其擴展 A、B 區中了！<br>
以「新倉頡輸入法 2007」在 Word 2007 中輸入<br>
「駅」、「曱」、「甴」、「𠗟」這些 HKSCS 的字元為例，<br>
並不會出現兩種選擇。<br>
<br>
在圖3「字元集設定」的畫面中，<br>
建議勾選前兩個核取框就好<br>
（也就是只勾選擴充 A、B 區的字元），<br>
因為「新細明體更新套件」並不支援 HKSCS 字元集，<br>
一旦用到 HKSCS 字元集時，<br>
只有 Vista（或以後的 Windows）才有對應的字型可以顯示字元，<br>
Windows XP/Server 2003 即使安裝了「新細明體更新套件」，<br>
還要再安裝額外的字型才能顯示字元<br>
（除非 XP/Server 2003 的使用者另外再安裝「Vista 新細明體字型」 ）。<br>
<br>
另外，不管從圖1中點選倉頡或注音輸入法→「內容」→「字元集設定」，<br>
會套用同一個共用的組態值；<br>
點選新倉頡或新注音後，則會套用另一個共用的組態值，<br>
也就是說無法針對各別的輸入法一一套用不同的設定。<br>
<br>
在 Windows XP/Server 2003 中，<br>
想要能顯示這些罕見字就要安裝「新細明體更新套件」（最多更改顯示字型，但不必再做額外的設定），<br>
或安裝「Vista 新細明體字型」、其他「支援 CJK 及其擴展 A、B 區的字型」<br>
（安裝此類字型時，除了更改顯示字型外，還需要再做額外的設定）。<br>
但想要打出這些字，則必須安裝 Office 2007，<br>
或安裝我提供的「泰瑞倉頡輸入法」、「泰瑞嘸蝦米輸入法」。<br>
（<span style="color: blue">安裝「新細明體更新套件」後，<br>
會更新 XP/Server 2003 的倉頡和注音輸入法，<br>
但只是補上擴展 A 區字元的拆碼方式；<br>
雖然它的說明檔裡有提到安裝 Microsoft New IME 6.0，<br>
也就是 Office XP 的新倉頡和新注音輸入法即可輸入擴展 B 區的字元，<br>
但我試驗的結果是失效的！</span>）<br>
<br>
在安裝 Office 2007 時，<br>
它會將 Windows XP/Server 2003 的新注音和新倉頡輸入法更新為 2007 版，<br>
這個版本和 Vista/Server 2008 的大同小異，<br>
如下圖：<br>
<br>
圖6：<br>
![PMingLiU-Update-Pack-06](/assets/img/font/PMingLiU-Update-Pack-06.jpg)
<br>
圖7：<br>
![PMingLiU-Update-Pack-07](/assets/img/font/PMingLiU-Update-Pack-07.jpg)
<br>
圖8：<br>
![PMingLiU-Update-Pack-08](/assets/img/font/PMingLiU-Update-Pack-08.jpg)
<br>
圖9：<br>
![PMingLiU-Update-Pack-09](/assets/img/font/PMingLiU-Update-Pack-09.jpg)
<br>
如果你不想安裝 Office 2007 的話，<br>
網路上有獨立出來的 Office 2007 輸入法安裝程式，<br>
各位可以用 Google 搜尋「Office 2007 輸入法」，<br>
就能獲得很多的訊息，在此就不多做說明了！<br>
（微軟官方提供的「獨立的」輸入法安裝程式只有到 2003，<br>
網友獨立出來的 Office 2007 輸入法安裝程式會有一百多 MB，<br>
並不是它對 CNS11643 及擴充 A、B 區、HKSCS 字元的支援而使檔案變得如此龐大，<br>
主要原因在於它包含了手寫和語音輸入的功能）。<br>
