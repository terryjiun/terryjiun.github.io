---
title: 支援 CJK Ext-B 字元的「泰瑞倉頡輸入法對照表」（特色說明篇）
date: 2009-04-27 10:12:00 +0800
categories: [輸入法]
tags: [CJK, 倉頡, 碼表]
---

◎下載網址：<br>
　[https://www.mediafire.com/file/cwicp98a065lxda/THCJ5.zip](https://www.mediafire.com/file/cwicp98a065lxda/THCJ5.zip){:target="_blank"}<br>
<br>
◎官方網址：<br>
　[https://terryjiun.github.io](https://terryjiun.github.io){:target="_blank"}<br>
<br>
◎特色說明：<br>
　1.支援下列 Unicode Block 的漢字：<br>
　　(1)CJK Unified Ideographs（中日韓統一表意文字，本區收錄 20,902 個漢字）<br>
　　(2)CJK Unified Ideographs Extension A（中日韓統一表意文字擴充A，本區收錄 6,582 個漢字）<br>
　　(3)CJK Unified Ideographs Extension B（中日韓統一表意文字擴充B，本區收錄 42,711 個漢字）<br>
　2.此輸入法對照表已為三區合計 70,195 個漢字的每個字編列「組字字根：詞組」對照。<br>
　3.此輸入法對照表支援符號輸入，組字字根最多 5 鍵（不含空白鍵）。<br>
　4.此輸入法對照表支援「倉頡第三代」及「倉頡第五代」拆碼原則。<br>
　　因教育部較晚制定標準字體及其他原因，不可能每個字都符合「理論上」應有的拆碼原則，<br>
　　如「今」字的標準字體，「人」下方應為「一」而非「丶」，但大多數倉頡使用者已習慣拆為「人戈弓」；<br>
　　雖然此輸入法亦支援「人一弓」這條組字字根，<br>
　　但由於字型及書寫習慣的關係，無法確保每個字都能按照您的認知來正確拆碼。<br>
　　朱邦復先生制定的原則也未必是最好的，否則就不會不斷的改良<br>
　　（如「┐」究竟應為「中」或「弓」的輔根，就一再的修改），<br>
　　所以此輸入法對照表只是儘可能滿足不同的拆碼原則。<br>
　5.您可能需要安裝（或更新）系統字型以顯示擴充A、B區的漢字：<br>
　　(1)Windows Vista、Server 2008 或更新的 Windows：不需要安裝或更新字型。<br>
　　(2)Windows XP、Server 2003：請安裝「新細明體字型更新套件」，安裝後可再更新為「Vista 新細明體字型」。<br>
　　　 （安裝方式請上官方網站查看）<br>
<br>
◎特別注意：<br>
　因為「通用輸入法編輯工具」有 Bug，組字字根以「/」開頭時，必須再於組字字根之前加一個「/」，<br>
　所以輸入「？」時，雖是鍵入「/」加空白鍵，但在對照表裡，看到的會是「// ？」。<br>
　「Yahoo! 奇摩輸入法」目前的版本不支援擴充B區的漢字，<br>
　如有擴充B區漢字的需求，請改用「通用輸入法編輯工具」或「OpenVanilla 香草輸入法」。<br>
<br>
◎安裝方式：<br>
　1.將「THCJA.txt」（「組字字根 V.S. 詞組」對照表）複製到「C:&#92;」，<br>
　　（如果複製到有中文路徑的資料夾下，<br>
　　等會兒使用「通用輸入法編輯工具」匯入時，會產生錯誤）。<br>
　2.如果是 Windows XP、Server 2003 的使用者，<br>
　　請執行「程式集→附屬應用程式→通用輸入法編輯工具」。<br>
　3.如果是 Windows Vista、Server 2008 的使用者，<br>
　　因為 Windows 並無內建「通用輸入法編輯工具」，<br>
　　請下載：[https://www.mediafire.com/file/8ve8veq1wfe87bq/WinXP_IME.zip](https://www.mediafire.com/file/8ve8veq1wfe87bq/WinXP_IME.zip){:target="_blank"}<br>
　　解壓縮後，將「miniime.tpl」、「Uimetool.exe」、「uniime.dll」<br>
　　複製到「C:&#92;Windows&#92;System32」，並執行「Uimetool.exe」，<br>
　　這時「通用輸入法編輯工具」即可正常執行。<br>
　4.在「通用輸入法建立精靈」視窗中，<br>
　　只有四個地方要作設定：<br>
　　(1)輸入法名稱：請填入「泰倉」。<br>
　　(2)產生 .IME 檔的英文檔名：請填入「THCJA」。<br>
　　(3)對照表檔案：請以瀏覽檔案的方式帶入步驟 1 的「C:&#92;THCJA.txt」。<br>
　　(4)最大組字字根數目：請調成「5」。<br>
　5.上一步驟按「完成」按鈕後，<br>
　　會在「C:&#92;Windows&#92;System32」之下產生四個檔名以「THCJA」開頭的檔案，<br>
　　之後即可使用下列方式新增／移除這套輸入法：<br>
　　【控制台→地區及語言選項→「語言」頁籤→「詳細資料」按鈕】，<br>
　　叫出「文字服務及輸入語言」視窗，<br>
　　並在它的「設定」頁籤下新增或移除「泰倉」。<br>
<br>
◎對照表編輯方式：<br>
　1.可使用文書編輯軟體（建議使用 EditPlus 或 Notepad2，字型設為新細明體）開啟。<br>
　2.txt 格式的對照檔，最前面以「/S」開頭的那幾列，作用為宣告輸入法可用的按鍵，<br>
　　例如：「/S A日」，代表宣告「A」成為可用的按鍵，<br>
　　按下「A」時，會出現「日」，但不會直接出字，<br>
　　需按下「空白鍵」後，輸入法才會去找對應的「組字字根 V.S. 詞組」。<br>
　3.「組字字根 V.S. 詞組」：<br>
　　「組字字根」限用「半型」英數字，最多 5 個；<br>
　　「詞組」可以是英數字、中文字或混合，字數不限<br>
　　（字數不要太多，不然會超出候選字窗格的寬度）<br>
　　「組字字根」和「詞組」中間要留一個「空格」，<br>
　　一列只能定義一個詞組。<br>
　4.排越前面的詞組，會成為輸入法裡越前面的候選字。<br>
<br>
◎擴充方式：<br>
　編輯「THCJA.txt」後存檔，<br>
　再按照上述安裝步驟 5 的方式先移除「泰倉」輸入法，<br>
　然後重新開機（不這麼做的話，可能無法更新那四個檔名以「THCJA」開頭的檔案），<br>
　最後重新執行上述安裝步驟 4、5，即可完成改造這套輸入法的程序。<br>
<br>
◎符號輸入方式：<br>
　★參見：https://terryhung.pixnet.net/blog/post/25102388<br>
<br>
◎改版建議：<br>
　★此輸入法對照表製作過程請參考：https://terryhung.pixnet.net/blog/post/24862369<br>
　★此輸入法對照表建議修改的部分請參考：https://terryhung.pixnet.net/blog/post/24828383<br>
<br>
◎檔案說明：<br>
　THCJ3.txt：對照表完整版 for「通用輸入法編輯工具」（只包含第三代倉頡拆碼方式）<br>
　THCJ5.txt：對照表完整版 for「通用輸入法編輯工具」（只包含第五代倉頡拆碼方式）<br>
　THCJC.txt：對照表完整版 for「通用輸入法編輯工具」（包含第三代及第五代倉頡拆碼方式）<br>
　THCJA.cin：對照表完整版 for「Yahoo! 奇摩輸入法」、「OpenVanilla 香草輸入法」（包含第三代及第五代倉頡拆碼方式，且經過調整）<br>
　THCJA.txt：對照表完整版 for「通用輸入法編輯工具」（包含第三代及第五代倉頡拆碼方式，且經過調整）<br>
　THCJA-Lite.cin：對照表精簡版 for「Yahoo! 奇摩輸入法」、「OpenVanilla 香草輸入法」（只支援 CJK 的 20,902 個字元）<br>
　THCJA-Lite.txt：對照表精簡版 for「通用輸入法編輯工具」（只支援 CJK 的 20,902 個字元）<br>
　註：安裝「Yahoo! 奇摩輸入法」後，請直接開啟您想要匯入的 cin 檔，即可看到詢問您是否要安裝的畫面。<br>
　　　匯入後，可至「Yahoo! 奇摩輸入法」設定畫面的「泛用」項下進行相關設定。<br>
　　　安裝「OpenVanilla」後，請直接將您想要使用的 cin 檔複製到「C:&#92;OpenVanilla&#92;Modules&#92;OVIMGeneric」，<br>
　　　切換輸入法至「OpenVanilla」後，即可點選該 cin 檔的輸入法來使用。<br>
