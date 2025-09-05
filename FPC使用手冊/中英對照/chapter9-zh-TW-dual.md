CHAPTER 9. ADVANCED UTILITIES
第 9 章。先進的實用程序




9.1. REBUILDING THE SYSTEM
9.1.重建系統


If you need to change a parameter or function in the F-PC system, you
如果您需要更改 F-PC 系統中的參數或功能，您可以
will need to re-compile F- PC and/or KERNEL. This is simply done with
將需要重新編譯 F-PC 和/或 KERNEL。這只需使用
the provided batch files as follows:
提供的批次檔案如下：


C> FMETA <enter> Re-compiles KERNEL.COM
C> FMETA <enter> 重新編譯 KERNEL.COM
C> EXTEND <enter> Re-extends to create F-PC.EXE
C> EXTEND <enter> 重新延伸以建立 F-PC.EXE


Either of these may be performed from the keyboard while in DOS. FMETA
在 DOS 中，這些操作都可以從鍵盤執行。菲美塔
invokes F-PC, loads the meta compiler, and recompiles the kernel. The
調用 F-PC，加載元編譯器，然後重新編譯內核。這
resulting new kernel is stored back as KERNEL.COM. Utilities and
產生的新核心會儲存回 KERNEL.COM。公用程式和
applications are then compiled on the top of KERNEL by EXTEND to generate
然後，應用程式會由 EXTEND 在 KERNEL 的頂端編譯，以產生
a new F-PC system.
一個新的 F-PC 系統。


To extend the F-PC system with your application, edit the F-PC.SEQ file
若要使用應用程式擴充 F-PC 系統，請編輯 F-PC。SEQ 檔案
to include FLOAD instructions to load your application files. You may
以包含載入應用程式檔案的 FLOAD 指令。你可以
want to change the name of the EXE file finally saved. This can be done
想要更改最終保存的 EXE 文件的名稱。這是可以做到的
by editing the filename after the SAVE-EXE statement in F- PC.SEQ file.
通過在 F-PC 中編輯 SAVE-EXE 語句後的文件名。SEQ 檔案。


Meta compilation the the darkest art in Forth. Do not be fooled by the
元彙編 福斯最黑暗的藝術。不要被
above simple discussions to think that meta compilation can be practiced
以上簡單的討論認為元編譯可以實踐
easily. You have to understand F-PC completely to made modifications in
輕鬆。您必須完全了解 F-PC 才能進行修改
the kernel files to rebuild a Forth to your own liking. Only Tom Zimmer
內核文件以根據您自己的喜好重建 Forth。只有湯姆·季默
is entrusted to make modification to F-PC. Nevertheless, you have all
受委託對 F-PC 進行修改。儘管如此，你擁有一切
the source code and the tools to roll your own Forth in F-PC.
在 F-PC 中滾動您自己的 Forth 的源代碼和工具。


9.2. TURNKEY SYSTEMS
9.2.交鑰匙系統


The word TURNKEY and some associated words are included in the file
檔案中包含 TURNKEY 一詞和一些相關單字
SAVESYS.SEQ. TURNKEY is used as follows:
SAVESYS.SEQ. TURNKEY 的用途如下：


' MYAPPL IS DEFAULT TURNKEY MYAPP <enter>
' MYAPPL 是默認的統包 MYAPP <enter>


After completing an application compile, the word MYAPPL is defined to be
完成應用程式編譯之後，單字 MYAPPL 會定義為
performed by the program name MYAPP.COM. TUNRKEY automatically sets up
由程式名稱執行 MYAPP.COM。TUNRKEY 自動設定
the proper memory management to allocate 64k for your program, but does
適當的記憶體管理為您的程式分配 64k，但確實如此
not save the heads. Minimum initialization is performed. A file
不救頭。執行最少初始化。一個檔案
specified on the command line will be opened, and you can use BL WORD to
命令列上指定的會開啟，可以使用 BL WORD 來
pick up additional parameters from the command line. You will of course
從命令列挑選其他參數。你當然會的
not be able to interpret, since heads are not saved, and your application
無法解釋，因為頭部未保存，並且您的應用程序
will need to handle all errors and return to DOS when the program
將需要處理所有錯誤，並在程式
completes.
完成。


Before attempting to build an application, you will need to make a copy
在嘗試構建應用程序之前，您需要製作一個副本
of F-PC.SEQ, for customization. Many of the later files in F-PC.SEQ are
F-PC 的。SEQ，用於客製化。F-PC 中的許多後來的文件。序列是
utilities, and will not be needed in your application. Start by writing
公用程式，而且您的應用程式中不需要。從寫作開始
your program and compiling it on F-PC.EXE. Work in this environment
您的程式並在 F-PC.EXE 上編譯它。在這種環境中工作
until you are sure your program works. Now insert your program filename
直到您確定您的程序有效為止。現在插入您的程序文件名
into the copy of F-PC.SEQ you made, about half way down, and try to
進入 F-PC 的副本。你做的 SEQ，大約在一半處，並嘗試
compile the copy of F-PC.SEQ. If it compiles then you can move your
編譯 F-PC.SEQ 的副本。如果它編譯，那麼您可以移動
application file lower, until you have determined what utilities are
應用程式檔案較低，直到您確定公用程式是什麼
needed by your application. Strip out all files above your application
您的應用程式需要。刪除應用程式上方的所有檔案
file, and load the file SAVESYS.SEQ. Use TURNKEY as previously described
檔案，並載入檔案 SAVESYS.SEQ。如先前所述，使用 TURNKEY
to make an executable .EXE file.
製作可執行的.EXE 檔。


TURNKEY allow you to customize F-PC to build an independent application,
TURNKEY 允許您自定義 F-PC 以構建獨立的應用程序，
which may not allow the user to see the internal of the application. If
這可能不允許用戶看到應用程序的內部。如果
you are not so protective, a more convenient way to generate an
你沒有那麼保護，這是一種更方便的方式來生成
application is to use FSAVE, which saves the core image of F-PC after you
應用是使用 FSAVE，在你之後保存 F-PC 的核心映像
have loaded your application. F-PC is included inside your application
已載入您的應用程式。F-PC 包含在您的應用程序中
and the user have access to the entire system. This is a useful tool as
並且用戶可以訪問整個系統。這是一個有用的工具，因為
you can make a snapshot of your current system, save it to the disk, and
您可以製作當前系統的快照，將其保存到磁盤，然後
have it available the next time you resume your work. The commands are:
下次恢復工作時可以使用它。命令包括：


FSAVE MYSYSTEM <return>
FSAVE 我的系統<return>


A file MYSYSTEM.EXE is saved in your current directory which contains
檔案 MYSYSTEM.EXE 儲存在目前目錄中，其中包含
everything you compiled so far. Next time when you execute MYSYSTEM
到目前為止，您彙編的所有內容。下次執行 MYSYSTEM 時
under DOS, your current system will be loaded and F-PC will be at your
在 DOS 下，您當前的系統將被加載，並且 F-PC 將在您的
service.
服務。


9.3. MACROS IN F-PC AND SED
9.3. F-PC 和 SED 中的巨集


A file called MACROS.SEQ is provided,. This file implements keyboard
一個名為 MACROS 的檔案。提供了 SEQ，。此檔案實作鍵盤
macros in Forth at the level of KEY. These macros can therefore be used
KEY 層級的 Forth 中的巨集。因此，可以使用這些巨集
in the editor also. The macros are used as follows: (the sequence
在編輯器中也是如此。巨集的使用方式如下： （序列
"Alt-M" means hold down the "Alternate" key and press the "M" key.)
“Alt-M”表示按住“備用”鍵並按“M”鍵。


Alt-M Start defining a macro.
Alt-M 開始定義巨集。
Alt-1 We are defining the Alt-1 macro.
Alt-1 我們正在定義 Alt-1 巨集。


Enter any keys you want in the macro, up to 128 keys.
在巨集中輸入您想要的任何鍵，最多 128 個鍵。


Alt-M Complete the definition of the Alt-1 macro.
Alt-M 完成 Alt-1 巨集的定義。


Any keys available on the keyboard except Alt-m, and Alt-1 to Alt-5 can
鍵盤上除 Alt-m 和 Alt-1 到 Alt-5 之外的任何可用鍵都可以
be included within a macro. To execute a macro, simply type its key
包含在巨集中。若要執行巨集，只需鍵入其鍵即可
name:
名字：


Alt-1 Execute the macro key sequence for the Alt-1 key.
Alt-1 執行 Alt-1 鍵的巨集鍵序列。


Currently macros may be only 127 characters in length, although this can
目前巨集的長度可能只有 127 個字元，但這可以
be changed by modifying the constant MAXMAC and recompiling the system.
透過修改常數 MAXMAC 並重新編譯系統來變更。
See the example in Appendix B-3.
請參閱附錄 B-3 中的範例。


9.4. F-PC PREFERENCES
9.4. F-PC 首選項


While F-PC may seem like a nebulous glob of stuff, some things about it
雖然 F-PC 可能看起來像是一堆模糊的東西，但關於它的一些事情
can be adjusted fairly simply. The install process, for example, allows
可以相當簡單地調整。例如，安裝程序允許
you to tell F-PC where its source file will be located, whether you want
您可以告訴 F-PC 其源文件的位置，無論您是否願意
to have backup copies made of your edited files, and what you want to
將編輯的檔案以及您想要的內容製作備份副本
call your installed version of F-PC. There are however a number of other
呼叫您安裝的 F-PC 版本。然而，還有許多其他的
things you might like to adjust to your personal way of doing things.
您可能想根據您個人的做事方式進行調整。
Here is a list:
這是一個列表：


The status line display may be turned on/off.
狀態行顯示可以開啟/關閉。


STATON Enable status line display at top of screen.
STATON 在螢幕頂部啟用狀態行顯示。
STATOFF Disable status line display.
STATOFF 停用狀態行顯示。


The decompile display during debugging may be turned on/off.
偵錯期間的反編譯顯示可能會開啟/關閉。


SRCON Source display enabled during debug.
在除錯期間啟用 SRCON 來源顯示。
SRCOFF Source display disabled during debug.
SRCOFF 來源顯示在除錯期間已停用。


The default file extension for the system and the file specification
系統的預設副檔名和檔案規格
string for the popup window file selector may be changed.
字串可能會變更快顯視窗檔案選取器。


DEFEXT Default file extension string.
DEFEXT 預設副檔名字串。
HIDDEN DIRSPEC$ Directory specification for popup window.
HIDDEN DIRSPEC$ 快顯視窗的目錄規格。


The format of date printing can be adjusted to one of the three supported
日期列印的格式可以調整為三種支援的格式之一
formats, or you can add your own.
格式，或者您可以添加自己的格式。


M/D/Y Month/Day/Year (default format)
M/D/Y 月/日/年（預設格式）
Y-M-D Year-Month-Day
Y-M-D 年月日
D.M.Y Day.Month.Year
D.M.Y 日.月.年


You can manually turn editor backups on or off without going through the
您可以手動開啟或關閉編輯器備份，而無需經過
install process.
安裝程序。


BACKUPOFF Disables the editor from making backup files.
BACKUPOFF 停用編輯器建立備份檔案。
BACKUPON Enables the keeping of editor backup files.
BACKUPON 啟用保留編輯器備份檔案。


F-PC will automatically save any changes you made to a file you are
F-PC 將自動保存您對文件所做的任何更改
editing, if you stop touching the keyboard for 10 minutes.
編輯，如果您停止觸摸鍵盤 10 分鐘。


AUTOSAVEON Turn on auto save.
自動儲存開啟自動儲存。
AUTOSAVEOFF Stop auto save.
自動儲存 停止自動儲存。
AUTOSAVE-MINUTES Value of minutes to wait before saving.
AUTOSAVE-MINUTES 儲存前要等待的分鐘數值。
Default is 10.
預設值為 10。


Screen display output can be switched between DOS and Direct Video output
螢幕顯示輸出可在 DOS 和直接視訊輸出之間切換
for all screen text display.
用於所有螢幕文字顯示。


FAST Direct video screen write for all displayed text.
FAST Direct 視頻屏幕寫入所有顯示的文本。
SLOW Use DOS for all screen display.
慢速 將 DOS 用於所有螢幕顯示。


F-PC defaults to automatically entering the editor when an error is
F-PC 預設在錯誤時自動進入編輯器
encountered during a file load. You can control this with the following
在檔案載入期間遇到。您可以使用以下方式控制這一點
words.
言。


AUTOEDITON Automatically enter editor on load error.
AUTOEDITON 載入錯誤時自動進入編輯器。
AUTOEDITOFF Don't enter editor on load error.
AUTOEDITOFF 載入錯誤時不要進入編輯器。


When an error occurs, the base for number conversions will be change back
發生錯誤時，數字轉換的基數將改回
to DECIMAL. This feature can be turn off so that the base is not affect
到 DECIMAL。可以關閉此功能，以免影響底座
by errors.
通過錯誤。


DECIMALBASE Change to DECIMAL after an error.
DECIMALBASE 錯誤後變更為 DECIMAL。
HEXBASE Change to HEX after an error.
HEXBASE 發生錯誤後變更為 HEX。
NOBASE Do not change base on error.
NOBASE 不要根據錯誤變更基礎。
DEFBASE A value to restore base. 0 for NOBASE, 10 for
DEFBASE 要還原基礎的值。0 代表 NOBASE，10 代表
DECIMAL and 16 for HEXBASE. User can choose his
DECIMAL 和 HEXBASE 為 16。用戶可以選擇他的
default base here.
這裡的預設基礎。


If you are using a CGA (Color Graphics Adapter) type of video display
如果您使用的是 CGA（彩色圖形轉接器）類型的視訊顯示器
board, you will probably want to use BLANKON to reduce the amount of snow
板上，您可能會想使用 BLANKON 來減少積雪量
or sparkle on your screen. This word causes the screen to be blanked
或在您的屏幕上閃閃發光。這個字會導致螢幕空白
while text is being written to the display to reduce this effect. These
同時將文字寫入顯示器以減少這種影響。這些
words have no effect on monochrome display adapters. Use BLANKOFF for an
文字對單色顯示適配器沒有影響。將 BLANKOFF 用於
EGA or VGA adapter.
EGA 或 VGA 轉接器。


BLANKON Enable screen blanking during text output.
BLANKON 在文字輸出期間啟用螢幕空白。
BLANKOFF Disable screen blanking during text output.
BLANKOFF 在文字輸出期間停用螢幕空白。


Most green or amber monochrome monitors display light characters on a
大多數綠色或琥珀色單色顯示器在
dark background. If you have a color monitor or true white on black
深色背景。如果您有彩色顯示器或黑底純白
monitor you may want to reverse foreground and background, giving a page
監視您可能想要反轉前景和背景，給出一個頁面
white look with dark characters on a white background. I have found this
白色外觀，白色背景上帶有深色字符。我發現了這個
to be more comfortable for my own use. You might also try the
為了更舒適地使用我自己。您也可以嘗試
BLACK-ON-WHITE mode with an Liquid Crystal or Florescent display.
帶有液晶或熒光顯示器的黑底白模式。


WHITE-ON-BLACK Normal, light chars on dark background.
WHITE-ON-BLACK 深色背景上的正常、淺色字符。
BLACK-ON-WHITE Invert the screen to dark on light.
白底黑字 將螢幕反轉為淺色。


With a color monitor, F-PC can display different classes of words in
透過彩色顯示器，F-PC 可以顯示不同類別的單字
different color. It is a very interesting demonstration to impress
不同的顏色。這是一個非常有趣的演示，可以給人留下深刻的印象
novice programmers when executing WORDS, SEE, or DBG. It is probably not
新手程式設計師在執行 WORDS、SEE 或 DBG 時。可能不是
very useful in normal programming because you cannot see very well words
在正常編程中非常有用，因為你看不清單詞
in blue and light grey.
藍色和淺灰色。


COLORIZEON Turn on colors in word list.
COLORIZEON 打開單詞列表中的顏色。
COLORIZOFF Go back to work
COLORIZOFF 回去工作


The number of screen F-PC will save on its screen stack if adjustable
如果可調整，F-PC 的屏幕數量將保存在其屏幕堆棧中
within the range 1 to 14. SVSIZE bytes (~4000) are allocated for each
在 1 到 14 的範圍內。SVSIZE 位元組 （~4000） 會為每個
screen stacked. F-PC needs SVMAX to be at least three (3) for all of the
屏幕堆疊。F-PC 需要 SVMAX 至少為三 （3） 個
existing utilities to function properly.
現有公用事業正常運作。


SVMAX is a "VALUE" that can be changed with "=:". You will only need to
SVMAX 是一個“VALUE”，可以用“=：”來更改。您只需要
do this if you write a program that needs to stack screens more than the
如果您編寫的程式需要堆疊螢幕超過
default number of screen deep.
預設的螢幕深度數。


5 =: SVMAX \ increase number of buffers to 5
5 =： SVMAX \ 將緩衝區數目增加至 5
FSAVE F <enter> \ resave the system
FSAVE F <enter> \ 重新儲存系統
BYE \ leave after changing and saving
BYE \ 更改並存續後離開
F <enter> \ now the screen stack is 5 deep.
F <enter> \ 現在螢幕堆疊有 5 深。


Your preferences can be edited into the configuration file F-PC.CFG.
您的首選項可以編輯到配置文件 F-PC 中。CFG。
This file is executed by F- PC immediately after it is loaded into
該文件在加載到
memory. Only a few of the preferences were included into the
記性。只有少數偏好設定包含在
configuration file during the installation/configuration process, and
安裝/組態程序期間的組態檔，以及
most preferences were set to default choices. In the hypertext root
大部分的偏好設定都設定為預設選項。在超文本根目錄中
screen, a link item 'Preferences' is available for you to see all the
畫面中，連結項目「首選項」可供您查看所有
possible choices on-line.
在線可能的選擇。


9.5. TASK CHAINING
9.5. 任務鏈結


Tom Zimmer developed a very powerful technique by which more functions
湯姆·季默 （Tom Zimmer） 開發了一種非常強大的技術，通過該技術可以發揮更多功能
can be added to a word as the needs grow. He called it background task
可以隨著需求的增長添加到單詞中。他稱之為後台任務
chaining. The idea is to use a DEFERred word as a basis. Some time
鏈條。這個想法是使用 DEFERred 詞作為基礎。一段時間
later this deferred word is resolved to do one task. We can add some
稍後，這個延遲字被解析為執行一項任務。我們可以添加一些
more tasks to this word by defining a new word and compiling the contents
通過定義一個新單詞並編譯內容來對這個單詞進行更多任務
of the deferred word into the new word with other functions. The
將延遲的詞轉換為具有其他功能的新詞。這
deferred word is then re-vectored to the new definition. When the
然後，延遲的單字會重新向量化為新定義。當
deferred word is executed, new functions are added to the old task. This
延遲字執行時，新函數會新增至舊任務。這
task chain can thus be extended to your heart's desire. The words
因此，任務鏈可以擴展到您內心的願望。這些話
involved in task chaining are:
涉及任務鏈結的有：


DEFER <name>
延 <name>


to define a deferred word whose function can be changed by re-vectoring,
若要定義其功能可以透過重新向量化來變更的延遲字，
and
和


DEFERS <name>
延期<name>


an immediate compiler word which compiles the contents of the next
立即編譯器字，可編譯下一個
deferred word in a colon definition. It allows many functions to be
冒號定義中的延遲單字。它允許許多功能
added to the deferred word.
添加到延期詞中。


In F-PC, KEY is a user deferred word. We have to use DEFERS to extend
在 F-PC 中，KEY 是使用者延遲字。我們必須使用 DEFERS 來擴展
its function. BGSTUFF is a regular deferred word to extend functions like
它的功能。BGSTUFF 是一個常規的延遲詞，用於擴展諸如
the status line display. BYESTUFF is used to extend the cleaning up task
狀態行顯示。BYESTUFF 用於擴展清理任務
before F-PC exits to DOS. Let's use BGSTUFF as an example:
在 F-PC 退出 DOS 之前。我們以 BGSTUFF 為例：


DEFER BGSTUFF
推遲 BGSTUFF
' NOOP IS BGSTUFF
' NOOP 是 BGSTUFF
: (KEY?)
：（鑰匙？
DEFERS BGSTUFF
推遲 BGSTUFF
{ the words to do (KEY?) }
{ 要做的字詞 （KEY？
;


' (KEY?) IS BGSTUFF \ BGSTUFF = (KEY?)
'（鑰匙？是 BGSTUFF \ BGSTUFF = （鍵？
: TIME
：時間
DEFERS BGSTUFF
推遲 BGSTUFF
#OUT @ #LINE @ \ save cursor position
#OUT @ #LINE @ \ 儲存游標位置
64 0 AT .TIME \ print time at upper-right corner
64 0 在 .右上角的 TIME \ 列印時間
AT \ restore cursor
AT \ 還原游標
;
' TIME IS BGSTUFF \ BGSTUFF = (KEY?) + .TIME
' 時間是 BGSTUFF \ BGSTUFF = （鍵？） + 。時間


This technique allows you to dynamically change the behavior of a
此技術可讓您動態變更
deferred word while keeping most of its old functionality. As the system
延遲字，同時保留其大部分舊功能。作為系統
grows, it is easier to add new functions to an existing word than to
grows，則向現有單字添加新功能比在現有單字中添加新功能更容易
define new words and mess up the existing environment.
定義新詞並擾亂現有環境。


9.6. CONTROL STRUCTURE ENHANCEMENTS
9.6. 控制結構增強功能


Bill Muench contributed a modified set of control structures. The
比爾·穆恩奇 （Bill Muench） 貢獻了一套修改後的控制結構。這
changes are very very minor, but result in a significant increase in
變化非常非常小，但會導致
versatility. The change is effectively to move a 2SWAP from the
多才多藝。此變更實際上是將 2SWAP 從
beginning of REPEAT and put it at the end of UNTIL. Some additional
REPEAT 的開頭，並將其放在 UNTIL 的結尾。一些額外的
words have also been added to take advantage of the increased
還添加了單詞以利用增加的
versatility. The changes have been added to the system, the meta
多才多藝。這些變化已添加到系統中，元數據
compiler, and the assembler.
編譯器，以及組譯器。


Some possible combinations of the structures are shown in the following
以下顯示了一些可能的結構組合
cases. However, the possible combinations are only limited by your
案例。但是，可能的組合僅受您的限制
imagination.
想像力。


WHILE can be used to exit a DO...LOOP conditionally. The WHILE structure
WHILE 可用來退出 DO...LOOP 有條件地執行。WHILE 結構
can be nested.
可以巢狀。


DO ...
做。。。
WHILE ...
時間。。。
WHILE ...
時間。。。
LOOP ...
圈。。。
ELSE UNDO ... \ drop or use index and limit
ELSE UNDO ... \ 刪除或使用索引和限制
THEN ...
當時。。。
ELSE UNDO ... \ drop or use index and limit
ELSE UNDO ... \ 刪除或使用索引和限制
THEN
當時


A normal BEGIN..WHILE..REPEAT loop behaves like it always did:
一個正常的開始......時間。。REPEAT 迴圈的行為就像往常一樣：


BEGIN ...
開始。。。
WHILE ... \ normal structure
WHILE ... \ 正常結構
REPEAT
重


CONTINUE allows a conditional branch back to BEGIN:
CONTINUE 允許條件分支返回 BEGIN：


BEGIN ...
開始。。。
IF ...
如果。。。
CONTINUE ... \ now branch back to begin
繼續 ... \ 現在分支回開始
UNTIL \ otherwise, conditionally branch
UNTIL \ 否則，有條件地分支


WHILE can also leave a BEGIN..UNTIL loop conditionally.
而也可以留下一個開始。UNTIL 迴圈。


BEGIN ...
開始。。。
WHILE ... \ multiple exit tests
WHILE ... \ 多次退出測試
UNTIL ...
洎。。。
ELSE ... \ and possibly different action
ELSE ... \ 和可能不同的動作
THEN
當時


WHILE can also be nested in a BEGIN..UNTIL loop.
WHILE 也可以嵌套在 BEGIN..UNTIL 迴圈。


BEGIN ...
開始。。。
WHILE ... \ multiple exit tests
WHILE ... \ 多次退出測試
WHILE ... \ multiple exit tests
WHILE ... \ 多次退出測試
UNTIL ...
洎。。。
ELSE .. \ and possibly different action
其他的。。\ 和可能不同的動作
THEN ...
當時。。。
ELSE ... \ and possibly different action
ELSE ... \ 和可能不同的動作
THEN
當時


AFT..THEN structure can be nested inside BEGIN..WHILE..REPEAT loop. The
船尾..THEN 結構可以嵌套在 BEGIN 內。時間。。REPEAT 迴圈。這
clause inside AFT..THEN is executed only once in the first looping.
AFT 內的條款。THEN 在第一次迴圈中只會執行一次。


BEGIN ...
開始。。。
AFT ... \ executed only once
AFT ... \ 僅執行一次
THEN .. \ ignored afterwards
當時。。\ 事後忽略
WHILE ...
時間。。。
REPEAT
重


The FOR...NEXT structure was proposed by Chuck Moore in the cmForth for
為了...NEXT 結構由 Chuck Moore 在 cmForth 中提出，用於
the Novix NC4000 Forth chip. FOR takes a count from the data stack and
Novix NC4000 Forth 芯片。FOR 從資料堆疊中獲取計數，而
pushes it onto the return stack. NEXT decrements the count on the return
將其推送到返回堆疊上。NEXT 會遞減傳回的計數
stack. If the count becomes zero after being decremented, the loop is
堆。如果計數在遞減後變為零，則迴圈為
terminated; otherwise, the loop is repeated.
終止;否則，循環會重複。


The FOR...NEXT loop can also use WHILE to exit conditionally:
為了...NEXT 迴圈也可以使用 while 有條件地退出：


FOR ...
為。。。
WHILE ... \ in effect an immediate ?leave
雖然 ... \ 實際上是立即 “休假”
NEXT ...
下一個 ...
ELSE ... R> ( DROP ) \ drop or use the loop index
其他的。。。R> （ DROP ） \ 刪除或使用循環索引
THEN
當時


AFT..THEN structure can also be nested in a FOR..NEXT loop.
船尾..THEN 結構也可以嵌套在 FOR..NEXT 迴圈。


FOR ...
為。。。
AFT ... \ this is only executed the first
AFT ... \ 這只會在第一個執行
\ time through the loop
\ 循環時間
THEN ... \ this is executed every time
然後 ... \ 每次都會執行此操作
NEXT
下一頁


Another way to exclude the n=0 case and also have the loop execute n
排除 n=0 情況並讓循環執行 n 的另一種方法
times, but is longer and slower specifically on a FORTH machine like the
時間，但更長、更慢，特別是在像
NC4000 or Harris RTX.
NC4000 或 Harris RTX。


( n ) ?DUP IF 1- FOR ... NEXT ... THEN
（ n ） ？DUP IF 1- 為 ...下一個 ...當時


BREAK allows the construction of a case structure in a colon definition:
BREAK 允許在冒號定義中建構大小文字結構：


... IF ... BREAK \ case like structure
...如果。。。BREAK \ 類似大小寫的結構
... IF ... BREAK \ break compiles an exit
...如果。。。BREAK \ break 編譯一個結束
... IF ... EXIT THEN \ same as break
...如果。。。EXIT THEN \ 與 break 相同


9.7. HEADLESS WORDS
9.7. 無頭詞


This is a neat utility from George T. Hawkins to allow the extraction and
這是 George T. Hawkins 的一個簡潔的實用程序，允許提取和
removal of the unwanted heads in the Forth system and any application you
刪除 Forth 系統和任何應用程序中不需要的磁頭
may write in F-PC.
可以用 F-PC 書寫。


Any words to be later beheaded are identified with a "HEADERLESS"
任何稍後要斬首的單詞都用“HEADERLESS”標識
keyword. This is followed by the colon definitions or code words
關鍵字。後面是冒號定義或代碼字
themselves. You re-establish standard words (i.e., words with headers)
他們自己。您重新建立標準單字（即帶有標題的單字）
with the keyword "HEADERS".
使用關鍵字“HEADERS”。


When you have finished your use/referencing of headerless words, you then
當您完成無標題單詞的使用/引用後，您
use the keyword: "BEHEAD". This will completely remove the definition of
使用關鍵字：「BEHEAD」。這將完全刪除
any headerless words from the directory.
目錄中的任何無標頭單字。


Once headerless words are BEHEADed they are lost forever; i.e., their
一旦無標題詞被斬首，它們就會永遠消失;即，他們的
code and list space is not lost - but they are unknown so far as the
程式碼和清單空間不會遺失 - 但它們是未知的，因為
dictionary is concerned. Note that you cannot ever reference a
字典是關於的。請注意，您永遠無法參考
HEADERLESS word once it is BEHEADed. So the logic to using HEADERLESS
HEADERLESS 單字。所以使用 HEADERLESS 的邏輯
words is as follows:
詞語如下：


ONLY FORTH ALSO EDITOR ALSO HIDDEN \ set up search order as needed
僅 FORTH ALSO EDITOR ALSO HIDDEN \ 根據需要設置搜索順序
HEADERLESS
無標頭
... \ put headerless words here
... \ 把無標題的詞放在這裡
HEADERS
標頭
... \ put words which reference
... \ 放置引用的單詞
\ the previous group of
\ 上一組
\ headerless words here
\ 這裡的無標題單詞
EDITOR DEFINITIONS \ switch to EDITOR vocabulary
編輯器定義 \ 切換至 EDITOR 詞彙
\ but don't change order.
\ 但不要改變順序。
\ repeat above sequence of:
\ 重複上述順序：
HEADERLESS \ Turn off heads in editor vocabulary
HEADERLESS \ 關閉編輯器詞彙中的頭部
... <words> ...
...<words> ......
HEADERS \ Turn heads back on
標題 \ 重新引人注目
... <words> ...
...<words> ......
HIDDEN DEFINITIONS \ switch to HIDDEN vocabulary but don't
隱藏定義 \ 切換到 HIDDEN 詞彙，但不要
\ change order.
\ 變更順序。
\ as desired
\ 根據需要
BEHEAD
斬


Although the use of headerless words can save you head space, their main
雖然使用無標題單字可以節省您的頭部空間，但它們的主要內容
advantage is in the software engineering they provide. That is, the
優勢在於他們提供的軟件工程。也就是說，
definitions/names are *completely lost* not just stashed away in some
定義/名稱*完全丟失*，而不僅僅是隱藏在某些地方
obscure vocabulary. (If you attempt to "see" or "debug" headerless words
晦澀難懂的詞彙。（如果您嘗試「查看」或「偵錯」無標題單字
through regular words you get a garbage ID.)
通過常規單詞，你會得到一個垃圾 ID。


In general you should set up your {HEADERLESS/HEADERS}/ BEHEAD
一般來說，您應該設定 {HEADERLESS/HEADERS}/ BEHEAD
definitions as described above, but precede it with a single "HWORDS-".
如上所述，但前面有一個“HWORDS-”。
HWORDS- will cause HEADERLESS, HEADERS, and BEHEAD to be treated as
HWORDS- 會導致 HEADERLESS、HEADERS 和 BEHEAD 被視為
noops. Once you've finished debugging and are ready to go to production,
嗚嗚。完成偵錯並準備好投入生產環境之後，
then change "HWORDS-" to "HWORDS+". This will give the HEADERLESS,
然後將 “HWORDS-” 更改為 “HWORDS+”。這將使 HEADERLESS，
HEADERS, and BEHEAD words their standard meaning. If you ever need to
HEADERS 和 BEHEAD 詞的標準含義。如果您需要
debug the code again, and want to see the names, then change HWORDS+ to
再次偵錯程式碼，並想要查看名稱，然後將 HWORDS+ 變更為
HWORDS-.
HWORDS-。


As can be seen in the above example, you should setup your vocabulary
如上例所示，您應該設置詞彙表
search order prior to starting a sequence of definitions in which some
在開始定義序列之前搜尋順序，其中某些定義
words will be headerless. After setting the search order, you can still
單詞將是無標題的。設定搜尋順序後，您仍然可以
select different vocabularies in which you place definitions, but you
選取不同的詞彙來放置定義，但您
MUST NOT change the search order, that is you MUST NOT use "ONLY" or
不得更改搜索順序，即您不得使用“ONLY”或
"ALSO". Also the current vocabulary should not be changed while in
“還”。此外，當前詞彙不應在
HEADERLESS mode.
HEADERLESS 模式。


9.8. SAVE AND RESTORE
9.8. 儲存和還原


At times one needs to change various global attributes of the Forth
有時，人們需要改變 Forth 的各種全局屬性
system while preserving their value to be later restored. An example of
系統，同時保留其價值以供以後恢復。範例
this might be changing CAPS to ON, while saving its current value to
這可能會將 CAPS 變更為 ON，同時將其目前值儲存至
restore later. Here is a typical code segment to save CAPS, turn it on,
稍後還原。這裡有一個典型的程式碼段來保存大寫，打開它，
and restore it at later in a definition:
並稍後在定義中還原它：


: DEF1 ( --- )
： DEF1 （ --- ）
CAPS @ >R CAPS ON \ Save CAPS and turn ON
大寫 @ >R CAPS ON \ 儲存大寫並開啟
...
use SEARCH for something ...
使用 SEARCH 來做某件事......
...
R> CAPS ! \ restore CAPS
R> 大寫字母！\ 還原大寫
;


While this is an acceptable way to save and restore a variable, it is
雖然這是儲存和還原變數的可接受方式，但它確實如此
difficult to read, and not particularly efficient in terms of
難以閱讀，而且在
performance. A new mechanism has been introduced which enhances
演奏。引入了一種新機制，增強了
readability, and improves performance at the same time. Here is an
可讀性，同時提高效能。這是一個
example of SAVE!> and RESTORE>:
SAVE！>和 RESTORE 的範例>：


: DEF1 ( --- )
： DEF1 （ --- ）
TRUE SAVE!> CAPS \ save and set CAPS
> 大寫字母 \ 儲存並設定大寫字母
...
use SEARCH for something ...
使用 SEARCH 來做某件事......
...
RESTORE> CAPS \ restore CAPS
還原> CAPS \ 還原大寫
;


These words allow a VARIABLE or VALUE to be saved for later, and set to a
這些字組允許儲存 VARIABLE 或 VALUE 以供日後使用，並設定為
new value for temporary use. Another word included in the set allows
臨時使用的新值。套裝中包含的另一個詞允許
saving a VARIABLE or VALUE without changing it, for later restoration:
儲存變數或值而不變更它，以便稍後還原：


: DEF1 ( --- )
： DEF1 （ --- ）
SAVE> CAPS \ save CAPS
儲存>大寫 \ 儲存大寫
...
do something that may change CAPS...
做一些可能改變大寫字母的事情......
...
RESTORE> CAPS \ restore CAPS
還原> CAPS \ 還原大寫
;


The only problem with these words is they cannot be use with user
這些詞的唯一問題是它們不能與用戶一起使用
variables, as they are fairly dumb and fast. They simply work with the
變數，因為它們相當愚蠢且快速。他們只是使用
contents of the body of the definition following.
定義正文的內容如下。


9.9 LINE EDITOR
9.9 行編輯器


F-PC provides a very nice general purpose line editor for use in your
F-PC 提供了一個非常好的通用行編輯器，用於您的
application programs. It allows you to request a line of input from the
應用程式。它可讓您從
user, while allows him to edit the text before pressing <return> to send
user，同時允許他在按發送之前編輯文本<return>
it to the program. The word to invoke it is LINEEDITOR. Its usage is as
它到程序。調用它的詞是 LINEEDITOR。其用法是
follows:
如下：


20 8 MYBUF 22 LINEEDITOR ( -- f )
20 8 MYBUF 22 行編輯器 （ -- f ）


In this example, the text buffer will start at column 20 of row 8.
在此範例中，文字緩衝區將從第 8 列的第 20 欄開始。
Editing will be performed on the counted string in MYBUF, and the maximum
編輯將對 MYBUF 中的計數字串執行，最大值
length allowed is 22 characters. The line editor is terminated by either
允許的長度為 22 個字元。行編輯器會由下列任一
<return> or ESC key. If the ESC key is pressed than a false boolean flag
<return> 或 ESC 鍵。如果按下 ESC 鍵，則會顯示 false 布林標誌
is returned; otherwise, a true flag is returned. A mouse can be used to
被傳回;否則，會傳回 true 旗標。滑鼠可用於
position the cursor within the edit line.
將游標放在編輯行內。


If the editing is completed with <return>, then the edit string is placed
如果編輯是使用 完成，則<return>會放置編輯字串
back into MYBUF. If the editing is terminated with ESC, then MYBUF will
回到 MYBUF。如果使用 ESC 終止編輯，則 MYBUF 將
contain the original string unmodified by any edit operations performed
包含未執行任何編輯作業修改的原始字串
during the editing session.
在編輯過程中。


During editing, you can use the Right arrow, Left arrow, Home, End, and
在編輯期間，您可以使用向右鍵、向左鍵、首頁、結尾和
Delete keys to position the cursor to edit the string.
刪除鍵以定位游標以編輯字串。

