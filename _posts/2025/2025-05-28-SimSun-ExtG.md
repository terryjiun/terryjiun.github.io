---
title: Windows 10/11 內建的字型已經支援 CJK Ext-E/F/G/H/I 字元集了！
date: 2025-05-28 10:10:00 +0800
categories: [字碼與字型]
tags: [字型, CJK]
---

筆者之前曾經發布過《Windows 8 內建的新細明體已經支援 CJK Ext-C/D 字元集了！》一文，<br>
當時 Windows 8 內建的新細明體僅支援到 CJK Ext-D 的字元，而就連後來初上市的 Windows 10 也是如此。<br>
但是近日筆者發現在未額外安裝字型的 Windows 10、Windows 11 環境下，<br>
瀏覽《倉頡之友．九萬漢字》的網頁時，也能正確顯示 Ext-H 的字元，<br>
後來稍微研究了一下，才知道原因出在「SimsunExtG.ttf」這套字型上。<br>
<br>
SimsunExtG.ttf 在「維基百科」對應的條目是「中易宋體」，該條目有提到：<br>
「<br>
目前最新版是 Windows 11 的 5.07 版本，已實現對擴充 B—F 區的完整支援。<br>
2024 年又另外組態了該字型的擴充字型「擴充G」，英文稱為 SimSun-ExtG，檔案名 SimSunExtG.ttf，<br>
支援擴充 G、H 和 I 區共計 9,753 個字元，<br>
於 2025 年 1 月起隨預覽版更新向 Windows 10 和 Windows 11 使用者全量推播。<br>
」<br>
所以，只要透過 Windows Update 將 Windows 10/11 更新到 2025 年 2 月以後的狀態，<br>
就會一併更新相關的字型。<br>
<br>
雖然，目前還沒有「新細明體-ExtG」的擴充字型，<br>
但是因為 Windows 會利用登錄檔來調用其他字型，<br>
所以在很多應用程式下，只要有 SimSunExtG.ttf 可供借助，都能順利顯示 CJK Ext-A～Ext-I 的字元。<br>
而在 Word、Excel 中，也能手動選擇「SimSun-ExtG」來顯示出正確的漢字。<br>
<br>
Ext-A 屬於基本多文種平面，對應的字型是 mingliu.ttc(新細明體)、simsun.ttc(SimSun)；<br>
Ext-B/C/D/E/F 屬於第二輔助平面，對應的字型是 mingliub.ttc(新細明體-ExtB)、simsunb.ttf(SimSun-ExtB)；<br>
Ext-G/H 屬於第三輔助平面、Ext-I 屬於第二輔助平面，對應的字型是 SimsunExtG.ttf(SimSun-ExtG)。<br>
