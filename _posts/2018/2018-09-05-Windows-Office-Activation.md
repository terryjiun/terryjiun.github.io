---
title: 使用 KMS 搭配指令「啟用」Windows 及 Office（免破解檔即可成功「激活」之方式）
date: 2018-09-05 10:10:00 +0800
categories: [作業系統]
tags: [Windows, 實用工具]
---

◎免責聲明：<br>
　本文講述的內容是作業系統的操作技術問題，而不涉及正版或盜版之法律問題或道德問題。<br>
　使用者需對自己選用 KMS Server 的結果負責，筆者不對任何使用後果負任何責任。
<hr>
KMS 是 Key Management Service 的縮寫，中文意思是（產品）金鑰管理服務，<br>
可以將它想像成 Windows 使用者在「控制台→系統管理工具→服務」之下所能查看到的一種程式運作的機制，<br>
而運行 KMS 的伺服器，也就被稱為 KMS Server。<br>
<br>
微軟提供企業用戶、學校用戶可以購買大量授權版的產品（Windows、Office…），並且架設自己的 KMS Server，<br>
然後讓數以百計（甚至千計、萬計）的用戶端透過連線到 KMS Server 來「啟用」（激活）這些產品。<br>
但是，透過 KMS Server 成功「啟用」的產品，日後如果不再連回 KMS Server 認證的話，就只能使用 180 天。<br>
不過，如果用戶端經常開機連網，而且能與 KMS Server 保持連線的話，<br>
這些產品會自動背景更新「啟用」的狀態（每週至少一次），也就是：<br>
本週三背景啟用完畢，從本週三算起的 180 天後激活狀態才會到期；<br>
下週三背景啟用完畢，從下週三算起的 180 天後激活狀態才會到期…永遠用不完的 180 天。<br>
<br>
這些採購大量授權軟體的組織（公司行號、機關、校園…）<br>
通常會將 KMS Server 架設在內網（Intranet），別人是無法連線的；<br>
但是，某些組織會提供 VPN 的連線方式，讓其所屬的用戶可以在家就能連上 KMS Server 並啟用產品。<br>
<br>
啟用的步驟很簡單，以激活 Windows 7/8/8.1/10 為例，<br>
只要「以系統管理員身分」執行「命令提示字元」，然後再執行下列 3 道指令：<br>
<span style="color: blue">slmgr /skms </span><span style="color: red">kms.xxx.xxx</span><br>
<span style="color: blue">slmgr /ato<br>
slmgr /dlv</span><br>
<br>
第一道指令是更改（指定）KMS Server 為「<span style="color: red">kms.xxx.xxx</span>」，<br>
<span style="color: red">這是筆者假設的網域名稱</span>，必須替換為「可用的 KMS」Server（域名或 IP Address）才能成功啟用。<br>
因為這道指令只在本機運算，所以不需等候，也不會有失敗的問題。<br>
<br>
第二道指令是向 KMS Server 請求認證，<br>
因為用戶端與伺服器端要連線溝通，需要等待一段時間，而且有可能會收到錯誤訊息。<br>
諸如：用戶端安裝的是零售版的 Windows、網路（含防火牆）設置出錯、KMS Server 被啟用的次數到達極限…<br>
這些問題都會導致認證失敗。<br>
<br>
第三道指令是顯示詳細的授權資訊，<br>
如果第二道指令執行完成時，收到「產品已成功啟用」的訊息，那麼此道指令可以不必執行。<br>
<br>
企業版的 Windows 一定要透過 KMS Server 啟用，而且安裝時就算遇到請您填入產品金鑰的畫面，也可以跳過；<br>
專業版的 Windows 則有分零售版（或隨機版）、大量授權版，安裝時可能必須要先填入產品金鑰才能完成安裝。<br>
教育版的 Windows 筆者未曾使用，不清楚情況如何。<br>
另外值得一提的事：<br>
如果 Windows 已經指定過 KMS Server 並且透過它啟用成功，<br>
後續再安裝大量授權版的 Office 時，Office 有可能就會自動使用該指定的 KMS Server 自行激活成功。<br>
<br>
筆者看過一些裝有 Windows 7 的電腦，當初的安裝者使用破解檔來啟用 Windows，<br>
這類破解檔大多是在用戶端的作業系統安裝簡易的 KMS，然後再透過自身激活產品。<br>
它不只容易被防毒軟體視為病毒而直接刪除，也容易被微軟後續推送的 Windows Update 更新檔反破解，<br>
因此不值得使用。<br>
<br>
另外有個以訛傳訛的流言，大意是「使用 KMS Server 激活後，該 Server 的管理員可以 Reset 用戶端的電腦」。<br>
其實，用 KMS 啟用 Windows，並不是將 Windows 由「本機」加入到「AD」（Active Directory，微軟的「目錄服務」產品），<br>
KMS 伺服器只是用來啟用產品，並不能操作用戶端。<br>
最壞的情形是 KMS 伺服器不能訪問（不能連線）而已，可以用第一道指令再換一個就好；<br>
KMS 伺服器管理者並不能像 AD 網域服務管理者那樣能向用戶端發送指令。<br>
<br>
至於 Office 啟用指令則列示如下（括號內為解說文字，請勿複製），供讀者參考及備用：<br>
<span style="color: blue">cd C:&#92;Program Files&#92;Microsoft Office&#92;Office</span><span style="color: red">16</span>（切換指令所在路徑，以 Office 2016 為例）<br>
<span style="color: blue">cscript ospp.vbs /sethst:kms.xxx.xxx</span>（更改 KMS 伺服器）<br>
<span style="color: blue">cscript ospp.vbs /act</span>（向 KMS 伺服器請求認證）<br>
<span style="color: blue">cscript ospp.vbs /dstatus</span>（顯示詳細授權資訊）<br>
