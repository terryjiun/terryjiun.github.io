---
title: 淺析 NTFS Data Streams（資料串流）
date: 2012-10-13 10:10:00 +0800
categories: [應用軟體]
tags: [Windows, 實用工具]
---

2015.11.01 補充說明：<br>
有關 Windows 10 的 NTFS Data Streams 問題及刪除方式，<br>
請參考「★Windows 10 解除封鎖檔案與 AlternateStreamView 程式的應用」一文。<br>
<br>
Word 2010 的使用者應該蠻常看到下列這張圖片的情況：

![Word 2010](assets/img/app/Data-Stream-01.png)

也就是從某些網站下載而來的 Word 檔，Word 2010 會發出警告通知您：<br>
「受保護的檢視　此檔案源自於網際網路位置，可能不安全。請按一下這裡取得詳細資料。」<br>
您必須點選「啟用編輯」按鈕，才能對它加以編輯。<br>
（當然您也可以調整 Word 2010 的環境設定，讓它不發出警告，但那不是本文的重點）<br>
<br>
上面這個檔案有什麼問題呢？<br>
如果在檔案總管中，對它按右鍵，選內容，會發現它有一個特別的地方：

![檔案總管](assets/img/app/Data-Stream-02.png)

「安全性」這一欄顯示：<br>
「這個檔案來自另一部電腦，可能會封鎖以協助保護您的電腦。」<br>
<br>
其實，自從 Windows XP（或更早版本的 Windows）以來，<br>
凡是磁碟格式化為 NTFS 檔案系統，都有這個特性：<br>
只要是經由瀏覽器、eMule 下載到 NTFS 磁碟機的檔案，<br>
不管它是什麼類型（Word、Excel、PowerPoint、應用程式、圖片…），<br>
Windows 都會自動為您加上「NTFS Data Streams」（備用資料流），<br>
所以「安全性」這一欄都會出現「解除封鎖」的按鈕，<br>
而且，開啟應用程式（&#42;.exe、&#42;.msi…）時，甚至不會直接執行，<br>
而是會先出現一個警告畫面，使用者必須先點選「是」或「執行」按鈕後，<br>
程式才會被執行，如下面2張圖片所示：

![Windows 8 使用者帳戶控制](assets/img/app/Data-Stream-03.png)

![Windows XP 安全性警告](assets/img/app/Data-Stream-04.png)

唯一例外的情況是：<br>
只有從 IE「信任的網站」下載的檔案，才不會被加上「NTFS Data Streams」。<br>
需要注意的地方是：<br>
Windows 只判斷檔案是不是從「信任的網站」下載來的，與下載的瀏覽器無關，<br>
即使是用 Firefox 下載，如果檔案不是從「信任的網站」下載來的，<br>
一樣會被加上「NTFS Data Streams」。<br>
（這也可以看出 IE 的設置與 Windows 有多密切了！）<br>
<br>
另外，某些下載軟體在下載時會協助移除 NTFS Data Streams，<br>
像是 SmartGet、YouTubeDownloaderHD…<br>
還有，每個檔案的 NTFS Data Streams、相容性、安全性設定都是儲存在檔案系統裡，<br>
不是記錄在檔案本身裡，所以即使有兩個相同的檔案，<br>
一個有「解除封鎖」，一個沒有「解除封鎖」，兩者的 SHA1 值仍會是相同的！<br>
<br>
在本文的第2張圖片中，我們可以按下「解除封鎖」按鈕，<br>
這樣就能去除「NTFS Data Streams」，<br>
讓應用程式執行時，不必再按一次「執行」按鈕（而且開啟速度會較快）；<br>
或是讓 Word 2010 不再提示我們「啟用編輯」。<br>
但是，如果下載的檔案數量很多，要對每一個檔案都作「解除封鎖」的動作，<br>
這可是一件非常煩人的事情。<br>
好在有網友編寫了一支工具程式，<br>
我們只要執行它就可以把「NTFS Data Streams」一次消除。<br>
這支工具程式的名稱及版本是：Streams v1.56<br>
下載網址是：[https://www.mediafire.com/file/7y0p9suap9vay6s/Streams.zip](https://www.mediafire.com/file/7y0p9suap9vay6s/Streams.zip){:target="_blank"}<br>
建議下載後，解壓縮到 D:&#92;，然後先執行一次「streams.exe」，

![Streams v1.56](assets/img/app/Data-Stream-05.png)

出現上圖中的畫面後，點選「Agree」。<br>
然後再以「系統管理員」身分執行「命令提示字元」，<br>
假設要消除 C:&#92;Downloads 資料夾內所有檔案（含子資料夾的檔案）的 Data Stream，<br>
先切換至「D:」後，執行「streams.exe -s -d C:&#92;Downloads」即可！<br>
雖然這支工具程式對中文路徑的支援程度並不完善，執行過程中，中文路徑會變成「??」，<br>
但是不需要理會它，執行完成後，它會回到「D:&#92;&#62;」，<br>
此時，「C:&#92;Downloads」裡所有檔案的「Data Streams」就會全部被移除，<br>
我們也就省去一一作「解除封鎖」的動作了！<br>
<br>
如果甲、乙兩人下載了同一個檔案，<br>
甲沒有移除「Data Streams」，而乙有移除「Data Streams」，<br>
甲、乙只是改了檔名，就把檔案原封不動複製給丙（透過 NTFS 的外接式磁碟傳送），<br>
丙從甲那裡得來的檔案還是會有「Data Streams」，<br>
只有從乙那裡得來的檔案不會有「Data Streams」，<br>
雖然丙用「HashMyFiles」這類的軟體，對這兩個檔案算出的 SHA1 值仍會一樣，<br>
但丙應該會覺得甲提供的檔案比較安全！<br>
因為沒有「啟用編輯」這類的問題了！<br>
