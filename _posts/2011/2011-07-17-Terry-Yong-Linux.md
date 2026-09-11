---
title: ★泰瑞版小小輸入法 for Linux
date: 2011-07-17 10:10:00 +0800
categories: [泰瑞版小小輸入法]
tags: [Terry_Yong, 倉頡, 注音, Linux]
---

筆者在 2011 年安裝了一套 64 位元版的 Ubuntu 10.04 Desktop 系統來玩，<br>
同時也弄了一套 for Linux 系統的「泰瑞版小小輸入法」，<br>
目前最新版本（<span style="color: red"><b>核心為 2018.10.19 版</b></span>）的下載網址是：<br>
[https://www.mediafire.com/file/dtlh1tl3hduba4z/Terry_Yong_Linux.zip](https://www.mediafire.com/file/dtlh1tl3hduba4z/Terry_Yong_Linux.zip){:target="_blank"}<br>
（無法連上 MediaFire 免費空間，或是此連結失效的話，<br>
　請進入【[輸入法檔案@Google](https://docs.google.com/leaf?id=0B_9ob1iJjpkLMmRjODE2NWQtNjViNC00ZWRkLTgyY2ItNGJhOWEzODU1ZDNh){:target="_blank"}】或【[輸入法檔案@OneDrive](https://1drv.ms/f/c/01b7d23cf55aac84/QoSsWvU80rcggAHPAgAAAAAAEkEClyhF5XEafA){:target="_blank"}】，<br>
　再切換至「輸入法相關→輸入法軟體」目錄下載）<br>
<span style="color: purple">許多較新的 Linux 系統已不再支援第三方的輸入法軟體，<br>
如果您按照 Readme.htm 所述的步驟完成安裝，並重新開機後，<br>
請開啟文字編輯軟體，並使用「Ctrl + Alt + /」切換至小小輸入法，<br>
試看看能不能打出中文，如果不行，筆者也愛莫能助！<br>
如果您只是想安裝 Linux 系統來玩玩，沒有偏好哪一個分支的話，<br>
建議您下載並安裝 Lubuntu Desktop Version 16.04.3 LTS，<br>
（請使用 64-bit 版本來安裝小小輸入法，這樣比較不容易出錯）<br>
筆者在這個版本的環境裡可以正常安裝及使用「泰瑞版小小輸入法」。</span><br>
<br>
因為 Windows 與 Linux 所用之檔案系統（前者大多使用 NTFS，後者大多使用 Ext4）不同，<br>
於 Windows 系統解壓縮後，將遺失各檔案之 Ext4 檔案系統權限，<br>
所以請不要在 Windows 系統解壓縮、編修後再重新打包為壓縮檔。<br>
請直接於 Linux 系統解壓縮、編修碼表檔或設定檔。<br>
下面兩張圖片即為 Ext4 檔案系統的權限設定，<br>
如果在 Windows 系統解壓縮後重新壓縮，再儲存至 Linux 系統解壓縮的話，<br>
原本已勾選「容許檔案作為程式執行」（Allow executing file as program）選項，<br>
將變成不勾選，最後導致安裝過程發生錯誤。

![Properties-LinuxMint](/assets/img/terry_yong/Terry-Yong-Linux-1.png)

![Properties-Ubuntu](/assets/img/terry_yong/Terry-Yong-Linux-2.png)

Linux 版的「泰瑞版小小輸入法」界面和操作方式和 Windws 版並無太大的差異，<br>
只有一個地方需要特別處理：<br>
因為「泰瑞版小小輸入法」在輸入法對照表（碼表）裡有包含 CJK Ext-B/C/D 字元，<br>
而且外觀界面（Skin）的組態設定裡也有指定以「新細明體」呈現候選字，<br>
但是大多數的 Linux 平台並無內建支援 CJK Ext-B/C/D 的字型，<br>
所以必須將 Windows 8（或 Win 10）的新細明體移植至 Linux。<br>
<span style="color: purple">（筆者最新測試的 Lubuntu 16.04.3 Desktop 64-bit 已內建支援 CJK Ext-B 之字型 ）</span><br>
<br>
以 Ubuntu 10.04 為例，步驟如下：<br>
1.開啟「終端機」，<br>
　輸入「sudo chown -R <span style="color: blue">terry</span> /usr/share/fonts/truetype」（<span style="color: blue">請將 terry 改為您登入 Linux 的帳戶名稱</span>），<br>
　然後按「Enter」鍵（可能會提示輸入登入 Linux 的密碼），<br>
　執行完成後，「/usr/share/fonts/truetype」就會解除鎖定。<br>
2.Windows 10 v1903 內建的新細明體下載網址為：<br>
　[https://www.mediafire.com/file/62yzw0mbqd9twm9/Win10_v1903_MingLiu.zip](https://www.mediafire.com/file/62yzw0mbqd9twm9/Win10_v1903_MingLiu.zip){:target="_blank"}<br>
　解壓縮後，將「mingliu.ttc」、「mingliub.ttc」複製到「MingLiu」資料夾（請自行建立該資料夾），<br>
　然後再複製到 Linux 的系統字型資料夾，一般是這個目錄：/usr/share/fonts/truetype。<br>
3.開啟「終端機」，<br>
　輸入「sudo fc-cache -f -v」，<br>
　執行完成後，會立即更新系統字型檔，<br>
　之後便可順利以「新細明體-ExtB」顯示 CJK Ext-B/C/D 字元。<br>
<br>
關於 Linux 版的「泰瑞版小小輸入法」安裝方式，<br>
已於壓縮檔內的「Readme.htm」文件裡載明，此處不再贅述。<br>
必須要注意的是：<br>
有些 Linux 的軟體會用到「Ctrl + 空白鍵」當作快捷鍵，<br>
比如：Geany 預設使用這組快捷鍵當做自動補齊語法的按鍵，<br>
因此新版的泰瑞版小小輸入法已經將「yong.ini」內指定的開啟主視窗快捷鍵改為「<span style="color: blue"><b>Ctrl + Alt + /</b></span>」，<br>
成功開啟主視窗後，您就能在 Linux 系統裡愉快的使用「泰瑞版小小輸入法」了！<br>
