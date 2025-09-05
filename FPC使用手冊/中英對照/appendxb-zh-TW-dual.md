B-1


APPENDIX B: SAMPLES AND TUTORIALS
附錄 B：範例和教學課程



F-PC is such a monstrous system that most Forth users would feel lost
F-PC 是一個如此可怕的系統，大多數 Forth 用戶都會感到迷失
facing it the first time. To make a new user feel more at home with it
第一次面對它。讓新用戶對它有賓至如歸的感覺
and help him overcome the initial shock, Tom Zimmer prepared a set of
並幫助他克服最初的震驚，湯姆·季默準備了一套
tutorial examples illustrating many unique and interesting features in
教學範例說明了
F-PC. These examples are collected in the EXAMPLES.ARC file. You will
F-PC。這些範例收集在範例中。ARC 檔案。你會
also find many good tutorial materials in the user contributed files.
在用戶貢獻的文件中也可以找到很多不錯的教程資料。
However, these user contributed files are more application oriented and
然而，這些使用者貢獻的檔案更面向應用程式，並且
do assume that you are familiar with the F-PC system.
請假設您熟悉 F-PC 系統。


B1. MEMORY ALLOCATION
B1.記憶體分配


SALLOC.SEQ contains an example of how to use the memory allocation and
薩洛克。SEQ 包含如何使用記憶體配置和
deallocation words. This example allocates space at F-PC cold start time
解除分配詞。此示例在 F-PC 冷啟動時分配空間
by placing the word MY-INIT into the deferred word chain called
透過將單字 MY-INIT 放入名為
INITSTUFF. You do not have to allocate your memory at this time, but it
初始內容。此時您不必分配記憶體，但
will prevent your memory allocation from interfering with the editor's
將防止您的記憶體分配干擾編輯器的
usage of memory. It is fairly easy using allocation and deallocation to
記憶體的使用。使用分配和解除分配相當容易
cause memory to get fragmented to the point where almost any ALLOC will
導致記憶體碎片化到幾乎所有 ALLOC 都會
fail.
敗。


hidden clearmem forth \ make sure the editor is not using memory
隱藏的 clearmem forth \ 確保編輯器沒有使用記憶體


16000 constant bytes_needed \ Size of the array I need in bytes.
16000 常數 bytes_needed \ 我需要的數組大小（以位元組為單位）。


0 value myseg \ a place to put my base segment pointer.
0 值 myseg \ 放置我的基段指針的位置。


: alloc-myseg ( --- ) \ allocate the space I need
： alloc-myseg （ --- ） \ 分配我需要的空間
myseg ?exit \ don't allocate again if already done
myseg ？exit \ 如果已經完成，則不要再次分配
bytes_needed paragraph \ adjust needed to # of paragraphs
bytes_needed 段落 \ 調整為 # 個段落
alloc \ allocate the space test for error in alloc
alloc \ 分配分配 alloc 中錯誤的空間測試
8 = abort" Not enough memory forMYSEG"
8 = 中止「MYSEG 記憶體不足」
nip \ discard largest block available
nip \ 丟棄可用的最大塊
!> myseg ; \ asign start of array into MYSEG
！> myseg ;\ a 將陣列的開頭指派給 MYSEG


alloc-myseg \ really allocate the space now so we can
alloc-myseg \ 現在真正分配空間，這樣我們就可以
\ experiment
\試


: my-init ( --- )
：我的初始化 （---）
defers initstuff \ inserted into INITSTUFF chain
延遲 initstuff \ 插入 INITSTUFF 鏈結
off> myseg
關閉> myseg
alloc-myseg ;
分配-米塞格;


\ ' my-init is init-stuff \ un-comment this line to cause
\ ' my-init 是 init-stuff \ 取消註解此行會導致
\ initialization to be done at cold boot
\ 初始化要在冷啟動時完成


If you need to deallocate the space that you have allocated, you can use
如果您需要解除配置已配置的空間，您可以使用
DEALLOC to release the space back to DOS.
DEALLOC 將空間釋放回 DOS。


: release-myseg ( -- )
： 釋放 myseg （ -- ）
myseg dealloc abort" failed to deallocate MYSEG" ;
myseg dealloc abort“ failed to delocate MYSEG” ;


The other operation you can perform on an allocated memory segment is to
您可以在已配置的記憶體區段上執行的另一個作業是
resize it to a new size. This is done with SETBLOCK.
將其調整為新大小。這是透過 SETBLOCK 完成的。


: resize-myseg ( n1 -- ) \ adjust myseg to new size n1 in bytes
： resize-myseg （ n1 -- ） \ 將 myseg 調整為新的大小 n1（以位元組為單位）
myseg swap paragraph setblock
MySeg 交換段落集塊
abort" Failed to resize MYSEG" ;
abort“ 無法調整 MYSEG 的大小” ;


To put something into the array MYSEG, I might do something like the
要將某些東西放入陣列 MYSEG 中，我可能會執行類似
following.
跟隨。


: string-save ( | <string> -- ) \ accept a <string> to save
： 字串儲存 （ |<string> -- ） \ 接受 a <string> 儲存
?cs: 0 word dup>r \ moving FROM here
？cs：0 個單詞 dup>r \ 從這裡移動
myseg 0 \ TO the beginning of MYSEG
myseg 0 \ 到 MYSEG 的開頭
r> c@ 1+ CMOVEL ; \ move the data with CMOVE LONG
r> c@ 1+ 克莫爾 ;\ 使用 CMOVE LONG 移動數據


And you can then display the text from MYSEG.
然後，您可以顯示來自 MYSEG 的文字。


: type-string ( -- )
： 類型字串 （ -- ）
myseg 0 \ FROM myseg
myseg 0 \ 來自 myseg
2dup c@L >r \ fetch the count
2dup c@L >r \ 取得計數
?cs: here \ TO here
？cs：這裡 \ 到這裡
r> 1+ CMOVEL \ move data to HERE
r> 1+ CMOVEL \ 將資料移至此處
here count type ; \ display it
這裡計數類型;\ 顯示它


B2. USER BOOT PROCESS
B2.使用者開機程序


SBOOT.SEQ contains an example of how to make F-PC perform your own
SBOOT 的。SEQ 包含如何讓 F-PC 執行您自己的範例
function in place of starting F-PC and just running Forth. Before
功能代替啟動 F-PC 並僅運行 Forth。以前
describing how to modify F-PC, let us first look at the things F-PC does
描述如何修改 F-PC，我們先來看看 F-PC 是做什麼的
at BOOT time so you can have a better understanding of the startup
在啟動時，以便您可以更好地了解啟動
process.
過程。


At BOOT time F-PC proceeds through the following sequence:
在啟動時，F-PC 將按照以下順序進行：


: COLD
：冷
{deferred} SETSEG
{延期}套裝
Setup Segments
設定區段
Verify DOS > 2
驗證 DOS > 2
Adjust memory allocation
調整記憶體配置
Seg cursor position
Seg 游標位置
{deferred} VMODE.SET
{延期}VMODE。鑲
test Video mode
測試視訊模式
Adjust display attributes
調整顯示屬性
{deferred} >COLOR
{延遲} >顏色
or
或
{deferred} >MONO
{延期} >猴子
Set the Video segment
設定視訊區段
{deferred} INITSTUFF
{延期}初始內容
\ Various initializations, performed in a chain through this
\ 各種初始化，通過這個鏈式執行
\ Deferred word. Things like:
\ 延期詞。諸如此類的事情：
MACROS
巨集
EDITOR
主筆
SAVE SCREEN
儲存畫面
READ BUFFER SIZE
讀取緩衝區大小
FILE SYSTEM
檔案系統
DIRECTORY BUFFER etc.
DIRECTORY BUFFER 等。
{deferred} BOOT
{延期}靴子
HELLO
你好
Initialize TIB
初始化 TIB
Initialize VOCABULARY to FORTH
將詞彙初始化為 FORTH
{deferred} DEFAULT
{延期}預設
HDEFAULT
Move command line to TIB
將命令列移至 TIB
OPEN a file if available
如果有的話，請開啟檔案
{deferred} .HELLO
{延期}。你好
Display signon message
顯示登入訊息
{deferred} .CURFILE
{延期}。CURFILE
Display current file
顯示目前檔案
{deferred} INTERPRET
{延期}繙
Process command line
進程命令列
QUIT ;
放棄;


As you can see from the above sequence, there are several places you can
從上面的順序可以看出，有幾個地方可以
modify what F-PC does at boot time. A substantial portion of the above
修改 F-PC 在啟動時執行的動作。上述內容的很大一部分
process must be done, and so we want to be careful to tie in at the right
流程必須完成，因此我們要小心翼翼地將正確的聯繫起來
point. In general eveything before BOOT must be done for F-PC to operate
指。一般來說，在啟動之前必須完成所有操作才能使 F-PC 運行
properly. If we tie in at BOOT though we will have to do some additional
當然地。不過，如果我們在 BOOT 上合作，我們將不得不做一些額外的事情
initialization to specifically much of the stuff done by HELLO. If we
初始化到專門由 HELLO 完成的大部分事情。如果我們
tie in at DEFAULT, we usually still want the DOS command line to be moved
在 DEFAULT 時，我們通常仍然希望移動 DOS 命令列
to TIB, and probably still want a file to be opened, so my normal choice
到 TIB，並且可能仍然希望打開一個文件，所以我的正常選擇
would be to use DEFERS to link into DEFAULT without eliminating the
會使用 DEFERS 連結至 DEFAULT，而不移除
function that is already there. This will then turn DEFAULT into a
已經存在的功能。然後，這會將 DEFAULT 變成
DEFERred chain. If we want in addition to have our own sign-on message,
DEFERred 鏈。如果我們想要除了擁有自己的登入訊息之外，
we can replace the functions in .HELLO and/or .CURFILE although a user
我們可以替換 中的函數。HELLO 和/或 。CURFILE 雖然是使用者
application need not return from the chained DEFAULT, and as such .HELLO
應用程式不需要從鏈結的 DEFAULT 傳回，因此 .你好
will never get performed. Here then without further delay is MYDEFAULT.
永遠不會被執行。那麼，這裡毫不拖延地說是 MYDEFAULT。


: mydefault ( -- )
： 我的預設值 （ -- ）
defers default \ link into default as additional
將預設 \ 連結延遲為預設值作為附加
\ stuff to be done.
\ 要做的事情。


\ Your program stuff goes here.
\ 你的程序內容在這裡。
\ *****************************


cr ." This is my program "
cr “。這是我的節目”
cr ." Press a key to terminate "
cr。按一個鍵終止”
key drop \ wait for a key before leaving
key drop \ 等待鑰匙後再離開
cr
鉻


\ This ends your program, so leave.
\ 您的計劃到此結束，所以離開。
\ *************************


bye ; \ got it so leave
再見;\ 知道了，所以離開


' mydefault is default
' mydefault 是預設值


FSAVE MYBOOT.EXE \ Now save the system back to disk with the
FSAVE MYBOOT.EXE \ 現在使用
\ name MYBOOT.EXE.
\ 名稱 MYBOOT.EXE。


B3. F-PC KEYSTROKE MACROS
B3.F-PC 按鍵巨集


SMACRO.SEQ contains an example of how to use macros in the F-PC editor to
斯宏。SEQ 包含如何在 F-PC 編輯器中使用巨集的範例
reduce the keystrokes required to perform a given task. The first
減少執行給定任務所需的擊鍵次數。第一個
example is a real one. We want to shorten the glossary entries. A
例子是真實的。我們想縮短詞彙表條目。一個
typical entry is shown below for +! :
+的典型條目如下所示！:


+! ( n1 a1 -- )
+!（ N1 A1 -- ）
FORTH KERNEL1
第四 KERNEL1
Increment the value at a1 by n1. This is equivalent
將 a1 處的值遞增 n1。這相當於
to the following: DUP @ ROT + SWAP ! but
到以下內容：DUP @ ROT + SWAP！卻
much faster.
快得多。


Since all of the words in the glossary are in the FORTH vocabulary, we
由於詞彙表中的所有單詞都在 FORTH 詞彙表中，因此我們
can delete the word FORTH . Furthermore, the second line containing the
可以刪除 FORTH 一詞。此外，包含
source file name can be joint with the first line, and a little more
源文件名可以與第一行聯合，再多一點
editing can also be done at the same time. The desired new entry would
編輯也可以同時進行。所需的新條目將
be:
是：


+! ( n1 a1 -- ) KERNEL1
+!（ N1 A1 -- ）KERNEL1
Increment the value at a1 by n1. This is equivalent
將 a1 處的值遞增 n1。這相當於
to the following: DUP @ ROT + SWAP ! but
到以下內容：DUP @ ROT + SWAP！卻
much faster.
快得多。


The glossary is a very large file, and the manual editing required to
詞彙表是一個非常大的檔案，手動編輯需要
correct this would have been prohibitive, so a macro is created to join
糾正這將是令人望而卻步的，因此創建了一個巨集來加入
the second line with the first line and remove the Vocabulary from each
第二行與第一行，並從每個行中刪除詞彙
entry when a single MACRO key is pressed.
輸入。


Here then is the key sequence that will make a macro to join the first
這是將創建巨集以連接第一個的關鍵序列
and second lines of the second type glossary entry and remove the
和第二種類型詞彙表項目的第二行，並移除
vocabulary from the entry. The macro will then go to the next paragraph
詞彙。然後，巨集將轉到下一個段落
which starts the next entry.
開始下一個條目。


This macro is always executed when the cursor in on the first line of a
當游標進入 的第一行時，一律會執行此巨集
glossary entry at the leftmost column, and we are in INSERT mode.
詞彙表條目，我們處於 INSERT 模式。


Alt-M Start a MACRO
Alt-M 啟動巨集
Alt-1 We are starting the macro for Alt-1
Alt-1 我們正在啟動 Alt-1 的巨集
INS Select OVERWRITE mode
INS 選擇覆蓋模式
TAB Move to first TAB position
TAB 移至第一個 TAB 位置
Ctrl-T Remove spaces before stack picture
Ctrl-T 刪除堆疊圖片前的空格
TAB Move to 2nd TAB
TAB 移至第二個 TAB
TAB Move to 3rd TAB
TAB 移至第 3 個 TAB
TAB Move to 4th TAB
TAB 移至第 4 個 TAB
INS Go back into INSERT mode
INS 返回 INSERT 模式
DEL Delete the last char in the line forcing a join line. Cursor is now on
DEL 刪除強制連接行的行中的最後一個字符。游標現在開啟
the word FORTH
FORTH 這個詞
Ctrl-T Delete the Vocabulary
Ctrl-T 刪除詞彙
HOME Move back to beginning of line
首頁 移回行首
Alt-G_N Goto Next paragraph
Alt-G_N 轉到下一個段落
Alt-M Complete macro
Alt-M 完整巨集


Macros are performed as they are created, so you must be on a glossary
巨集會在建立時執行，因此您必須在詞彙表上
entry that needs to be modified while you are in the process of making
在製作過程中需要修改的條目
the macro.
宏觀。


In the following section I have included several copies of the +!
在下一節中，我包含了幾份 +！
glossary entry. Try making the macro described above while you are on
詞彙表條目。嘗試在上邊進行上述巨集
the first entry, then press Alt-1 to try the macro on each successive
第一個條目，然後按 Alt-1 在每個連續的條目上嘗試巨集
entry.
入口。


Macros can be saved with Alt-M_S, and loaded again with Alt-M_L. You can
巨集可以使用 Alt-M_S 儲存，然後使用 Alt-M_L 再次載入。你可以
view the currently defined macros with Alt-M_V, but they will look very
使用 Alt-M_V 查看當前定義的宏，但它們看起來非常
funny since they are mostly graphics characters.
很有趣，因為它們大多是圖形角色。


---------------------- Try some macros here --------------------
---------------------- 在這裡嘗試一些巨集--------------------


+! ( n1 a1 -- )
+!（ N1 A1 -- ）
FORTH KERNEL1
第四 KERNEL1
Increment the value at a1 by n1. This is equivalent
將 a1 處的值遞增 n1。這相當於
to the following: DUP @ ROT + SWAP ! but
到以下內容：DUP @ ROT + SWAP！卻
much faster.
快得多。


+! ( n1 a1 -- )
+!（ N1 A1 -- ）
FORTH KERNEL1
第四 KERNEL1
Increment the value at a1 by n1. This is equivalent
將 a1 處的值遞增 n1。這相當於
to the following: DUP @ ROT + SWAP ! but
到以下內容：DUP @ ROT + SWAP！卻
much faster.
快得多。


+! ( n1 a1 -- )
+!（ N1 A1 -- ）
FORTH KERNEL1
第四 KERNEL1
Increment the value at a1 by n1. This is equivalent
將 a1 處的值遞增 n1。這相當於
to the following: DUP @ ROT + SWAP ! but
到以下內容：DUP @ ROT + SWAP！卻
much faster.
快得多。


+! ( n1 a1 -- )
+!（ N1 A1 -- ）
FORTH KERNEL1
第四 KERNEL1
Increment the value at a1 by n1. This is equivalent
將 a1 處的值遞增 n1。這相當於
to the following: DUP @ ROT + SWAP ! but
到以下內容：DUP @ ROT + SWAP！卻
much faster.
快得多。


+! ( n1 a1 -- )
+!（ N1 A1 -- ）
FORTH KERNEL1
第四 KERNEL1
Increment the value at a1 by n1. This is equivalent
將 a1 處的值遞增 n1。這相當於
to the following: DUP @ ROT + SWAP ! but
到以下內容：DUP @ ROT + SWAP！卻
much faster.
快得多。


+! ( n1 a1 -- )
+!（ N1 A1 -- ）
FORTH KERNEL1
第四 KERNEL1
Increment the value at a1 by n1. This is equivalent
將 a1 處的值遞增 n1。這相當於
to the following: DUP @ ROT + SWAP ! but
到以下內容：DUP @ ROT + SWAP！卻
much faster.
快得多。


HRENAME ( handle1 handle2 -- return-code )
HRENAME （ handle1 handle2 -- 回覆碼 ）
FORTH HANDLES
第四個手柄
Change the name of the file specified in handle1 to the name
將 handle1 中指定的檔案名稱變更為名稱
specified in handle2. Can be used to move a file from one
在 handle2 中指定。可用來將檔案從
directory to another on the same drive. Returns 18 if the
目錄到同一磁碟機上的另一個目錄。如果
rename was good, not zero.
重命名是好的，而不是零。


HRENAME ( handle1 handle2 -- return-code )
HRENAME （ handle1 handle2 -- 回覆碼 ）
FORTH HANDLES
第四個手柄
Change the name of the file specified in handle1 to the name
將 handle1 中指定的檔案名稱變更為名稱
specified in handle2. Can be used to move a file from one
在 handle2 中指定。可用來將檔案從
directory to another on the same drive. Returns 18 if the
目錄到同一磁碟機上的另一個目錄。如果
rename was good, not zero.
重命名是好的，而不是零。


As you can see, having performed the macro on one of the last two
如您所見，在最後兩個之一上執行了巨集
glossary entries for HRENAME, a macro will not always work as you expect.
詞彙表項目，巨集不一定會如您預期般運作。
If the information being manipulated does not follow the rules, you can
如果作的資訊不符合規則，您可以
get quite unexpected results. Use caution with macro, they can be
得到相當意想不到的結果。謹慎使用巨集，它們可能是
wonderful time savers, but it is difficult to make a macro that will
很棒的時間節省，但很難製作出一個能節省時間的巨集
always work.
總是工作。


This is only the start for macros. Experiment with some junk text to see
這只是巨集的開始。嘗試一些垃圾文本來查看
what other neat things they can do. When you leave this file you
他們還能做些什麼其他巧妙的事情。當您離開此檔案時，您將
probably DO NOT want to save your changes.
可能不想保存您的更改。


Press Alt-F10 to leave SED without saving any changes.
按 Alt-F10 離開 SED 而不儲存任何變更。


cr .( Use LISTING to print this file and then try editing it. )
cr 。（ 使用 LISTING 列印此文件，然後嘗試編輯它。


B4. A SAMPLE MENU FILE
B4.範例功能表檔案


SMENU.SEQ is an example of menu usage. You can make a copy of this file
斯梅布。SEQ 是菜單使用的一個示例。您可以製作此檔案的副本
and edit it to suit your need. Deferred routine to handle all keys the
並編輯它以滿足您的需求。延遲常式來處理所有索引鍵
menu handler doesn't understand. It can be used to insert any unknown
選單處理程式無法理解。它可以用來插入任何未知的
key pressed in an editor if you want, or it can just throw the keys away
如果需要，可以在編輯器中按下按鍵，或者它可以直接丟棄按鍵
as is done here. The character the menu driver didn't understand is on
就像這裡所做的那樣。菜單驅動程序不理解的字符是
the stack when AOTHER is called.
呼叫 AOTHER 時的堆疊。


The word AMENU is then called whenever a menu operation is to be
然後，每當要進行選單操作時，都會呼叫 AMENU 一詞
performed. In an editing application, use ESC to enable this menu. To
執行。在編輯應用程式中，使用 ESC 啟用此功能表。到
do this you look for the user to press the ESC key while typing in text.
這樣做，您會尋找用戶在鍵入文本時按 ESC 鍵。
If ESC key is pressed, then execute RMENU rather than inserting the next
如果按下 ESC 鍵，則執行 RMENU 而不是插入下一個
key pressed.
按鍵。


only forth also definitions hidden also
只有 forth 也 定義 隱藏 也


\ Install the functions into these deferred words you want performed when
\ 將函數安裝到您想要執行的這些延遲字中
\ a menu item is selected.
\ 已選取功能表項目。


defer item1
防禦項目 1
defer item2
防禦項目2
defer item3
防禦項目 3
defer item4
延期第 4 項
defer item5
防禦項目 5
defer item6
防禦項目 6
defer item7
延期項目7
defer item8
延期項目8
defer item9
防禦項目 9


0 value amsave \ a place to save the previous menu column
0 值 amsave \ 儲存上一個功能表欄的位置
0 value amline \ Menu starting line and column on screen
0 值 amline \ 屏幕上的菜單起始行和列
0 value amcolumn
0 值 amcolumn


newmenu menu1$
新菜單菜單1$
menuline" A item1 Alt-1 " item1
menuline“ A 項目 1 Alt-1 ” 項目 1
menuline" B item2 Alt-2 " item2
menuline“ B 項目 2 Alt-2 ” 項目 2
menuline" --------------------------" noop
menuline“ --------------------------” noop
menuline" C item3 " item3
menuline“ C 項目 3 ” 項目 3
menuline" D item4 Alt-4 " item4
menuline“ D 項目 4 Alt-4 ” 項目 4
menuline" --------------------------" noop
menuline“ --------------------------” noop
menuline" Quit item5 F10 " item5
menuline“ 退出項目 5 F10 ” 項目 5
endmenu
結束功能表


newmenu menu2$
新菜單菜單2$
menuline" E item6 Alt-6 " item6
menuline“ E 項目 6 Alt-6 ” 項目 6
menuline" F item7 Alt-7 " item7
menuline“ F 項目 7 Alt-7 ” 項目 7
menuline" --------------------------" noop
menuline“ --------------------------” noop
menuline" G item8 F8 " item8
菜單行“ G 項目 8 F8” 項目 8
menuline" --------------------------" noop
menuline“ --------------------------” noop
menuline" H item9 F9 " item9
菜單行“ H 項目 9 F9 ” 項目 9
endmenu
結束功能表


newmenubar amenubar
新選單列選單列
+," A menu1 " \ the menu bar contains only two items
+，“ A menu1 ” \ 選單列只包含兩個項目
+," B menu2 "
+，“ B 選單 2 ”
endmenu
結束功能表


create amenulist menu1$ , \ and two lists of functions
建立 amenulist menu1$ 、\ 和兩個函數清單
menu2$ ,
菜單2$ ，


\ initialize the default condition of the menu bar
\ 初始化選單列的預設條件


amenubar =: menubar
amenubar =： 選單列
amenulist =: menulist
amenulist =： menulist
' amline is mline
“阿姆琳就是姆琳
' amcolumn is mcolumn
'Amcolumn 是 Mcolumn
' drop is doother
“下降是做的


defer aother ' drop is aother
推遲其他' drop is aother


: amenu ( -- ) \ the sample menu driver
： amenu （ -- ） \ 範例功能表驅動程式
amsave =: mcol
AMSAVE =： 麥科爾
savemenu
儲存選單
amenubar =: menubar
amenubar =： 選單列
amenulist =: menulist
amenulist =： menulist
['] amline is mline
['] Amline 是 Mline
['] amcolumn is mcolumn
['] amcolumn 是 mcolumn
['] aother is doother
['] aother 是 doother
menu
菜單
restmenu
休息菜單
mcol =: amsave ;
mcol =： 安保存 ;


B5. MY STARTUP MESSAGE
B5.我的啟動訊息


SMESSAGE.SEQ contains an example of how to change the sign-on message to
訊息。SEQ 包含如何將登入訊息變更為
display a user defined message in place of the default system message.
顯示使用者定義的訊息，以取代預設系統訊息。


: myhello ( -- )
：我的你好 （ -- ）
." Hello!" ; \ here is the message
."你好！\ 這是訊息


' myhello is .hello \ install new hello function into .HELLO
' myhello 是 .hello \ 將新的 hello 函數安裝到 .你好


\ We will also disable the displaying of the current file at boot time
\ 我們還將禁用啟動時顯示當前文件


' noop is .curfile
'noop 是 .curfile'


B6. SUBSCREEN SCROLLING
乙6.子螢幕捲動


SSCROLL.SEQ contains an example of how to make the screen scroll only a
捲軸。SEQ 包含如何讓螢幕捲動僅
limited set of lines. The file contains three user words as follows:
有限的線路集。該檔案包含三個使用者字詞，如下所示：


SUB-SET ( n1 -- ) \ set the line where scrolling starts
SUB-SET （ n1 -- ） \ 設定捲動開始的行
SUB-ON \ start sub screen scrolling
SUB-ON \ 開始子螢幕捲動
SUB-OFF \ stop sub screen scrolling
SUB-OFF \ 停止子螢幕捲動


Following is the code to implement sub-screen scrolling:
以下是實現子螢幕捲動的程式碼：


0 value sub-line
0值子線


: sub-scroll ( -- ) \ scroll only a portion of the screen
： 子捲動 （ -- ） \ 僅捲動螢幕的一部分
#line @ sub-line <
#line @ 子行<
if crlf \ scroll only a portion
如果 crlf \ 只捲動一部分
else 0 sub-line 1 max rows 1- min at -line
否則 0 個子行 1 最大行數 1 - 最小值 - 在 -line
0 rows 1- at \ move to last line of screen
0 行 1- 在 \ 移動到屏幕的最後一行
then ;
當時;


\ ******************* User words start here *******************
\ ******************* 使用者字詞從這裡開始*******************


: sub-set ( n1 -- ) \ set the starting sub screen scroll line
： sub-set（ n1 -- ） \ 設定起始子畫面捲動線
1 max 23 min !> sub-line ;
1 最多 23 分鐘 ！> 子線;


: sub-on ( -- ) \ Turn on sub screen scrolling
： sub-on（ -- ） \ 開啟子螢幕捲動
['] sub-scroll is cr ;
['] 子捲軸是 cr ;


: sub-off ( -- ) \ Turn off sub screen scrolling
： sub-off（ -- ） \ 關閉子螢幕捲動
['] crlf is cr ;
['] crlf 是 cr ;


B7. USAGE OF VALUES
乙7.值的使用


SVALUES.SEQ contains an example of how an existing program can be
SVALUES。SEQ 包含現有程式如何
modified to use a VALUE word in place of a VARIABLE to enhance program
修改為使用 VALUE 字代替 VARIABLE 來增強程式
readability and performance. You must be aware that VALUEs are not
可讀性和性能。您必須注意，VALUE 不是
portable. It will make your programs more difficult to move to another
輕便的。這將使您的程序更難轉移到另一個程序
Forth system.
第四個系統。


Observe the use of the word COUNTER in the following program segments.
請觀察以下程式段中 COUNTER 一詞的使用。


\ Program segment using a VARIABLE named COUNTER
\ 使用名為 COUNTER 的 VARIABLE 的程式段


create vowels ," aeiouAEIOU"
創建元音，“aeiouAEIOU”
variable counter
變數計數器


: vcount ( | <string> -- ) \ get count of vowels in <string>
： vcount （ |<string> -- ） \ 取得元<string>音的計數
counter off
計數器關閉
0 word drop
0 字下降
vowels count bounds
元音計數界限
?do here count
？這裡算數
begin i c@ scan dup
開始我 c@掃描 DUP
while 1 counter +!
而1個櫃檯+！
1 -1 d+
1 -1 天+
repeat 2drop
重複 2drop
loop
圈
cr ." Found "
cr。找到”
counter @ . ." vowels" ;
計數器@。元音“;


\ Program segment using a VALUE named COUNTER
\ 使用名為 COUNTER 的 VALUE 的程式段


create vowels ," aeiouAEIOU"
創建元音，“aeiouAEIOU”
0 value counter
0 值計數器


: vvcount ( | <string> -- ) \ get count of vowels in <string>
： vvcount （ |<string> -- ） \ 取得元<string>音的計數
off> counter
非櫃檯>
0 word drop
0 字下降
vowels count bounds
元音計數界限
?do here count
？這裡算數
begin i c@ scan dup
開始我 c@掃描 DUP
while incr> counter
而 incr> 計數器
1 -1 d+
1 -1 天+
repeat 2drop
重複 2drop
loop
圈
cr ." Found "
cr。找到”
counter . ." vowels" ;
計數器。元音“;


B8. POPUP WINDOW
B8.彈出視窗


SWINDOW.SEQ contains an example on how to make a popup window. While it
SWINDOW 的。SEQ 包含如何製作彈出視窗的範例。雖然它
may seem complicated at first, we are really doing only a few simple
乍一看可能看起來很複雜，我們實際上只是在做幾個簡單的
things. We save the screen positon, turn off the cursor, and save the
事情。我們保存屏幕位置，關閉光標，然後保存
screen before drawing the box and writing into it. After the user views
屏幕，然後再畫框並寫入其中。在使用者檢視之後
the box and presses a key, we restore the things we saved. It is
盒子並按下一個鍵，我們恢復我們保存的東西。這是
actually pretty simple.
其實很簡單。


: popup ( -- )
： 彈出視窗（ -- ）
#out @ #line @ 2>r \ save cursor position for later
#out @ #line @ 2>r \ 儲存游標位置以供日後使用
cursor-off \ remove cursor from screen
游標關閉 \ 從螢幕上移除遊標
savescr \ preserve current screen contents
保存\保留目前的螢幕內容
15 05 60 09 box&fill \ DRAW THE BOX on the screen
15 05 60 09 框&填充 \ 在屏幕上繪製框
\ PUT SOME TEXT IN IT
\ 在裡面放一些文字
." This is a sample POPUP window" bcr
."這是一個示例 POPUP 窗口“ bcr
\ following line in reverse video
\ 反向視頻中的後線
>rev ." Screen attributes can be used as well "
>修訂版。螢幕屬性也可以使用 ”
>norm bcr
." Press a key to restore the previous screen"
."按一個鍵恢復上一個畫面”
key drop \ wait for user to press a key
按鍵下放 \ 等待使用者按下按鍵
restscr \ restore previous screen
RestsCR\還原上一個畫面
cursor-on \ turn cursor back on
游標開啟 \ 重新開啟游標
2r> at ; \ restore cursor position
第二>在;\ 恢復光標位置

