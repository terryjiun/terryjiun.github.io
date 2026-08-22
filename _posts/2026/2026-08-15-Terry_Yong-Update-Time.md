---
title: 關於「泰瑞版小小輸入法」的更新頻率
date: 2026-08-15 10:10:00 +0800
categories: [泰瑞版小小輸入法]
tags: [Terry_Yong, 碼表更新]
---

#泰瑞君的部落格（新文）@GitHub

最新版本的泰瑞版小小輸入法，以後會放在這個 Google Drive 路徑之下：<br>
<a href="https://drive.google.com/drive/folders/1a6KmtMCETshYAzzX6RzHZ6m5s00IijEL" target="_blank">https://drive.google.com/drive/folders/1a6KmtMCETshYAzzX6RzHZ6m5s00IijEL</a><br>
（會保留一些相對較舊的版本，檔名會夾帶更新日期，請下載自己所需的，解壓縮密碼都是：yong）<br>
<br>
就如這篇文章：<a href="https://terryhung.pixnet.net/blog/posts/2036779276" target="_blank">https://terryhung.pixnet.net/blog/posts/2036779276</a><br>
開頭的「重要提醒」所述，<br>
該路徑會儲存集大成、最新、最正確的版本，如果有需要引用碼表的話，請自行提取，<br>
以文字編輯器搜尋「&#35;&#35;」，即可在碼表裡找到各字元集的段落，讀者可以自行剪裁不需要的段落。<br>
<br>
泰瑞版小小輸入法使用的 yong.exe 及其相關的核心程式不會使用周永先生發布的「正式版」，<br>
因為正式版發布間隔通常長達一年以上，有些問題不會被及時修復，<br>
所以筆者會使用「相對較新」的「測試版」，<br>
但是最新測試版更新頻率太高，可能間隔不到十天就會有新的更新，<br>
所以筆者不會使用「最新」的測試版。<br>
<br>
如果 Unicode 有發布新的 CJK 字元集，而且倉頡之友論壇有網友分享對應的碼表後，<br>
筆者就會儘快更新泰瑞版小小輸入法的倉頡碼表。<br>
如果 Unicode 沒有發布新的 CJK 字元集，筆者大約每半年會將倉頡碼表裡的股名、股號輸入法更新一次。<br>
每次更新倉頡碼表時，也會同時更新 yong.exe 及其相關的核心程式。<br>
<br>
yong.exe 及其相關的核心程式是指在「w64」資料夾下的4個檔案：<br>
libl.dll、libmb.so、yong.exe、yong-config.exe<br>
它們是64位元的版本，<br>
在「Terry_Yong」根目錄下「相同檔名與副檔名」的那4個檔案是32位元的版本，<br>
周永先生自2026年6月起已不再更新32位元的版本，<br>
所以除非是在32位元版的 Windows 下使用，不然的話，應該使用64位元版的 yong.exe。<br>
<br>
讀者也可以「隨時」自行更新 libl.dll、libmb.so、yong.exe、yong-config.exe，<br>
方式是先建立一個暫存資料夾，比如 D:\Test，然後將「Terry_Yong」資料夾複製到裡面，<br>
然後設定防毒軟體排除 D:\Test，再結束執行中的 yong.exe，<br>
然後開啟「D:\Test\Terry_Yong\w64」路徑下的 yong.exe，<br>
在小蝸牛（或藍色Ｔ）圖示上透過右鍵→幫助→更新，獲取4個「w64」資料夾下的新檔案，<br>
再複製到「C:\Program Files\Terry_Yong\w64」資料夾下，覆蓋（取代）原本的檔案即可。<br>
有時也要取代「C:\Program Files\Terry_Yong\tsf」資料夾下的 yong.dll、yong64.dll。<br>
這樣就能自己完成更新。<br>
