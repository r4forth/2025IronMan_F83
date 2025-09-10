# DosBOX 專案介紹

## 專案概述

![](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e2/DOSBox_screenshot.png/330px-DOSBox_screenshot.png)

* DOSBox 是一款開源的 x86 模擬器，內建 BIOS 與 DOS-like shell，可讓現代作業系統執行舊 DOS 程式與遊戲。
* 最初版本於 2002 年發佈，由 Peter "Qbix" Veenstra 與 Sjoerd "Harekiet" van der Berg 共同開發

## 跨平台支援與技術架構

* 程式以 C/C++ 編寫，透過 SDL（Simple DirectMedia Layer） 處理圖形、音效與輸入輸出。

* 支援平台包括 Windows、macOS、Linux、FreeBSD、OS/2、RISC OS、BeOS、AmigaOS、Solaris 等。

## 主要的模擬與功能

* 模擬 CPU（支持實模式與保護模式）
* 顯示系統（CGA、EGA、VGA、VESA、S3 Trio 等）
* 音效卡（如 AdLib、Sound Blaster、Gravis Ultrasound 等）
* 支援模擬網路（IPX/TCP/IP）、模擬光碟機、存取序列埠與對遊戲手把支援

## 應用情境與影響力

* 被廣泛用於執行懷舊遊戲
* Internet Archive 使用 Emscripten 版 DOSBox 在瀏覽器上展示老遊戲，作為數位典藏用途。


## DOSBox-X 專案，加強版的 DOSBox

1. 專案定位與目標

DOSBox-X 是從 DOSBox 分支出來的開源 DOS 模擬器，目標是成為 “完整且精準” 的 DOS+Windows 3.x/9x/Me 模擬平台，支援各種 DOS 及早期 Windows 應用與遊戲執行環境。

旨在涵蓋 2000 年前所有主流 DOS/Windows 平台情境，包括周邊設備、主機板、處理器等完整模擬；也是歷史保存與新 DOS 軟體開發的理想環境。

2. 多平台支援與精確 emulation

* 支援模擬 DOS/V 和日本 NEC PC-98 平台，適合執行不同地區語系遊戲與應用。
* 模擬 Windows 3.x、9x、Me，包括完整加速效果，甚至可開機進入這些環境。

3. 使用者介面與操作便利性

* 擁有 GUI 下拉選單系統，可透過 GUI 操作設定而非僅文字指令。
* 內建圖形化設定工具，可直接在介面上修改設定。
* 支援即時「Save & Load State」（遊戲存檔機制），方便實境測試與恢復。


我們本次的教學都會以 DOSBox-X 為主要的模擬環境。

