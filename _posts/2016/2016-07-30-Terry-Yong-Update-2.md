---
title: 泰瑞版小小輸入法─軟體更新篇（Windows 8/8.1/10/11）
date: 2016-07-30 10:10:00 +0800
categories: [泰瑞版小小輸入法]
tags: [Terry_Yong, 小小更新]
---

前文提到：「小小輸入法」必須設為內置版，才能在 Windows 8/8.1/10/11 的 Modern APP 內使用，<br>
而且程式目錄必須儲存在 C:&#92;Program Files 或 C:&#92;Program Files (x86) 或 C:&#92;Windows。<br>
「小小輸入法」作者建議如果是 32 位元 Windows，就將程式目錄複製到「C:&#92;Program Files」；<br>
如果是 64 位元 Windows，就將程式目錄複製到「C:&#92;Program Files (x86)」；<br>
而筆者的建議是一律將程式目錄複製到「C:&#92;Windows」。<br>
<br>
程式目錄儲存在「C:&#92;Program Files」或「C:&#92;Program Files (x86)」的話，<br>
執行「yong.exe」，然後在其對應的工作列圖示上按右鍵，選擇「工具」→「軟體更新」後，<br>
「yong-config.exe」會被呼叫，但是在它被執行之前，會出現如下的警告視窗，

![UAC](/assets/img/terry_yong/Terry-Yong-Update-05.png)

點選「是」後，即可成功更新「小小輸入法」，舊版程式會被保留，並加上「.del」的副檔名。<br>
而如果程式目錄儲存在「C:&#92;Windows」的話，則會出現「文件"libl.dll"正在被使用」的訊息，而造成更新失敗。<br>
但是，不論程式目錄儲存在「C:&#92;Program Files」、「C:&#92;Program Files (x86)」或「C:&#92;Windows」，<br>
受 UAC（使用者帳戶控制）保護這 3 個資料夾（含其下的檔案及子資料夾內的檔案）的關係，<br>
原本使用者在候選字窗格以「Ctrl + ↑」、「Ctrl + ↓」 進行的「在線調頻」動作，<br>
應該被儲存到「.yong」目錄下的「user.txt」，結果卻遭受阻擋而並不會被正確儲存。<br>
（註：系統不會發出錯誤訊息，而是會直接導致無法儲存，而使調頻工作白忙一場！）<br>
<br>
解決這個問題的方向很明確，就是執行「yong.exe」及「yong-config.exe」時，都以系統管理員身分執行，<br>
這樣既可成功執行軟體更新，又可讓「調頻」的結果被正確保存到「user.txt」。<br>
不過，如果要在登入 Windows 時，就讓「yong.exe」以系統管理員身分執行，就需要運用一個特別的方式。<br>
起初，筆者是在程式集的「啟動」資料夾內設置「yong.exe」的捷徑，<br>
然後在這個捷徑上按右鍵，選「內容」，到「捷徑」頁籤下，點選「進階」按鈕，<br>
出現如下畫面後，再勾選「以系統管理員身分執行」。

![捷徑-1](/assets/img/terry_yong/Terry-Yong-Update-06.png)

不過，這樣的設定方式是無效的，因為登入 Windows 後，「yong.exe」反而不會正確被執行。<br>
<br>
後來，筆者直接對「yong.exe」按右鍵，選「內容」，出現如下畫面後，切換到「相容性」頁籤，<br>
然後勾選「以系統管理員的身分執行此程式」，結果重新開機後，「yong.exe」仍然不會正確被執行。

![捷徑-2](/assets/img/terry_yong/Terry-Yong-Update-07.png)

後來筆者找到正確的解決方法：<br>
一、首先，對「yong-config.exe」按右鍵，選「內容」，<br>
　　在「相容性」頁籤下，勾選「以系統管理員的身分執行此程式」；而對於「yong.exe」則不需要進行此設定。<br>
二、程式集的「啟動」資料夾內，如果有「yong.exe」的捷徑，就將它刪除。<br>
三、開啟「控制台」→（系統及安全性）→「系統管理工具」→「排程工作」（工作排程器），<br>
　　然後點選右側「動作」選單內的「建立工作」，並依下列畫面進行設定。<br>
<br>
　1.在「一般」頁籤下，除了輸入排程名稱外，最重要的就是勾選「以最高權限執行」。

![排程-1](/assets/img/terry_yong/Terry-Yong-Update-08.png)

　2.在「觸發程序」頁籤下，點選「新增」，出現下圖畫面時，在「開始工作」右側的選單中，選擇「登入時」。

![排程-2](/assets/img/terry_yong/Terry-Yong-Update-09.png)

　3.在「動作」頁籤下，點選「新增」，然後按「瀏覽」按鈕，帶入「yong.exe」在磁碟中的位置。

![排程-3](/assets/img/terry_yong/Terry-Yong-Update-10.png)

　4.在「條件」頁籤下，可以仿照下圖取消勾選全部的核取框。

![排程-4](/assets/img/terry_yong/Terry-Yong-Update-11.png)

　5.在「設定」頁籤下，可以仿照下圖取消勾選或勾選部分的核取框。

![排程-5](/assets/img/terry_yong/Terry-Yong-Update-12.png)

建立好每次登入 Windows 時以最高權限執行「yong.exe」的排程後，日後即可成功更新小小輸入法，<br>
在線調頻的動作也會被完整記錄下來！<br>
註：「user.txt」使用 ANSI 編碼，在繁體中文 Windows 下開啟後會看到亂碼，<br>
但在簡體中文 Windows 下開啟則不會看到亂碼（除非儲存了 GB2312 編碼以外的字元）。<br>
<br>
小小輸入法的程式已經非常成熟，長期（二年以上）不更新的話，使用上並不會有任何的問題，<br>
因此，不需要在線調頻、在線升級的使用者，依照【安裝設置篇】的介紹，設為內置版後即可，無須理會本文的介紹。<br>
