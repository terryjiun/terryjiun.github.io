---
title: 「亂倉打鳥」輸入法─安裝及改造篇
date: 2009-01-09 10:20:00 +0800
categories: [輸入法]
tags: [倉頡, 碼表, 符號]
---

「亂倉打鳥」輸入法的官方網址是：<br>
[https://hyperrate.com/thread.php?tid=5775](https://hyperrate.com/thread.php?tid=5775){:target="_blank"}<br>
官方網頁上有提供 for Windows、Linux、Mac OS X 的檔案，<br>
本文講述則以 Windows 環境為主。<br>
<br>
「亂倉打鳥」輸入法其實並沒有安裝檔，<br>
只有一個「組字字根 V.S. 詞組」的對照表檔案（純文字檔），<br>
下載網址是：<br>
一般版（七萬個詞）：<br>
[https://www.mediafire.com/file/kf4f8um8j221hf0/NewCJ3Win.zip](https://www.mediafire.com/file/kf4f8um8j221hf0/NewCJ3Win.zip){:target="_blank"}<br>
Google 全詞庫版（二十二萬個詞）：<br>
[https://www.mediafire.com/file/gmcf8mg2v82amyd/NewCJ3WinGoogle.zip](https://www.mediafire.com/file/gmcf8mg2v82amyd/NewCJ3WinGoogle.zip){:target="_blank"}<br>
（括號裡的「詞」指的是複數的字元，也就是辭典裡的「詞」。<br>
如果不管單、複數的話，<br>
一般版的「組字字根 V.S. 詞組」條目近 14 萬條；<br>
Google 全詞庫版的「組字字根 V.S. 詞組」條目共 29 萬餘條）<br>
得到這樣的對照表有個優點，<br>
就是我們可以對它進行編修，<br>
加入自己想要的條目、刪除覺得多餘的條目。<br>
<br>
初次使用的人可以先不考慮編修的問題，<br>
使用後有什麼好的 idea，<br>
可以統一記下來，日後再改造（更新、擴充）這套輸入法。<br>
<br>
它的安裝方式是：<br>
1.解壓縮上述的「NewCJ3Win.zip」檔，<br>
　將「NewCJ3Win.txt」複製到「C:\」，<br>
　（如果複製到有中文路徑的資料夾下，<br>
　等會兒使用「通用輸入法編輯工具」匯入時，會產生錯誤）<br>
2.如果是 Windows XP、Server 2003 的使用者，<br>
　請執行「程式集→附屬應用程式→通用輸入法編輯工具」<br>
3.如果是 Windows Vista、Server 2008 的使用者，<br>
　因為 Windows 並無內建「通用輸入法編輯工具」，<br>
　所以請依照這篇文章──<br>
　「[移植 Windows XP 內建中文輸入法至 Windows Vista/Server 2008](https://terryjiun.github.io/posts/Port-WinXP-IME/){:target="_blank"}」<br>
　的指示，下載：[https://www.mediafire.com/file/8ve8veq1wfe87bq/WinXP_IME.zip](https://www.mediafire.com/file/8ve8veq1wfe87bq/WinXP_IME.zip){:target="_blank"}<br>
　解壓縮後，將「miniime.tpl」、「Uimetool.exe」、「uniime.dll」<br>
　複製到「C:\Windows\System32」，並執行「Uimetool.exe」，<br>
　這時「通用輸入法編輯工具」即可正常執行。<br>
4.在「通用輸入法建立精靈」視窗中，<br>
　要設定的地方，只有四個：<br>
　(1)輸入法名稱：請填入「亂倉」<br>
　(2)產生 .IME 檔的英文檔名：請填入「NewCJ3」<br>
　(3)對照表檔案：請以瀏覽檔案的方式帶入步驟 1 的「C:\NewCJ3Win.txt」<br>
　(4)最大組字字根數目：請調成「5」<br>
5.上一步驟按「完成」按鈕後，<br>
　會在「C:\Windows\System32」之下產生四個檔名以「NewCJ」開頭的檔案，<br>
　之後即可使用下列方式新增／移除這套輸入法：<br>
　【控制台→地區及語言選項→「語言」頁籤→「詳細資料」按鈕】<br>
　叫出「文字服務及輸入語言」視窗，<br>
　並在它的「設定」頁籤下新增或移除「亂倉」。<br>
<br>
使用一段時間後，<br>
您可能想要改造這套輸入法，<br>
這時可以用「程式集→附屬應用程式→WordPad」開啟「C:\NewCJ3Win.txt」，<br>
（不建議使用「記事本」開啟，因為會顯示「斷行符號」，造成版面錯亂）<br>
比如您試過「pig」這個組字字根，並無對應任何詞組，<br>
（有對應到也沒關係，只是會變成：<br>
原來不顯示候選字就能直接出字的組字字根，會變成有候選字；<br>
原來有顯示候選字才能出字的組字字根，會變成多了一組候選字；<br>
在「C:\NewCJ3Win.txt」檔裡排越前面的詞組，會成為越前面的候選字）<br>
這時就可以在「C:\NewCJ3Win.txt」裡加入「pig 豬仔」（中間要空一格），<br>
我的習慣是會先用搜尋的方式找到「cat 貓咪」後，<br>
把「pig 豬仔」按照英文字母順序加到這個文字檔裡，<br>
您也可以把不要的「組字字根 詞組」刪除，<br>
然後存檔。<br>
<br>
接下來按照上述步驟 5 的方式先移除「亂倉」輸入法，然後重新開機！<br>
（不這麼做的話，可能無法更新上述那四個檔名以「NewCJ」開頭的檔案，<br>
如果您不想重新開機，請確認使用過輸入法軟體的應用程式，如：Word、msn…都已正常結束）<br>
接下來，重新執行上述步驟 4、5 即可完成改造這套輸入法的程序。<br>
