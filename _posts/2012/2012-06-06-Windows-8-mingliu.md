---
title: Windows 8 內建的新細明體已經支援 CJK Ext-C/D 字元集了！
date: 2012-06-06 10:10:00 +0800
categories: [字碼與字型]
tags: [字型, CJK]
---

Microsoft 對「新細明體」字型算是照顧有加！<br>
<br>
首先，針對某一區字元集而言，不會有「漏字」的情形發生。<br>
<br>
一旦支援「中日韓統一表意文字擴展B區」，<br>
就會將「擴展B區」（或稱「擴充B區」、「延伸B區」）的所有漢字全部納入「新細明體-ExtB」，<br>
不會像 Apple Mac OS 出的字型會有漏字的情形（詳見：[老刀發布的文章](https://www.techbang.com/posts/6632-os-x-107-lion-characters-support-of-large-medical?page=2){:target="_blank"}）。<br>
<br>
其次，微軟會與時俱進，更新「新細明體」。<br>
<br>
Windows 2000、Windows XP 分別發表於2000年第1季、2001年第4季，<br>
它們內建的新細明體即已支援1993年 Unicode 收錄的「[中日韓統一表意文字](https://www.chinesecj.com/unihan.php?ccode=CJK){:target="_blank"}」。<br>
<br>
2000年、2001年，Unicode 先後收錄「[擴展A區](https://www.chinesecj.com/unihan.php?ccode=Ext-A){:target="_blank"}」、「[擴展B區](https://www.chinesecj.com/unihan.php?ccode=Ext-B){:target="_blank"}」的漢字之後，<br>
微軟在2005年第2季隨後推出「[新細明體字型更新套件](https://www.tbmc.com.tw/computerese/pdf/PMingLiU%20Update%20Pack.msi){:target="_blank"}」供 Windows XP、2003 使用者更新，<br>
更新後的新細明體便可顯示「擴展A區」、「擴展B區」的漢字；<br>
而2007年第1季推出的 Windows Vista、2009年第4季推出的 Windows 7，<br>
其內建的新細明體字型亦可直接顯示「擴展A區」、「擴展B區」的漢字。<br>
<br>
2009年、2010年，Unicode 先後收錄「[擴展C區](https://www.chinesecj.com/unihan.php?ccode=Ext-C){:target="_blank"}」、「[擴展D區](https://www.chinesecj.com/unihan.php?ccode=Ext-D){:target="_blank"}」的漢字之後，<br>
微軟在2012年第1季、第2季先後推出的 Windows 8 Consumer Preview、Release Preview，<br>
其內建的新細明體字型已可顯示「擴展C區」、「擴展D區」的漢字。<br>
<br>
Windows 8 Release Preview 的光碟 ISO 檔可以從 Microsoft 的網站下載，<br>
下載網址是：https://windows.microsoft.com/zh-TW/windows-8/iso<br>
我將它內建的「新細明體」、「新細明體-ExtB」兩套字型擷取出來，<br>
存放於免費空間：[https://www.mediafire.com/?h8ag5ihc2sh8ii3](https://www.mediafire.com/?h8ag5ihc2sh8ii3){:target="_blank"}<br>
<span style="color: purple">（2013年8月11日補充說明：<br>
我使用 HashMyFiles 計算過 Win8 Release Preview、Win8 正式版、Win8.1 Preview、Win8.1 Enterprise Preview<br>
這四種版本 Windows 裡的這兩個字型檔，所得到的 SHA1 值相同，<br>
所以在 Win9 出現前，各位不用再找最新版的新細明體了，使用這個免費空間的版本就可以了！）</span><br>
<br>
安裝方式簡要說明如下：<br>
<br>
一、Windows XP：<br>
<br>
1.必須先安裝「新細明體字型更新套件」，否則作業系統會無法建立與「新細明體-ExtB」的關聯。<br>
2.到 XP 控制台的「字型」裡，在「新細明體-ExtB」上按右鍵，選「刪除」，<br>
　再將「新細明體」拉到桌面上<br>
　（在 XP 下，這種拖曳的動作會等同「移動檔案」，<br>
　不做這個動作的話，等會兒新安裝的「mingliu.ttc」會被改名，<br>
　而原來「C:&#92;WINDOWS&#92;Fonts」的「mingliu.ttc」會被保留，<br>
　以致無法達到置換字型的目的）。<br>
3.下載前述免費空間的壓縮檔，<br>
　最後依照一般安裝字型的方式，指定安裝來源為解壓縮後的「Win8&#95;Fonts」資料夾，<br>
　安裝後再重新開機，就可以使用最新版的「新細明體」了！<br>
　（被拉到桌面上的舊版「mingliu.ttc」就可以刪除或移到別的地方了！）<br>
<br>
二、Windows Vista、7：<br>
<br>
目前我還沒有找到比較好的方法，有嘗試過在 WinPE 下刪除「新細明體-ExtB」，結果失敗！<br>
所以用下面的方法比較省事一點！<br>
1.下載前述免費空間的壓縮檔，解壓縮到「C:&#92;Win8&#95;Fonts」資料夾（路徑不要有中文）。<br>
2.確定桌面上有「我的電腦」圖示，然後下載 Ubuntu，並燒錄為光碟，然後用它開機，<br>
　進入 LiveCD 的檔案總管裡，切換到 Windows 系統磁碟下的「Windows&#92;Fonts」，<br>
　將「mingliu.ttc」及「mingliub.ttc」刪除。<br>
3.重開機，進入 Windows 7（或 Vista），進入桌面後，所有漢字會變成「□」，<br>
　暫時不要恐慌，立即開啟「我的電腦」圖示，切換到「C:&#92;Win8&#95;Fonts」資料夾，<br>
　然後選取「mingliu.ttc」及「mingliub.ttc」，並按右鍵選「□□<span style="color: red">(I)</span>」，<br>
　接下來會出現一堆「□□□」的提示訊息，一律按「□<span style="color: red">(Y)</span>」。<br>
4.重開機後，新細明體已經被置換為最新版本了！<br>
<br>
置換前及置換後的差異如下：

![字型置換前](assets/img/font/Windows-8-mingliu-1.png)

▲置換前，無法顯示擴展C、D區字元。

![字型置換後](assets/img/font/Windows-8-mingliu-2.png)

▲置換後，已可顯示擴展C、D區字元。<br>
