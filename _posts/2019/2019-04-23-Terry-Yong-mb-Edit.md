---
title: 泰瑞版小小輸入法─碼表格式與編修要領
date: 2019-04-23 10:10:00 +0800
categories: [泰瑞版小小輸入法]
tags: [Terry_Yong, 碼表]
---

今天筆者回覆了一位網友使用自定義碼表的問題，<br>
想說可能也會有其他讀者有同樣的疑問，因此將回覆內容整理如下。<br>
<br>
<span style="color: purple">一、小小輸入法有自己的碼表格式，不能直接使用 cin 檔的格式。</span><br>
<br>
cin 檔是 gcin 這類軟體（在 Linux 作業系統上運行的中文輸入法平台）的碼表格式，組成段落如下：<br>
（<span style="color: blue">以「&#35;」開始的那一列為下一列的註解</span>）<br>
&#35;輸入法英文名稱：<br>
%ename Dayi4<br>
&#35;輸入法中文名稱：<br>
%cname 大易四碼<br>
&#35;候選字選擇鍵：<br>
%selkey 1234567890<br>
%keyname begin<br>
（使用按鍵與顯示字根，略）<br>
%keyname end<br>
%chardef begin<br>
（碼表內容，略）<br>
%chardef end<br>
<br>
而小小輸入法則有自己的專屬碼表格式，<br>
詳細說明請開啟「Terry&#95;Yong\yong.chm」這個檔案，參閱「其他說明→碼表設置」。<br>
小小輸入法不必指定各個輸入法的英文名稱，而各個輸入法的中文名稱則定義在 yong.ini 裡。<br>
以泰瑞版小小輸入法的「大易四碼」為例，<br>
它的「候選字選擇鍵」定義在「Terry&#95;Yong\ini\Dayi.ini」這個檔裡。<br>
「使用按鍵與顯示字根」儲存於「Terry&#95;Yong\Key\DayiKey.txt」這個檔裡（它是一個 GB18030 編碼的文字檔）。<br>
碼表則儲存於「Terry&#95;Yong\mb\Dayi4.txt」這個檔裡，它的組成段落如下：<br>
（<span style="color: blue">以「&#35;」開始的那一列為下一列的註解</span>）<br>
&#35;碼表編碼：<br>
encode=UTF-8<br>
&#35;碼表名稱（參考用）：<br>
name=大易四碼<br>
&#35;使用按鍵（<span style="color: red">注意！大小寫視為不同</span>）<br>
key=abcdefghijklmnopqrstuvwxyz1234567890=;,./<br>
&#35;最大碼長：<br>
len=5<br>
&#35;上屏設置（commit=全碼不自動上屏 空碼自動上屏碼長 空碼時上屏的碼長，看不懂的話，只改「中間的數值=最大碼長」就好）：<br>
commit=1 5 0<br>
&#35;精確匹配（1=是）：<br>
match=1<br>
&#35;空碼時自動清空輸入欄（1=是）：<br>
auto&#95;clear=1<br>
&#35;萬能鍵設置：<br>
wildcard=`<br>
&#35;第一碼不應用萬能鍵（0=否）：<br>
dwf=0<br>
&#35;指定輔助碼表（設定「'」為引導鍵，按此鍵後，可進入注音輸入模式）<br>
assist=' mb\Phon.txt<br>
&#35;碼表內容開始：<br>
&#91;data&#93;<br>
（碼表內容，略）<br>
<br>
<span style="color: purple">二、除非必要，否則碼表內容最好全部用小寫，不要大小寫夾雜。</span><br>
<br>
<span style="color: purple">三、碼表內容由「編碼 字詞」組成，統一用〝一個〞「半型空白」分隔，不要夾雜用「TAB」分隔。</span><br>
<br>
<span style="color: purple">四、避免碼表內容出現「新細明體」、「新細明體-ExtB」顯示不出來的字元。</span><br>
<br>
雖然筆者在「[★泰瑞版小小輸入法 for CJK Ext-E](https://terryjiun.github.io/posts/Terry-Yong-CJK-Extension-E/){:target="_blank"}」這篇文章有介紹如何安裝大字集的字型，<br>
並且提供了一套特製版的泰瑞版小小輸入法供大家下載使用，<br>
但是因為設定頗為煩瑣，建議分享給別人使用時，仍應注意「系統字型」（或「指定字型」）支援字元的問題。<br>
<br>
<span style="color: purple">五、避免碼表內容出現空白列。</span><br>
<br>
如果要區分段落，可以用「&#35;」或「&#35;&#35;」作為開頭，然後為下一個段落留個註解。<br>
<br>
<span style="color: purple">六、找出最大碼長的方式：</span><br>
<br>
先將碼表內容（開端設置不算，只算 &#91;data&#93; 以後的部分）裡的兩個「半型空白」取代成一個「半型空白」（兩空變一空），<br>
執行一次，再執行一次，直到編輯軟體（EditPlus、NotePad++…）提示「找不到可以取代的內容」，<br>
然後再將「半型空白」取代成「TAB」（需使用「\t」這個正則運算式，不可以取代成「TAB」三個英文字母），<br>
複製後，開啟 Excel，先將 A、B 欄的格式設為「文字」（用意是避免「04」這樣的編碼被 Excel 自動修正為「4」），<br>
再貼到 Excel 的 A1 儲存格，碼表內容就會自動分成 A、B 兩欄，<br>
然後在 C1 儲存格填入「<span style="color: red">=LEN(A1)</span>」，再用「填滿」的方式填滿 C 欄（過程會用到 Excel 操作技巧，此處不贅述），<br>
最後篩選 C 欄，即可找出最大碼長。<br>
<br>
<span style="color: purple">七、小小輸入法會自動過濾重複的編碼：</span><br>
<br>
如果碼表內容裡有出現「a 人」兩次（在不同列，也許隔了很多列），<br>
使用小小輸入法組字時，顯示在候選字視窗的當下，只會顯示一個「1.人」。<br>
如果讀者不熟悉 Excel 移除重覆字詞的作法（或小小輸入法自帶的優化碼表操作方式），<br>
可以忽略碼表中有重複編碼的問題，不去管它。<br>
