---
title: Windows 8 無法連上網路的解決方式
date: 2012-12-01 10:10:00 +0800
categories: [作業系統]
tags: [Windows]
---

我的 Windows 8 蠻常發生一開機就不能連網的現象，<br>
（我使用桌上型電腦，主機板為 ASUS P7H55，它使用 Realtek 的網路卡晶片組；<br>
我安裝的是 Windows 8 繁體中文 64 位元專業版，搭配 Windows Media Center）<br>
我推測可能是驅動程式有問題（使用的是 Windows 8 內建的 Drivers），<br>
或者 Driver 與 VirtualBox 之間有衝突<br>
（當我不安裝 VirtualBox，就不會出現這個情形）。<br>
如果您也有這樣的問題，先不用擔心是網路卡壞掉，<br>
畢竟現在網路卡大多做成 Onboard 的，如果要更換、維修的話，都挺費事的，<br>
您可以參考以下的說明嘗試解決這個問題。<br>
<br>
一、在工作列右邊的「網路」圖示上按右鍵，選「開啟網路和共用中心」。

![Windows 8 Lan Error](/assets/img/windows/Windows-8-Lan-1.png)

二、在接下來出現的畫面裡，選「變更介面卡設定」。

![Windows 8 Lan Fix 1](/assets/img/windows/Windows-8-Lan-2.png)

三、在接下來出現的畫面裡，點選「乙太網路」，此時會看到 IPv4 和 IPv6 連線能力都是「未連線」，<br>
　　這時請點選畫面中的「診斷」。

![Windows 8 Lan Fix 2](/assets/img/windows/Windows-8-Lan-3.png)

四、接著，系統會進行診斷，診斷完成後會出現下列畫面，<br>
　　請點選「請嘗試以系統管理員身分進行這些修復」。

![Windows 8 Lan Fix 3](/assets/img/windows/Windows-8-Lan-4.png)

五、接著系統會進行修復，修復完成會出現下列畫面，請點選「關閉疑難排解員」。

![Windows 8 Lan OK 1](/assets/img/windows/Windows-8-Lan-5.png)

六、接著，可以看到 IPv4 或 IPv6 連線能力顯示為「網際網路」，<br>
　　這時您可以關閉這個視窗，並安心上網了！

![Windows 8 Lan OK 2](/assets/img/windows/Windows-8-Lan-6.png)
