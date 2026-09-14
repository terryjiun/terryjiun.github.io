---
title: 「跳過 Windows 登入步驟，開機直接進入桌面」的設定方式
date: 2015-11-22 10:10:00 +0800
categories: [作業系統]
tags: [Windows, 實用工具]
---

現在很多人都是擁有一部屬於自己的桌上型電腦、筆記型電腦，或者是平板（以下統稱「電腦」），<br>
在 Windows 環境下也只有建立一個使用者帳戶，<br>
而且這部電腦只有自己在用，不會借給他人使用，不會分享給家人、室友、朋友使用，<br>
電腦也保管得很好，不必擔心遺失、竊盜的問題。<br>
在這種（前提）情況下，開機後，還要再經過輸入帳號、密碼的程序，似乎顯得有點多餘。<br>
尤其 Windows 8/8.1/10 具備「快速啟動」功能，<br>
關閉電源後，下次開機（不是從 Windows 選擇重新開機），開機速度會變得飛快，<br>
但是，如果卡在登入畫面，就不能享受到「開機後快速進入桌面」的好處。<br>
<br>
Windows XP 允許使用者建立「空密碼」（沒有密碼）的使用者帳戶，<br>
而且如果系統只有啟用這個帳戶，開機後就會自動進到桌面。<br>
不過，這種空密碼的帳戶並不好！因為它會伴隨較多的安全性問題。<br>
倒不是因為別人摸走您的電腦，可以直接開機後讀取您的檔案（前面已經有假設前提了），<br>
而是駭客可能會用遠端操控的方式，神不知、鬼不覺的侵入您的系統。<br>
所以設定 Windows 帳戶的密碼，而且設得複雜一點，是絕對有必要的！<br>
<br>
但是一旦設定 Windows XP 的帳戶密碼，開機後就會停留在「<span style="color: purple">歡迎畫面</span>」（登入畫面），<br>
而且 Windows 8/8.1/10 預設會停留在「<span style="color: purple">鎖定畫面</span>」，<br>
必須按一下滑鼠或用手指觸控將鎖定畫面撥開，才會進入登入畫面，<br>
這並不是具備前面前提的人所樂見的，<br>
因此，我們可以透過下列的設定方式，來更改這種情形。<br>
<br>
<span style="color: blue">Windows Vista/7/8/8.1/10：<br>
以系統管理者身分執行【命令提示字元】（cmd），</span><br>
<span style="color: red">再執行「netplwiz」指令</span>，出現下圖時，<br>
先在中間的使用者名稱清單裡選取要自動登入的帳戶（只有一個時就不需選擇了），<br>
<span style="color: blue">取消勾選【必須輸入使用者名稱和密碼後，才能使用這台電腦】，再按【確定】，</span><br>
最後會出現對話方塊，請您輸入選取的使用者名稱之密碼、確認密碼。<br>
（注意！如果已經綁定 Microsoft 帳戶的話，使用者名稱要輸入完整的 E-Mail Address）<br>
完成設定後，以後開機時就會自動登入 Windows，直接到桌面了！

![netplwiz](/assets/img/windows/netplwiz.png)

Windows XP：<br>
<span style="color: blue">與上述的設定方式大同小異，只不過要把執行指令（netplwiz）改為「</span><span style="color: red">control userpasswords2</span><span style="color: blue">」。</span><br>
<br>
備註：<br>
此種設定方式不適用於已加入網域的電腦，因為網域伺服器指派的 Policy 可能不允許您這樣做，<br>
不過，已加入網域的電腦，似乎也超出本文要講述的範圍了！<br>
<br>
參考文章：<br>
[https://www.eightforums.com/threads/log-on-user-account-automatically-at-windows-8-startup.2894/](https://www.eightforums.com/threads/log-on-user-account-automatically-at-windows-8-startup.2894/){:target="_blank"}<br>
