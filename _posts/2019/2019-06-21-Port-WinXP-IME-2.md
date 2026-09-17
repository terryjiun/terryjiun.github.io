---
title: 移植 Windows XP 內建中文輸入法至 Windows 8/8.1/10
date: 2019-06-21 10:10:00 +0800
categories: [輸入法]
tags: [Windows, 通用輸入法編輯工具]
---

筆者曾經發表過【[移植 Windows XP 內建中文輸入法至 Windows 7/Vista/Server 2008](https://terryjiun.github.io/posts/Port-WinXP-IME-1/){:target="_blank"}】一文，<br>
也在【[「亂倉打鳥」輸入法─安裝及改造篇](https://terryjiun.github.io/posts/Luan-Cang-Da-Niao-2/){:target="_blank"}】一文裡介紹過「通用輸入法編輯工具」的操作方式，<br>
而在【[「輸入法對照表」的妙用與「通用輸入法編輯工具」的限制](https://terryjiun.github.io/posts/Terry-mb-Windows-XP-IME/){:target="_blank"}】一文裡則介紹了「通用輸入法編輯工具」的使用條件。<br>
對於有使用 WinXP 內建輸入法需求的人而言，要將 WinXP 內建的傳統輸入法移植至 Win7，並沒有太大的困難。<br>
如果採用「通用輸入法編輯工具」匯入自訂對照表（碼表）的方式，來產生輸入法（程式），那就更容易了！<br>
「通用輸入法編輯工具」是 WinXP 內建的一支程式，<br>
用它產生出來的輸入法與 WinXP 內建的輸入法，其實是同一系列的檔案，<br>
在本文中統一將此系列的檔案都簡稱為「XP輸入法」。<br>
<br>
筆者多年前幫朋友在 64 位元的 Windows 7 上，用「通用輸入法編輯工具」產生過自訂的XP輸入法，<br>
最近，因為朋友的電腦換成 64 位元的 Windows 10（版本 1803），再度求助筆者，<br>
所以筆者抽空實測了一下，並將移植過程、結果發表於本篇文章。<br>
（雖然筆者在 Win8、8.1 未曾實測過，但移植過程、結果應該與 Win10 是一樣的）<br>
<br>
【[移植 Windows XP 內建中文輸入法至 Windows 7/Vista/Server 2008](https://terryjiun.github.io/posts/Port-WinXP-IME-1/){:target="_blank"}】一文介紹的移植方式，<br>
同樣也能適用於 Windows 8/8.1/10，<br>
只是近幾年的電腦大多配備 4GB 以上的記憶體（RAM），<br>
所以幾乎都安裝 64 位元的 Windows（8、8.1、10），而較少人安裝 32 位元的 Windows。<br>
在 64 位元 Windows 裡，只能使用「通用輸入法編輯工具」匯入自訂碼表；<br>
不像在 32 位元 Windows 裡，可以直接複製原生的 WinXP 輸入法檔案，再匯入機碼，即可使用。<br>
因此，筆者將「XP輸入法」移植至 Win10 過程中會使用的檔案，另外壓縮成一個檔案，下載網址為：<br>
[https://www.mediafire.com/file/0w5hm1k09a7vvlc/WinXP_IME_Lite.zip](https://www.mediafire.com/file/0w5hm1k09a7vvlc/WinXP_IME_Lite.zip){:target="_blank"}<br>
<br>
壓縮檔內的資料夾／檔案說明如下：<br>
Win32 資料夾：必要檔案，擷取自 Windows XP Professional with SP3；<br>
Win64 資料夾：必要檔案，擷取自 Windows Server 2003 R2 x64。<br>
Lctool：相關字詞編輯工具（備用檔案，檔名後面的數字用來區分係屬 32 或 64 位元版）<br>
Uimetool：通用輸入法編輯工具（主要檔案，檔名後面的數字用來區分係屬 32 或 64 位元版）<br>
THCJA-Lite：倉頡（三代及五代混合）碼表，僅包含 CJK 字元集的漢字（20,902 個字）及大量符號<br>
THPho-Lite：注音碼表，僅包含 CJK 字元集的漢字（20,902 個字）及大量符號<br>
<br>
產生「XP輸入法」的步驟如下（以倉頡為例）：<br>
如果是 32 位元 Windows，只需操作步驟一至三；如果是 64 位元 Windows，需操作步驟一至五。<br>
一、視自己的 Windows 版本（32 位元或 64 位元），<br>
　　複製 Win32 或 Win64 資料夾下的「子資料夾」（Win32 只有一個，而 Win64 則有兩個），<br>
　　然後進入 C:&#92;Windows，再選「貼上」，然後按「繼續」（或「是」、「確定」）。<br>
二、以系統管理員身分執行「<span style="color: red">Uimetool&#95;32.exe</span>」。<br>
三、出現「通用輸入法建立精靈」視窗後，依序執行：<br>
　　(1)輸入法名稱：請填入 2 個漢字，如：「泰倉」，然後按「下一步」。<br>
　　(2)產生 .IME 檔的英文檔名：請填入英數字（大小寫不拘），如：「THCJA」，然後按「下一步」。<br>
　　(3)對照表檔案：請以瀏覽檔案的方式帶入上述的「THCJA-Lite.txt」，然後按「下一步」。<br>
　　(4)最大組字字根數目：請調成「5」，嗶聲請視個人需要選擇，然後按「完成」。<br>
四、以系統管理員身分執行「<span style="color: purple">Uimetool&#95;64.exe</span>」。<br>
五、出現「通用輸入法建立精靈」視窗後，執行過程全部如上，<br>
　　<span style="color: purple">最後按「完成」時，可能會出現錯誤提示，可先忽略。</span><br>
<br>
建立好「XP輸入法」後，可開啟「記事本」來測試，然後按「Win+空白鍵」，切換輸入法。<br>
筆者切換到上例的「泰倉」輸入法後，預設會出現「<span style="color: blue">，半</span>」（如下圖），<br>
將滑鼠移到「，」上面，點一下，就會切換成「<span style="color: blue">泰半</span>」，然後即可正常輸入文字。

![XP-IME-1](/assets/img/windows_ime/WinXP-IME-1.png)

如果想編輯下列畫面出現的「相關字詞」（綠色字），<br>
可以執行「Lctool&#95;32.exe」、「Lctool&#95;64.exe」（需以系統管理員身分執行）來編修。<br>
至於其編修方式，本文省略，不做介紹，請有需要的人自行摸索。

![XP-IME-2](/assets/img/windows_ime/WinXP-IME-2.png)

而在上例的「泰倉」方塊裡按右鍵，選「內容」，會出現下列對話方塊，可視個人需求再做進階設定。

![XP-IME-3](/assets/img/windows_ime/WinXP-IME-3.png)

注意：<br>
<span style="color: blue">因為「通用輸入法編輯工具」是採用 IMM（Input Method Manager）架構，而非 TSF（Text Service Framework），<br>
所以產生後的「XP輸入法」，只能在桌面環境的應用程式裡使用，在「市集應用程式」（包括 Edge）裡無法使用。</span><br>
如果想將產生的「XP輸入法」從按下「Win+空白鍵」跳出的清單中移除，<br>
請參閱【[解決 Windows 10 無法移除「僅桌面」類型的輸入法](https://terryjiun.github.io/posts/Windows-10-IMM/){:target="_blank"}】一文。<br>
<br>
因為筆者以前用 64 位元版的「Uimetool.exe」產生「XP輸入法」後，<br>
原本碼表裡的 CJK Ext-B/C/D/E 字元會被全部顯示成「□」（框框），因而無法滿足筆者的需求。<br>
所以<span style="color: purple">筆者建議改用「小小輸入法」這套輸入法框架軟體，搭配自訂碼表，會比使用「XP輸入法」來得好。<br>
如果有讀者覺得「小小輸入法」並不適合自己，也可以改用「DIME」這套 Windows 輸入法軟體。</span><br>
它可以匯入自訂的碼表（cin 檔格式），而且有以下兩個特點：<br>
(1)支援 CJK Ext-B/C/D/E 字元集、(2)採用 TSF 輸入法架構。<br>
（值得注意的是它預設最大碼長是 4 碼，匯入倉頡碼表時，應將最大碼長手動調為 5 碼，不然會打不出 5 碼的字。<br>
詳細操作說明，請見筆者寫的【★簡單易用的自建輸入法軟體─DIME 教學說明】一文）<br>
現今的 Windows 輸入法，如果沒支援以上這兩個特點的話，就太弱了！<br>
第一個特點是支援的字數會變多，碼表編修得宜的話，至少七萬個漢字起跳；<br>
第二個特點則是讓輸入法能夠在 Metro APP（從 Microsoft Store 下載、安裝的 APP）裡使用。<br>
