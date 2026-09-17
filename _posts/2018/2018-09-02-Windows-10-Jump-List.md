---
title: Windows 10 工作列「跳躍清單」（已釘選的應用程式捷徑之右鍵清單）顯示數目調整教學
date: 2018-09-02 10:10:00 +0800
categories: [作業系統]
tags: [Windows]
---

因為筆者上班時，經常需要使用 Excel，於是就將 Excel 的捷徑「釘選到工作列」，以便迅速開啟。<br>
如果先清理「最近開啟的項目」，也就是先按下 Windows 10 的「開始」，<br>
再點選「設定」、「個人化」，進入「開始」項下，<br>
將「在 &#91;開始&#93; 或工作列上的捷徑清單中顯示最近開啟的項目」調整成「關閉」，再恢復成「開啟」，<br>
然後再回到工作列，對 Excel 圖示按右鍵，就會看到如下圖的畫面：

![Win10_JumpList_Default](/assets/img/windows/Win10-Jump-List-1.png){:target="_blank"}

上圖中出現的「黑色方塊」即為 Windows 7 所稱的「跳躍清單」，它會顯示最近開啟過的檔案名稱，<br>
也可以將最近開啟的檔案中最常用到的一個（或數個）釘選到此「跳躍清單」，方便日後快速開啟。<br>
「跳躍清單」的顯示數量在 Windows 7 可以透過設定「開始功能表」的介面來調整，如下圖：

![Win7_JumpList_Setting](/assets/img/windows/Win10-Jump-List-2.png){:target="_blank"}

就算是使用 Windows 8.1，<br>
也有 GUI（Graphical User Interface，圖形使用者介面）可以用來調整「跳躍清單」的項目數，<br>
只不過 Microsoft 在 Windows 8.x 裡把「跳躍清單」這個名稱換成了「捷徑清單」。

![Win81_JumpList_Setting](/assets/img/windows/Win10-Jump-List-3.png){:target="_blank"}

但是在 Windows 10 裡，卻沒有可供調整的介面，<br>
儘管筆者已經開過 24 個檔案，但 Windows 10 的「跳躍清單」預設最多只會顯示 12 個，<br>
如下圖：

![Win10_JumpList_Max](/assets/img/windows/Win10-Jump-List-4.png){:target="_blank"}

在上圖中，因為「最近」這兩個字也佔了一列，所以其實應該算成「跳躍清單」預設最多只顯示 13 列。<br>
這和螢幕解析度沒有太大的關係，因為筆者有將解析度調整成最大的 1920&#42;1080，結果也是一樣。<br>
如果有釘選某些常用的 Excel 檔案到這個「跳躍清單」的話，會多出一列「已釘選」的字樣，<br>
筆者曾釘選 9 個常用的檔案，最後「最近」底下只會列出 2 個檔案，這對筆者來說根本不夠用！<br>
（「已釘選」字樣佔 1 列、常用檔案佔 9 列、「最近」字樣佔 1 列、最近的檔案佔 2 列，1+9+1+2=13）<br>
<br>
筆者曾試過用「中文關鍵字」（類似：windows 10 釘選 資料夾 數目）上 Google 搜尋，<br>
結果找到了這個【微軟官方無三小路用的回答】！（該連結已失效）<br>
（回答者宣稱：Windows 10 目前沒有這個功能選項，目前只能等以後更新來豐富它的功能）<br>
後來試著用「英文關鍵字」（類似：windows 10 jump list size）上 Google 搜尋，<br>
很快的就找到了這篇【[教學文章](https://www.techrepublic.com/article/windows-10-hack-how-to-beef-up-your-jump-lists-to-show-more-pinned-items/){:target="_blank"}】，照著設定後，就解決了筆者的問題。<br>
<br>
以下就簡單的介紹如何將上圖黑色方塊的「跳躍清單」增高，使它能容納 20 列。<br>
<br>
一、先在 Windows 10 開始圖示上按右鍵，再點選「<span style="color: blue">命令提示字元(系統管理員)</span>」，<br>
　　然後輸入「<span style="color: blue">regedit</span>」，並按下 <span style="color: blue">Enter</span> 鍵，就會出現「登錄編輯程式」的畫面。<br>
<br>
二、複製這一行字串（路徑及機碼）：<br>
　　<span style="color: blue">HKEY&#95;CURRENT&#95;USER&#92;SOFTWARE&#92;Microsoft&#92;Windows&#92;CurrentVersion&#92;Explorer&#92;Advanced</span><br>
　　把它貼到「登錄編輯程式」的最上列，也就是「網址列」，然後按下 <span style="color: blue">Enter</span> 鍵。<br>
　　（若未顯示網址列，可點選功能表「檢視→網址列」，將它顯示出來）<br>
<br>
三、手動建立「<b>JumpListItems&#95;Maximum</b>」這個 DWORD 名稱，如下圖所示。<br>
　　(1) 先複製【<span style="color: blue">JumpListItems&#95;Maximum</span>】這組字串，<br>
　　　　再到「<b>登錄編輯程式</b>」列出的上述路徑及機碼下，在其右側窗格空白處<span style="color: blue">按右鍵</span>，<br>
　　　　選「<span style="color: blue">新增</span>」、「<span style="color: blue">DWORD (32-位元) 值</span>」。

![Win10_Regedit](/assets/img/windows/Win10-Jump-List-5.png){:target="_blank"}

　　(2) 在「<b>新數值 &#35;1</b>」上<span style="color: blue">貼上</span>剛才複製的 DWORD 名稱，然後按 <span style="color: blue">Enter</span> 鍵。

![Win10_Regedit_Edit_1](/assets/img/windows/Win10-Jump-List-6.png){:target="_blank"}

四、點選「<span style="color: blue">JumpListItems&#95;Maximum</span>」，對其<span style="color: blue">按右鍵</span>，選「<span style="color: blue">修改</span>」，之後會出現下圖。<br>
　　先點選右方的「<span style="color: blue">十進位</span>」，然後在左方填入「<span style="color: blue">20</span>」，再按「<span style="color: blue">確定</span>」，最後即可關閉「登錄編輯程式」。

![Win10_Regedit_Edit_2](/assets/img/windows/Win10-Jump-List-7.png){:target="_blank"}

大功告成！之後「跳躍清單」不只能顯示 20 列，也會出現垂直捲軸，可往下捲動選取更多最近開啟過的項目。

![Win10_JumpList_Finish](/assets/img/windows/Win10-Jump-List-8.png){:target="_blank"}

<hr>
補充：<br>
現在（2018 年 9 月初）Windows 10 的「跳躍清單」仍然有個最大的問題：「不能透過拖曳的方式來排序」，<br>
Windows 8/8.1 承襲 Windows 7 的「跳躍清單」，因此沒有這個問題。<br>
筆者有時會覺得如果自己要重灌作業系統的話，就灌 Windows 8.1 好了，<br>
市集應用程式也能用，也不用每半年跟著微軟更新 Windows 版本，而且跳躍清單也能隨心所欲的調整。<br>
