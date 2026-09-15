---
title: 讓 Windows 7 專業版「文字轉換語音」可以選擇「zh-TW HanHan」語音
date: 2017-04-05 10:10:00 +0800
categories: [作業系統]
tags: [Windows, 實用工具, 小小特殊功能, 小小設定]
---

## 前言

筆者今天在 Windows 7 繁體中文專業版（32 位元版和 64 位元版）測試「泰瑞版小小輸入法」的〝語音校對〞功能，<br>
結果發現「開啟語音輸出」功能後，系統並不會朗讀筆者打出的漢字，<br>
於是筆者到控制台（檢視方式：大圖示或小圖示）裡依序點選「語音辨識」→「文字轉換語音」（切換到「文字轉換語音」頁籤）後，<br>
看到了一個令筆者無言以對的畫面，截圖如下：

![Windows 7 文字轉換語音](/assets/img/windows/Windows-7-Speech-1.png)

它的「語音選取」只有一項：Microsoft Anna - English (United States)<br>
因此它不會朗讀漢字也是很正常的現象，<br>
但是不能在此畫面新增「語音選取」的項目，著實讓人感到無奈！<br>
於是筆者搜尋並試驗了一些方法和軟體，後來用英文搜尋並找到【[這一篇文章](https://superuser.com/questions/590779/how-to-install-more-voices-to-windows-speech){:target="_blank"}】，終於解決了筆者的問題！<br>
以下就將筆者的試驗結果寫成教學文件，避免有需要的使用者再走冤枉路。

## 教學指南

32 位元版 Windows 7（x86 版）只要下載並依序執行下列三個檔案：<br>
1.[SpeechPlatformRuntime&#95;x86.msi](https://www.mediafire.com/file/79mn57j6azbjqxt/SpeechPlatformRuntime_x86.msi){:target="_blank"}<br>
2.[MSSpeech&#95;TTS&#95;zh-TW&#95;HanHan.msi](https://www.mediafire.com/file/e3i738ka4ui9j3g/MSSpeech_TTS_zh-TW_HanHan.msi){:target="_blank"}<br>
3.[Patch&#95;x86.reg](https://www.mediafire.com/file/0w8d5lrkv0dn401/Patch_x86.zip){:target="_blank"}（下載後，請先解壓縮）<br>
<br>
64 位元版 Windows 7（x64 版）則要下載並依序執行下列五個檔案：<br>
1.[SpeechPlatformRuntime&#95;x86.msi](https://www.mediafire.com/file/79mn57j6azbjqxt/SpeechPlatformRuntime_x86.msi){:target="_blank"}<br>
2.[SpeechPlatformRuntime&#95;x64.msi](https://www.mediafire.com/file/5pi26tgy4mtishm/SpeechPlatformRuntime_x64.msi){:target="_blank"}<br>
3.[MSSpeech&#95;TTS&#95;zh-TW&#95;HanHan.msi](https://www.mediafire.com/file/e3i738ka4ui9j3g/MSSpeech_TTS_zh-TW_HanHan.msi){:target="_blank"}<br>
4.[Patch&#95;x86.reg](https://www.mediafire.com/file/0w8d5lrkv0dn401/Patch_x86.zip){:target="_blank"}（下載後，請先解壓縮）<br>
5.[Patch&#95;x64.reg](https://www.mediafire.com/file/4d3nmgc05bwmn10/Patch_x64.zip){:target="_blank"}（下載後，請先解壓縮）<br>
<br>
值得注意的是：<br>
1. 安裝 MSSpeech&#95;TTS&#95;zh-TW&#95;HanHan.msi 時並不會出現任何畫面，點選後幾秒鐘的時間，它就安裝完成了！<br>
<br>
2. 32 位元版 Windows 7 的使用者，執行上述三個檔案後，<br>
　即可到控制台（檢視方式：大圖示或小圖示）裡依序點選「語音辨識」→「文字轉換語音」（切換到「文字轉換語音」頁籤後），<br>
　選取「Microsoft Server Speech Text to Speech Voice (zh-TW, HanHan)」這一個選項，<br>
　然後在「使用下列文字來測試語音」這一列輸入一串中文，<br>
　再按下「測試語音」按鈕，聽看看系統是否正確讀出句子。<br>
　如果沒問題，就可以按下「套用」、「確定」（畫面截圖如下）。

![Windows 7 文字轉換語音](/assets/img/windows/Windows-7-Speech-2.png)

　64 位元版 Windows 7 的使用者，執行上述五個檔案後，<br>
　請勿回到控制台（檢視方式：小圖示）裡依序點選「語音辨識」→「文字轉換語音」。<br>
　因為仿照 32 位元版的方式進行設定的話，只會出現下列警告：<br>
　「無法播放這個語音。請嘗試選取另一個語音或選取一個不同的音訊輸出裝置。」

![Windows 7 語音錯誤](/assets/img/windows/Windows-7-Speech-3.png)

　正確的設定方式如下：<br>
　請先複製【<span style="color: red">%windir%&#92;sysWOW64&#92;speech&#92;SpeechUX&#92;SAPI.cpl</span>】這串指令，<br>
　然後以系統管理員身分執行「命令提示字元」（cmd），在命令提示字元的視窗標題列按右鍵，<br>
　選擇「編輯」→「貼上」，帶入上述指令後，再按下 Enter 鍵，<br>
　出現「語音內容」對話方塊後，切換至「文字轉換語音」頁籤，<br>
　選取「Microsoft Server Speech Text to Speech Voice (zh-TW, HanHan)」此一選項，<br>
　然後在「使用下列文字來測試語音」這一列輸入一串中文，<br>
　再按下「測試語音」按鈕，聽看看系統是否正確讀出句子。<br>
　如果沒問題，就可以按下「套用」、「確定」。

## 新增其他語音的方式

假設您需要添加日文「文字轉語音」的 Voice 檔，首先連至「[微軟官網](https://www.microsoft.com/en-us/download/details.aspx?id=27224){:target="_blank"}」點選【Download】，<br>
在展開的檔案列表中，選擇以「MSSpeech&#95;<span style="color: blue">TTS</span>」開頭的檔案（不要選擇以「MSSpeech&#95;<span style="color: red">SR</span>」開頭的檔案），<br>
日文語音檔的縮寫為「ja」，因此選擇下載「MSSpeech&#95;TTS&#95;ja-JP&#95;Haruka.msi」這一個檔案，<br>
安裝完成後，執行「regedit」指令，匯出下列 2 個資料夾的內容（<span style="color: purple"><b>如果是 32 位元 Windows，只需匯出第一個</b></span>）：<br>
HKEY&#95;LOCAL&#95;MACHINE&#92;SOFTWARE&#92;Microsoft&#92;Speech Server&#92;v11.0&#92;Voices&#92;Tokens&#92;<span style="color: blue">TTS&#95;MS&#95;ja-JP&#95;Haruka&#95;11.0</span><br>
HKEY&#95;LOCAL&#95;MACHINE&#92;SOFTWARE&#92;Wow6432Node&#92;Microsoft&#92;Speech Server&#92;v11.0&#92;Voices&#92;Tokens&#92;<span style="color: blue">TTS&#95;MS&#95;ja-JP&#95;Haruka&#95;11.0</span><br>
（前兩行藍色字部分，應依您安裝的語言進行變換）<br>
匯出的具體作法為依序展開至上述資料夾，然後在「<span style="color: blue">TTS&#95;MS&#95;ja-JP&#95;Haruka&#95;11.0</span>」資料夾上按右鍵，選「匯出」，<br>
再分別儲存為「ja&#95;x86.reg」及「ja&#95;x64.reg」，然後以文字編輯器（記事本、EditPlus…）對這兩個 reg 檔的內容進行下列取代工作：<br>
尋找目標：<span style="color: blue"><b>&#92;Speech Server&#92;v11.0&#92;</b></span><br>
（全部）取代為：<span style="color: blue"><b>&#92;Speech&#92;</b></span><br>
存檔後，再執行修改完成的 reg 檔，最後即可開啟「語音內容」對話方塊選擇日文語音檔。

## 後記

筆者在 32 位元及 64 位元 Windows 7 專業版（繁體中文版）依照上述教學指南安裝後，<br>
可以使「小小輸入法」（安裝版或免安裝版皆可）順利調用「文字轉換語音」模組，<br>
達到和自然輸入法的「同步發音」相同的功能。<br>
只要開啟「小小輸入法」主視窗，然後按下 Ctrl + Alt + Shift + S，畫面成功提示「開啟語音輸入」後，<br>
打開喇叭或戴上耳機，就會聽到系統朗讀出使用者打出的漢字，<br>
直到使用者再次按下 Ctrl + Alt + Shift + S，畫面成功提示「停止語音輸入」；<br>
或使用者結束 yong.exe（或重新載入後），才會停止朗讀。<br>
