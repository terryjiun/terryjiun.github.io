---
title: 移植 Windows XP 內建中文輸入法至 Windows 7/Vista/Server 2008
date: 2008-06-17 10:10:00 +0800
categories: [輸入法]
tags: [Windows, 通用輸入法編輯工具]
---

◎ 緣起：<br>
Windows 7/Vista/Server 2008 內建的中文輸入法，<br>
改良了倉頡、速成、注音三種輸入法，<br>
除了使其具備「輸入法整合器」（可支援符號及手寫輸入）之外，<br>
還支援 CNS11643 的組字字根，可用來輸入 CJK、CJK Ext-A/B 區字元集的漢字。<br>
<br>
註：<br>
在 Windows XP 環境下，<br>
「輸入法整合器」的功能只有新注音及新倉頡才有，<br>
這裡指的新注音、新倉頡不是 Windows XP 內建的，<br>
而是安裝 Office XP 或其以後版本的 Office 而更新過的新注音、新倉頡；<br>
安裝 Office 2007 後，更新過的新注音、新倉頡雖然可以支援 CNS11643 的組字字根，<br>
但是如果要顯示 CJK Ext-A/B 區的漢字，還必須另外安裝「新細明體更新套件」。<br>
（微軟的下載中心已經移除這個套件，Windows XP SP3 也不包含這個套件，<br>
有需要的人可以連到這個網址下載：<br>
[https://www.tbmc.com.tw/computerese/pdf/PMingLiU%20Update%20Pack.msi](https://www.tbmc.com.tw/computerese/pdf/PMingLiU%20Update%20Pack.msi){:target="_blank"}）<br>
<br>
Windows Vista/Server 2008 的倉頡、速成、注音，仍然保留「反查組字字根」的功能，<br>
但新的大易、行列取消輸入法程式的「內容」設定，<br>
因此無法設定反查組字字根，同時也出現了不少問題（註：SP2 及 Win7 已修正這些問題）。<br>
另外，這五種新的輸入法雖然具備「相關字詞功能」<br>
（倉頡、速成、注音可以設定取消此功能；<br>
大易、行列則無法設定取消此功能，除非升級到 SP2 或 Win7），<br>
但並無「相關字詞編輯工具」可以使用<br>
（這個工具是 Windows XP 附屬應用程式中的一個小程式），<br>
因此也就不能修改出現在相關字詞方塊內的文字選單。<br>
<br>
網路上流傳的解決方式是：<br>
將 Windows XP 內建的中文輸入法軟體移植至 Windows 7/Vista/Server 2008 上使用。<br>
我整理並擷取 Windows XP Professional with SP3 的檔案後，<br>
特別做成一個壓縮檔以方便網友們使用，<br>
下載網址是：<br>
https://www.mediafire.com/file/8ve8veq1wfe87bq/WinXP&#95;IME.zip<br>
<br>
◎ 使用方式：<br>
1.按照自己的需求，<br>
　將〝所需〞輸入法資料夾內的檔案複製至 C:\Windows\System32，<br>
　說明一：為避免檔案覆蓋問題，一些檔名已經先被修改過。<br>
　說明二：如果您要使用大易輸入法及反查注音功能，<br>
　　　　　請同時複製「大易」、「注音」兩資料夾內的檔案至 C:\Windows\System32<br>
2.複製「uniime.dll」至 C:\Windows\System32<br>
　說明：如果您想使用「通用輸入法編輯工具」，請將「miniime.tpl」一併複製至 C:\Windows\System32<br>
3.執行〝所需〞輸入法資料夾內的 &#42;.reg，匯入機碼至系統組態登錄。<br>
　說明一：筆者將 &#42;.reg 內的輸入法名稱皆以「中文 (繁體) - 大易 (XP)」格式命名，<br>
　　　　　網友如欲修改可先在 &#42;.reg 檔案上按右鍵，選「編輯」，修改並存檔後再匯入，<br>
　　　　　如已匯入者，可利用 regedit 指令叫出「登錄編輯程式」，<br>
　　　　　依 &#42;.reg 檔內的路徑找到資料後再自行修改。<br>
　說明二：有些網路文章將 &#42;.reg 檔內的「"Layout Text"」及「"Layout Display Name"」後面的文字設為同樣，<br>
　　　　　筆者則是將「"Layout Display Name"」後面的文字參考搜尋到的「機碼對應表.txt」做不同的設定。<br>
4.開啟「控制台／地區及語音選項」，點選「鍵盤及語言」頁籤內的「變更鍵盤」按鈕<br>
　（或直接於〝語音列〞上按右鍵選「設定值」），<br>
　即可「新增」匯入的輸入法。<br>
<br>
<br>
◎ 注意事項：<br>
1.欲使用「相關字詞編輯工具」，可直接執行「Lctool.exe」，<br>
　修改並存檔後即可在移植的輸入法上產生作用，但內建的新版輸入法的相關字詞並不會隨之改變。<br>
2.欲使用「通用輸入法編輯工具」，可直接執行「Uimetool.exe」。<br>
3. 「相關字詞編輯工具」及「通用輸入法編輯工具」的使用教學請網友利用 Google 搜尋。<br>
4.在 Windows 7/Vista/Server 2008 的「使用者帳戶控制（UAC）」開啟的情況下，<br>
　可能會造成移植過程中的困擾，<br>
　建議先至「控制台／使用者帳戶」關閉該功能。<br>
<br>
<br>
◎ 對 64 位元版 Windows 7/Vista/Server 2008 的特別說明：<br>
1.Windows XP x64，只有英文版，沒有繁體中文版，<br>
　英文版本身沒有中文輸入法的相關檔案，必須加裝繁體中文語言套件才會有。<br>
　但即使加裝繁體中文語言套件後，仍然少了「Lctool.exe」、「Uimetool.exe」這兩個檔案。<br>
　所幸，Windows Server 2003 R2 x64 有繁體中文版，而且有「Lctool.exe」、「Uimetool.exe」這兩個檔案。<br>
　將上述「WinXP&#95;IME.zip」解壓縮後，「x64」資料夾內的檔案即擷取自 Windows Server 2003 R2 x64。<br>
2.使用方式及注意事項大致同上，但必須將檔案複製至 C:\Windows\SysWOW64（而不是 C:\Windows\System32），<br>
　缺點是：移植後的輸入法只能在 32 位元的應用程式（如：IE）環境下使用，<br>
　在 64 位元的應用程式（如：記事本）環境下是無法使用的！<br>
3.如果想要讓移植的輸入法能同時在 32 位元及 64 位元的應用程式環境下使用，<br>
　必須先將「x64」資料夾裡「System32」、「SysWOW64」這兩個子資料夾內的檔案分別複製到：<br>
　「C:\Windows\System32」及「C:\Windows\SysWOW64」路徑下，<br>
　再分別用 WinXP 及 Win2003 x64 的「通用輸入法編輯工具」（Uimetool.exe）產生輸入法，<br>
　產生時請注意：<br>
　(1)需先準備對照表，並且放在 C:\ 路徑下。<br>
　(2)「輸入法名稱」、「產生 .IME 檔的英文檔名」、「對照表檔案」、「最大組字字根數目」要做同樣的設定。<br>
4.用「通用輸入法編輯工具」產生的輸入法，候選字方塊內的文字選單當中的 CJK Ext-B 字元會變成「|  |」<br>
　（32 位元 Windows 環境下沒有這個問題）。<br>
5.無論是用 WinXP 或 Win2003 x64 的「相關字詞編輯工具」（Lctool.exe）編修後的相關字詞，<br>
　都能正常在 32 位元及 64 位元的應用程式環境下使用。<br>
6.因為取得各種輸入法對照表並非難事（可上 gcin 網站下載後加以編修），<br>
　所以使用第 3 點的方式相較之下較無缺點，<br>
　只是對照表裡最好不要有 CJK Ext-B 的字元，以免候選字方塊內出現「|  |」。<br>
