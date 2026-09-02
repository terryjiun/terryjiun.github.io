---
title: ★泰瑞版小小輸入法 for CJK Ext-I
date: 2025-08-14 10:10:00 +0800
categories: [泰瑞版小小輸入法]
tags: [Terry_Yong, 碼表更新, CJK]
---

重要提醒：<br>
「泰瑞版小小輸入法 for CJK Ext-J」已經發布於筆者的【[Google 雲端硬碟](https://docs.google.com/leaf?id=0B_9ob1iJjpkLMmRjODE2NWQtNjViNC00ZWRkLTgyY2ItNGJhOWEzODU1ZDNh){:target="_blank"}】或【[OneDrive](https://1drv.ms/f/c/01b7d23cf55aac84/QoSsWvU80rcggAHPAgAAAAAAEkEClyhF5XEafA){:target="_blank"}】<br>
「<span style="color: red">輸入法相關</span>→<span style="color: red">輸入法軟體</span>→<span style="color: red">公開測試版</span>」目錄之下，<br>
以後這個目錄之下所存放的泰瑞版小小輸入法內含的泰瑞倉頡碼表（及其相關檔案）<br>
會是集大成、最新、最正確的版本，如果有需要引用該碼表的話，請自行提取，<br>
以文字編輯器搜尋「&#35;&#35;」即可找到各字元集的段落，讀者可自行剪裁不需要的段落。
<hr>
本文開始：<br>
因為 Windows 10/11 內建的字型已經支援 CJK Ext-E/F/G/H/I 字元集，<br>
（詳情請參閱【[Windows 10/11 內建的字型已經支援 CJK Ext-E/F/G/H/I 字元集了！](https://terryjiun.github.io/posts/SimSun-ExtG/){:target="_blank"}】一文）<br>
所以筆者也就更新了一下「泰瑞版小小輸入法」。<br>
這個版本（以下簡稱「<span style="color: red">Ext-I 版本</span>」）會單獨發布，<br>
存放於筆者的【Google 雲端硬碟】或【OneDrive】（「<span style="color: red">輸入法相關</span>→<span style="color: red">輸入法軟體</span>」目錄之下），<br>
檔名為：<b>Terry&#95;Yong&#95;ExtI(Core20250906).zip</b><br>
以後筆者會優先維護、更新這個版本，至於其他版本有可能不再維護及更新。<br>
如只需擷取碼表（對照表）的話，請自行擷取，不需通知或徵求筆者同意<br>
另外，筆者也可能不再更新以前的碼表。<br>
<br>
「<span style="color: red">Ext-I 版本</span>」獨特之處說明如下：<br>
一、「泰瑞倉頡」碼表（mb&#92;Chajei.txt）<br>
　1.檔名中的「ExtI」代表「倉頡碼表」除了支援 CJK 基本平面的漢字外，還支援 Ext-A～Ext-I 的漢字。<br>
　　雖然全字庫（CNS11643）支援超過9萬個漢字，但是很多 Ext-E～Ext-I 的漢字未獲支援，<br>
　　所以 Ext-E 及其之後的漢字碼表來源幾乎得靠「[馬來西亞‧倉頡之友](https://www.chinesecj.com/){:target="_blank"}」團隊的付出與貢獻，<br>
　　而該團隊目前公開的碼表只有支援到 Ext-G 的漢字，<br>
　　Ext-H、Ext-I 的漢字為網友們自行發布，所以會有較多種拆法。<br>
　2.此碼表重新界定漢字範圍，以維基百科的「[中日韓統一表意文字](https://zh.wikipedia.org/wiki/中日韓統一表意文字){:target="_blank"}」條目下的「版本」表格為基準，<br>
　　2024年底前 Unicode 已收錄的漢字，此碼表都有收錄。<br>
　　（為此筆者還特意補上了一些「馬來西亞‧倉頡之友」沒有收錄的漢字及編碼）<br>
　3.漢字候選字視窗一律使用「調整顯示」（詳見【[特殊碼表系列Ⅴ：倉頡字區輸入法](https://terryjiun.github.io/posts/Terry-Yong-Special-mb-5/){:target="_blank"}】一文），<br>
　　這樣可以方便得知想打出的漢字所屬的字元集（分區）。<br>
二、「倉頡聯想」、「倉頡注音」碼表（mb&#92;Chajei&#95;noBlock.txt）<br>
　　此碼表與「mb&#92;Chajei.txt」（泰瑞倉頡碼表）列數相同，<br>
　　差別僅在於不使用「調整顯示」（看不出想打出的漢字所屬的字元集）。<br>
三、「倉頡提示」碼表（mb&#92;Chajei&#95;Big5.txt）<br>
　　此碼表僅包含 Big5 字元集的「常用漢字」及「次常用字」，並且<b>會在候選字窗格提示注音</b>，<br>
　　此碼表<b>不支援符號</b>，但是<b><u>可以直接打出常用標點符號，而且不需要搭配空白鍵</u></b>。<br>
　　例如：「打,出，」、「打.出。」、「打/出？」、「打;出；」、「打'出、」，<br>
　　或是「打&#91;出【」（或出「，連按時會形成對稱的左右括號）。<br>
　　因為在候選字窗格提示注音的關係，所以此碼表搭配相關字詞功能時，會無法正常出現聯想詞，<br>
　　所以筆者將原有的「韓文」輸入模式取消（yong.ini 的第8個輸入法），改成「倉頡提示（注音）」輸入模式，<br>
　　如果讀者需要恢復為「韓文」輸入模式，請將 yong.ini 的第8項更改為：<br>
　　&#35;輸入法模式<br>
　　8=Hangul<br>
　　&#35;輸入法模式定義<br>
　　&#91;Hangul&#93;<br>
　　name=韓文<br>
　　engine=libmb.so<br>
　　arg=mb/Hangul.txt<br>
　　overlay=ini/Hangul.ini<br>
四、「泰瑞注音」碼表（mb&#92;Phon.txt）<br>
　　原碼表裡的Big5字元之注音改用「香草輸入法注音碼表」，且採用其排序方式。<br>
　　因為有些Big5次常用字在注音候選字的排序較常用字優先，<br>
　　所以取消先排常用字，再排次常用字的設計，其餘字元集的碼表則保持不變。<br>
　　與香草注音碼表唯一的不同是「彝」字，香草注音誤用到不是Big5編碼的「彞」字。<br>
　　（此二字在新細明體、微軟正黑體、宋體下字形皆正確，但在標楷體下字形卻相互錯置）<br>
五、「倉頡聯想」的聯想詞庫（LC&#92;LC.txt）<br>
　　改用「香草輸入法聯想詞庫」，唯一不同的是筆者將不屬於Big5編碼的「彞」改回「彝」，<br>
　　並加上「彝陵之戰」這組聯想詞（注意：LC.txt需以GB18030編碼方式開啟及儲存）。<br>
六、核心程式<br>
　1.檔名中的「Core20250906」代表核心程式是在2025年9月6日更新至最新版。<br>
　2.因為64位元的 Windows 作業系統已經普及，<br>
　　所以請使用者們將「Terry&#95;Yong」資料夾改成儲存於「C:&#92;Program Files」之下，<br>
　　並執行「w64」資料夾下的「yong.exe」（如需建立捷徑，請指向此路徑下的「yong.exe」）。<br>
　　惟需注意的是：<br>
　　每次修改 yong.ini 時，請先結束小小輸入法，然後將此路徑：<span style="color: blue">%AppData%</span><br>
　　（Windows Path，對應《C:&#92;Users&#92;使用者帳戶名稱&#92;AppData&#92;Roaming》資料夾）<br>
　　之下的《yong》資料夾刪除，再更新，最後再執行小小輸入法。<br>
七、新增腳本（twdate.js）<br>
　1.作用是實現今天日期以中華民國年月日、民國年月日的格式輸出。<br>
　　（限「泰瑞倉頡」、「倉頡聯想」、「倉頡注音」輸入模式，<br>
　　其他輸入模式需在對應的碼表裡添加對應的編碼，可依樣畫葫蘆）<br>
　2.操作方式：假設今天日期為「2025年8月14日」<br>
　　按鍵打「,date」再按空白鍵，輸出：中華民國114年8月14日<br>
　　按鍵打「,date」再按「2」，輸出：民國114年8月14日<br>
　　（另外也有明天、後天、昨天、前天的日期可供選擇）<br>
八、更換皮膚（顯示介面）<br>
　　採用「暗黃中標」作為預設的皮膚。<br>
