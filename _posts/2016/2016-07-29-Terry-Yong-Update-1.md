---
title: 泰瑞版小小輸入法─軟體更新篇（Windows XP/Vista/7）
date: 2016-07-29 10:10:00 +0800
categories: [泰瑞版小小輸入法]
tags: [Terry_Yong, 小小更新]
---

2015 年 4 月 24 日起，dgod（周永）先生為小小輸入法加入了「在線升級」功能，<br>
此後，使用者可以隨時在 Windows 通知區域的 Yong 輸入法圖示（泰瑞版為「小鍋牛」Icon）上按右鍵，<br>
然後選擇「工具」→「軟體更新」，即可將小小輸入法平台的程式升級為最新版。<br>
不過<span style="color: blue">要成功執行更新程序，有 2 個必要條件，分別說明如下。</span><br>
（本文僅談論小小輸入法 Windows 版；Linux 版、Android 版不在本文討論範圍）<br>
<br>
<span style="color: blue">一、根目錄下必須具備「yong-config.exe」、「yong.ini」這兩個檔案。</span><br>
　　前者是視窗（視覺化）版的組態編輯程式，而後者則是儲存組態設定值的檔案。<br>
　　筆者在發布新版的「泰瑞版小小輸入法」時，通常會開啟「yong-config.exe」，<br>
　　將視窗內顯示的簡體字記錄下來，然後編輯「translate.txt」（GB18030 編碼），<br>
　　讓原本視窗內顯示的簡體字自動「翻譯」而顯示為正體字。<br>
　　（翻譯後的用詞會顯示為符合台灣網友習慣的稱呼，<br>
　　但是有一些程式回傳的訊息，並不是筆者未翻譯，而是這些訊息並不接受用翻譯的方式顯示為正體字）<br>
　　以往筆者為了避免使用者濫用「yong-config.exe」而破壞「yong.ini」的內容，<br>
　　而且也為了縮小「泰瑞版小小輸入法」的壓縮檔容量，<br>
　　因此筆者通常會將「yong-config.exe」摒除在「泰瑞版小小輸入法」的 ZIP 檔之外。<br>
　　不過現在發現這個「yong-config.exe」其實與小小輸入法的「軟體更新」功能有著莫大的關係，<br>
　　沒有它的話，在小鍋牛圖示上按右鍵，選擇「工具」選單時會出現如下的畫面：

![工具選單-1](/assets/img/terry_yong/Terry-Yong-Update-01.png)

　　有了它的話，在小鍋牛圖示上按右鍵，選擇「工具」選單時將出現如下的畫面：

![工具選單-2](/assets/img/terry_yong/Terry-Yong-Update-02.png)

　　因此為了方便使用者執行「軟體更新」，筆者從善如流將「泰瑞版小小輸入法」ZIP 檔納入這個檔案。<br>
　　但是縱使根目錄下有了「yong-config.exe」，沒有「yong.ini」的話，更新過程仍會出現錯誤，<br>
　　所以筆者只好再將「yong.ini」由原來的「.yong」目錄（資料夾）下，移回根目錄。<br>
　　使用者第一次執行「yong.exe」後，「.yong」目錄會自動被建立，<br>
　　而根目錄的「yong.ini」也會被複製到「.yong」目錄內，日後編輯組態設定的話，以「.yong」目錄內的為準。<br>
　　如果「.yong」目錄沒有自動被建立，可能原因為程式儲存在使用者帳戶控制（UAC）技術保護的資料夾內，<br>
　　像是：「C:&#92;Program Files」、「C:&#92;Program Files (x86)」、「C:&#92;Windows」。<br>
<br>
<span style="color: blue">二、使用者必須有足夠的系統權限執行「yong-config.exe」。</span><br>
　　筆者近日於「使用說明」（ReadMe.htm）內，提醒使用者下載完成 ZIP 檔後，<br>
　　務必先對 ZIP 檔「解除封鎖」（於檔案總管內對 ZIP 檔按右鍵，選「解除封鎖」），再執行解壓縮，<br>
　　目的就是為了避免執行「yong.exe」、「yong-config.exe」時出現如下的「安全性警告」畫面：

![安全性警告-1](/assets/img/terry_yong/Terry-Yong-Update-03.png)

![安全性警告-2](/assets/img/terry_yong/Terry-Yong-Update-04.png)

　　解決了出現「安全性警告」的問題後，接下來就是程式儲存在下列路徑下的問題：<br>
　　「C:&#92;Program Files」、「C:&#92;Program Files (x86)」、「C:&#92;Windows」。<br>
　　這個問題通常只會出現在 Windows 8/8.1、Windows 10 Version 1607（2016 年 7 月周年更新版），<br>
　　因為「小小輸入法」必須存放在這些資料夾內，<br>
　　而且執行「tsf」目錄下的「install.bat」，將「小小輸入法」設為內置版，<br>
　　才能在 Windows 8/8.1、Windows 10 周年更新版的 Modern (Metro) APP （市集應用程式）下，<br>
　　順利使用「小小輸入法」打字，這是 Win 8/8.1 獨有的限制，某些版本的 Win 10 也會有此限制。<br>
　　（不過，根據筆者在乾淨的 64 位元 Windows 10 Version 1511 繁體中文企業版環境下的實測結果，<br>
　　只要將「小小輸入法」的目錄存放於 C:&#92;，路徑如：「C:&#92;Terry&#95;Yong」、「C:&#92;yong」，<br>
　　不必安裝為內置版，只要執行「yong.exe」仍可順利在 Edge、天氣等內建的 Modern APP 下使用）<br>
　　因此，除非您有保護（鎖住）「小小輸入法」目錄下所有檔案的需要，<br>
　　不然在 Windows 8/8.1/10 以外的 Windows 中，不要將「小小輸入法」目錄儲存到：<br>
　　「C:&#92;Program Files」、「C:&#92;Program Files (x86)」、「C:&#92;Windows」這些系統保護的路徑下，<br>
　　只需儲存到「C:&#92;Terry&#95;Yong」或「C:&#92;yong」，即可成功執行「軟體更新」，並順利在 Modern APP 下打字。<br>
　　<span style="color: red">囿於篇幅的關係，Windows 8/8.1/10 安裝到上述系統保護的資料夾內如何更新的問題將另外發表文章論述。</span><br>
<br>
<span style="color: blue">註：<br>
Windows 10「周年更新版」最明顯的特徵就是工作列上的「重要訊息中心」圖示變成在小時鐘的右方，<br>
此外，在工作列的空白處按右鍵後，出現的選單最下方的項目不是「內容」，而是「設定」。</span><br>
