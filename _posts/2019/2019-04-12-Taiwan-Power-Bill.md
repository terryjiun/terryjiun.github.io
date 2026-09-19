---
title: 台電-非時間電價-電費計算方式（自製 xlsx 檔，附常見電器耗電量計算表）
date: 2019-04-12 10:10:00 +0800
categories: [財經企管]
tags: [實用工具]
---

<b>針對2023年4月1日起實施的新電價，請使用下列 Google 線上試算表計算：<br>
2025年10月1日起實施之電價線上試算表：<br>
[https://docs.google.com/spreadsheets/d/1YCA_NB0_xFHuI5ITki_h2tFX_TydizfnnnaddyzWXAg/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1YCA_NB0_xFHuI5ITki_h2tFX_TydizfnnnaddyzWXAg/edit?usp=sharing){:target="_blank"}<br>
2024年4月1日起實施之電價線上試算表：<br>
[https://docs.google.com/spreadsheets/d/1g_dvhDsFOXOgl3e1Cr76arDuxL46xKj02SShZKw5jms/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1g_dvhDsFOXOgl3e1Cr76arDuxL46xKj02SShZKw5jms/edit?usp=sharing){:target="_blank"}<br>
<span style="color: blue">筆者公開之 Google 試算表一律設定保護（以免下一位開啟之讀者無法使用），<br>
請讀者點選試算表右上方之「登入」，然後登入自己的 Google 帳戶，<br>
再按試算表「檔案」下拉式功能表裡的「</span><span style="color: red">建立副本</span><span style="color: blue">」，<br>
就可以</span><span style="color: red">另存新檔</span><span style="color: blue">到讀者自己的 Google 雲端硬碟，</span><span style="color: red">讀者可對自己的副本任意編輯、查看公式（函數）及各種設定值。<br>
請勿要求存取權！</span>不然筆者將公告違規者的 GMail！<br>
本文所述新、舊電價計算原理相同，有興趣的網友仍可參考下文，惟筆者自製之 Excel 檔已不再更新。<br>
<hr>
<span style="color: fuchsia">本行(列)以下內容係針對2018年4月1日至2022年6月30日實施的舊電價進行分析、設計，無興趣之讀者可自行略過！</span></b><br>
<br>
對台灣電力公司公告的「電價表」有興趣的讀者，可以先連結至下列網頁查看：<br>
[https://www.taipower.com.tw/2289/2290/46940/46945/normalPost](https://www.taipower.com.tw/2289/2290/46940/46945/normalPost){:target="_blank"}<br>
<br>
目前大家使用的電價計算種類可能以「非時間電價」為主（只區分夏月及非夏月，不區分每日用電時段），<br>
台電雖然有提供試算電費的網頁：[https://service.taipower.com.tw/ebpps2/electricityFeeTrial](https://service.taipower.com.tw/ebpps2/electricityFeeTrial){:target="_blank"}<br>
但是它不會列出詳細的計算過程，<br>
所以筆者參考了一些電費收據，然後編製出一個會自動計算電費的 Excel 檔，它的下載網址如下：<br>
[https://www.mediafire.com/file/6tea8gedl897o2c/Terry_Power.zip](https://www.mediafire.com/file/6tea8gedl897o2c/Terry_Power.zip){:target="_blank"}<br>
（下載後，解壓縮，即可使用 Excel 開啟）<br>
<br>
這個 Excel 檔只針對「非時間電價」進行設計，<br>
不適用於二段式（尖峰+離峰）、三段式（尖峰+半尖峰+離峰）或其他計價方式的用戶。<br>
一般大眾使用的是「非時間電價」之「表燈用電」，它又可分為：非營業用、營業用、臨時用電。<br>
計費期間又有分隔月（兩個月）、單月（通常是用電量較大的用戶）；<br>
如果是離島居民，台電依照「離島建設條例」減免營業稅，所以每度用電的單價就要除以 1.05。<br>
臨時電的單價是「營業用電」單價的 1.6 倍，但如果是離島地區，則是乘以 1.6，再除以 1.05。<br>
筆者目前看過的臨時電都是以「營業用」計算，<br>
即使是以個人名義申請臨時用電（帳單上未列出用戶統編），仍然是以「營業用」計算。<br>
<br>
因此，筆者將前述的 Excel 檔區分出不同的工作表，對應到上述各種情形。<br>
工作表名稱中帶有「住家」二字，代表「非營業用」；工作表名稱中帶有「公司」二字，代表「營業用」。<br>
讀者應該不難找出適合自己情形的工作表，如下圖所示：

![台電-非時間電價-電費計算方式-Excel畫面](/assets/img/other/Taiwan-Power-Bill.png)

筆者在各個工作表中已先填入紅色數值作為測試之用，<br>
使用者只需要依自身的狀況修改紅色數值，然後 Excel 就會幫您計算出對應的結果。<br>
值得一提的是「節電獎勵」這一項，只有住家及學校（限國中、國小）等一些特定的用戶才能享受，<br>
而且一定要【[上網登錄電號](https://www.taipower.com.tw/2289/2406/2407/2408/11869/normalPost){:target="_blank"}】（或打1911電話聯絡台電客服），完成報名後，<br>
當期用電度數比去年同期「有減少」就會獲得「每度 0.6 元」的獎勵（會從應繳金額中直接扣抵）！<br>
<span style="color: red">沒有登錄電號的話，即使當期用電度數比去年同期「有減少」，並不會獲得獎勵！</span><br>
台電的活動辦法規定：「當期用電每節省一度，可獲得0.6元獎勵金，如每期(2個月)獎勵金低於84元者，按84元計算」，<br>
所以省1度電，獎勵金是84元；省10度電，獎勵金也是84元；省140度電(84÷0.6)，獎勵金仍是84元。<br>
要省到140度以上，才是適用「節省度數×0.6元=獎勵金」的計算公式！<br>
<br>
離島居民則是獲得「每度 0.6/1.05 元，約等於 0.5714285 元」的獎勵。<br>
台電很奇怪，離島適用的單價數值通常都算到小數點後 7 位數，<br>
而且是用無條件捨去法（Excel 函數中的「ROUNDDOWN」），<br>
但是金額則是「元」以下用四捨五入法（Excel 函數中的「ROUND」）。<br>
<br>
另外，筆者還套用了公式，讓使用者輸入某一段用電的日期區間後，<br>
Excel 就會自動計算出總天數及符合夏月（6/1～9/30）的天數。<br>
<span style="color: purple">在台電公布新的電價方案之前，筆者並不會修改 Excel 檔案裡的「夏月起始日：夏月結束日」，<br>
所以，如果使用者計算的年份不是 2019 年的話，請記得手動修改這兩個對應的儲存格。<br>
其實輸入日期時，也可以簡化成輸入「6/1」，Excel 就會判斷當前作業系統的時間，然後補上當前的年度。</span><br>
<b>（假設 Windows 當前時間為 2019/4/12 PM8:00，輸入「6/1」後，就會自動轉為「2019/6/1」）</b><br>
<br>
最後，筆者還在前述 Excel 檔裡附上「冬季用電」、「夏季用電」這兩個工作表，<br>
想要試算自己每天、每月會用多少度電的讀者，可自行增、修來計算看看。<br>
通常電器上都會貼上防水貼紙（或印上表格），標示「耗電量(W)」、「耗功率(W)」，<br>
讀者可先查看、確認自己的電器後，再將正確瓦數（W）填入這兩個工作表。<br>
（但是有時電器並不會以最高速、最耗電方式運轉，所以填入工作表後，可能發生高估的情形）<br>
如果電器上沒標示出多少 W（瓦特）的話，可以上網查詢，或是看變壓器上的數值。<br>
像是變壓器或電器上有標示「DC 9V」、「2A」，則經由「功率＝電壓×電流」的公式可得出 18 W。<br>
<br>
因為台電電價是採「累進計費」，企圖「以價制量」，<br>
所以用電量越過下一級的門檻後，超過的度數就會用下一級的單價計費，<br>
因此以小家庭（3～5 人）來看，<br>
夏天能控制在每兩個月 2000 度以內最好；冬天能控制在每兩個月 660 度以內最好。<br>
<br>
歷史版本留存：<br>
2023年4月1日～2024年3月31日實施之電價線上試算表：<br>
[https://docs.google.com/spreadsheets/d/1skUwyMelLOwuGe7yry9Gf0QoMLNRuNSJMeekJf5hJuw/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1skUwyMelLOwuGe7yry9Gf0QoMLNRuNSJMeekJf5hJuw/edit?usp=sharing){:target="_blank"}<br>
