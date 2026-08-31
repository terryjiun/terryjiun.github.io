---
title: 泰瑞版小小輸入法─Adobe 篇
date: 2013-08-21 10:10:00 +0800
categories: [泰瑞版小小輸入法]
tags: [Terry_Yong, 輸入法程式]
---

小小輸入法和一些需要另外安裝（非 Windows 內建）的輸入法一樣，<br>
在某些軟體環境裡不能正常運作，即使將小小輸入法安裝為內置版本，問題仍然存在。<br>
問題發生的原因其實是這些軟體的設計問題，而不是小小輸入法本身的缺漏。<br>
最有名的就是「風之谷」這套遊戲軟體，它幾乎只支援 Windows 內建的輸入法。<br>
「風之谷」可以不玩，它的玩家人數佔（台灣）電腦族的比例應該也不會超過 5%，<br>
但是，Adobe 出產的 Reader（或 Acrobat）、Flash Player 卻有很多人在用，<br>
所以，本文將說明小小輸入法與它們之間不相容的情形，以及如何解決。<br>
<br>
大概是因為 Adobe 產品具有某些弱點，<br>
以致於會讓使用者的電腦存在資訊安全方面的問題，<br>
所以，Adobe 將 Reader（或 Acrobat）、Flash Player 預設用「沙箱」保護著，<br>
如果不關閉沙箱的話，在 Reader（或 Acrobat）裡尋找字元，<br>
或是在 Firefox 裡玩 Flash 遊戲時需要打字，就無法成功調用小小輸入法。<br>
目前，小小輸入法的作者─周永先生[已經表明暫時不處理這個問題](https://yong.dgod.net/read.php?tid=214&fid=2){:target="_blank"}，<br>
因此，以下就說明一下如何關閉沙箱吧！<br>
<br>
Adobe Acrobat XI Pro（預設情況是關閉沙盒）：<br>
編輯→偏好設定→保全(增強)→保護檢視→調為「關閉」→確定<br>
<br>
Adobe Reader XI（預設情況是開啟沙盒）：<br>
編輯→偏好設定→保全(增強)→啟動時啟用受保護模式→取消勾選→確定<br>
<br>
Adobe Flash Player for Firefox：<br>
1.開啟 mms.cfg 設定檔所在的資料夾<br>
　32 位元 Windows：C:&#92;Windows&#92;System32&#92;Macromed&#92;Flash<br>
　64 位元 Windows：C:&#92;Windows&#92;SysWOW64&#92;Macromed&#92;Flash<br>
2.用文字編輯軟體（如：記事本）開啟 mms.cfg，<br>
　在 mms.cfg 裡新增一行：ProtectedMode=0<br>
　（如果 Windows 已開啟「使用者帳戶控制」，可能會無法修改，<br>
　這時可先將 mms.cfg 複製到桌面，改完再複蓋原來路徑下的）<br>
PS: 用此方法就不用安裝「★在 Flash Player 中無法使用中文輸入法的解決方式」一文裡<br>
　　所介紹的「Windows Flash Player 11.3 Plugin content debugger」這支程式了！<br>
