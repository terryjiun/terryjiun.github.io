---
title: Windows 10 升級新版本後，「Windows.old」資料夾的正確清除方式
date: 2018-05-17 10:10:00 +0800
categories: [作業系統]
tags: [Windows, 實用工具]
---

Windows 10 使用者每年都會被 Microsoft 折騰兩次，<br>
一次是 3 月更新，一次是 9 月更新（只不過微軟通常會拖延一兩個月），<br>
每次更新後重開機，可能要等待半小時至一小時才能進入桌面（視硬體配備而有所不同）。<br>
<br>
每次完成新版本升級後，最困擾的狀況就是作業系統磁碟可用空間縮水了！<br>
因為微軟的設計是保留舊版本，並將它儲存在「<span style="color: blue">Windows.old</span>」資料夾，<br>
目的是讓使用者一旦發現新版本有相容性問題時，可以恢復成舊版本。<br>
<br>
不過，大多數的使用者並不會遭遇相容性的問題，磁碟可用空間變小才是最惱人的！<br>
此時，有些人就會乾脆手動刪除「Windows.old」資料夾，<br>
但是，筆者建議改採另一個方式：透過 Windows 內建的「<span style="color: blue">磁碟清理</span>」來幫 Windows 瘦身。<br>
<br>
以筆者的電腦為例，筆者升級到 v1803 之後，C: 可用空間只剩 9.96GB！

![Free Space](/assets/img/windows/Win10-Disk-Clean-1.png)

查看了一下「Windows.old」資料夾，它不過佔用 6.58GB 的大小。

![Windows.old](/assets/img/windows/Win10-Disk-Clean-2.png)

執行「<span style="color: blue">磁碟清理</span>」的方式很簡單，只要開啟「<span style="color: red">檔案總管</span>」（點選桌面上的「本機」二下即可開啟），<br>
然後點一下 <span style="color: red">C 磁碟代號</span>，再點選上方工具列選單的「<span style="color: red">管理</span>」→「<span style="color: red">清理</span>」圖示，<br>
出現下列畫面後，直接點選「<span style="color: red">清理系統檔</span>」按鈕。

![Disk Clean](/assets/img/windows/Win10-Disk-Clean-3.png)

接著，<span style="color: red">將全部的核取框勾選</span>，再點選「<span style="color: red">確定</span>」按鈕，如下圖：

![Disk Clean](/assets/img/windows/Win10-Disk-Clean-4.png)

系統清理過程會出現詢問視窗，請點選「<span style="color: red">是</span>」按鈕；<br>
完成全部的清理作業後，清理的進度視窗會自動關閉，<br>
但也有可能遇到顯示卡重新整理畫面出現問題，最後停留在「<span style="color: purple">清理 Windows 升級記錄檔</span>」許久，<br>
此時，移動一下滑鼠，該視窗就會自動消失了！<br>
<br>
完成磁碟清理後，筆者的 C: 可用空間回復為 33.5GB，如下圖：

![Free Space](/assets/img/windows/Win10-Disk-Clean-5.png)

回到檔案總管查看，「Windows.old」資料夾已經被澈底刪除了！<br>
磁碟清理程式總共幫筆者清出 33.5GB - 9.96GB = 23.54GB 的空間，<br>
這遠比「Windows.old」資料夾佔用的 6.58GB 多上 3 倍以上！<br>
至於在 C: 根目錄還會留有一個升級後的「<span style="color: blue">$WINRE_BACKUP_PARTITION.MARKER</span>」檔，<br>
就只能靠使用者手動刪除它了！<br>
