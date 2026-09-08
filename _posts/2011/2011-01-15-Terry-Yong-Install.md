---
title: ★泰瑞版小小輸入法─安裝設置篇
date: 2011-01-15 10:10:00 +0800
categories: [泰瑞版小小輸入法]
tags: [小小設定]
---

閱讀本文之前，請先閱讀【[使用說明篇](https://terryjiun.github.io/posts/Terry-Yong-Guide/){:target="_blank"}】，瞭解最基本的操作方式之後，再依照本文執行內置程序。
<hr>
Windows 版的小小輸入法雖然可以不用安裝，直接執行主程式（yong.exe）就可以輕鬆輸入中文，<br>
但是「免安裝版」（外掛版）仍然有些限制，比如：<br>
(1)組字窗格可能不會跟隨插入點位置。<br>
(2)「預編輯模式」不能實現。<br>
(3)不能在 Windows 8/8.1/10 的市集應用程式（Modern APPs、Metro APPs）裡使用。<br>
(4)在 Excel 文字方塊內或使用文字藝術師時無法輸入文字。<br>
因此使用「安裝版」（內置版）對很多使用者而言是非常需要的。<br>
<br>
有鑑於此，筆者自 2011 年起將「泰瑞版小小輸入法」加上〝安裝版〞所需的檔案。<br>
習慣用免安裝版的人，或是無法取得「系統管理員」身分的使用者，可以繼續使用外掛版；<br>
想要使用安裝版的人，則可以依照下列步驟設置。

## 一、下載泰瑞版小小輸入法，並解壓縮

　　正常版（支援字數較多，涵蓋 CJK、CJK Ext-A/B/C/D 字元集）下載網址是：<br>
　　[https://www.mediafire.com/file/7jv61zelyxp0q94/Terry_Yong.zip/file](https://www.mediafire.com/file/7jv61zelyxp0q94/Terry_Yong.zip/file){:target="_blank"}<br>
　　Lite 版（支援字數較少，僅涵蓋 CJK 字元集）下載網址是：<br>
　　[https://www.mediafire.com/file/c3ruafpfdh8z7y8/Terry_Yong_Lite.zip](https://www.mediafire.com/file/c3ruafpfdh8z7y8/Terry_Yong_Lite.zip){:target="_blank"}<br>
　　<span style="color: red">解壓縮密碼皆為：</span><span style="color: purple">yong</span><br>
　　（無法連上 MediaFire 免費空間，或是此連結失效的話，<br>
　　請進入【[輸入法檔案@Google](https://docs.google.com/leaf?id=0B_9ob1iJjpkLMmRjODE2NWQtNjViNC00ZWRkLTgyY2ItNGJhOWEzODU1ZDNh){:target="_blank"}】或【[輸入法檔案@OneDrive](https://1drv.ms/f/c/01b7d23cf55aac84/QoSsWvU80rcggAHPAgAAAAAAEkEClyhF5XEafA){:target="_blank"}】，<br>
　　再切換至「輸入法相關→輸入法軟體」目錄下載）<br>
　　<span style="color: purple">下載完成後，請在 ZIP 檔上按右鍵，選「內容」，再點選「解除封鎖」按鈕（或勾選「解除封鎖」後按「套用」），<br>
　　然後再解壓縮，這樣之後執行「yong.exe」時才不會出現警告，而且後續使用上也比較不會遇到問題。</span>

## 二、修改「yong.ini」

　　如果是<span style="color: red"><b>行列</b></span>使用者，請再將「default=0」修改為「default=<span style="color: red"><b>3</b></span>」；<br>
　　如果是<span style="color: red"><b>大易</b></span>使用者，請再將「default=0」修改為「default=<span style="color: red"><b>4</b></span>」；<br>
　　如果是<span style="color: red"><b>無蝦米</b></span>使用者，請再將「default=0」修改為「default=<span style="color: red"><b>5</b></span>」；<br>
　　這項修改目的是方便 Windows XP/Vista/7 的使用者，<br>
　　使用【Ctrl + Space】就能順利切換到「內置版」的小小輸入法，避免再誤以「免安裝版」模式執行小小輸入法。<br>
　　Windows 8/8.1/10 的使用者，安裝完成後，需以【Win + Space】切換到內置版的小小輸入法。<br>
　　<span style="color: red"><b>修改完成後，請將「Terry&#95;Yong」資料夾複製到「C:&#92;Windows」之下，</b></span><br>
　　複製完成後，「yong.exe」的絕對路徑必須為「C:&#92;Windows&#92;Terry&#95;Yong&#92;yong.exe」。

## 三、以系統管理員身分執行安裝指令

　　首先，打開「C:&#92;Windows&#92;Terry&#95;Yong&#92;tsf」資料夾，<br>
　　<span style="color: red"><b>對「install.bat」按右鍵，選擇「以系統管理員身分執行」，這樣就能成功安裝。</b></span><br>
　　（如果無此選項，則代表您登入 Windows 所使用的帳戶權限不足）。<br>
　　接下來：<br>
　　①Windows XP/Vista/7 使用者請先新增「泰瑞版小小輸入法」（新增方式與新增內建的輸入法一樣），<br>
　　　再到「控制台→地區及語言選項」，點選「語言」頁籤、「詳細資料」按鈕，<br>
　　　然後點選「進階」頁籤，<span style="color: red">勾選「延伸對所有程式的進階文字服務支援」</span>，按下「確定」後，再重新開機。<br>
　　②Windows 8/8.1/10 使用者請到「控制台」→「語言」（或「新增語言」）項下，<br>
　　　點選「中文(台灣)」旁的「選項」，再依照下列畫面（截圖自 Windows 8.1）新增「泰瑞版小小輸入法」：

![新增「泰瑞版小小輸入法」-1](/assets/img/terry_yong/Windows-8-Terry-Yong-A.png)

![新增「泰瑞版小小輸入法」-2](/assets/img/terry_yong/Windows-8-Terry-Yong-B.png)


## 四、製作「yong.exe」的捷徑，並存放到 Windows 程式集的「啟動」資料夾內

　　<span style="color: red">這個步驟是小小輸入法比較特殊而且必要的地方，</span><br>
　　因為執行上述步驟後，雖然 C:&#92;Windows 資料夾和系統組態裡已經有小小輸入法的相關檔案及設置，<br>
　　但是 Windows 處理程序裡並不會有「yong.exe」，<br>
　　所以<span style="color: red">此步驟的目的是讓「yong.exe」在開機後，就立刻被載入到 Windows 處理程序裡並常駐。</span><br>
　　製作捷徑的具體作法如下：<br>
　　打開「C:&#92;Windows&#92;Terry&#95;Yong」資料夾，對「yong.exe」按右鍵，選擇「複製」，<br>
　　再打開「啟動」資料夾，在空白處按右鍵，選擇「貼上捷徑」。<br>
　　因為「使用者帳戶控制」的關係，選擇「貼上捷徑」後，可能遇到錯誤提示，詢問您是否將捷徑改放在桌面上，<br>
　　請選「是」，然後將桌面上的「yong.exe - 捷徑」（可先重新命名）重新複製到「啟動」資料夾裡，<br>
　　貼上時會出現提示，請選「繼續」。<br>
　　（註：Windows 8/8.1/10 預設的「啟動」資料夾路徑是：<br>
　　【C:&#92;ProgramData&#92;Microsoft&#92;Windows&#92;Start Menu&#92;Programs&#92;StartUp】）<br>
　　將「yong.exe」的捷徑存放至「啟動」資料夾後請重新開機，<br>
　　或手動執行「yong.exe」（在檔案總管中對 C:&#92;Windows→Terry&#95;Yong→yong.exe 各點兩下）。

## 五、將泰瑞版小小輸入法的小鍋牛圖示「永遠顯示」在工作列上（此步驟非必要，可省略）

　　操作方式請參閱【★將「泰瑞版小小輸入法」小鍋牛圖示固定於 Windows 工作列之方法】一文。<br>
　　此步驟的目的是避免小鍋牛圖示被隱藏，而不易判斷「yong.exe」是否已常駐於記憶體中。<br>
<br>
上述一至四步驟執行完成後，正常情況下，應可順利使用「泰瑞版小小輸入法」。<br>
以下再針對一些可能遇到的問題補充說明，已可順利使用「泰瑞版小小輸入法」的使用者不需參閱。

## 六、補充說明

### (一)安裝錯誤

　　在正常情況下，泰瑞版小小輸入法應該會被安裝到「中文(繁體，台灣)」（或「中文(台灣)」）這個輸入語言之下，<br>
　　如果被安裝到「中文(簡體，中國)」這個輸入語言之下，<br>
　　請執行「uninstall.bat」後，再重新執行「install.bat」試試。<br>
　　如果安裝後，輸入法名稱顯示為亂碼，<br>
　　請下載【[Terry&#95;Yong&#95;Rename.reg](https://www.mediafire.com/file/dld9j694cd59jlo/Terry_Yong_Rename.zip){:target="_blank"}】（下載後解壓縮即可得到此檔），<br>
　　然後以系統管理員身分執行此登錄檔，即可修正亂碼情形。

### (二)輸入切換

　　Windows XP/Vista/7 預設的輸入法切換鍵是「Ctrl + Shift」，<br>
　　如果您已經將「泰瑞版小小輸入法」調整到第一順位的話，開啟／關閉輸入法，可以使用「Ctrl + 空白鍵」。<br>
　　對於 Windows 8/8.1/10 使用者，筆者建議保留一個微軟內置的輸入法，<br>
　　詳情請參考【★泰瑞版小小輸入法在 Windows 8/8.1/10 的設置方式（建議）】一文的介紹，<br>
　　之後再用 Win + Space 或 Ctrl+ Shift 切換到泰瑞版小小輸入法。

### (三)客製化

　　如果想要進一步客製化泰瑞版小小輸入法的話，請參考「[泰瑞版小小輸入法─常見問答篇](https://terryjiun.github.io/posts/Terry-Yong-FAQ/){:target="_blank"}」。

### (四)更新／修改輸入法檔案

　　日後如需修改輸入法組態設定或對照表（碼表）的方式說明如下：<br>
　　先結束泰瑞版小小輸入法（在工作列的小蝸牛圖示上按右鍵，選「結束」），<br>
　　然後將舊有的碼表檔、&#42;.ini 檔刪除，換為新版的，最後再重新執行「yong.exe」就可以了！<br>
　　<span style="color: blue">Windows 8/8.1/10 在開啟 UAC 的情況下，不允許直接編輯 C:&#92;Windows 底下的檔案，<br>
　　所以，如果要編輯碼表檔、yong.ini 或其他檔案，<br>
　　請先將檔案複製到桌面，編輯好並存檔後，<br>
　　再複製回 C:&#92;Windows&#92;Terry&#95;Yong 底下（貼上時，先選「取代…」、再選「繼續」）。</span>

### (五)外掛版／內置版判斷

　　值得注意的是：<br>
　　紅色小篆寫法的「永」字圖案必須出現在「Windows 語言列」（工作列右側）上，<br>
　　這時才是「真正」在使用「內置版」的小小輸入法，不然只是在用外掛版的小小輸入法。<br>
　　註：「永」字為小小輸入法原作者─周永（dgod）先生的名字。

### (六)程式升級

　　有關於「泰瑞版小小輸入法」程式升級的方式，請參考：<br>
　　【[軟體更新篇（Windows XP/Vista/7）](https://terryjiun.github.io/posts/Terry-Yong-Update-1/){:target="_blank"}】<br>
　　【[軟體更新篇（Windows 8/8.1/10）](https://terryjiun.github.io/posts/Terry-Yong-Update-2/){:target="_blank"}】<br>
　　Windows XP/Vista/7 使用者只需參閱第一篇文章；Windows 8/8.1/10 使用者兩篇文章請都參閱。<br>
　　不需要更新程式、調整候選字順序的使用者，就不需要參閱以上兩篇文章。<br>
