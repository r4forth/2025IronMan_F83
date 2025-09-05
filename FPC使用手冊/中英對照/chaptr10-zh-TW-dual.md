CHAPTER 10. USER CONTRIBUTIONS
第 10 章。用戶貢獻




This is the fun part of this manual because it shows the human side of
這是本手冊有趣的部分，因為它展示了人性的一面
F-PC. F-PC is a platform, from which one can launch whatever his
F-PC。F-PC 是一個平台，人們可以從中啟動他的任何內容
imagination carries him. Here you will see how different people use this
想像力承載著他。在這裡您將看到不同的人如何使用它
platform to build a wide variety of programs doing totally different
平台來構建各種程序，做完全不同的
things. Many of them deal with very serious subjects, like object
事情。其中許多涉及非常嚴肅的主題，例如客體
oriented programming, floating point mathematics, etc. Many of them are
定向程式設計、浮點數學等。他們中的許多人是
very lighthearted, drawing pictures, running a clock, printing a banner,
很輕鬆，畫畫、跑時鐘、印橫幅、
and so forth. With such a broad spectrum of topics, you will surely find
依此類推。有了如此廣泛的主題，您一定會發現
many programs useful and enlightening. We hope that in seeing these
許多有用且具有啟發性的程序。我們希望看到這些
applications, you will also be motivated to polish up some of your
應用程序，您還將有動力完善您的一些
programs by adapting them to the F-PC environment and contribute them to
程式，使其適應 F-PC 環境，並貢獻給
this section.
本節。


In F-PC 2.25 there were a set of .ARC files containing contributions from
在 F-PC 2.25 中，有一組 .ARC 檔案包含來自
many users:
許多用戶：


ZIMMER.ARC Utilities provided by Tom Zimmer.
季默。ARC 實用程序由 Tom Zimmer 提供。
SMITH.ARC Floating pointing packages by Bob Smith.
鐵匠。Bob Smith 的 ARC 浮點包。
CURLEY.ARC Disassembler by Charles Cureley.
柯利。查爾斯·庫雷利 （Charles Cureley） 的 ARC 反彙編器。
TING.ARC Multitasking and other applications by C. H. Ting.
婷。ARC 多任務處理和其他應用程序，作者：C. H. Ting。
SMILEY.ARC Graphics by Mark Smiley.
笑臉。馬克·斯邁利 （Mark Smiley） 的 ARC 圖形。
SLICE_FF.ARC Slice data base by Robert Gesswein.
SLICE_FF。羅伯特·格斯溫 （Robert Gesswein） 的 ARC 切片資料庫。
MISC.ARC Extended data objects by George Hawkins.
其他。喬治·霍金斯 （George Hawkins） 的 ARC 擴展數據對象。
MODROW.ARC Clock by Jerry Modrow.
莫德羅。傑里·莫德羅 （Jerry Modrow） 的 ARC 時鐘。
TANG.ARC Multiple precision integer math by S. Y. Tang.
強烈的味道。ARC 多重精度整數數學，作者：S. Y. Tang。


In F-PC 3.5, only the ZIMMER, SMITH, and CURLEY files are retained in
在 F-PC 3.5 中，只有 ZIMMER、SMITH 和 CURLEY 檔案會保留在
the ZIP format, because there is not enough space on the diskettes and
ZIP 格式，因為軟碟上沒有足夠的空間，並且
there is not enough time to test all the user contributions on the
沒有足夠的時間來測試所有使用者貢獻
enhanced platform. The contributions not included will be distributed
增強的平台。未包括的捐款將被分配
separately from F-PC by the Silicon Valley FIG Chapter after they are
與 F-PC 分開，由矽谷 FIG 分會分開，之後
tested and verified.
經過測試和驗證。


10.1. FROM TOM ZIMMER
10.1. 來自湯姆·齊默


Tom Zimmer is the principal author of F-PC, besides many other Forth
湯姆·齊默 （Tom Zimmer） 是《F-PC》的主要作者，此外還有許多其他 Forth
systems and applications. The files in ZIMMER.ARC are examples of his
系統和應用程序。The files in ZIMMER.ARC 是他的例子
minor works tailored for F-PC.
為 F-PC 量身定制的小作品。


AUTOFOR.SEQ
自動。序


This file contains the tools to allow automatic forward reference
此檔案包含允許自動前向參照的工具
resolution of Forth words. There is a runtime overhead which is
第四個詞的解決。運行時額外負荷是
equivalent to a DEFERred word. Words that are forward referenced are
相當於 DEFERred 字。前向引用的單字是
automatically defined, and then when really defined, they are
自動定義，然後當真正定義時，它們是
automatically resolved.
自動解決。


AUTOLOAD.SEQ
自動載入。序


A simple utility to make F-PC load a file automatically at boot time. Add
一個簡單的實用程序，可使 F-PC 在啟動時自動載入檔案。加
this to the system and resave the system. Place your forth commands in
這給系統並重新保存系統。將您的第四個命令放在
the file F-PC.CFG and they will be executed before F-PC handles the
檔案 F-PC。CFG 的 CFG ，它們將在 F-PC 處理
command line.
命令列。


BLKTOSEQ.SEQ
BLKTOSEQ。序


This file contains the source for a utility to convert your .BLK files
此檔案包含公用程式的來源，可將 .BLK 檔案
into .SEQ files. Type the following to convert a file:
進入 。SEQ 檔案。輸入下列內容以轉換檔案：


FLOAD BLKTOSEQ <enter>
CONV <enter>
轉換<enter>
<file_to_convert> <enter>


You will be prompted for a name of a block file. The .BLK file will be
系統會提示您輸入區塊檔案的名稱。這。BLK 檔案將是
converted to a sequential file, with the new extension .SEQ. All extra
轉換為順序文件，副檔名為 .SEQ。所有額外
blank lines will be omitted. Shadow screens in .BLK files will be
空行將被省略。中的陰影幕。BLK 檔案將是
enclosed in F-PC's "Comment:" mechanism, and appended to each source
包含在 F-PC 的「評論：」機制中，並附加到每個來源
block. If a BLOCK file does not have shadows, then change its extension
塞。如果 BLOCK 檔案沒有陰影，則變更其副檔名
to .SCR, and F-PC will convert all screens sequentially.
到。SCR 和 F-PC 將按順序轉換所有螢幕。


BLOCK.SEQ
塞。序


A new virtual block system for Forth. This is Tom's own implementation.
Forth 的新虛擬方塊系統。這是湯姆自己的實作。
It is very fast, and uses a true 'Least Recently Used' buffer allocation
它非常快，並且使用真正的「最近最少使用」緩衝區分配
mechanism. You can also change the block size to be anything you want,
機械。您還可以將塊大小更改為您想要的任何大小，
as well as specify as many or as few block buffers as you can hold in
以及指定您可以保留的盡可能多或盡可能少的區塊緩衝區
memory.
記性。


BOOKMARK.SEQ
書籤。序


A Bookmark utility for the F-PC editor, allows saving and restoring 5
F-PC 編輯器的書籤實用程序，允許保存和恢復 5
different file and line offsets. For example:
不同的檔案和線偏移。比如：


OPEN F-PC 3 LIST \ Open a file and specify a line.
開啟 F-PC 3 清單 \ 開啟檔案並指定一行。
M1 \ Save place with Bookmark # 1
M1 \ 使用書籤保存地點 #1
OPEN SEDITOR \ Open the editor
開啟編輯器 \ 開啟編輯器
400 LIST \ Specify line 400
400 LIST \ 指定第 400 行
M2 \ Save place with Bookmark # 2
M2 \ 使用書籤保存位置 #2
BM1 \ Go Back to bookMark # 1
BM1 \ 返回書籤 #1
L \ List line 3 of F-PC
L \ F-PC 的第 3 行列表
BM2 \ Go Back to bookMark # 2
BM2 \ 返回書籤 #2
L \ List line 400 of SEDITOR
L \ SEDITOR 的第 400 行列表


M1 to M5 and BM1 to BM5 are valid bookmarks.
M1 到 M5 和 BM1 到 BM5 是有效的書籤。


CARDFILE.SEQ
卡片檔案。序


A card contains 1024 characters arranged in 16 lines of 64 characters.
一張卡片包含 1024 個字符，排列成 16 行，每行 64 個字符。
CARDFILE uses menus and windows to edit and manipulate cards. Back to
CARDFILE 使用菜單和窗口來編輯和操作卡片。返回
blocks!
塊！


CODEHIGH.SEQ
CODEHIGH 的。序


Utility to allow calling high level words from assembly (code)
允許從彙編調用高級單詞的實用程序（代碼）
definitions.
定義。


COMMAND.SEQ
令。序


A nestable comment line entry routine. Can be placed in a program to
可巢狀註解行輸入常式。可以放置在程式中，以
allow entering Forth commands without fear of aborting the currently
允許輸入 Forth 命令，而不必擔心中止當前
running Forth word.
跑出一個字。


CONSTANT.SEQ
恆。序


A utility to allow defining multiple constants and variables as follows:
允許定義多個常數和變數的公用程式，如下所示：


CONSTANTS 3 george 12 robert
常數 3 喬治 12 羅伯特
14 betty 72 bongo ;
14 貝蒂 72 邦戈;


VARIABLES Gort! clatoo
變數戈特！克拉圖
borada nicto ;
博拉達·尼克托;


Note the ";" terminating the list of constants. If you use multiple
請注意終止常數清單的 “;”。如果您使用多個
lines, you can put "\" delimited comments on the same line as the
行，您可以將 “\” 分隔的註解放在與
constants or variables.
常數或變數。


DOSIO.SEQ
多西奧。序


A conversion utility to allow F-PC to accept re-directed input and output
允許 F-PC 接受重定向輸入和輸出的轉換實用程序
from the DOS command line. You can make filters that use all of the
從 DOS 命令列。您可以製作使用所有
power of Forth.
福斯的力量。


EVAL.SEQ
評估。序


A utility to allow run-time interpretation of compiled strings. This
允許執行階段解譯已編譯字串的公用程式。這
implements text macros.
實作文字巨集。


EMMEXMPL.SEQ
埃默姆普爾。序


An example of how to use the Expanded Memory Manager. Tests and uses
如何使用擴充記憶體管理員的範例。測試和用途
expanded memory to save a bunch of screens and display them on the screen
擴充記憶體，保存一堆螢幕，顯示在螢幕上
very quickly.
很快。


EMMHEADS.SEQ
埃姆黑茲。序


After loading EXPANDED.SEQ, you can load this file and save the system to
加載 EXPANDED 後。SEQ，您可以載入此檔案並將系統儲存至
a new file. The new resulting .EXE file will use expanded memory for
一個新檔案。新的生成.EXE 檔案將使用擴充記憶體來
HEADS, freeing up 64k of normal RAM for other uses. This will mostly be
HEADS，釋放 64k 的普通 RAM 用於其他用途。這主要是
useful if you are trying to write a LARGE application.
如果您嘗試編寫大型應用程式，則很有用。


EXPANDED.SEQ
擴大。序


An interface to EMM (Expanded Memory Manager). Most of this file was
EMM（擴展內存管理器）的接口。該文件的大部分內容是
developed by using the examples right out of the INTEL book.
使用英特爾書中的示例開發。


FORWARD.SEQ
前。序


A neat mechanism to handle forward references, and have them
處理前向引用的簡潔機制，並擁有它們
automatically resolved.
自動解決。


FUNKEY.SEQ
FUNKEY 的。序


A simple utility to allow the 10 function keys to be assigned to Forth
一個簡單的實用程序，允許將 10 個功能鍵分配給 Forth
words. Saves some key strokes.
言。節省一些按鍵。


HANOI.SEQ
河內。序


A cute demo of a character graphics Towers of Hanoi.
河內塔的角色圖形的可愛演示。


LOCALS.SEQ
當地人。序


An implementation of local variables for F-PC, places then in a separate
F-PC 局部變數的實作，然後放置在單獨的
stack for flexibility. Four locals are defined, LOCALA through LOCALD. A
堆疊以獲得靈活性。定義了四個本地人，LOCALA 到 LOCALD。一個
simple syntax is provided for allocating these variables, and
提供簡單的語法來分配這些變數，並且
deallocation is automatic at definition end.
解除配置會在定義結束時自動執行。


MONITOR.SEQ
班長。序


An on screen editor, allows you to cursor up and change all the stuff on
屏幕編輯器，允許您向上遊標並更改所有內容
the screen, then re-enter it by pressing <enter> on a line.
屏幕，然後按<enter>一行重新進入它。


NEWCOM.SEQ
新通訊。序


A utility to allow the easy creation of VERY SMALL .COM files.
一個允許輕鬆創建非常小的.COM 文件的實用程序。


OBJECT.SEQ
物體。序


Object oriented utility words from Forth Dimensions Volume 10, number 2
來自 Forth Dimensions 第 10 卷第 2 期的面向對象實用詞
by Rick Hoselton. Sightly modified to run on F-PC.
里克·霍塞爾頓 （Rick Hoselton） 著。視覺上修改為在 F-PC 上運行。


SCROLL.SEQ
卷。序


Some simple code utilities to allow scrolling an area of the screen as
一些簡單的代碼實用程序，允許將屏幕的某個區域滾動為
specified by two pairs of x/y coordinates up or down one line.
由兩對 X/Y 座標向上或向下一行指定。


SEQTOBLK.SEQ
塞克托布爾克。序


This file contains the source for a utility to convert your .SEQ files
此檔案包含公用程式的來源，可將 .SEQ 檔案
back to .SCR files. Type the following to convert a file:
返回 。SCR 檔案。輸入下列內容以轉換檔案：


FLOAD SEQTOBLK <enter>
CONV <enter>
轉換<enter>
<file_to_convert> <enter>


You will be prompted for a name of the sequential file. The .SEQ file
系統會提示您輸入循序檔案的名稱。這。SEQ 檔案
will be converted to a BLOCK file, with the new extension .SCR. Screen 0
將轉換為 BLOCK 文件，副檔名為 .SCR。螢幕 0
will be blank. The first line of each block will be blank, preceded by a
將是空白的。每個區塊的第一行將是空白的，前面有一個
"\". The last line of each block will also be blank. The resulting will
"\".每個區塊的最後一行也將是空白的。由此產生的遺囑
be an exact multiple of 1024 bytes in length. The resulting file will
是長度為 1024 位元組的精確倍數。產生的檔案將
need to be substantially edited, to move entire definitions onto one
需要進行大量編輯，將整個定義移到一個定義上
screen, as they are likely to be split across screens in the move.
屏幕，因為它們很可能在移動中被分割到各個屏幕。


WINDEX.SEQ
WINDEX。序


Displays a more or less alphabetized list of Forth words showing
顯示或多或少按字母順序排列的 Forth 單字清單，顯示
vocabulary and file where it was defined. Just type
詞彙表和定義位置的檔案。只需輸入


ALLWORDS <enter>
所有詞<enter>


to display an index of all forth words. Load PRINT.SEQ and use PFILE
以顯示所有第四個單字的索引。載入 PRINT。SEQ 並使用 PFILE
<name>, then print the file to disk with
<name>，然後使用


PRINT ALLWORDS.
列印所有字詞。


WINDOW.SEQ
窗。序


A nice window package for Forth. Much is in assembly, so its very fast.
福斯的一個不錯的窗口包。很多東西都在組裝中，所以速度非常快。
Primarily useful in an application package. Try the demo.
主要在應用程式套件中有用。嘗試演示。


WYSE50.SEQ
WYSE50 號。序


A simple package to allow EMITted Wyse 50 terminal escape codes to be
一個簡單的封裝，允許 EMITted Wyse 50 終端轉義碼
emulated on the IBM screen. This has limited functionality, since only a
在 IBM 屏幕上模擬。這的功能有限，因為只有
few of the sequences are implemented.
很少有序列被實現。


10.2. FROM CHARLES CURLEY
10.2. 來自查爾斯·柯利


Charles Curley is the F-PC team's devil's advocate. His lean, mean,
查爾斯·柯利 （Charles Curley） 是 F-PC 團隊的魔鬼代言人。他瘦弱、卑鄙、
implementations of real- FORTH run on 6502, 6809, LSI-11, 80X8X and
在 6502、6809、LSI-11、80X8X 和
680XX, both under operating systems and stand alone. Prior to working at
680XX，無論是在操作系統下還是獨立。在工作之前
Maxtor he worked at or contracted to Rockwell International, Jet
他曾在 Jet 的 Rockwell International 工作或與 Rockwell International 簽約
Propulsion Lab, Hughes Aircraft, Strand Lighting and other companies.
推進實驗室、休斯飛機、Strand Lighting 等公司。
His code has been used to check out the Gallileo spacecraft, write and
他的程式碼已被用於檢查加利略太空船、編寫和
debug rock shooting games, and light exhibits at world fairs. He sees
調試搖滾射擊遊戲，並在世界博覽會上進行燈光展覽。他看到了
F-PC as a sneaky plot to sell more Maxtor hard disk drives.
F-PC 作為銷售更多邁拓硬碟的偷偷摸摸的陰謀。


DISASSEM.SEQ
迪薩西姆。序


A 8086 disassembler. This disassembler is patched into SEE, so all you
8086 反彙編器。這個反組譯器已修補到 SEE 中，所以所有你
have to do is type:
必須做的是輸入：


SEE <code_word> <enter>
看 <code_word> <enter>


You will see a line of Assembly code. Continuing to press <enter> after
您將看到一行彙編代碼。繼續按<enter>後
each line shows additional instructions. Press ESC to terminate
每一行都顯示其他指示。按 ESC 終止
disassembly.
拆卸。


You can also disassemble from an address:
您也可以從位址進行反組譯：


<addr> DISASSEM <enter>
<addr> 迪薩西姆<enter>


The disassembler displays Postfix notation ala F83.
反組譯器會顯示 F83 的後綴表示法。


FDIS.SEQ
外國金融業。序


A disassembler for 8087 machine code. Extension of the F-PC
8087 機器碼的反彙編器。F-PC 的擴展
disassembler. Bob Smith did it, but the file is grouped here.
反彙編器。鮑勃·史密斯做到了，但文件在這裡分組。


DIS8086.SEQ
DIS8086。序


Donation from Bill Muench, is a modified version of Curley's DISASSEM.SEQ
Bill Muench 的捐贈是 Curley 的 DISASSEM 的修改版本。序
above, adjusted to disassemble in PREFIX mode. The disassembly can be
以上，調整為在 PREFIX 模式下拆卸。拆卸可以是
sent to a file from either of the above files by using PFILE to specify a
從上述任一檔案傳送至檔案，方法是使用 PFILE 指定
<printfile>, then typing:
<printfile>，然後輸入：


PFILE EXIT.SEQ <enter>
PFILE 結束。序<enter>
PRINT SEE EXIT <enter>
列印 參見出口<enter>
PCLOSE <enter>
關閉<enter>


to disassemble EXIT to the file EXIT.SEQ.
將 EXIT 反組譯為檔案 EXIT.SEQ。


10.3. FROM BOB SMITH
10.3. 來自鮑勃·史密斯


Dr. Robert L. Smith was a member of IEEE Floating Point Standards
Robert L. Smith 博士是 IEEE 浮點標準的成員
Committee. He was also a member of the Forth Implementation Team which
委員會。他也是第四個實施團隊的成員，該團隊
gave us figForth. He has heavily participated in the Forth Standards
給了我們 figForth。他大量參與了第四標準
Team and the current ANS Forth Standards Committee. Bob is well know for
團隊和現任 ANS Forth 標準委員會。鮑勃眾所周知
his meticulous coding style and his attention to precision to the last
他一絲不苟的編碼風格和對精確度的關注到最後
half bit. He generously contributed his 8087 floating point package and
半位。他慷慨地貢獻了他的 8087 浮點包和
a software floating point package to F-PC.
F-PC 的軟件浮點包。


COMPLEX.SEQ
繁。序


Some complex number routines, notably, a complex square root algorithm.
一些複數例程，特別是複平方根演算法。
Requires HFLOAT or SFLOAT and FLT-EXT.
需要 HFLOAT 或 SFLOAT 和 FLT-EXT。


DMULDIV.SEQ
德穆爾迪夫。序


A 64 bit by 32 bit mixed divide, with a 32 bit quotient and a 32 bit
64 位 x 32 位混合除法，具有 32 位商和 32 位
remainder result. Also, a 32 bit by 32 bit multiply, yielding a 64 bit
剩餘結果。此外，32 位乘以 32 位，得到 64 位
product (all unsigned). Written by Robert L. Smith in 8086 assembly.
產品（全部未簽名）。由羅伯特·史密斯 （Robert L. Smith） 在 8086 年集會中撰寫。


HFLOAT.SEQ
HFLOAT 的。序


Software support for the 8087 floating point chip. This package was
8087浮點晶片的軟體支援。這個包裹是
modified from a version by Mark Smiley to support the prefix assembler
從 Mark Smiley 的版本修改為支援前置詞組譯器
used in F-PC.
用於 F-PC。


SFLOAT.SEQ
SFLOAT 的。序


Software floating point package for those of us who don't have an 8087.
軟件浮點包，適合我們這些沒有 8087 的人。
It is compatible with the Forth Venders Group floating point standard.
它與 Forth Venders Group 浮點標準相容。
Several files are loaded by SFLOAT.SEQ. This IS a COPYRIGHTed package,
SFLOAT.SEQ 會載入數個檔案。這是一個受版權保護的包，
and may be used for your personal purposes only. You may not sell it as
並且只能用於您的個人目的。您不得將其作為
part of any software package without the consent of Robert Smith.
未經 Robert Smith 同意的任何軟件包的一部分。


This is a software floating point package for use with the F-PC Forth
這是一個軟體浮點套件，可與 F-PC Forth 搭配使用
system. It follows most of the recommendations of the FVG (Forth Vendors
系統。它遵循 FVG（第四供應商）的大部分建議
Group) Standard Floating-Point Extension. The intention is that the
Group） 標準浮點擴展。其目的是
functions be as accurate as is reasonable, consistent with speed as the
函數應盡可能準確，與速度一致，如
secondary goal. The basic four functions plus square root should be
次要目標。基本四個函數加上平方根應該是
precise to one half a bit in the least significant bit of the
精確到最低有效位的半位
representation. The higher functions have intrinsic errors no larger
代表。較高的函數具有不大的固有誤差
than one bit in the least significant place.
比最不重要的位置的一位。


The representation uses a 16 bit word for the sign and biased exponent of
該表示使用 16 位字作為符號和偏向指數
the floating point number, and 32 bits for the significand (sometimes
浮點數，以及有效值和 32 位（有時
called the "mantissa"). That means that the intrinsic accuracy is
稱為“尾數”）。這意味著內在精度為
approximately 9 and a half decimal digits. The largest and smallest
大約十進制點後 9 個半數字。最大和最小
representable numbers cover roughly the range from 10 to the plus and
可表示的數字大致涵蓋從 10 到加號的範圍，並且
minus 4000 power, which is far greater than almost anyone would ever
減去 4000 的功率，這遠遠超過了幾乎任何人
need. The representation does NOT include special cases for infinity,
需。表示不包括無窮大的特殊情況，
unnormalized numbers, and Not-A-Number. The format is definitely NOT the
非正規化數字和非 A 數字。格式絕對不是
IEEE Floating Point Standard format. The reason is basically one of
IEEE 浮點標準格式。原因基本上是
speed. The functions in this package are approximately 5 (FIVE) times
速度。此套件中的功能約為 5 （五） 次
faster than software implementations using the IEEE standard. In spite
比使用 IEEE 標準的軟體實作更快。儘管如此
of that, it does meet the basic requirement of having the basic four
其中，它確實滿足了擁有基本四項的基本要求
functions be accurate to within one-half a bit. The precision is
函數的精度在二分之一位以內。精度為
somewhat greater than one would obtain from the 32-bit IEEE format.
略大於從 32 位 IEEE 格式獲得的。


To load the package from F-PC, type FLOAD SFLOAT followed by a carriage
若要從 F-PC 載入套件，請鍵入 FLOAD SFLOAT，然後鍵入托架
return. After SFLOAT has been loaded, you may enter floating point
回。載入 SFLOAT 後，您可以輸入浮點
numbers in exponential format. The following is a list of possible
指數格式的數字。以下是可能的清單
entries:
條目：


-1.2345E4
.9876E-3
.9876E-3 號
123.456(10)


The rules are: If the number is negative, it must be preceded with a
規則是：如果數字為負數，則必須以
minus sign. Do not use "+" with positive numbers. The separator between
減號。請勿將「+」與正數搭配使用。之間的分隔符
the mantissa and exponent must be either the letter "E" or a left
尾數和指數必須是字母「E」或左
parenthesis. In the examples above, the "E" is used for compliance with
括弧。在上述範例中，「E」用於符合
FVG, but the left parenthesis may be used, especially if you desire to
FVG，但可以使用左括號，特別是如果您希望
enter your numbers in another base. The terminating symbol may be
在另一個基數中輸入您的數字。終止符號可以是
omitted, but you may wish to use a right parenthesis, as in the third
省略，但您可能希望使用右括號，如第三個
example above.
上面的例子。


The simplest numeric output is E. . Other possible functions are: E.R ,
最簡單的數值輸出是 E。其他可能的功能包括：E.R、
F. , and F.R . There is also a floating point stack printout word, .FS .
F. 和 F.R .還有一個浮點堆疊列印字。FS .
If you wish to turn off the Floating Point interpreter, enter NOFLOATING
如果您想要關閉浮點解譯器，請輸入 NOFLOATING
. To re-enter the floating point interpreter, enter FLOATING .
.若要重新進入浮點解譯器，請輸入 FLOATING 。


FLOATING POINT GLOSSARY
浮點詞彙表


The low level words in the HFLOAT and SFLOAT packages differ
HFLOAT 和 SFLOAT 套件中的低階字不同
significantly because of the hardware facilities. However, the high
很大程度上是因為硬體設施。然而，高
level application words are very similar, based on the proposed FVG
水平應用詞非常相似，基於提出的 FVG
floating point standard. These high level words will be used in
浮點標準。這些高級詞將用於
applications requiring floating point numbers. It is thus appropriate to
需要浮點數的應用程式。因此，適合
summarize this set of high level floating point words common to both
總結這組兩者共有的高階浮點字
HFLOAT and SFLOAT.
HFLOAT 和 SFLOAT。


HFLOAT/SFLOAT GLOSSARY
HFLOAT/SFLOAT 詞彙表


FLOATING POINT STACK WORDS
浮點堆疊字


FDUP ( F: r -- r r )
FDUP （ F： r -- r r ）
Duplicate the floating point number at the top of the stack.
複製堆疊頂端的浮點數。


FDROP ( F: r -- )
FDROP （ F： r -- ）
Drop the top floating point number from the stack.
從堆疊中捨棄最上方的浮點數。


FNIP ( F: r1 r2 -- r1 )
FNIP （ F： r1 r2 -- r1 ）
Remove the second floating point number from the stack.
從堆疊中移除第二個浮點數。
Equivalent to FSWAP FDROP .
相當於 FSWAP FDROP 。


FOVER ( F: r1 r2 -- r1 r2 r1 )
FOVER （ F： r1 r2 -- r1 r2 r1 ）
Push a copy of the floating point number second on the stack.
將浮點數字的副本推送到堆棧上。


FSWAP ( F: r1 r2 -- r2 r1 )
FSWAP （ F： r1 r2 -- r2 r1 ）
Interchange the top two floating point numbers on the stack.
交換堆疊上前兩個浮點數。


FROT ( F: r1 r2 r3 -- r2 r3 r1 )
FROT （ F： r1 r2 r3 -- r2 r3 r1 ）
Rotate the top three elements on the floating point stack,
旋轉浮點堆疊上的前三個元素，
bringing the third element to the top.
將第三個元素帶到頂部。


F-ROT ( F: r1 r2 r3 -- r3 r1 r2 )
F-腐爛 （ F： r1 r2 r3 -- r3 r1 r2 ）
Reverse rotate the top three elements on the floating point
反向旋轉浮點上前三個元素
stack, putting the top element to the third position.
堆疊，將頂部元素放在第三個位置。


FPICK ( F: rn rn-1 ... r0 -- rn rn-1 ... r0 rn ; n -- )
FPICK （ F： rn rn-1 ...r0 -- rn rn-1 ...r0 rn ;n -- )
Using a zero referenced value of n , pick the n-th value from the
使用零參考值 n ，從
floating point stack and push it onto the floating point stack.
浮點堆疊，並將其推送到浮點堆疊上。
Thus 0 FPICK is equivalent to FDUP .
因此，0 FPICK 相當於 FDUP 。


FNSWAP ( F: rn rn-1 ... r0 -- r0 rn-1 ... r1 rn ; n -- )
FNSWAP （ F： rn rn-1 ...r0 -- r0 rn-1 ...r1 rn ;n -- )
Exchange the floating point value at the n-th location on the
交換
floating point stack with the floating point value at the top of
浮點堆疊，浮點值位於
the floating point stack. Thus 1 FNSWAP is equivalent to FSWAP
浮點堆疊。因此，1 個 FNSWAP 相當於 FSWAP
.


FLOATING POINT MATH WORDS
浮點數學單字


F- ( F: r1 r2 -- r3 )
F- （ F：r1 r2 -- r3 ）
Subtract the floating point number at the top of the stack from
從中減去堆疊頂部的浮點數
the floating point number second on the stack. Report overflow
堆疊上的浮點數秒。報表溢位
errors.
錯誤。


F\- ( F: r1 r2 -- r3 )
F\- （ F： r1 r2 -- r3 ）
Reverse subtraction. Subtract the floating point number second
反向減法。減去浮點數秒
on the stack from the floating point number at the top of the
從頂部的浮點數
stack. Report overflow errors.
堆。報告溢位錯誤。


F+ ( F: r1 r2 -- r3 )
F+ （ F： r1 r2 -- r3 ）
Add the two floating point numbers at the top of the stack. The
將堆疊頂端的兩個浮點數相加。這
result is placed back on the stack. Report overflow errors.
結果放回堆疊上。報告溢位錯誤。


F* ( F: r1 r2 -- r3 )
F* （ F： r1 r2 -- r3 ）
Multiply the top two floating point numbers on the stack. Report
將堆疊上前兩個浮點數相乘。報
overflow errors.
溢位錯誤。


F/ ( F: r1 r2 -- r3 )
F/ （ F： r1 r2 -- r3 ）
Divide the floating point number second on the stack by the
將堆疊上的浮點數秒除以
floating point number at the top of the stack. Report overflow
堆疊頂端的浮點數。報表溢位
errors and division by zero.
錯誤和除以零。


FSQRT ( F: r1 -- r2 )
FSQRT （ F： r1 -- r2 ）
Replace the floating point number at the top of the stack with
將堆疊頂端的浮點數取代為
its square root. Report an error if r1 is negative.
它的平方根。如果 r1 為負數，請報告錯誤。


FMAX ( F: r1 r2 -- r3 )
FMAX （ F： r1 r2 -- r3 ）
Replace the top two numbers on the floating point stack with the
將浮點堆疊上前兩個數字取代為
greater of the two.
兩者中更大的。


FMIN ( F: r1 r2 -- r3 )
FMIN （ F： r1 r2 -- r3 ）
Replace the top two numbers on the floating point stack with the
將浮點堆疊上前兩個數字取代為
smaller of the two.
兩者中較小。


FABS ( F: r1 -- r2 )
FABS （ F： r1 -- r2 ）
Replace the floating point number at the top of the floating
取代浮動頂部的浮點數
point stack with its absolute value.
point stack 及其絕對值。


FNEGATE ( F: r1 -- r2 )
FNEGATE （ F： r1 -- r2 ）
Negate the floating point number at the top of the floating
否定浮動頂部的浮點數
point stack.
點堆疊。


1/F ( F: r1 -- r2 )
1 樓 （ F： r1 -- r2 ）
Take the reciprocal of the floating point argument.
以浮點論數的倒數為例。


FLOATING POINT LOGIC WORDS
浮點邏輯字


F0< ( F: r1 -- ; -- flag )
F0< （ F： r1 -- ; -- 旗標 ）
Test the floating point number at the top of the floating point
測試浮點頂部的浮點數
stack. If the number is less than zero, push a -1 flag on the
堆。如果數字小於零，請在
parameter stack. If the floating point number is greater than or
參數堆疊。如果浮點數大於 或
equal to zero, push a 0 flag on the parameter stack. In either
等於零，則在參數堆疊上推送 0 旗標。在任一
case, drop the floating point number from the floating point
case，則從浮點中刪除浮點數
stack.
堆。


F0> ( F: r1 -- ; -- flag )
F0> （ F： r1 -- ; -- 旗幟 ）
Test the floating point number at the top of the stack, then
測試堆疊頂端的浮點數，然後
drop the number. If the number was greater than zero, push a -1
刪除數字。如果數字大於零，請按 -1
flag on the parameter stack. Otherwise push a zero.
參數堆疊上的旗標。否則推一個零。


F0= ( F: r -- ; -- flag )
F0= （ F： r -- ; -- 旗幟 ）
Test the floating point number at the top of the stack, then
測試堆疊頂端的浮點數，然後
drop it. If the number is zero, push a -1 on the parameter stack.
放下它。如果數字為零，請在參數堆疊上按 -1。
The flag is set to 0 if the floating point number was not zero.
如果浮點數不是零，則旗標會設為 0。


F= ( F: r1 r2 -- ; -- flag )
F= （ F： r1 r2 -- ; -- 旗幟 ）
Compare the top two floating point numbers. If the numbers are
比較前兩個浮點數。如果數字是
equal, push a flag of -1 on the parameter stack. If the two
等於，則在參數堆疊上推送旗標 -1。如果兩個
numbers are not equal, push a zero. In either case, drop the two
數字不相等，推一個零。無論哪種情況，都刪除兩個
numbers from the floating point stack.
浮點堆疊中的數字。


F< ( F: r1 r2 -- ; -- flag )
F< （ F： r1 r2 -- ; -- 旗幟 ）
Compare the top two floating point numbers. If the number
比較前兩個浮點數。如果數字
second on the floating point stack is less than the top number,
浮點堆疊上的第二個小於頂部的數字，
push a flag of -1 onto the parameter stack. Otherwise push a 0
將旗標 -1 推送到參數堆疊上。否則，請推 0
onto the parameter stack. In either case, the top two numbers on
到參數堆疊上。無論哪種情況，上
the floating point stack are dropped.
浮點堆疊會捨棄。


F> ( F: r1 r2 -- ; -- flag )
F> （ F： r1 r2 -- ; -- 旗幟 ）
Compare the top two floating point numbers. If the number
比較前兩個浮點數。如果數字
second on the floating point stack is greater than the top
浮點堆疊上的第二個大於頂部
number, push a flag of -1 onto the parameter stack. Otherwise
number，則將旗標 -1 推送到參數堆疊上。否則
push a 0 onto the parameter stack. In either case, the top two
將 0 推送到參數堆疊上。無論哪種情況，前兩名
numbers on the floating point stack are dropped.
浮點堆疊上的數字會被丟棄。


TRANSDENTIAL FUNCTIONS
跨齒功能


FLN ( F: r1 -- r2 )
民陣 （ F： r1 -- r2 ）
Natural logarithm function. Time: 1260 usec.
自然對數函數。時間：1260 usec。


FLOG ( F: r1 -- r2 )
FLOG （ F： r1 -- r2 ）
Logarithm of base 10.
以 10 為底的對數。


FEXP ( F: r1 -- r2 )
FEXP （ F： r1 -- r2 ）
Floating point exponential function e^x
浮點指數函數 e^x


FALN ( F: r1 -- r2 )
FALN （ F： r1 -- r2 ）
Alternative name for the exponential function. This is the name
指數函數的替代名稱。這就是名字
specified in the FVG Standard Floating Point Extension.
在 FVG 標準浮點擴展中指定。


FALOG ( F: r1 -- r2 )
法洛格 （ F： r1 -- r2 ）
Take the inverse log of r1, i.e., raise 10 to the power of r1.
取 r1 的逆對數，即將 10 提高到 r1 的次方。


FTAN ( F: r1 -- r2 )
FTAN （ F： r1 -- r2 ）
The input is a floating point number in radians. The output is
輸入是以弧度為單位的浮點數。輸出為
is the tangent of the number. An error condition exists for
是數字的切線。存在錯誤條件
sufficiently large input values.
足夠大的輸入值。


FSIN ( F: r1 -- r2 )
FSIN （ F： r1 -- r2 ）
Returns the sine of the input number in radians. Input and
傳回輸入數字的正弦，以弧度為單位。Input 和
output values are floating point numbers. An error condition
輸出值是浮點數。錯誤狀況
exists for sufficiently large input values.
存在足夠大的輸入值。


FCOS ( F: r1 -- r2 )
FCOS （ F： r1 -- r2 ）
Returns the cosine of the floating point argument in radians. An
傳回浮點引數的餘弦，以弧度為單位。一
error condition exists for sufficiently large input arguments.
對於足夠大的輸入引數，存在錯誤條件。


FATAN ( F: r1 -- r2 )
法坦 （ F： r1 -- r2 ）
Returns a floating point value equal to the arctangent of the
傳回等於
input argument. The result is expressed in radians.
input 引數。結果以弧度表示。


FASIN ( F: r1 -- r2 )
法辛 （ F： r1 -- r2 ）
Returns a floating point value equal to the arcsine of the input
傳回等於輸入反正弦的浮點值
argument. The result is expressed in radians. If the input
論點。結果以弧度表示。如果輸入
argument exceeds 1.0 in value, an error condition results.
引數的值超過 1.0，則會產生錯誤狀況。


FACOS ( F: r1 -- r2 )
FACOS （ F： r1 -- r2 ）
Returns a floating point value equal to the arccosine of the
傳回等於
input argument. The result is expressed in radians. If the input
input 引數。結果以弧度表示。如果輸入
argument exceeds 1.0 in value, an error condition results.
引數的值超過 1.0，則會產生錯誤狀況。


FSINH ( F: r1 -- r2 )
FSINH （ F： r1 -- r2 ）
Hyberbolic sin function. Not in HFLOAT.
高博罪功能。不在 HFLOAT 中。


FCOSH ( F: r1 -- r2 )
FCOSH （ F： r1 -- r2 ）
Hyperbolic cosine function. Not in HFLOAT.
雙曲餘弦函數。不在 HFLOAT 中。


FTANH ( F: r1 -- r2 )
FTANH （ F： r1 -- r2 ）
Hyperbolic tangent function. Not in HFLOAT.
雙曲正切函數。不在 HFLOAT 中。


FASINH ( F: r1 -- r2 )
法辛 （ F： r1 -- r2 ）
Inverse hyperbolic sin function. Not in HFLOAT.
逆雙曲罪函數。不在 HFLOAT 中。


FACOSH ( F: r1 -- r2 )
法科什 （ F： r1 -- r2 ）
Inverse hyperbolic cosine function. Not in HFLOAT.
反雙曲餘弦函數。不在 HFLOAT 中。


FATANH ( F: r1 -- r2 )
法坦 （ F： r1 -- r2 ）
Inverse hyperbolic tangent function. Not in HFLOAT.
反雙曲正切函數。不在 HFLOAT 中。


FTRIG0 ( F: r1 -- r2 )
FTRIG0 （ F： r1 -- r2 ）
Returns a floating point value equal to the square root of the
傳回等於
absolute value of (1.0 - (r1^2)). This is a useful auxiliary
絕對值為 （1.0 - （r1^2））。這是一個有用的輔助工具
function suggested in APL. Not in HFLOAT.
APL 中建議的功能。不在 HFLOAT 中。


FLN2 ( F: -- r1 )
FLN2 （ F： -- r1 ）
Push a floating point number with a value approximately equal to
推送一個值約等於
the natural logarithm of 2. Not in HFLOAT.
2 的自然對數。不在 HFLOAT 中。


F**N ( F: r1 -- r2 ; n -- )
F**N （ F： r1 -- r2 ; n -- ）
Raise the floating point number to the integral power specified
將浮點數提高到指定的整數冪
by the number on top of the parameter stack. Not in HFLOAT.
依參數堆疊頂端的數字。不在 HFLOAT 中。


F/LN2 ( F: r -- r/ln2 )
F/LN2 （ F： r -- r/ln2 ）
Divide the floating point number by the natural logarithm of 2.
將浮點數除以自然對數 2。
Not in HFLOAT.
不在 HFLOAT 中。


MISCELLANEOUS WORDS
雜詞


FCONSTANT ( F: -- r )
常數 （ F： -- r ）
Create a floating point constant.
建立浮點常數。


FVARIABLE ( -- addr )
FVARIABLE （ -- 附加 ）
Create a floating point variable.
建立浮點變數。


PI ( F: -- r1 )
PI （ F： -- r1 ）
Push a floating point number with a value approximately equal to
推送一個值約等於
pi.
圓周率。


F0.0 ( F: -- r1 )
F0.0 （ F： -- r1 ）
Push a floating point number with a value equal to 0.
推送值等於 0 的浮點數。


F1.0 ( F: -- r1 )
F1.0 （ F： -- r1 ）
Push a floating point number with a value equal to 1.
推送值等於 1 的浮點數。


FINFINITY ( F: -- r1 )
無窮大 （ F： -- r1 ）
Push the floating point number representing the largest
推送代表最大值的浮點數
representable number onto the floating point stack.
可表示的數字到浮點堆疊上。


E. ( F: r -- )
E. （ F： r -- ）
Print a floating point number in exponential (power of ten)
以指數（10 的冪）列印浮點數
format
格式


.FSINH ( F: r1 -- r2 )
.FSINH （ F： r1 -- r2 ）
Hyberbolic sin function. Not in HFLOAT.
高博罪功能。不在 HFLOAT 中。


E.R ( F: r -- ; n1 n2 )
E.R （ F： r -- ; n1 n2 ）
Display the floating point number r on the currently selected
在目前選取的
output device in exponential form with n1 digits to the right of
指數形式的輸出裝置，右側有 n1 位數字
the decimal point, right justified in a field of width n2. Not in
小數點，在寬度為 n2 的欄位中右對齊。不在
HFLOAT.
HFLOAT 的。


F. ( F: r -- )
F. （ F： r -- ）
Display the floating point number on the currently selected
在目前選取的
output device in fixed-point form; i.e., the location of the
定點形式的輸出設備;即
decimal point is adjusted so that no exponent need be displayed.
小數點會調整，因此不需要顯示指數。
The number of digits to the right of the decimal point specified
指定小數點右側的位數
by the most recent execution of the word PLACES are printed to
通過最近執行的單詞 PLACES 被打印到
the right of the decimal point. A trailing blank follows. For
小數點的右邊。後面是尾隨空白。為
example, 4 PLACES 1.2345E02 F. will display as 123.4500b (where
例如，4 個 PLACES 1.2345E02 F. 將顯示為 123.4500b （其中
the "b" denotes an ASCII blank). If the number of digits to the
“b” 表示 ASCII 空白）。如果位數為
left of the decimal point is greater than 14, the error routine
小數點左邊大於14，錯誤常式
is called. Not in HFLOAT.
被稱為。不在 HFLOAT 中。


F.R ( F: r -- ; n1 n2 )
F.R （ F： r -- ; n1 n2 ）
Display r on the currently selected output device in fixed point
在目前選取的輸出裝置上以定點顯示 r
form with n1 digits to the right of the decimal place, right
小數位右邊有 n1 位數字的表格，右邊
justified in a field of width n2. If the number cannot be
在寬度為 n2 的欄位中對齊。如果號碼不能
represented within the given field width, the error routine is
在給定欄位寬度內表示，錯誤常式為
called and the value is printed in exponent form. For example,
呼叫，且值會以指數形式列印。比如
1.2345e2 4 12 F.R will display as bbbb123.4500 (where each "b"
1.2345e2 4 12 F.R 將顯示為 bbbb123.4500（其中每個“b”
character denotes an ASCII blank). Not in HFLOAT.
字元表示 ASCII 空白）。不在 HFLOAT 中。


FLOATS ( -- )
浮點數 （ -- ）
Set the flag FLTS . Allows floating point numbers to be input
設定旗標 FLTS 。允許輸入浮點數
using imbedded decimal points and optional exponent fields. For
使用嵌入的小數點和可選的指數欄位。為
example:
例：
FLOATS 1.234 -5.4
浮點數 1.234 -5.4
will produce two floating point numbers. Note, however, that a
會產生兩個浮點數。不過請注意，一個
single precision integer, such as 7 , will remain a single
單精度整數，例如 7 ，將保持單一
precision integer, and a double number with a terminating decimal
精確整數，以及帶有終止小數的雙精度
point, such as 1234. , will remain a double number.
點，例如 1234。，將保持雙倍數字。


FNUMBER ( F: -- r ; adr -- -1 )
FNUMBER （ F： -- r ; adr -- -1 ）
( adr -- d 1 )
（ ADR -- d 1 ）
Convert the string at the specified address into a real or
將指定位址的字串轉換為實數或
integer number, with a flag of -1 or 1, respectively. If the
整數，旗標分別為 -1 或 1。如果
number cannot be converted, print an error message. Not in
數字無法轉換，則列印錯誤訊息。不在
HFLOAT.
HFLOAT 的。


F# ( F: -- r )
F# （ F： -- r ）
Convert the string following F# into a floating point number.
將 F# 後面的字串轉換成浮點數。
This includes numbers with or without decimal points. Thus F# 34
這包括帶或不帶小數點的數字。因此 F# 34
yields the equivalent of 34X0 . If SFLOAT is loaded, even if in
產生相當於 34X0 的 。如果載入 SFLOAT，即使
NOFLOATING mode, F# still converts the following number and
NOFLOATING 模式時，F# 仍會轉換下列數字，而
pushes it onto the floating point stack. Not in HFLOAT.
將其推送到浮點堆疊上。不在 HFLOAT 中。


#? ( number --- d 1 )
#?（ 編號 --- d 1 ）
( F: -- r ; number --- -1 )
（ F： -- r ; 編號 --- -1 ）
If possible, convert the following word in the input stream into
可能的話，請將輸入資料流程中的下列單字轉換為
a number. If the string converts to a floating point number, the
一個數字。如果字串轉換為浮點數，則
flag is set to -1 . If the string converts to an integer, the
旗標設定為 -1 。如果字串轉換為整數，則
flag is set to 1. If the string cannot be converted, a standard
旗標設定為 1。如果字串無法轉換，則標準
error message is sent. Not in HFLOAT.
錯誤訊息。不在 HFLOAT 中。


FLITERAL ( F: -- r )
文字 （ F： -- r ）
Create an in-line literal.
建立內嵌文字。


F@ ( F: -- r ; addr -- )
F@ （ F： -- r ; addr -- ）
Fetch the floating point number at the specified address and
取得指定位址的浮點數，並
push it onto the floating point stack. Drop the address from the
將其推送到浮點堆疊上。從
parameter stack.
參數堆疊。


F! ( F: r -- ; addr -- )
F!（ F： r -- ; 地址 -- ）
Store the floating point number at the top of the floating point
將浮點數儲存在浮點的頂部
stack in the area specified by the address at the top of the
堆疊在頂端位址所指定的區域中
parameter stack. Drop the address from the parameter stack and
參數堆疊。從參數堆疊中刪除位址，並
drop the top element from the floating point stack.
從浮點堆疊中刪除頂端元素。


F, ( F: r -- )
F， （ F： r -- ）
Allot space at HERE and store the floating point number. Similar
在 HERE 分配空間並儲存浮點數。俏
to , . Not in HFLOAT.
到。不在 HFLOAT 中。


FLOAT ( F: -- r ; dbl -- )
浮點 （ F： -- r ; dbl -- ）
Convert the double number at the top of the parameter stack to a
將參數堆疊頂端的雙精度數字轉換為
floating point number which is then pushed onto the floating
浮點數，然後推送到浮點
point stack. As with all double numbers, the location of the
點堆疊。與所有雙倍數字一樣，位置
decimal point is effectively ignored.
小數點實際上被忽略。


FIX ( F: r -- ; -- d )
FIX （ F： r -- ; -- d ）
Convert a floating point number to the nearest signed double
將浮點數轉換為最接近的有符號雙精度
integer equivalent, removing the real number from the floating
整數等效，從浮點中刪除實數
point stack and leaving the double integer result on the Forth
點堆疊並將雙整數結果留在第四個
parameter stack. When the real number lies exactly halfway
參數堆疊。當實數正好在一半時
between two integers, the result is the nearest EVEN number.
在兩個整數之間，結果是最接近的偶數。
Underflow gives a zero result. An error condition results if the
下溢給出的結果為零。如果
resulting number is too large to be represented as an UNSIGNED
結果數字太大，無法表示為 UNSIGNED
double number. If more error control is desired, you may create
雙倍數字。如果需要更多的錯誤控制，您可以創建
your own version using DINTABS.
您自己的版本使用 DINTABS。


INT ( F: r -- ; -- d )
INT （ F： r -- ; -- d ）
Convert a signed floating point number to its truncated double
將帶正負號的浮點數轉換為其截斷的雙精度
integer value. If the conversion did not succeed, report an
integer 值。如果轉換未成功，請回報
error.
錯。


