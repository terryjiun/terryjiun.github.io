---
title: 分享一些利用AI產生的JScript及VBScript，並說明小小輸入法如何調用它們
date: 2025-08-28 19:00:00 +0800
categories: [泰瑞版小小輸入法]
tags: [小小輸入法, 直通車, AI, Script]
---
#泰瑞的世界（舊文）@痞客邦

存放於筆者的【Google 雲端硬碟】或【OneDrive】的「輸入法相關→輸入法軟體」目錄之下，<br>
有個檔案名為「Terry_Yong_AI_Script.zip」，將其下載並解壓縮（解壓縮密碼：yong），<br>
再儲存到《泰瑞版小小輸入法》的安裝目錄下（即「Terry_Yong」資料夾下），<br>
然後可以在輸入法碼表裡運用小小輸入法的「命令直通車」功能來擴增一些實用且有趣的功能。<br>
<br>
命令直通車功能會透過打字的方式被呼叫到背景裡執行 cscript 指令，<br>
這個指令需要搭配已經寫好的 *.js 或 *.vbs 類型的腳本（Script，程式碼），<br>
然後執行結果會回傳給小小輸入法，再輸入到 Windows 當前開啟的應用程式裡。<br>
小小輸入法碼表裡的設置語法是：<br>
編碼 $[候選框提示字串]$GO(|cscript$_程式碼目錄/程式碼檔名.副檔名$_參數$_//Nologo)<br>
其中「$_」代表的是一個空白字元。<br>
例如：lotto $[大樂透隨機選號]$GO(|cscript$_script/lotto.vbs$_d$_//Nologo)<br>
代表在小小輸入法裡打「lotto」後，會出現「大樂透隨機選號」的提示，<br>
按空白鍵或對應的選取數字鍵後，<br>
就會背景裡開啟 cscript，去執行 script 目錄（資料夾）下的 lotto.vbs，<br>
使用 d 作為參數，同時在輸出結果裡隱藏 Windows 運行環境的橫幅文字（//Nologo）。<br>
<br>
這些 *.js 或 *.vbs 也可以先暫存在 C:\Temp 下，<br>
然後開啟「命令提示字元」（Win+R 輸入「cmd」，再按確定），<br>
用 cd\temp 指令切換到程式碼所在的目錄，<br>
最後再輸入 cscript lotto.vbs d //nologo 來查看執行結果。<br>
不過，目前在繁體中文版的 Windows 10/11 環境下，<br>
小小輸入法的命令直通車功能尚未支援回傳非 Big5 的字元，<br>
所以儘管在「命令提示字元」環境下，可輸出非 Big5 的字元，<br>
但是經由小小輸入法打出結果時，這些非 Big5 的字元仍會顯示為「?」，<br>
因此，寫好程式碼時，仍需避免產生此種情況（意即：不使用非Big5的字元且儲存為ANSI編碼）。<br>
現在不只 ChatGPT 可以幫忙使用者寫出程式碼，<br>
Copilot、Gemini、Grok 等 AI 也行，大家可以善加利用（Grok似乎較強一些）。<br>
只是AI寫出的程式碼未必一次就能完善，所以需要反覆的測試，並將錯誤訊息回報給AI，<br>
它們會不斷的修正程式碼，使用者只要有足夠的耐心及毅力即可。<br>
<br>
目前「Terry_Yong_AI_Script.zip」裡的程式碼都是筆者利用以上的AI寫出來的，<br>
全部都在 Windows XP/7/8.1/10/11 環境下實際測試過，測試結果皆能正確執行。<br>
有些不需要有輸入界面（如樂透選號），這類程式碼較容易處理，因為只要運算後將結果輸出即可。<br>
有些原本應該要有輸入界面，但是可以透過讀取剪貼簿的內容來處理，<br>
只要使用者先將要處理的字串先剪下或複製，<br>
即可用輸入法編碼（如 lotto 加空白鍵）在背景裡呼叫程式來執行，並將結果輸出到前景。<br>
這個「Terry_Yong_AI_Script.zip」筆者會不定期更新，並將使用方式列於下方。<br>
<br>
1. calculator.vbs<br>
　碼表設置（可自行更改編碼及提示）：<br>
　　.cal $[四則運算(結果)]$GO(|cscript$_script/calculator.vbs$_//Nologo)<br>
　　.cal $[四則運算(算式+結果)]$GO(|cscript$_script/calculator.vbs$_l$_//Nologo)<br>
　用途：<br>
　　對剪貼簿內容進行四則運算，可接受千分位符號、百分比，<br>
　　並接受以下3個進位函數（大小寫可以混合）：<br>
　　ROUND（四捨五入）、ROUNDUP（無條件進位）、ROUNDDOWN（無條件捨去）<br>
　用法舉例：<br>
　　(1)碼表裡不指定 calculator.vbs 的參數（只輸出計算結果）<br>
　　　複製 round(38*1,000,0)-round(38*1,000*0.1425%*37%,0)-round(38*1,000*0.3%,0)-31,070<br>
　　　然後在小小輸入法裡打「.cal」再按空白鍵，就會出現「6,796」<br>
　　　（註：電腦速度較慢的話可能會等超過5秒，正常只需要等3秒左右，以下範例皆相同）<br>
　　(2)碼表裡指定 calculator.vbs 的參數：l（先輸出剪貼簿內容，再輸出 = 計算結果）<br>
　　　剪下 round(38*1,000,0)-round(38*1,000*0.1425%*37%,0)-round(38*1,000*0.3%,0)-31,070<br>
　　　然後在小小輸入法裡打「.cal」再按「2」，會出現：<br>
　　　round(38*1,000,0)-round(38*1,000*0.1425%*37%,0)-round(38*1,000*0.3%,0)-31,070=6,796<br>
<br>
2. convert.vbs<br>
　碼表設置（可自行更改編碼及提示）：<br>
　　.cv $[英文字母→倉頡字母]$GO(|cscript$_script/convert.vbs$_c$_//Nologo)<br>
　　.cv $[英文字母→注音符號]$GO(|cscript$_script/convert.vbs$_p$_//Nologo)<br>
　　.cv $[倉頡或注音→英文(小寫)]$GO(|cscript$_script/convert.vbs$_e1$_//Nologo)<br>
　　.cv $[倉頡或注音→英文(大寫)]$GO(|cscript$_script/convert.vbs$_e2$_//Nologo)<br>
　用途：<br>
　　對剪貼簿內容進行倉頡字母、注音符號、英文字母之間的轉換。<br>
　　(1)參數c：將剪貼簿內容裡的「英文字母」轉換為「倉頡字母」。<br>
　　(2)參數p：將剪貼簿內容裡的「英文字母」轉換為「注音符號」。<br>
　　(3)參數e1：將剪貼簿內容裡的「倉頡字母」或「注音符號」轉換為「小寫英文字母」。<br>
　　(4)參數e2：將剪貼簿內容裡的「倉頡字母」或「注音符號」轉換為「大寫英文字母」。<br>
　用法舉例：<br>
　　參數及說明在此略過！<br>
　　讀者可使用「痞客邦」為範例自行試驗，<br>
　　英文轉倉頡使用「kmfr   jher   qjnl」；倉頡轉英文使用「大一火口   十竹水口   手十弓中」<br>
　　英文轉注音使用「qu3   dk4   1;」；注音轉英文使用「ㄆㄧˇ   ㄎㄜˋ   ㄅㄤ」。<br>
<br>
3. datecalc.vbs<br>
　碼表設置（可自行更改編碼及提示）：<br>
　　date. $[計算日期：日,日→天數]$GO(|cscript$_script/datecalc.vbs$_a1$_//Nologo)<br>
　　date. $[計算日期：日,日→天數(區間在後)]$GO(|cscript$_script/datecalc.vbs$_a2$_//Nologo)<br>
　　date. $[計算日期：日,日→天數(區間在前)]$GO(|cscript$_script/datecalc.vbs$_a3$_//Nologo)<br>
　　date. $[計算日期：日,±天數→日期]$GO(|cscript$_script/datecalc.vbs$_b1$_//Nologo)<br>
　　date. $[計算日期：日,±天數→日期(整句)]$GO(|cscript$_script/datecalc.vbs$_b2$_//Nologo)<br>
　用途：<br>
　(1)對剪貼簿內容計算「yyyy.mm.dd,yyyy.mm.dd」（限定此格式）兩個日期的間隔天數。<br>
　(2)對剪貼簿內容計算「yyyy.mm.dd,±n」（限定此格式）該日期之後（前）n天的日期。<br>
　用法舉例：<br>
　　參數及說明在此略過！<br>
　　讀者可使用「2025.08.28,2025.12.31」、「2025.08.28,100」自行試驗。<br>
<br>
4. dateformat.vbs<br>
　碼表設置（可自行更改編碼及提示）：<br>
　　date, $[日期轉換(西元年月日)]$GO(|cscript$_script/dateformat.vbs$_a$_//Nologo)<br>
　　date, $[日期轉換(中華民國年月日)]$GO(|cscript$_script/dateformat.vbs$_b$_//Nologo)<br>
　　date, $[日期轉換(民國年月日)]$GO(|cscript$_script/dateformat.vbs$_c$_//Nologo)<br>
　用途：<br>
　　將對剪貼簿內容「yyyy.mm.dd」（限定此格式）轉換為西元年月日、中華民國年月日、民國年月日。<br>
　用法舉例：<br>
　　參數及說明在此略過！<br>
　　讀者可使用「8.28」（未指定年份時代表今年）、「2025.08.28」自行試驗。<br>
<br>
5. checkid.vbs<br>
　碼表設置（可自行更改編碼及提示）：<br>
　　.id $[身分證字號驗證]$GO(|cscript$_script/checkid.vbs$_a$_//Nologo)<br>
　　.id $[統一編號驗證]$GO(|cscript$_script/checkid.vbs$_b$_//Nologo)<br>
　用途：<br>
　　將對剪貼簿內容（限定10個字元）驗證其是否為有效的身分證字號或統一編號。<br>
　　（統一編號邏輯檢查採用財政部110年12月22日公布之新規則，即可被5整除）<br>
　用法舉例：<br>
　　參數及說明在此略過！<br>
　　讀者可使用「A123456789」及「87654321」自行試驗。<br>
<br>
6. lotto.vbs<br>
　碼表設置（可自行更改編碼及提示）：<br>
　　lotto $[大樂透隨機選號]$GO(|cscript$_script/lotto.vbs$_d$_//Nologo)<br>
　　lotto $[威力彩隨機選號]$GO(|cscript$_script/lotto.vbs$_w$_//Nologo)<br>
　用途：<br>
　　產生「大樂透」、「威力彩」的隨機選號（每次產生的結果幾乎都是不同的）。<br>
　用法舉例：<br>
　　參數及說明在此略過！<br>
<br>
其他可以創作的題材有文字格式轉換、規則檢核（驗證），或是：<br>
開啟指定網址並後綴股票代號（用來查股票資訊）或特定字元（用來查線上字典）…等，<br>
讀者可以自行摸索或來信交流、討論。<br>
