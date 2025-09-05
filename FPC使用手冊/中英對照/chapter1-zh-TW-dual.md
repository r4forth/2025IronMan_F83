# CHAPTER 1. WHAT IS F-PC? 第 1 章 什麼是 F-PC？

## 1.1. HOW DID WE GET HERE? 1.1. 我們是如何走到這一步的？

Over the past several years, the programming community for other
在過去的幾年裡，編程社區為其他
languages has changed somewhat. Several years ago, Forth had enormous
語言發生了一些變化。幾年前，符式語言擁有巨大的
advantages over Fortran, Pascal, and C in terms of development
在開發方面優於 Fortran、Pascal 和 C
interactivity. The Forth development cycle was very short, and new code
互動性。Forth 的開發週期很短，而且新程式碼
modules could be put together for experimentation very quickly. As the
模塊可以非常快速地組合在一起進行實驗。作為
years went by, programmers for these other languages began to realize
多年過去了，這些其他語言的程式設計師開始意識到
there had to be something better than their traditional debug cycle:
必須有比傳統調試週期更好的東西：
EDIT-COMPILE-LINK-DEBUG and repeat. This debugging loop could be
EDIT-COMPILE-LINK-DEBUG 並重複。這個偵錯迴圈可能是
measured in days, and each error correction session was normally at least
以天為單位，每個糾錯會話通常至少
30 minutes long.
30分鐘長。


Forth did away with much of the above delays. The editor was integrated
符式語言消除了上述大部分延誤。編輯器被整合
into the Forth operating system environment, so the time to start up or
進入 Forth 作業系統環境，因此啟動或啟動的時間
leave the editor was zero. The compiler was incremental, so programs
離開編輯是零。編譯器是增量的，因此程式
could be debugged a piece at a time, and there was no linker at all.
可以一次調試一段，而且根本沒有鏈接器。
This naturally resulted in a productivity improvement and a significant
這自然導致了生產力的提高和顯著的
reduction in programmer frustration.
減少程序員的挫敗感。


As the years went by, other programmers noticed how much easier BASIC was
隨著歲月的流逝，其他程式設計師注意到 BASIC 是多麼容易
to use than other compiled languages, since it had a built in editor, and
使用比其他編譯語言，因為它有一個內置的編輯器，並且
didn't have to be compiled at all. Of course it was so slow..., but then
根本不需要編譯。當然，速度很慢......，但隨後
along came TURBO PASCAL. It created fast compiled code, had an
隨之而來的是 TURBO PASCAL。它創建了快速編譯的代碼，有一個
integrated SCREEN editor, and compiled like blazes.
集成了 SCREEN 編輯器，並像火焰一樣編譯。


We now start to see some similarities to Forth, a much superior
我們現在開始看到與符式語言的一些相似之處，一個優越得多的
development environment, where the development iteration cycle has been
開發環境，開發迭代週期已
reduced to a very small number. But Turbo Pascal still lacked the Forth
減少到非常小的數字。但 Turbo Pascal 仍然缺少 Forth
interactivity, and the ability to incrementally debug programs as they
互動性，以及增量調試程式的能力，因為它們
were developed.
被開發。


Finally along came the Macintosh and Light Speed Pascal (LSP). It had
最後出現了 Macintosh 和 Light Speed Pascal （LSP）。它有
evolved from Mac Pascal, an interactive and pseudo interpreted Pascal for
從 Mac Pascal 演變而來，Mac Pascal 是一種交互式和偽解釋的 Pascal for
the Mac. LSP had windows, a built-in screen editor, compiled modules, a
LSP 有 windows、內置屏幕編輯器、編譯模塊、
very fast compiler and a light speed linker, with the ability to test
非常快的編譯器和光速連結器，具有測試能力
small segments of code, and two built-in debuggers: one for Pascal, and
小段程式碼，以及兩個內建偵錯器：一個用於 Pascal，以及
one for Assembly. The only problem was that it was PASCAL, not Forth.
一個用於集會。唯一的問題是它是 PASCAL，而不是 Forth。


It is interesting to ask: "What is holding Forth back and preventing it
問這個問題很有趣：“是什麼阻礙了 Forth 並阻止了它
from being more popular?" In spite of the strength Forth has in
從更受歡迎？儘管符式語言擁有強大的力量
conciseness, interactiveness, and speed, there are weaknesses which
簡潔、互動性和速度，但存在弱點
hinders it's rapid spread in the general computing community. The most
阻礙了它在一般計算社區中的快速傳播。最
important weaknesses are in its user interface and its interface to
重要的弱點在於它的用戶界面和界面
standard operating systems, which can be attributed directly to the use
標準操作系統，可以直接歸因於使用
of blocks in storing source code.
儲存原始程式碼的區塊。


In the early days of personal computing, programmers had their one and
在個人計算的早期，程序員擁有自己的
only choice of editor: the line editor ED and its clone EDLIN. Comparing
編輯器的唯一選擇：行編輯器 ED 及其克隆 EDLIN。比較
to this environment, the polyForth or figForth block editor was obviously
對於這種環境，polyForth 或 figForth 區塊編輯器顯然是
superior. However, after WordStar and its derivatives established a firm
上。然而，在 WordStar 及其衍生品成立公司後
position in programmers' toolboxes, most people would reject the Forth
在程序員工具箱中的位置，大多數人會拒絕 Forth
block editor as too primitive a tool for substantial coding efforts.
區塊編輯器作為對大量編碼工作來說過於原始的工具。
After IBM-PC's replaced CPM machines, the majority of programmers and
在 IBM-PC 取代 CPM 機器後，大多數程序員和
users expect and demand source code and data being made available in
使用者期望並要求原始程式碼和資料在
sequential files on 5.25" DOS diskettes. Blocked text files as used in
5.25 英寸 DOS 軟盤上的連續文件。封鎖的文字檔案，如
F83 was only a half- hearted effort to come to term with reality.
F83 只是為了接受現實而做出的半心半意的努力。


Forth systems perform better if they can access the hardware resources
如果系統可以存取硬體資源，則效能會更好
directly, rather than through the arbitration of an inefficient operating
直接，而不是通過對低效運營的仲裁
system. This was one reason why Chuck Moore invented Forth in the first
系統。這就是查克·摩爾 （Chuck Moore） 在第一部中發明 Forth 的原因之一
place. Ignoring the operating systems in the early days of main frames
放。忽略主機早期的作業系統
and minicomputers was advantageous because there were as many
小型計算機是有利的，因為有同樣多的
incompatible operating systems as there were brands of computers. In
不兼容的操作系統，因為有計算機品牌。在
personal computing, this advantage is rapidly diminishing as the species
個人計算，隨著物種的出現，這種優勢正在迅速減弱
of operating systems disappeared rapidly due to natural selection. It
的操作系統由於自然選擇而迅速消失。它
looks like we will end up with DOS, MAC, and UNIX (may be OS2). In this
看起來我們最終會得到 DOS、MAC 和 UNIX（可能是 OS2）。在這個
situation, Forth systems must provide smooth and efficient interface to
情況下，Forth 系統必須提供流暢高效的接口
the operating systems, to be accessed conveniently by the users.
操作系統，方便用戶訪問。


F-PC provides a much polished interface between a user and his
F-PC 在用戶和他的用戶之間提供了一個非常精緻的界面
IBM-PC/XT/AT or compatible computer. Sequential files are adopted as the
IBM-PC/XT/AT 或相容的電腦。循序檔案會採用為
principal means of programming and documentation. The user is comforted
編程和文檔的主要手段。用戶感到安慰
by a very sophisticated and intuitive text editor to enter and modify his
通過一個非常複雜和直觀的文本編輯器來輸入和修改他的
code and documentation, not constrained by the very limiting block
程式碼和文件，不受限制性區塊的限制
structure. The interface to the underlying DOS is seamless to allow the
建築物。底層 DOS 的介面是無縫的，允許
user full access to tools and services provided by DOS and other
用戶完全訪問 DOS 和其他提供的工具和服務
utilities. In so doing, F-PC can be installed on all DOS compatible
公用事業。這樣，F-PC 就可以安裝在所有兼容的 DOS 上
machines.
機器。


Speed is another major character in F-PC. Most of its text interpreter
速度是 F-PC 中的另一個主要角色。它的大部分文本解釋器
and compiler are coded in assembly to make sure that it matches the speed
和編譯器在彙編中編碼，以確保它與速度相符
and convenience of a block based system. 64K byte memory limit is
以及基於塊的系統的便利性。64K 位元組記憶體限制為
removed by placing code, names, colon definitions, and text files in
透過將程式碼、名稱、冒號定義和文字檔案放入
different segments in the 1M byte addressing space. Utility is also
1M 位元組尋址空間中的不同段。實用性也是
provided to address extended memory.
提供以處理擴充記憶體。


Since F-PC is a public domain software package, it has attracted many
由於 F-PC 是一個公共領域的軟體包，因此吸引了許多人
experienced Forth programmers to contribute utilities and applications.
經驗豐富的 Forth 程序員貢獻實用程序和應用程序。
It is quickly becoming a huge resource pool where old and new Forth users
它正迅速成為一個巨大的資源池，新老 Forth 用戶
can draw inspirations and practical solutions to their programming needs.
能夠為自己的程式設計需求汲取靈感和實用的解決方案。


Because the sequential files were the major focus of F-PC when it was
因為順序文件是 F-PC 的主要關注點
first evolved it is important that we summarize the distinct advantages
首先進化，我們總結獨特的優勢很重要
of using sequential files to store source code. Here is a partial list:
使用順序檔案來儲存原始程式碼。以下是部分列表：


1. Source files are smaller, so backing up or transporting files is easier.
>1. 原始檔案較小，因此備份或傳輸檔案是更容易。

2. Sequential source files can be manipulated or examined by editors that other people have, not just by the Forth block editor.
>2. 順序源文件可以由編輯者操作或檢查其他人都有，而不僅僅是 Forth 區塊編輯器。

3. There is no artificial limit on the size of a file. The file can be extended as needed. White space in a file does not take up extra bytes.
>3. 文件大小沒有人為限制。檔案可以根據需要進行擴展。檔案中的空格不會佔用額外的位元組。

4. There is no artificial limit placed on the size of word definitions. In the block based system we usually give up line zero for a comment line, and line 15 for nudge space.
>4. 對字的大小沒有人為的限制定義。在基於塊的系統中，我們通常會放棄線路零表示註解行，第 15 行表示微移空間。

5. There is no artificial limit placed on the amount of comments one can place with the source. Again, compared to blocks with shadows, 16 lines of shadow were either too much or too little.
>5. 對一條評論的數量沒有人為的限制可以與源一起放置。同樣，與陰影，16 行陰影要麼太多，要麼太少。

6. Sequential files provide a much more natural interface to the operating systems which were designed to handle them.
>6. 順序文件為旨在處理它們的操作系統。

7. It allows plenty of room for inserting a new line in the middle of a source file, without having to drop out of the editor, and use special commands to move things around. All we have to do is pressing <enter>.
> 7. 它為在中間插入新線提供了足夠的空間源文件，而不必退出編輯器，並且使用特殊命令來移動東西。我們所要做的就是按 <enter>。


So here we are at the end (or beginning) of a long road, looking back at
所以我們正處於一條漫長道路的盡頭（或開始），回頭看
what we have done, and looking forward to the future. Blocks were
我們所做的一切，並展望未來。街區是
certainly very useful for forcing us to modularize our code. That was a
當然對於迫使我們模組化程式碼非常有用。那是一個
big advantage while we were learning Forth. Maybe newcomers to Forth
當我們學習符式語言時，有很大的優勢。也許是符式語言的新人
should be required to learn the system on a BLOCK version. But now that
應該需要學習 BLOCK 版本的系統。但現在
we have come of age, we should know where to modularize our code better
我們已經成年了，我們應該知道在哪裡更好地模組化我們的程式碼
than the computer does.
比電腦更重要。


## 1.2. F-PC, WHAT IS IT ALL ABOUT? 1.2. F-PC，這到底是怎麼回事？

This Forth was implemented by Tom Zimmer, with substantial help from
這個 Forth 是由 Tom Zimmer 實現的，並得到了
Robert L. Smith. Some of the direct threaded low level code
羅伯特·史密斯。一些直接執行緒的低階程式碼
modifications came from a LaForth implementation by Bob and LaFarr Stuart
修改來自 Bob 和 LaFarr Stuart 的 LaForth 實作
. George Hawkins contributed the Browser. This is yet another step in
.喬治·霍金斯 （George Hawkins） 貢獻了瀏覽器。這是
the Forth evolution being undertaken to obtain the ideal Forth system.
正在進行 Forth 演化以獲得理想的 Forth 系統。
This Forth maintains very high compatibility with F83, which was its
這個 Forth 與 F83 保持了非常高的兼容性，這是它的
predecessor.
前任。


F-PC is a Forth that uses three main segments for Forth itself, and
F-PC 是一個 Forth，它為 Forth 本身使用三個主要部分，並且
additional segments for other purposes, like the editor, screen saving,
用於其他用途的其他區段，例如編輯器、螢幕儲存、
etc. The three main segments in F-PC are: First, a 64K Code Segment for
等等。F-PC 中的三個主要部分是：首先，用於 64K 代碼段
code, variables, and any user arrays that are not specifically placed in
程式碼、變數以及任何未特別放置在
an external segment. The compiler also places the code field of all
外部區段。編譯器也會將所有
colon definitions in this Code Segment. Code fields in F-PC are three
冒號定義。F-PC 中的代碼字段有三個
(3) bytes in length. The second List Segment contains the bodies of
（3） 長度的位元組。第二個清單區段包含
colon definitions and strings. Its size is not limited to 64K bytes, and
冒號定義和字串。它的大小不限於 64K 位元組，並且
can use as much memory as allowed by the operating system. The third
可以使用作業系統允許的盡可能多的記憶體。第三個
segment of 64k contains the heads, or symbols in F-PC.
64k 的片段包含 F-PC 中的正面或符號。


Since a typical program is about half program and half data, the
由於典型的程式大約是一半程式和一半資料，因此
separation of code and colon space results in an easy doubling or more of
代碼和冒號空間的分離會導致輕鬆加倍或更多
effective program space. About 300K of total data/program space is
有效的程序空間。總數據/程序空間約為 300K
available, with most useful utilities already loaded. This can be
可用，並且已經加載了大多數有用的實用程序。這可以是
increased to over 400k by deleting things you don't need. A small loss
通過刪除不需要的東西增加到 400 萬以上。小損失
(about 5%) in performance resulted from this separation of colon
（約 5%） 的性能是由結腸的這種分離引起的
definitions from the code space, but the benefits of expanded program
定義，但擴充程式的好處
space greatly exceeds the disadvantages.
空間大大超過了缺點。


The primary difference from other Forth systems that you are likely to
您可能與其他 Forth 系統的主要區別
encounter is that code fields are three (3) bytes rather than 2, and the
遇到是程式碼欄位是三 （3） 個位元組而不是 2 個位元組，並且
code field of a low level code word does not point to code, but contains
低階碼字的 code 欄位不指向程式碼，而是包含
code. This is generally known as 'direct threaded code (DTC).' F-PC
法典。這通常稱為“直接執行緒代碼 （DTC）”。F-PC
has moved the address list in a colon word to a separate List segment, so
已將冒號單字中的地址清單移至單獨的 List 區段，因此
there are two bytes in the body (parameter field) of each colon
每個冒號的正文（參數欄位）中有兩個位元組
definition that points into the List space of the colon definition which
指向冒號定義的 List 空間的定義，其中
contains a list of code field addresses. The List space can expand to
包含程式碼欄位位址的清單。清單空間可以展開至
fill all available RAM memory. It is not limited to a single 64K byte
填滿所有可用的 RAM 記憶體。它不限於單個 64K 字節
segment.
瓣。


Variables, constants, and strings are handled in the same way as in F83.
變數、常數和字串的處理方式與 F83 中的處理方式相同。
That is, they are in the Code space. This segmentation seems to provide
也就是說，它們位於程式碼空間中。這種細分似乎提供了
a reasonable balance. As the dictionary expands, more user data space is
合理的平衡。隨著字典的擴展，更多的用戶數據空間
needed, which works well with F-PC, as most of the free space is in
需要，這與 F-PC 配合得很好，因為大部分可用空間都在
Code/Data space.
代碼/數據空間。


This system comes with a meta compiler. It can thus regenerate itself
該系統帶有一個元編譯器。因此它可以自我再生
with user extensions. DOS batch files are provided to ease the meta
與使用者擴充功能。提供 DOS 批次檔案以簡化元資料庫
compilation. Users can also produce turnkey systems without having to go
編輯。用戶還可以生產交鑰匙系統，而無需前往
through the meta compilation process.
通過元編譯過程。


As F-PC currently exists, there is about 27k of List dictionary space, 27
由於 F-PC 目前存在，大約有 27k 的列表詞典空間，27
K of Head space, and 35k of Code space. The List space can be increased
K 的頭部空間和 35k 的代碼空間。清單空間可以增加
by changing the number of segments assigned to it and save the system.
通過更改分配給它的段數並保存系統。
The new system thus saved will have a larger List space when executed.
這樣保存的新系統在執行時將具有更大的列表空間。
The usable memory can also be expanded by removing some of the optional
可用記憶體也可以透過移除一些可選的
files from the list of load files in F-PC.SEQ. The removable files are
F-PC.SEQ 中載入檔案清單中的檔案。抽取式檔案是
marked in F-PC.SEQ. Some of these files are listed as follows:
在 F-PC.SEQ 中標記。其中一些檔案如下：


PATHSET.SEQ WORDS.SEQ COLOR.SEQ DUMP.SEQ
路徑集。以下詞。順序顏色。序列轉儲。序
DECOM.SEQ DEBUG.SEQ STATUS.SEQ MACROS.SEQ
德科姆。SEQ DEBUG 的。序列狀態。序列宏觀。序
PATCHER.SEQ FILSTAT.SEQ FWORDS.SEQ
補丁機。序列 FILSTAT。序列詞。序


If some of these files are removed, a significant savings in dictionary
如果刪除其中一些文件，則可以節省大量字典
space will result. Fairly large programs can now be coded in F-PC,
空間將產生。現在可以在 F-PC 中編碼相當大的程序，
although there are still some obvious limits. It is doubtful that
雖然還是有一些明顯的限制。值得懷疑的是
ZoomRacks the database Tom coded while at QuickView Systems could be
ZoomRacks 是 Tom 在 QuickView Systems 時編碼的數據庫
compiled in F-PC without overlays. ZoomRacks consisted of more than 2M
在 F-PC 中編譯，沒有覆蓋。ZoomRacks 由超過 2M 組成
bytes of source screens, and used all RAM outside the program as
位元組，並將程式外部的所有 RAM 用作
contiguous data space for the user.
使用者的連續資料空間。


## 1.3. FEATURES IN F-PC 2.25 1.3. F-PC 2.25 中的功能

The first thing you should know is that F-PC is trying to achieve a
您應該知道的第一件事是 F-PC 正試圖實現
number of conflicting goals. It is intended to be a Forth system that
衝突目標的數量。它旨在成為一個 Forth 系統
provides all of the following:
提供下列所有項目：

Compatible to F83 and Forth-83 Standard
相容於 F83 和 Forth-83 標準
Smooth Interface to DOS, using sequential files
DOS 的平滑接口，使用順序文件
Fast compilation and execution
快速編譯和執行
Integrated text file editor for easy programming and documentation
整合的文字檔案編輯器，方便程式設計和記錄
Many utilities and tools
許多實用程式和工具
Room for very large application programs
非常大的應用程式空間


Impossible, you say. Perhaps, but if you give F-PC a chance you may find
你說，不可能。也許吧，但如果你給 F-PC 一個機會，你可能會發現
some things you like. In line with the above goals, here is a list of
一些你喜歡的東西。根據上述目標，這裡列出了
some of F-PC's major features:
F-PC 的一些主要特點：


Direct threaded dictionary for speed
直接執行緒字典以提高速度
Separated lists and heads to increase space
分開的列表和標題以增加空間
Prefix assembler to enhance readability
前綴彙編器，增強可讀性
Postfix assembly syntax for compatibility with F83
與 F83 相容的後綴組合語法
Full DOS access from system and command shell level control
從系統和命令 shell 層級控制的完整 DOS 存取
Full directory/path based file system
完整目錄/路徑型檔案系統
Viewing words across directory boundaries
跨目錄界限檢視單字
Full user configurable sequential text editor provided in source
源代碼中提供的完整用戶可配置的順序文本編輯器
Full DOS memory management interface
全 DOS 記憶體管理介面
Headers can be selectively removed
可以選擇性地移除標頭
Many contributions from users on a wide range of applications
用戶對廣泛應用的許多貢獻


F-PC is a Forth derived from many sources. Henry Laxen, and Michael Perry
F-PC 是源自許多來源的 Forth。亨利·拉克森和邁克爾·佩里
being the original developers of F83. Tom Zimmer, along with Robert L.
作為 F83 的原始開發者。湯姆·齊默 （Tom Zimmer） 和羅伯特·
Smith, Charles Curley, and Jerry Modrow put together the original
史密斯、查爾斯·柯利和傑瑞·莫德羅將原版放在一起
version. A F-PC Working Group was organized in the Silicon Valley
版本。在矽谷組織了一個 F-PC 工作組
Chapter of Forth Interest Group to coordinate the testing and
第四興趣小組分會協調測試和
documentation of this system. F-PC 2.25 was released in November, 1988,
該系統的文件。F-PC 2.25 於 1988 年 11 月發布，
and F-PC 3.5 is released in November 1989.
F-PC 3.5 於 1989 年 11 月發布。


F-PC is a Direct Threaded Code (DTC) Forth. That is it contains code in
F-PC 是直接執行緒代碼 （DTC） 端口。也就是說，它包含
the code field rather than pointing to code. DTC gives a noticeable
程式碼欄位，而不是指向程式碼。DTC 給出了明顯的
boost in performance, which was needed to counteract the next
性能提升，這是抵消下一個
enhancement.
增強。


F-PC keeps the body or the list portion of colon definitions in a
F-PC 將冒號定義的正文或清單部分保留在
separate segment-the List space. This substantially increases the space
分隔段 - 清單空間。這大大增加了空間
available for your program. There is a penalty to pay in performance,
可用於您的計劃。在表現中要付出代價，
with an extra level of indirect jump required in NEST.
在 NEST 中需要額外級別的間接跳躍。


F-PC has a prefix assembler. Code definitions are coded with a syntax
F-PC 有一個前綴彙編器。程式碼定義會使用語法編碼
similar to MASM, in the form " MOV AX, BX ". We have found this syntax
與 MASM 類似，形式為“ MOV AX， BX ”。我們找到了這個語法
to be much more readable to "traditional" programmers than the standard
對於「傳統」程式設計師來說，比標準更具可讀性
F83 postfix assembler. To reduce the pain to current F83 users, the
F83 後綴彙編器。為了減輕當前 F83 用戶的痛苦，該
assembler supports the old F83 assembler syntax as well. Just use the
彙編器也支援舊的 F83 彙編器語法。只需使用
word POSTFIX to select postfix assembler syntax, and then use PREFIX to
word POSTFIX 來選取後綴組譯器語法，然後使用 PREFIX 來
switch back to the prefix syntax. An 8086 family disassembler is
切換回前綴語法。8086系列反組譯器是
provided. The disassembler was written by Charles Curley, and includes
提供。反彙編器由 Charles Curley 編寫，包括
8087 support added by Robert L. Smith.
8087 支援由 Robert L. Smith 新增。


F-PC supports full pathnames and file handles. File names may be up to 63
F-PC 支援完整路徑名稱和檔案句柄。檔案名稱最多可為 63 個
characters in length including path. All source is in sequential files.
長度包括路徑的字元。所有來源都在順序檔案中。
No blocks in this system. The original F83 BLOCK system is available as a
這個系統中沒有方塊。原始的 F83 BLOCK 系統可作為
load-on if needed. Several powerful file words have been included. FLOOK
如果需要，可以加載。已包含幾個強大的文件詞。FLOOK
allows searching through one or many files for a particular character
允許在一個或多個檔案中搜尋特定字元
sequence. FPRINT allows you to make formatted listings of one, all, or a
序。FPRINT 可讓您建立一個、全部或
set of Forth source files. EDITALL allows you to edit a string through
Forth 源文件集。EDITALL 可讓您透過
many files. INDEX displays the first line of a set of files.
許多文件。INDEX 顯示一組檔案的第一行。


The compiler itself has been substantially optimized, with almost all of
編譯器本身已經進行了大幅優化，幾乎所有
WORD being in code. The system currently uses 64 threads, which is just
WORD 在程式碼中。系統目前使用 64 個線程，剛好
at the point of diminishing return for a 2000 word vocabulary. With the 8
在 2000 個單詞詞彙的收益遞減的地步。與 8
vocabularies this system has, only about 1k bytes of Code space is used
這個系統擁有的詞彙表，只使用了大約 1k 位元組的程式碼空間
for the vocabulary head pointers.
對於詞彙頭指針。


A help file is provided with each source file, these can be used like F83
每個源文件都提供了一個幫助文件，這些文件可以像 F83 一樣使用
shadow screens were used, that is to hold comments about the words in the
使用陰影螢幕，即保存對
source file. The word VIEW accesses the .SEQ file, and the word HELP
原始檔案。VIEW 一詞會存取 .SEQ 檔案，以及 HELP 一詞
accesses the .HLP file. As much or as little text can be placed in the
存取 .HLP 檔案。可以將盡可能多或盡可能少的文字放置在
help file for each word compiled.
每個編譯單字的幫助檔案。


Many utilities are included. An enhanced debugger allows nesting and
包括許多公用事業。增強型偵錯工具允許巢狀和
unnesting of colon definitions.
取消嵌套冒號定義。


## 1.4. NEW FEATURES IN F-PC 3.5 1.4. F-PC 3.5 的新功能

F-PC version 2.25 was released in November 1988. Tom Zimmer agreed, with
F-PC 2.25 版本於 1988 年 11 月發布。湯姆·齊默 （Tom Zimmer） 表示同意，並表示
great reluctance, not to make any changes so that it can be distributed
非常不情願，不做任何改變以便可以分發
among Forth users as a common programming environment for information
在 Forth 用戶中作為信息的通用編程環境
exchange. Modifications, enhancements, and bug-fixes implemented and
換。已實作的修改、增強功能和錯誤修正，以及
tested over the ten month period were distributed privately by Tom under
十個月期間的測試由 Tom 私下分發
the name F-TZ. The F-PC Working Group in their September 23, 1989
F-TZ 這個名字。F-PC 工作組在 1989 年 9 月 23 日
meeting decided to adopt F- TZ and distribute it as F-PC version 3.5. A
會議決定採用 F-TZ 並將其作為 F-PC 3.5 版本分發。一個
partial list of the added features are:
新增功能的部分清單包括：


Hypertext on-line help and documentation
超文本在線幫助和文檔
Browser to examine code and documentation
用於檢查程式碼和文件的瀏覽器
Mouse support in editor
編輯器中的滑鼠支援
Enhanced pull down menu and pop up windows
增強的下拉菜單和彈出窗口
Expanded memory support
擴充記憶體支援
Lots of bug fixes and minor enhancements
許多錯誤修復和小增強
Update and corrections on kernel help files
核心說明檔案的更新和更正


For those who have used F-PC 2.25 and like to know more about the
對於那些使用過 F-PC 2.25 並想了解更多關於 F-PC 2.25 的人
differences between it and F- PC 3.5, please consult the file
它與 F-PC 3.5 的區別，請查閱文件
FPCNOTES.TXT where Tom Zimmer logged the bug fixes and the enhancements.
FPCNOTES.TXT Tom Zimmer 記錄錯誤修復和增強功能的地方。


User contributed programs are deleted from the new version because of
使用者貢獻的程式會從新版本中刪除，因為
disk space limitations. However, user contributions will be continually
磁碟空間限制。但是，用戶貢獻將持續
solicited. The Silicon Valley Chapter of the Forth Interest Group will
徵求。第四興趣小組矽谷分會將
coordinate the consolidation and distribution of user contributed works.
協調用戶貢獻作品的整合和分發。

