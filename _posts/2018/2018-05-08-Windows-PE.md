---
title: 可掛載 ISO 檔來安裝 Windows，又具備備份／還原功能的 WinPE
date: 2018-05-08 10:10:00 +0800
categories: [作業系統]
tags: [Windows, 實用工具]
---

筆者去年入手一台 ASUS Transformer Mini T102HA（以下簡稱 T102），<br>
這是一台基本型的 Windows 10 平板電腦，有附可拆卸的實體鍵盤，也有內建一個 USB 連接埠。<br>
前陣子，筆者想要將它乾淨重灌（Clean install），上網爬文有找到了它的驅動程式，下載網址是：<br>
[https://www.asus.com/tw/supportonly/t102ha/helpdesk_download/](https://www.asus.com/tw/supportonly/t102ha/helpdesk_download/){:target="_blank"}<br>
有了驅動程式，再來就是要有「能從 USB 開機的隨身碟系統」（因為筆者沒有外接式光碟機），<br>
雖然微軟官網有提供工具程式，可以做出「由 USB 開機的 Windows 10 安裝媒體」，<br>
不過它並不具備將磁碟備份為映像檔的功能，所以筆者只好上網搜尋 Windows PE 來滿足需求。<br>
<br>
T102 這款平板只支援 UEFI 開機（非傳統的 BIOS），而且開機系統要能抓得到它內建的 SSD 硬碟，<br>
因此有一些限制條件，並不是所有的 WinPE 都合適。<br>
筆者曾經製作過某個 WinPE 隨身碟，在桌機上開機很順暢，不用 3 分鐘就能進入桌面，<br>
但將它插入 T102 這台平板上，卻要花 10 分鐘以上才能載入完成全部的程序進入桌面，<br>
因此，找到合適的 WinPE 非常的重要！<br>
<br>
筆者再此推薦兩個 WinPE，都是 64 位元的 Windows 環境，<br>
一個由 Windows 8.1 製作而成，下載網址是：<br>
[https://www.mediafire.com/file/3lpfdxxtkh1wy8f/WIN81PE.iso](https://www.mediafire.com/file/3lpfdxxtkh1wy8f/WIN81PE.iso){:target="_blank"}<br>
一個由 Windows 10 製作而成，下載網址是：<br>
[https://www.mediafire.com/file/hq9myea7uxlg1qv/Win10PEx64_TW.iso](https://www.mediafire.com/file/hq9myea7uxlg1qv/Win10PEx64_TW.iso){:target="_blank"}<br>
這兩個 WinPE 所需的隨身碟容量都不大，2GB 即綽綽有餘，隨身碟先不要儲存任何資料，<br>
然後用「Rufus」這一套免安裝的小程式，就可以將下載後的 WinPE ISO 檔轉換為 USB 開機系統。<br>
「Rufus」的操作方式，讀者可參閱【[可開機光碟映像檔(&#42;.ISO)轉換成可開機 USB 磁碟的利器─Rufus](https://terryjiun.github.io/posts/Rufus/){:target="_blank"}】一文。<br>
<br>
想要將 T102 重新安裝乾淨的作業系統，除了有 USB 開機磁碟外，最好還要有 USB Hub，<br>
因為安裝過程需要用到滑鼠操作，但是 T102 只有一個 USB Port，必須用 USB 集線器來分接。<br>
觸控操作、藍牙滑鼠可能皆無用武之地，因為大多數的 WinPE 不支援藍牙滑鼠、觸控螢幕，<br>
除非另外安裝驅動程式。<br>
<br>
您可以將想要安裝的 Windows 版本的 ISO 檔儲存在上述的 WinPE 開機磁碟裡，<br>
前提是磁碟空間要夠大，而且必須先用「Rufus」製作好開機系統，再來存放 Windows 的 ISO 檔。<br>
接好 USB 集線器、開機隨身碟、備份／還原隨身碟、滑鼠後，<br>
按下 T102 的電源開關，出現開機畫面時（黑底白字的 ASUS LOGO），<br>
連續按 ESC 鍵，就會出現開機選單，讓使用者選擇從哪項裝置開機。<br>
成功進入 WinPE 的桌面後，因為 T102 的畫面預設是直式的，<br>
此時請轉身對著畫面，在桌面空白處按一下滑鼠右鍵，選擇「螢幕解析度」，<br>
然後在〝方向〞這列上選擇「橫向」（Win10）或「橫向(翻轉)」（Win8.1）即可將畫面改為橫式。<br>
<br>
掛載 ISO 檔的步驟如下：<br>
一、開啟檔案總管（對桌面上的「本機」點兩下）。<br>
二、找到要掛載的 ISO 檔後，對它按右鍵，選擇「開啟檔案」→「Windows 檔案總管」（Win10），<br>
　　或「開啟檔案」→「繼續使用 Windows 檔案總管」（Win8.1）。<br>
三、掛載成功後，會自動跳出 ISO 檔的內容，點選 Setup.exe 即可進行安裝。<br>
<br>
備份／還原方面，可以使用 Ghost、GImageX、Acronis True Image 2016<br>
（Win10PE「程式集」裡選擇「安裝ATIH6569TW」，<br>
等待解壓縮完成後，即可再回程式集找到「Acronis True Image 2016」），<br>
筆者建議使用 Acronis True Image 2016 備份整個 SSD 硬碟，快速而且各分區都能完整備份。<br>
<br>
至於上述的兩個 WinPE 搭載的程式，列示如下。
<hr>
Windows 10 PE 搭載的程式如下：<br>
安裝輔助<br>
　WinNTSetup<br>
系統工具<br>
　AIDA64<br>
　BOOTICE<br>
　CPU-Z<br>
　Dism++<br>
　NTBOOTautofix<br>
　NtpwEdit64<br>
　RegWorkshop<br>
　清除Windows密碼<br>
其它軟體<br>
　BeyondCompare<br>
　EveryThing<br>
　FastCopy<br>
　PECAB<br>
　ResHacker<br>
　U+隱藏區掛載工具<br>
　UltraISO<br>
　wimboot<br>
　WINSNAP<br>
　掛載ESP分區<br>
　登入密碼解鎖器(DaRT版)<br>
　顯示普通隱藏分區<br>
附屬程式<br>
　小畫家<br>
　工作管理員<br>
　計算機<br>
　記事本<br>
　剪取工具<br>
　登錄編輯程式<br>
備份還原<br>
　GHOST<br>
　　GHOST 11.51<br>
　　GHOST 11.51伺服器<br>
　　GHOST 11.51瀏覽器<br>
　　Ghost64<br>
　OneKey<br>
　安裝ATIH6569TW<br>
磁碟工具<br>
　DiskGenius<br>
　DiskInfo<br>
　HDTunePro<br>
　PartAssist<br>
　SSD-Z<br>
　分割整數器<br>
管理工具<br>
　服務<br>
　裝置管理員<br>
　電腦管理<br>
　磁碟管理<br>
網路工具<br>
　Internet Explorer<br>
　Opera<br>
　PENetwork<br>
　遠端桌面<br>
　寬頻連線<br>
影音媒體<br>
　PotPlayer<br>
辦公應用<br>
　Notepad++<br>
　PDFXCview<br>
　安裝Office2007<br>
　馴碼快手<br>
壓縮軟體<br>
　EasyImageX<br>
　Gimagex<br>
　WimTool<br>
　WINRAR<br>
驅動程式<br>
　自訂驅動安裝

![Win10PE_10586](/assets/img/windows/Win10PE-1.png)

![Win10PE_System](/assets/img/windows/Win10PE-2.png)
<hr>
Windows 8.1 PE 搭載的程式如下：<br>
BOOTICE<br>
DiskGenius<br>
ESD Decrypter<br>
GHOST-GUI<br>
GImageX<br>
Internet Explorer<br>
Metro模式<br>
PENetwork<br>
Programs<br>
　Administrative Tools<br>
UltraISO<br>
WimTool<br>
WinNTSetup<br>
命令提示字元<br>
附屬應用程式<br>
　小算盤<br>
　工作管理員<br>
　記事本<br>
　登錄編輯程式<br>
記事本<br>
管理工具<br>
　服務<br>
　裝置管理員<br>
　電腦管理<br>
　磁碟管理<br>
遠端桌面<br>
寬頻連線<br>
整理磁碟代號<br>
檔案總管<br>

![Win8PE_16384](/assets/img/windows/Win81PE-1.png)

![Win8PE_System](/assets/img/windows/Win81PE-2.png)
