---
title: 支援 CJK Ext-B 字元的「泰瑞拼音輸入法對照表」（製作過程篇）
date: 2009-12-06 10:10:00 +0800
categories: [輸入法]
tags: [CJK, 拼音, 碼表]
---

整理好「泰瑞注音輸入法對照表」之後，<br>
我們當然可以將它轉換成拼音輸入法的對照表，<br>
但是如果沒有好的工具程式來輔助的話，<br>
注音轉拼音其實不是件容易的事！<br>
<br>
先將「泰瑞注音輸入法對照表」裡的「1」取代成「ㄅ」…「g」取代成「ㄕ」…「-」取代成「ㄦ」…<br>
也就是將全部的組字字根轉回注音，是必須花的基本工夫。<br>
另外，最好將聲調也獨立出來，<br>
因為拼音的聲調並不是用「ˊ-ˇ-ˋ-˙」表示，而是用「2-3-4-5」表示。<br>
使用 EditPlus 編輯時，只要把：<br>
「ˊ」+「空白」取代為「2」+「Tab 字元」；<br>
「ˇ」+「空白」取代為「3」+「Tab 字元」；<br>
「ˋ」+「空白」取代為「4」+「Tab 字元」；<br>
「˙」+「空白」取代為「5」+「Tab 字元」；<br>
最後再將「空白」取代為「1」+「Tab 字元」（或單獨的「Tab 字元」）就可以了！<br>
<br>
如果沒有工具程式輔助的話，就要依這個網頁（http://www.homeinmists.com/shuowen/zhuying.html）上的說明，<br>
將對照表的「&#42;ㄨㄥ」取代成「&#42;ong」<br>
（「&#42;」代表有聲母，如「ㄏㄨㄥ」就取代成「hong」、「ㄓㄨㄥ」就取代成「zhong」；<br>
「&#42;」從「ㄅ」到「ㄙ」都算，這類的規則要在第一階段轉換），<br>
再將「ㄨㄥ」取代成「weng」<br>
（前面沒有聲母的情況，例如「ㄨㄤ」，就取代成「wang」；<br>
這類的規則要在第二階段轉換），<br>
最後把「ㄅ」取代成「b」、「ㄕ」取代成「sh」…<br>
分階段轉換的原因是：<br>
如果不這麼做，而將「ㄅㄨㄥ」先轉換成「bㄨㄥ」，然後再將「bㄨㄥ」轉成「bweng」的話，就會產生錯誤。<br>
不只含有「ㄨ」音的字有這個問題，含有「ㄧ」、「ㄩ」音的字也有這個問題。<br>
<br>
但是這樣的轉換方式太累人了！<br>
所以我們要借助這個網頁的工具程式：<br>
[https://www.pinyin.info/tools/converter/bpmf2hp.html](https://www.pinyin.info/tools/converter/bpmf2hp.html){:target="_blank"}<br>
（上述網頁轉換功能已失效，可改用：<br>
[https://m-calc.com/zhuyin-pinyin](https://m-calc.com/zhuyin-pinyin){:target="_blank"}<br>
或<br>
[https://www.chineseconverter.com/zh-tw/convert/zhuyin](https://www.chineseconverter.com/zh-tw/convert/zhuyin){:target="_blank"}<br>
）
由於這個網頁的表單不接受斷行，<br>
所以我們要先將斷行都改為空白，<br>
轉好再將空白取代為斷行即可。<br>
<br>
「泰瑞拼音輸入法對照表」的製作過程就是這麼簡單，<br>
只是我是把「漢字及其組字字根」貼到 Excel 工作表裡再來整理，<br>
然後以一到兩萬字為單位，分批用上述的網頁及方法進行轉換。<br>
至於「符號及其組字字根」一樣是延用「泰瑞倉頡輸入法對照表」裡的內容。<br>
