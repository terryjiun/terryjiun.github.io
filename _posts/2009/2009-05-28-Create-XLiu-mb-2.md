---
title: 偽蝦米參考檔合法製作（二）
date: 2009-05-28 10:20:00 +0800
categories: [輸入法]
tags: [無蝦米, 偽蝦米]
---

本文要製作給「[偽‧蝦米](https://vmliu.xyz/xliu/){:target="_blank"}」使用的「參考檔」（以下簡稱「偽參考檔」）<br>
並不是由[行易有限公司](https://boshiamy.com/){:target="_blank"}發行的參考檔（以下簡稱「行易參考檔」）！<br>
<br>
有鑑於上一篇所採用的「偽參考檔」和「加字加詞檔」有太多的缺點，<br>
所以我建議各位重新製作新的「偽參考檔」和「加字加詞檔」。<br>
<br>
製作方向說明如下：<br>
<br>
1.<span style="color: red">Liu-AB.box：加字加詞檔</span>。<br>
　<span style="color: green">包含「中日韓統一表意文字擴充A區」（CJK Ext-A，6,582 個漢字）<br>
　和「中日韓統一表意文字擴充B區」（CJK Ext-B，42,711 個漢字），<br>
　並確保沒有一個字被遺漏！</span><br>
　（[蝦米族樂園](https://vmliu.xyz/){:target="_blank"}提供的「liubox-20090405-01.zip」，<br>
　少了 CJK Ext-A 的 674 個字，也少了 CJK Ext-B 的 2 個字，必須將其全部補齊）<br>
　考量到使用 CJK Ext-A/B 字元的機會並不多，<br>
　並且為使 CJK Ext-A/B 的字元不會加劇重碼字的問題，<br>
　所以延用蝦米族樂園的方式──<br>
　<span style="color: purple">CJK Ext-A/B 字元的組字字根為嘸蝦米碼末尾加上「;」，因此最大碼長變為 5 碼。</span><br>
　如果您使用的 Windows 不是 Vista 及其以後的版本，<br>
　或雖然是 Windows XP/Server 2003，但沒有安裝「新細明體更新套件」，<br>
　那麼您的系統字型將無法顯示 CJK Ext-A/B 合計的 49,293 個漢字，<br>
　此時您可以將「Liu-AB.box」放著不管。<br>
<br>
2.<span style="color: red">liu-uni2.tab：參考檔</span>。<br>
　<span style="color: green">「中日韓統一表意文字」（CJK，20,902 個漢字）扣除<br>
　「ANSI -繁體中文」（Big5）可顯示的 13,070 個漢字之後，所剩下的 7,832 個漢字，<br>
　再加上 32 個 CJK 相容字元。</span><br>
　（此 32 字為：<br>
　朗、隆、﨎、﨏、塚、﨑、晴、﨓、﨔、猪、益、礼、神、祥、福、靖、<br>
　精、羽、﨟、﨡、諸、﨣、﨤、逸、都、﨧、﨨、﨩、飯、飼、館、鶴）。<br>
　簡體字、「煊」、「堃」……等字都在這個參考檔裡。<br>
　<span style="color: purple">使用時需將「偽‧蝦米」的狀態由「無半」（切換鍵：「,,t」加空白鍵）<br>
　切換為「中半」（切換鍵：「,,c」加空白鍵）。</span><br>
　註：本來應該將所有 CJK 的 20,902 個漢字放在同一個參考檔裡，以方便蝦米族使用。<br>
　　　但因為 20,902 個漢字加上 vrsf 選字、簡碼、容錯碼、符號後，<br>
　　　一定會超過 33,000 行，這樣轉出的「liu-uni.tab」將無法被「偽‧蝦米」接受，<br>
　　　所以由「liu-uni.tab」分出這個檔來！<br>
<br>
3.<span style="color: red">liu-uni2.txt：「liu-uni2.tab」轉換前的純文字檔</span>，保留下來以便日後再作修改。<br>
<br>
4.<span style="color: red">liu-uni.tab：參考檔</span>。<br>
　<span style="color: green">包含「ANSI -繁體中文」（Big5）可顯示的 13,070 個漢字。</span><br>
　（詳見《[Big5 碼重複收錄的字與可用的字數](https://terryjiun.github.io/posts/Big5-Usable-Count/){:target="_blank"}》一文）。<br>
<br>
5.<span style="color: red">liu-uni.txt：「liu-uni.tab」轉換前的純文字檔</span>，保留下來以便日後再作修改。<br>
<br>
6.<span style="color: red">txt2uni.exe：將純文字檔轉換為參考檔的工具</span>。<br>
　檔案來源及使用說明請參考上一篇。<br>
<br>
7.<span style="color: red">Liu.box：加字加詞檔</span>。<br>
　<span style="color: green">為「liu-uni2.txt」的複製版本。</span><br>
　基於下列 3 項因素，<br>
　可將「預設的加字加詞檔」（Liu.box）的內容改為「liu-uni2.txt」的內容：<br>
　(1)Windows 的系統字型必須支援 CJK Ext-A/B 的字元，才能使用「Liu-AB.box」；<br>
　(2)一般人較少使用 CJK Ext-A/B 的字元，反而較常使用 Big5 以外的 CJK 字元，<br>
　　 如果每次要輸入這些字元時還要切換到「中半」模式會過於麻煩；<br>
　(3)「Liu-AB.box」的檔案 Size 過大，會使「偽‧蝦米」開啟時間變長。<br>
　不會用到 CJK Ext-A/B 字元的人可以維持原狀，<br>
　會用到的人，可以選擇以下三種方式中的任一種：<br>
　(1)將「Liu.box」刪除，再將「Liu-AB.box」更名為「Liu.box」；<br>
　(2)將「Liu-AB.box」的內容併入到「Liu.box」<br>
　　 （但這樣做，會使得「偽‧蝦米」開啟時間變得更長）。<br>
　(3)要使用 CJK Ext-A/B 字元前，先將「Liu.box」更名為「Liu2.box」；<br>
　　 再將「Liu-AB.box」更名為「Liu.box」；<br>
　　 用完後再改回原狀。<br>
<br>
上一篇所採用的「偽參考檔」和「加字加詞檔」的缺點，<br>
在這個新做的「偽參考檔」和「加字加詞檔」裡有了一些變化：<br>
1.降低遇到重碼字的機率：<br>
　因為在預設情況下，不使用 CJK Ext-A/B 的字元，<br>
　使用的字數變少，遇到重碼字的機會自然也會變少。<br>
2.有同音字的功能：<br>
　但是僅限於「無半」模式使用的「liu-uni.tab」裡的字。<br>
　除非切換到「中半」模式去使用「liu-uni2.tab」，<br>
　否則同音字功能只支援「ANSI -繁體中文」（Big5）可顯示的 13,070 個漢字。<br>
3.有萬用碼的功能：<br>
　情況同上。<br>
4.建議加入「vrsf 選字」的功能。<br>
<br>
但是<span style="color: purple">「重碼字排序方式和行易參考檔不一樣」的缺點仍然存在。<br>
如果您介意這個缺點，可自行編輯以上的純文字檔<br>
（行易參考檔的重碼字排序可參考此篇「[嘸蝦米重碼表](https://www.geocities.ws/mycj3/doc/liu55dup.PDF){:target="_blank"}」），<br>
再用「txt2uni.exe」轉換為新的參考檔。<br>
不過需要注意的是：不要破壞組字字根的排列方式，<br>
否則轉出的參考檔將無法被「偽‧蝦米」接受。</span><br>
<br>
另外，可將「♩、♪、♫、♬、♭、♮、♯」這 7 個符號，<br>
對應到「,son」這個字根，方便有這些符號需求的人使用。<br>
