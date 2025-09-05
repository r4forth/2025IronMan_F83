CHAPTER 8. PASM, THE F-PC ASSEMBLER
第 8 章。PASM，F-PC 彙編器




PASM is an assembler which is based on the F83 8088/86 assembler and an
PASM 是一個基於 F83 8088/86 彙編器和
8086 assembler published in Dr. Dobb's Journal, February 1982, by Ray
8086 彙編器發表在 Dr. Dobb's Journal，1982 年 2 月，作者：Ray
Duncan. This assembler was subsequently modified by Robert L. Smith to
鄧肯。該彙編器隨後被 Robert L. Smith 修改為
repair bugs, and support the prefix assembler notation. Bob discovered a
修復錯誤，並支援前綴彙編器表示法。鮑勃發現了一個
very simple method to force a postfix assembler to assemble prefix code,
強制後綴彙編器組合前綴代碼的非常簡單的方法，
by deferring assembly until the next assembler command or the end of
透過將組合延遲到下一個組合器指令或
line, when all the arguments for the previous assembler command are piled
line，當前一個組合器命令的所有參數都堆疊在一起時
up on the top of the data stack. Tom Zimmer has made additional
在資料堆疊的頂端。湯姆·齊默 （Tom Zimmer） 製作了額外的
modifications to allow syntax switching, and to increase compatibility in
允許語法切換的修改，並增加
postfix mode with the F83 Assembler.
後綴模式與 F83 彙編器。


Writing assembly programs is black magic. It is not appropriate to
編寫彙編程式是黑魔法。不宜
discuss the joys and frustrations in working at such a low level in this
討論在如此低的水平下工作的快樂和挫折
manual. However, F-PC provides the best environment for you to do
手工的。但是，F-PC 為您提供了最好的環境
experiments using assembly language, because you can first verify the
使用組合語言進行實驗，因為您可以先驗證
algorithm and methodology in high level Forth code and gradually reduce
演算法和方法論在高級 Forth 代碼中並逐漸減少
the code to the assembly level. You will find numerous examples in which
程式碼至元件層級。您會發現許多例子，其中
the high level code in F83 is recoded in assembly, in addition to many of
F83 中的高級代碼在彙編中重新編碼，此外還有許多
the F83 kernel words which were in assembly already.
已經在組裝中的 F83 內核詞。


The best way to learn 8086 assembly language is to use PASM, armed with
學習 8086 彙編語言的最佳方法是使用 PASM，配備
all the code words in F-PC as templates and examples. Factor your high
F-PC 中的所有代碼字作為模板和範例。考慮你的高潮
level words carefully so that words at the bottom level can be
仔細調平單詞，以便最底層的單詞可以
conveniently recoded in assembly. Take the F-PC kernel words as
在組裝中方便地重新編碼。將 F-PC 核心字視為
templates to start with, and modify them so that they will do exactly
模板，並修改它們，以便它們能夠完全完成
what you want them to do.
你希望他們做什麼。


8.1. PREFIX OR POSTFIX ?
8.1. 前綴還是後綴？


PASM supports dual syntaxes. The words PREFIX and POSTFIX switch between
PASM 支援雙語法。PREFIX 和 POSTFIX 這兩個詞會在
the two supported modes. The postfix mode is very similar to F83's
兩種支援的模式。後綴模式與 F83 的
CPU8086 Assembler. Prefix mode, which is the default mode, allows a
CPU8086 彙編器。前置詞模式 （預設模式） 允許
syntax which is much closer to MASM used by Intel and MicroSoft.
語法更接近英特爾和 MicroSoft 使用的 MASM。


The assembler supports prefix syntax in an attempt to provide a syntax
組譯器支援前置詞語法，以嘗試提供語法
which is more readable to programmers of other languages. The use of
對於其他語言的程式設計師來說，這更容易閱讀。使用
sequential text files for source code encourages the programmer to write
原始程式碼的順序文字檔案鼓勵程式設計師編寫
programs in the vertical code style with one statement per line. This
垂直程式碼樣式的程式，每行一個語句。這
style is what traditional assembler requires. F-PC works well in this
風格是傳統彙編商所需要的。F-PC 在這方面運作良好
style, if you choose to do so. However, F-PC does not prevent you from
風格，如果您選擇這樣做的話。但是，F-PC 並不妨礙您
writing in the horizontal code style, by which you can squeeze many
以水平代碼樣式編寫，通過它可以擠壓許多
statements into one line and make you own life miserable. It supports
陳述成一行，讓你自己的生活變得悲慘。它支持
postfix syntax to prevent alienating the established base of F83 users.
postfix 語法，以防止疏遠已建立的 F83 用戶基礎。


The prefix notation is close to the original Intel assembly syntax, and
前綴表示法接近原始 Intel 組件語法，並且
certainly will be more familiar to programmers of other languages. All
當然，其他語言的程式設計師會更熟悉。都
the code words defined in F-PC are coded in the prefix notation. Please
F-PC 中定義的碼字以前綴表示法編碼。請
consider writing any new assembly code you need in the prefix mode for
請考慮在前置詞模式下編寫您需要的任何新組合程式碼
distribution and assimilation with F-PC.
與 F-PC 的分佈和同化。


The assembly of a machine instruction is generally deferred to the
機器指令的組裝通常推遲到
following three events: when the next assembly mnemonic is encountered,
以下三個事件：當遇到下一個組合助記詞時，
at the end of a line, or when the command END-CODE or A; is executed.
在行尾，或當命令 END-CODE 或 A 時;被執行。
Therefore, a good style in writing code words in F-PC is to put one
因此，在 F-PC 中寫碼字的好風格就是放一個
assembly instruction in one line, followed by the parameter specification
一行組裝指令，後面是參數規格
or the arguments. Multiple assembly instructions are allowed in the same
或論點。允許在同一個
line. It is a good ideal to put the assembly structure words in separate
線。將組合結構字放在單獨的是一個很好的理想
lines with proper indentation so that the nested structures in a code
行具有適當的縮排，以便程式碼中的巢狀結構
definition can be perceived more readily.
定義可以更容易地被感知。


8.2. PASM GLOSSARY
8.2. PASM 詞彙表


Here we will only give a small list of PASM words in this glossary. All
在這裡，我們將在此詞彙表中只提供一小部分 PASM 單詞列表。都
assembly mnemonics are identical to those defined in F83 8086 Assembler.
組合助記詞與 F83 8086 Assembler 中定義的助記符相同。
All the structure directives and test conditions are also identical to
所有結構指令和測試條件也相同
those in F83. Only the most important FORTH words controlling the
F83 中的那些。只有最重要的 FORTH 詞控制
assembler are listed here.
彙編器會列在這裡。


PREFIX ( -- )
前綴 （ -- ）
Assert prefix mode for the following code definitions.
判斷提示下列程式碼定義的前置詞模式。


POSTFIX ( -- )
後綴 （ -- ）
Assert postfix mode for the following code definitions.
判斷提示下列程式碼定義的後置詞模式。


CODE <name> ( -- )
代碼 <name> （ -- ）
Define a new code definition using the following string as its
使用下列字串作為其定義新的程式碼定義
name. Assembly commands follow, terminated by END-CODE.
名字。接下來是組合命令，以 END-CODE 終止。


END-CODE ( -- )
結束代碼 （ -- ）
Terminate a code definition, check error conditions, and make
終止程式碼定義、檢查錯誤條件，並製作
the code definition available for searching and execution.
可用於搜尋和執行的程式碼定義。


LOCAL_REFS ( -- )
LOCAL_REFS （ -- ）
This mode WILL NOT allow local labels to cross CODE word
此模式「將不允許本機標籤跨越 CODE 字
boundaries. The local label mechanism is cleared each time a
邊界。每次
new CODE word is started. This is the DEFAULT mode.
新的 CODE 字開始。這是預設模式。


GLOBAL_REFS ( -- )
GLOBAL_REFS （ -- ）
All local labels will be available across all following code
所有本機標籤都將在下列所有程式碼中可用
definitions. The label mechanism is NOT reset at the beginning
定義。標籤機制一開始不會重設
of a CODE definition, so a local label reference can cross CODE
CODE 定義的，因此本機標籤參照可以跨越 CODE
word boundaries. The local label mechanism MUST be reset before
單詞邊界。本機標籤機制必須在之前重設
use in this mode, with the CLEAR_LABELS word.
在此模式下使用，並帶有 CLEAR_LABELS 字。


CLEAR_LABELS ( -- )
CLEAR_LABELS （ -- ）
Clear the local label mechanism, to the unused or clean state,
清除本地標籤機制，轉為未使用或乾淨狀態，
in preparation for using local labels. This word need only be
準備使用本地標籤。這個詞只需要是
used in the GLOBAL_REFS mode. The LOCAL_REFS mode automatically
在 GLOBAL_REFS 模式下使用。自動 LOCAL_REFS 模式
performs a CLEAR_LABELS each time a CODE definition is started.
每次啟動 CODE 定義時執行 CLEAR_LABELS。


A; ( -- )
一個;( -- )
Complete the assembly of the previous machine instruction.
完成上一個機器指令的組裝。


BYTE ( -- )
位元組 （ -- ）
Assemble current and subsequent code using byte arguments, if
使用位元組引數組合目前和後續程式碼，如果
register size is not explicitly specified in prefix mode. WORD
暫存器大小未在前置詞模式中明確指定。字
is default in postfix mode.
在後綴模式下是預設值。


WORD ( -- )
字 （ -- ）
Assemble current and subsequent code using 16 bit arguments, if
使用 16 位元引數組合目前和後續程式碼，如果
register size is not explicitly specified in postfix mode. BYTE
暫存器大小未在後置詞模式中明確指定。位元組
is default in prefix mode.
在前置詞模式下預設。


LABEL ( -- )
標籤 （ -- ）
Start an assembly subroutine or mark the current code address to
啟動組件子常式，或將現行程式碼位址標示為
be referenced later.
稍後參考。



Figure 8.1. Comparison of assembly syntax
圖 8.1.組合語法比較


PREFIX POSTFIX MASM
前綴後綴 MASM


AAA AAA AAA
ADC AX, SI SI AX ADC ADC AX,SI
ADC AX、SI SI AX、ADC ADC AX、SI
ADC DX, 0 [SI] 0 [SI] DX ADC ADC DX,0[SI]
ADC DX，0 [SI] 0 [SI] DX ADC ADC DX，0[SI]
ADC 2 [BX+SI], DI DI 2 [BX+SI] ADC ADC 2[BX][SI],DI
ADC 2 [BX+SI]，DI DI 2 [BX+SI] ADC ADC 2[BX][SI]，DI
ADC MEM BX BX MEM #) ADC ADC MEM,BX
ADC MEM BX BX MEM #） ADC ADC MEM，BX
ADC AL, # 5 5 # AL ADC ADC AL,5
ADC AL，#5 5 # AL ADC ADC AL，5
AND AX, BX BX AX AND AND AX,BX
和斧，BX，BX，AX，和斧，BX
AND CX, MEM CX MEM #) AND AND CX,MEM
和 CX、MEM CX MEM #） 和 CX，MEM
AND DL, # 3 3 # DL AND AND DL,3
和 DL，#3 3 # DL 和 DL，3
CALL NAME NAME #) CALL CALL NAME
呼叫名稱名稱 #） 呼叫呼叫名稱
CALL FAR [] NAME FAR [] NAME #) CALL ?????
呼叫遠方 [] 名稱 遠方 [] 名稱 #） 呼叫?????
CMP DX, BX BX DX CMP CMP DX,BX
CMP DX、BX BX DX CMP、CMP、CMP、DX、BX
CMP 2 [BP], SI SI 2 [BP] CMP CMP [BP+2],SI
CMP 2 [BP]，SI SI 2 [BP] CMP CMP [BP+2]，SI
DEC BP BP DEC DEC BP
12 月 BP BP 12 月 12 月 BP
DEC MEM MEM DEC DEC MEM
DEC 3 [SI] 3 [SI] DEC DEC 3[SI]
12 月 3 日 [SI] 3 [SI] 12 月 3 日
DIV CL CL DIV DIV CL
DIV MEM MEM DIV DIV MEM
IN PORT# WORD WORD PORT# IN IN AX,PORT#
IN PORT# WORD WORD PORT# IN IN AX，PORT#
IN PORT# PORT# IN IN AL,PORT#
在連接埠# 連接埠# 在 AL，連接埠#
IN AX, DX DX AX IN IN AX,DX
在 AX、DX DX AX 在 AX、DX 中
INC MEM BYTE MEM INC INC MEM BYTE
INC MEM WORD MEM #) INC INC MEM WORD
INT 16 16 INT INT 16
智力 16 16智力 16
JA NAME NAME JA JA NAME
JA 名稱 名稱 JA JA 名稱
JNBE NAME NAME #) JNBE JNBE NAME
JNBE 名稱名稱 #） JNBE JNBE 名稱
JMP NAME NAME #) JMP JMP
JMP 名稱名稱 #） JMP JMP
JMP FAR [] NAME NAME [] FAR JMP JMP [NAME]
JMP FAR [] 名稱 名稱 [] FAR JMP JMP [名稱]
JMP FAR $F000 $E987 JMP F000:E987
JMP 遠$F 000 $E 987 JMP F000：E987
LODSW AX LODS LODS WORD
LODSW AX LODS LODS 字
LODSB AL LODS LODS BYTE
LODSB AL LODS LODS 位元組
LOOP NAME NAME #) LOOP LOOP NAME
循環名稱 名稱 #） 循環循環名稱
MOV DX, NAME NAME #) DX MOV MOV DX,[NAME]
MOV DX，名稱名稱 #） DX MOV MOV DX，[名稱]
MOV AX, BX BX AX MOV MOV AX,BX
MOV AH, AL AL AH MOV MOV AH,AL
莫夫·阿，阿爾·阿爾·莫夫·莫夫·阿爾，阿爾·阿爾
MOV BP, 0 [BX] 0 [BX] BP MOV MOV BP,0[BX]
MOV BP，0 [BX] 0 [BX] BP MOV MOV BP，0[BX]
MOV ES: BP, SI ES: BP SI MOV MOV ES:BP,SI
MOV ES：BP，SI ES：BP SI MOV 移動 ES：BP，SI
MOVSW AX MOVS MOVS WORD
MOVSW AX MOVS MOVS 字
POP DX DX POP POP DX
流行 DX DX 流行流行 DX
POPF POPF POPF
PUSH SI SI PUSH PUSH SI
推 SI SI 推 推 SI
REP REP REP
代表
RET RET RET
雷特
ROL AX, # 1 AX ROL ROL AX,1
羅爾斧頭，#1 斧頭 羅爾羅爾斧頭，1
ROL AX, CL AX CL ROL ROL AX,CL
SHL AX, # 1 AX SHL SHL AX,1
SHL 斧頭，#1 AX SHL SHL AX，1
XCHG AX, BP BP AX XCHG XCHG AX,BP
XCHG 斧、BP BP AX、XCHG XCHG AX、BP
XOR CX, DX DX, CX XOR XOR CX,DX
異或 CX、DX DX、CX 異或異或 CX、DX



8.3. SYNTAX COMPARISON
8.3. 語法比較


The differences among the F-PC prefix mode, the F83 postfix mode, and the
F-PC 前綴模式、F83 後綴模式和
Intel MASM notation are best illustrated by the table in Figure 8.1.
英特爾 MASM 表示法最好地由圖 8.1 中的表格說明。
Although the table is not exhaustive, it covers most of the cases useful
雖然該表並不詳盡，但它涵蓋了大多數有用的情況
in doing PASM programming. You are welcome to suggest additional cases
在進行 PASM 編程時。歡迎您提出其他案例
to be included in this table.
要包含在此表中。


8.4. USAGE OF 8086 MACHINE REGISTERS IN F-PC
8.4. F-PC 中 8086 機器暫存器的使用


To write assembly code, you have to know the CPU real well. Most CPU's
要編寫彙編程式碼，您必須非常了解 CPU。大多數 CPU 的
can be understood and programmed using a CPU model, consisting of the
可以使用 CPU 模型來理解和編程，該模型由
register set and the instructions which manipulate data among the
暫存器集以及操作資料的指令
registers, memory, and external devices. In F83, only a 64K bytes
暫存器、記憶體和外部裝置。在 F83 中，只有 64K 位元組
segment of memory is used, and all segment registers in 8086 are
使用記憶體的段，8086中的所有段暫存器都是
generally pointing to the same code segment. Since F-PC uses many
一般指向同一個程式碼段。由於 F-PC 使用許多
segments to store code, heads, lists, and other data, you have to know
段來儲存程式碼、標題、清單等數據，你必須知道
how these segment registers are used and how information in different
如何使用這些段暫存器以及不同
segments can be accessed conveniently.
可以方便地訪問區段。


Following is a list of the 8086 registers and their usage in F-PC:
以下是 8086 暫存器及其在 F-PC 中的用法清單：


CS Code seg: used for any code definitions (Must be
CS Code seg：用於任何程式碼定義（必須是
preserved by code word.)
由代碼字保留。


DS Data seg: used for data other than ." strings (NOTE:
DS Data seg：用於“字符串以外的數據（注意：
CS=DS and underlying kernel primitives rely on this
CS=DS 和底層核心原語依賴於此
correspondence! Must be preserved by code word.)
函！必須以代碼字保留。


ES Extra seg: used as the segment location for the current
ES Extra seg：用作當前的區段位置
instruction pointer (IP). (Must be preserved by code
指令指標 （IP）。（必須透過程式碼保留
word.)
單詞。


SS Stack seg: used as the segment location for the current
SS 堆疊段：用作目前
stack pointer (SP). (Must be preserved by code word.)
堆疊指標 （SP）。（必須以代碼字保留。


BP Return Pointer (RP). (Must be preserved by code word.)
BP 返回指標 （RP）。（必須以代碼字保留。


SP Stack Pointer (SP). (Must be preserved by code word.)
SP 堆疊指標 （SP）。（必須以代碼字保留。


SI Instruction Pointer (IP). (Must be preserved by code
SI 指令指針 （IP）。（必須透過程式碼保留
word.)
單詞。


AX, BX, CX, DX, & DI Scratch registers free to use without
AX、BX、CX、DX 和 DI Scratch 暫存器免費使用，無需
restoration.
恢復。


PC Program Counter. Not used by F-PC.
PC 程式計數器。F-PC 不使用。


DF Direction Flag. Assumed to be 0/increment. Some older FF
DF 方向旗標。假設為 0/增量。一些較舊的 FF
(or before?) words do an initial CLD (e.g., CMOVE), but
（還是更早？單詞做一個初始 CLD（例如，CMOVE），但是
this shouldn't be necessary. If you specifically need
這應該沒有必要。如果您特別需要
DF=1, then do: STD ...code... CLD
DF=1，則執行：STD ...法典。。。CLD 的


AX is used as a general purpose accumulator. BX is most useful as a base
AX 用作通用累加器。BX 作為基礎最有用
register for indexing into an array. CX is used to hold a count for
註冊以索引到陣列中。CX 用於保留
looping and repeating operations. DX is useful in holding the address of
循環和重複操作。DX 可用於保存
an I/O port. DS:SI pair is used to read memory with auto-indexing, and
一個 I/O 連接埠。DS：SI 配對用於讀取具有自動索引的記憶體，並且
ES:DI pair is used to write memory with auto-indexing.
ES：DI 對用於寫入具有自動索引的記憶體。


F-PC uses SP as the data stack pointer and BP as the return stack
F-PC 使用 SP 作為資料堆疊指針，BP 作為返回堆疊
pointer. SP is convenient in the PUSH and POP instructions, while BP is
指標。SP 在 PUSH 和 POP 指令中很方便，而 BP 則是
more convenient in indexing. There are many occasions that you might
索引更方便。在很多情況下，您可能會
want to swap SP and BP to use the most effective way to address data on
想要交換 SP 和 BP，以使用最有效的方式處理資料
either stack.
任一堆疊。


The F-PC Technical Reference Manual discusses in great details how F-PC
F-PC 技術參考手冊詳細討論了 F-PC 如何
itself is constructed based on the 8086 assembly code. If you are
本身是根據 8086 彙編代碼構建的。如果你是
interested in squeezing the last drop of blood from PC/XT/AT, be sure to
有興趣從 PC/XT/AT 中榨出最後一滴血，一定要
study carefully the Technical Reference Manual and the kernel files in
仔細研究技術參考手冊和
F- PC.
F-個人電腦。


8.5. ADDRESSING MODES
8.5. 尋址模式


The most difficult problem in using 8086 assembler is to figure out the
使用8086彙編器最難的問題就是搞清楚
correct addressing mode and code it into an instruction. You can get a
正確的尋址模式並將其編碼為指令。您可以獲得一個
good ideal and probably figure out most of the addressing mode syntax
很好的理想，並且可能弄清楚大部分尋址模式語法
from the above table. However, there are cases where the table falls
從上表來看。但是，在某些情況下，桌子會倒下
short. Here we will try to summarize the addressing syntax more
短。這裡我們就嘗試對尋址語法進行更多的總結
systematically to show you how F-PC handles addresses in the prefix mode.
系統地向您展示 F-PC 如何在前綴模式下處理地址。


Register Mode
註冊模式


Source or destination is a register in the CPU. The source registers
來源或目的地是 CPU 中的暫存器。來源暫存器
are:
是：


AL BL CL DL AH BH CH DH
AX BX CX DX SP BP SI DI IP RP CS DS SS ES


Destination register specifications are:
目的地暫存器規格為：


AL, BL, CL, DL, AH, BH, CH, DH,
AL、BL、CL、DL、AH、BH、CH、DH、
AX, BX, CX, DX, SP, BP, SI, DI, IP, RP, CS, DS, SS, ES,
AX、BX、CX、DX、SP、BP、SI、DI、IP、RP、CS、DS、SS、ES、


The register name must be followed by a 'comma', to be recognized by PASM
暫存器名稱後面必須跟一個“逗號”，以便 PASM 識別
as a destination register.
作為目的地暫存器。


Immediate Mode
即時模式


The argument is assembled as a literal in the instruction. The immediate
引數在指令中組合為文字。即時
value must be preceded by the symbol #, which is a word and must be
value 前面必須有符號 #，這是一個單詞，必須是
delimited by spaces:
以空格分隔：


MOV AX, # 1234
莫夫斧頭，#1234
ADD CL, # 32
添加 CL，#32
ROL AX, # 3
羅爾·阿克斯，#3


Direct Mode
直接模式


An address is assembled into the instruction. This is used to specify an
位址會組合到指令中。這可用來指定
address to be jumped to or a memory location for data reference. The
要跳轉到的位址或用於資料參考的記憶體位置。這
address is used directly as a 16 bit number. Depending on the
地址直接用作 16 位數字。根據
instruction, the address may be assembled unmodified or assembled as an
指令，則該位址可以未經修改地組合，也可以組合為
eight or 16 bit offset in the branch instructions. To jump or call
分支指令中的 8 或 16 位偏移量。跳轉或呼叫
beyond a 64K byte segment, the address must be preceded by FAR [] .
超過 64K 位元組段，地址前面必須有 FAR []。
Examples are:
範例如下：


CALL FAR [] <label>
撥打遠方 [] <label>
JMP <dest>
MOV BX, <source>
莫夫 BX， <source>
INC <dest> WORD
INC <dest> 字
JZ <label>


The destination address may be taken from the data stack directly:
目的地位址可以直接從資料堆疊取得：


MOV CX, # 16
MOV CX，#16
HERE ( save current code address on stack) ...
HERE（將當前代碼地址保存在堆棧上）...
... LOOPZ ( loop back to HERE if condition fails)
...LOOPZ（如果條件失敗，則環回 HERE）


Index Mode
索引模式


One or two registers can be used as index registers to scan through data
一個或兩個暫存器可用作索引暫存器來掃描數據
arrays. The contents of the index register or the sum of the contents of
陣列。索引暫存器的內容或
two index registers are used to form a base address. An offset is added
兩個索引暫存器用於形成基地址。會加入偏移
to the base address to form the true address for data reference.
到基址，形成資料參考的真實位址。
Examples are:
範例如下：


CMP 2 [BP], SI
CMP 2 [BP]，SI
DEC 3 [SI]
12 月 3 日 [SI]
MOV BP, 0 [BX]
MOV BP，0 [BX]


The following register index specifications are allowed in F-PC:
F-PC 中允許以下暫存器索引規格：


[SI] [IP] [BP] [RP] [DI] [BX]
[SI][知識產權][BP][RP][迪] [BX]
[BX+SI] [SI+BX] [BX+IP] [IP+BX] [BX+DI] [DI+BX]
[BX+SI][SI+BX][BX+IP][IP+BX][BX+DI][DI+BX]
[BP+SI] [SI+BP] [BP+IP] [IP+BP] [RP+IP] [IP+RP]
[BP+SI][SI+BP][BP+IP][IP+BP][RP+IP][IP+RP]
[BP+DI] [DI+BP] [RP+DI] [DI+RP]
[BP+DI][DI+BP][RP+DI][DI+RP]


There must be an offset number preceding the index register
索引暫存器之前必須有一個偏移編號
specification, even if the offset is 0. When the index register is used
規格，即使偏移量為 0。使用索引暫存器時
as destination, a comma must be appended immediately:
作為目的地，必須立即附加逗號：


MOV 0 [BX+IP], AX
MOV 0 [BX+IP]、AX


Implied Mode and Segment Override
隱含模式和區段覆寫


The implied mode is where mistakes are most likely to occur because you
隱含模式是最有可能發生錯誤的地方，因為您
will have to be keenly aware of which segment register is used by the
必須敏銳地意識到
instruction at any instance. Since the segment register is implied and
在任何情況下的指示。由於段暫存器是隱含的 和
not stated explicitly, the bug generally can hide very securely
沒有明確說明，該錯誤通常可以非常安全地隱藏
underneath laughing at you. The code works when you test it but fails
下面嘲笑你。程式碼在您測試時運作，但失敗
when the segment register is modified.
當段暫存器被修改時。


Branch and jump instructions use CS segment register.
分支和跳轉指令使用 CS 段暫存器。
Data movement instructions use DS segment register.
資料移動指令使用 DS 區段暫存器。
Stack instructions use SS segment.
堆疊指令使用 SS 區段。
String instructions use DS:SI as source and ES:DI as destination.
字串指令使用 DS：SI 作為來源，並使用 ES：DI 作為目的地。


If you need to specify an address with a segment register other than the
如果您需要指定具有區段暫存器以外的位址
default implied register, use a segment override instruction before the
預設隱含暫存器，則在
address specification:
地址規格：


CS: DS: ES:
CS：DS：ES：


Examples are:
範例如下：


MOV ES: BP, SI
移動 ES：BP、SI
CMP CS: 2 [BP], AX
CMP CS：2 [BP]，AX
ADD AX, ES: 10 [BX+DI]
加軸，ES：10 [BX+DI]


The 8086 addressing modes are so confusing that even experienced
8086 尋址模式非常混亂，甚至有
programmers need a good Intel 8086 manual to find the right addressing
程式設計師需要一本好的 Intel 8086 手冊才能找到正確的尋址
mode and the F-PC assembler syntax table to determine the correct
mode 和 F-PC 組譯器語法表，以判斷正確的
argument list.
參數清單。


The best way to write assembly code is still to keep the code short and
編寫彙編程式碼的最佳方式仍然是保持程式碼簡短且
simple. It is very easy in F- PC to break a long CODE definition into
簡。在 F-PC 中，將長 CODE 定義分解為
many small fragments which are initially defined as separate CODE
許多小片段，最初定義為單獨的 CODE
definitions. After verifying that each fragment works, you can edit out
定義。確認每個片段正常運作後，您可以編輯掉
the CODE, NEXT, and END-CODE lines to combine the fragments into a single
CODE、NEXT 和 END-CODE 行，將片段合併為單一
CODE definition.
CODE 定義。


Charles Curley kindly contributed an 8086 disassembler. It is helpful to
Charles Curley 好心地貢獻了一個 8086 反彙編器。這對
disassemble the code word you defined and see what the computer thinks of
拆解你定義的碼字，看看電腦怎麼想
what you mean. There is always this 'Do what I mean, not what I say'
你的意思是什麼。總是有這樣的說法：『做我的意思，而不是我說的』
syndrome. When everything else has failed, you can jump into DOS and
綜合症。當其他一切都失敗時，您可以跳到 DOS 和
call up DEBUG and use the facility there to find what goes wrong. In DOS
調用 DEBUG 並使用那裡的工具來查找問題所在。在 DOS 中
DEBUG, you can step through a piece of code one instruction at a time.
DEBUG，您可以一次逐步執行一段程式碼。
This is absolutely the last thing you want to do.
這絕對是你最不想做的事情。


8.6. ASSEMBLY MACROS IN PASM
8.6. PASM 中的彙編巨集


Another area of interest is the assembly macros. Here is the definition
另一個感興趣的領域是組裝巨集。這是定義
of the NEXT macro:
下一個巨集：


: NEXT >PRE JMP >NEXT A; PRE> ;
：下一個 >JMP 之前>下一個 A;前> ;


The macro itself is simply assembling the sequence JMP >NEXT. The
巨集本身只是組裝序列 JMP >NEXT.這
surrounding words are used for support. Since PASM supports both postfix
周圍的詞語用於支持。由於 PASM 支援後綴
as well as prefix notation, it is not known on entry to a macro which
除了前綴符號之外，在進入巨集時也不知道，其中
mode is in effect. The words >PRE and PRE> select prefix, and restore
模式生效。單字 >PRE 和 PRE> select 前置詞，然後還原
the previous mode so macros will always be in prefix notation. The A;
先前的模式，因此巨集將始終採用前綴表示法。The A;
after >NEXT, forces the assembling of the JMP instruction before
在>NEXT 之後，強制彙編 JMP 指令之前
switching mode.
切換模式。


You can find many other examples of assembly macros in PASM.SEQ, like
您可以在 PASM 中找到許多其他組合宏範例。SEQ，如
1PUSH, 2PUSH, and all the assembly structure building directives.
1PUSH、2PUSH 及所有元件結構建置指令。


8.7. LOCAL LABEL
8.7. 本地標籤


To support large code definitions, Bob Smith introduced 'local labels' to
為了支援大型程式碼定義，Bob Smith 將「本機標籤」引入
F-PC. The local labels are place markers $: preceded by a number. They
F-PC。本機標籤是位置標記 $： 前面有一個數字。他們
are used to mark locations in a large code definition for forward and
用於標記大型程式碼定義中轉發和
backward jumps and branches which uses $ preceded by the number of the
向後跳轉和分支，使用 $ 前面的數字
local label as address specification. They can be used quite freely in a
本地標籤作為地址規格。它們可以非常自由地用於
range of code words and reused to save head space by replacing LABELs
代碼字的範圍，並重複使用，以取代 LABEL 來節省頭部空間
which have global names and cannot be reused.
具有全域名稱且無法重複使用。


The use of local labels is best demonstrated by an example taken from the
本地標籤的使用最好通過取自
software floating point package SFLOAT.SEQ by Bob Smith, shown in Figure
軟體浮點套件 SFLOAT。Bob Smith 的 SEQ，如圖所示
8.2. Up to 32 local labels can be used to mark addresses of assembly
8.2. 最多可使用 32 個本地標籤來標記組裝地址
code. They can be referred to before or after their placements. They
法典。可以在安置之前或之後參考它們。他們
can be referenced across code word boundaries.
可以跨代碼字界限引用。


Local labels in PASM are useful within a CODE definition, using
PASM 中的本機標籤在 CODE 定義中很有用，使用
LOCAL_REFS as the default label mode. If you need to use local labels
LOCAL_REFS 作為預設標籤模式。如果您需要使用本機標籤
between CODE definitions, you will have to select the GLOBAL_REFS mode,
在 CODE 定義之間，您必須選擇 GLOBAL_REFS 模式，
and use CLEAR_LABELS to initialize the local labels manually each time
並每次使用 CLEAR_LABELS 手動初始化本機標籤
you want to start a new set of local labels.
您想要開始一組新的本機標籤。


This technique is especially useful where the one-entry-one-exit dogma is
這種技術在一進一出教條的情況下特別有用
very awkward and when a piece of code has multiple entry points and can
非常尷尬，當一段程式碼有多個入口點並且可以
be shared among many code word definitions. It enables us to construct
在許多碼字定義之間共享。它使我們能夠建構
structured spaghetti code, if there were such thing.
結構化的義大利麵程式碼，如果有這樣的東西的話。


Local label allows relative short branches within 127 bytes. To jump
本機標籤允許 127 位元組內的相對短分支。跳躍
beyond this range, the long jump label L$ should be used:
超過此範圍，應使用跳遠標籤 L$：


...
...
JMP L$
...
...
L$: ...
L$：......
...


The long jump label can only be used to jump forward. After L$: is used,
跳遠標籤只能用於向前跳躍。使用 L$： 之後，
you can do another long forward jump using L$ again.
您可以再次使用 L$ 進行另一次向前跳遠。



8.8. INLINE CODE
8.8. 內聯程式碼



INLINE allows us to include machine code inside a high level colon
INLINE 允許我們將機器代碼包含在高級冒號中
definition. This is easily done in F-PC because it is built on direct
定義。這在 F-PC 中很容易完成，因為它是建立在直接
threaded code. Every word is compiled as a code address in the colon
執行緒程式碼。每個單字都被編譯為冒號中的代碼位址
definition. The code in the code segment pointed to by the code address
定義。代碼位址所指向的代碼段中的代碼
is executed directly because it contains genuine 8086 machine code.
直接執行，因為它包含正版8086機器碼。
Whether the code belongs to a colon definition or a code definition does
程式碼屬於冒號定義還是程式碼定義屬於冒號定義
not make any difference. INLINE only has to compile the address pointing
沒有任何區別。INLINE 只需要編譯指向的位址
to the top of the dictionary in the code segment. The assembler is then
到字典在程式碼區段中頂端。然後，組譯器是
invoked to compile machine code. If the code is terminated by NEXT or
呼叫來編譯機器碼。如果程式碼以 NEXT 或
one of its derivatives, the next word compiled in the colon definition
它的派生詞之一，在冒號定義中編譯的下一個詞
will be executed after the assembly code is done. END-INLINE only has to
將在彙編程式碼完成後執行。END-INLINE 只需要
clean up the assembly environment and return the control back to the
清理組裝環境，並將控制權傳回
colon compiler.
冒號編譯器。


Here is an example on how to use INLINE and END-INLINE to add assembly
以下是如何使用 INLINE 和 END-INLINE 新增彙編的範例
code in the middle of a colon definition:
冒號定義中間的程式碼：


: TEST ( -- )
： 測試 （ -- ）
5 0 DO
5 0 做
I \ Get loop index
I \ 取得循環索引
INLINE
內聯
pop ax \ pop I
流行斧頭 \ 流行 I
add ax, # 23 \ add 23
添加斧頭，# 23 \ 添加 23
1push \ push sum
1push \ push 總和
END-INLINE
內嵌端
. \ print results
.\ 列印結果
LOOP
圈
;


Figure 8.2. Examples of local labels
圖 8.2.本地標籤示例


LABEL DENORM \ CX = count, BX = Hi, DX = LO, AX = Guard, Round, & Sticky.
標籤 DENORM \ CX = 計數，BX = Hi，DX = LO，AX = Guard，Round 和 Sticky。
CLEAR_LABELS
XOR AX, AX \ Clear GRS bits
XOR AX， AX \ 清除 GRS 位元
CMP CX, # 10 \ Check size of shift
CMP CX，#10 \ 檢查班次規模
JL 7 $ \ Branch if shift less than 16
JL 7 $ \ 如果班次少於 16 點，則分行
CMP CX, # 18 \ Cnt >= 16. Compare with 24.
CMP CX，#18 \ Cnt >= 16。與 24 相比。
JGE 1 $ \ Branch if shift >= 24
JGE 1 $ \ 如果班次 >= 24 則分支
SUB CX, # 10 \ 16 <= cnt < 24. Subtract 16 from cnt.
SUB CX，#10 \ 16 <= cnt < 24。從 cnt 中減去 16。
MOV AX, DX \ Shift by one word.
MOV AX， DX \ 移動一個字。
MOV DX, BX
MOV DX、BX
XOR BX, BX \ Clear MS word.
XOR BX， BX \ 清除 MS 字。
AND AL, AL \ Don't miss any sticky bits.
還有 AL， AL \ 不要錯過任何粘性部分。
JZ 8 $
OR AH, # 2 \ Set a sticky bit.
或者 AH，#2 \ 設置一個粘性鑽頭。
JMP 8 $ \ Shift from 0 to 7 bits.
JMP 8 $ \ 從 0 位移至 7 位。
1 $: CMP CX, # 20 \ Cnt >= 24. Compare with 32.
1 $：CMP CX，# 20 \ Cnt >= 24。與 32 相比。
JGE 3 $ \ Branch if shift >= 32.
JGE 3 $ \ 如果班次 >= 32，則分支。
MOV AH, BL \ 24 <= cnt < 32, so shift by 3 bytes.
MOV AH， BL \ 24 <= cnt < 32，因此移動 3 位元組。
MOV AL, DH
莫夫阿爾，DH
OR AL, DL \ OR in the sticky bits.
或 AL、DL \ 或在粘性位中。
JZ 2 $ \ Shall we set a sticky bit?
JZ 2 $ \ 我們設置一個粘性位好嗎？
OR AH, # 2 \ Yes.
或者啊，#2 \ 是的。
2 $: MOV DL, BH \ Continue the 3-byte shift.
2 $： MOV DL， BH \ 繼續 3 位元組移位。
XOR DH, DH \ Clear the high 3 bytes.
XOR DH， DH \ 清除高 3 位元組。
XOR BX, BX
異或 BX、BX
SUB CX, # 18 \ Adjust the shift counter.
SUB CX，#18 \ 調整換檔計數器。
JMP 8 $ \ Shift remaining 0 to 7 places.
JMP 8 $ \ 將剩餘的 0 位移至 7 位。
3 $: CMP CX, # 28 \ Cnt >= 32. Check against 40.
3 $：CMP CX，# 28 \ Cnt >= 32。檢查 40。
JGE 5 $ \ Branch if shift count > 40.
JGE 5 $ \ 如果班次計數> 40 分行。
MOV AX, BX \ 32 <= cnt < 40. Do a 2 word shift.
MOV AX， BX \ 32 <= CNT < 40.做 2 個單詞的轉變。
OR AL, DH \ Check the sticky bits.
或 AL， DH \ 檢查粘性位。
OR AL, DL
或 AL，DL
JZ 4 $ \ If sticky byte not zero,
JZ 4 $ \ 如果黏性位元組不為零，
OR AH, # 2 \ then set sticky bit.
或 AH，#2 \ 然後設置粘性鑽頭。
4 $: XOR BX, BX \ Clear high and low words.
4 $：XOR BX、BX \ 清除高低單字。
XOR DX, DX
異或 DX、DX
SUB CX, # 20 \ Adjust shift counter.
SUB CX，#20 \ 調整換檔計數器。
JMP 8 $ \ Go to final shift area.
JMP 8 $ \ 前往最後一班區域。
5 $: OR BX, DX \ Shift count >= 40
5 $：或 BX，DX \ 班次計數 >= 40
JZ 0A $ \ In theory, this should never jump.
JZ 0A $ \ 理論上，這永遠不應該跳躍。
MOV AH, # 2 \ So set a sticky bit.
MOV AH，#2 \ 所以設置一個粘性位。
XOR BX, BX \ Clear all the rest.
XOR BX， BX \ 清除所有其餘部分。
XOR DX, DX
異或 DX、DX
RET
7 $: CMP CX, # 8 \ Count < 16. See if less than 8.
7 $：CMP CX，#8 \ 計數< 16。看看是否小於 8。
JL 8 $
MOV AH, DL \ 8 <= cnt < 16.
MOV AH， DL \ 8 <= CNT < 16.
MOV DL, DH \ Move by one byte.
MOV DL， DH \ 移動一個位元組。
MOV DH, BL
MOV DH、BL
MOV BL, BH
莫夫 BL，BH
XOR BH, BH \ Clear high byte.
XOR BH， BH \ 清除高位元組。
SUB CX, # 8 \ Adjust shift count.
SUB CX，#8 \ 調整班次計數。
8 $: AND CX, CX \ Test for zero count.
8 $：和 CX、CX \ 測試零計數。
JZ 0A $
9 $: SHR BX, # 1 \ Shift right by one bit.
9 $：SHR BX，#1 \ 向右移動一位。
RCR DX, # 1
RCR DX，#1
RCR AX, # 1
RCR AX，#1
LOOP 9 $ \ Loop until count is 0.
循環 9 $ \ 循環直到計數為 0。
0A $: RET
0A $：RET
END-CODE
結束代碼



8.9. ASSEMBLER STYLE
8.9. 彙編器風格



To code 80x86 assembly routines successfully, you have to pay attention
要成功編寫 80x86 彙編例程，您必須注意
to many things simultaneously, making it very exciting and interesting
同時進行許多事情，使其非常令人興奮和有趣
occasionally, but frustrating most of the time. To make it easier for
偶爾，但大多數時候都令人沮喪。為了方便
yourself, you can follow the following coding style to avoid the most
自己，可以按照以下編碼風格，避免最多
serious pitfalls in writing assembly code:
編寫彙編程式碼的嚴重陷阱：


code gizzmo ( input1 input2 input3 ... -- output1 output2 ...)
代碼 gizzmo （ 輸入 1 輸入 2 輸入 3 ... -- 輸出 1 輸出 2 ...）


pop ax \ input section
彈出斧\輸入部分
pop bx \ pop everything into registers
pop bx \ 將所有內容彈出到暫存器中
pop cx
流行 CX
...


push si \ saving section
push si \ saving 部分
push ds \ save all registers you will use
push ds \ 保存您將使用的所有暫存器
push es
推 ES
push cs
推送 CS


... \ code body
... \ 程式碼體
... \ do your creative coding
... \ 做你的創意編碼
...


pop cs \ restoring section
pop cs \ 恢復部分
pop es \ restore all saved registers
pop es \ 恢復所有已儲存的暫存器
pop ds
流行 DS
pop si
波普西


push cx \ output section
push cx \ 輸出部分
push dx \ 2push
推 DX \ 2 推
push ax \ 1push
推斧 \ 1push
next
下一頁


end-code \ you can breath now
end-code \ 你現在可以呼吸了


Make a boiler plate code template and delete whatever is not needed.
製作一個樣板代碼模板並刪除不需要的任何內容。
This style sheet will save you lots of grief if you follow it
如果您遵循此樣式表，它將為您節省很多悲傷
religiously, with a prayer, some incense, and a bottle of aspirins.
虔誠地，用祈禱、一些香和一瓶阿司匹林。


The 8086 registers have their special characteristics. Counts should be
8086 暫存器有其特殊性。計數應該是
popped into CX, data into AX or DX, and addresses into BX. For string
彈出到 CX 中，數據進入 AX 或 DX，地址進入 BX。對於字串
operations, DS:SI is used for source and ES:DI for destination. Because
作業，DS：SI 用於來源，ES：DI 用於目的地。因為
F-PC uses ES:SI as its IP, they must be saved and restored. You should
F-PC 使用 ES：SI 作為其 IP，必須保存和恢復它們。你應該
also constantly remind yourself that F-PC requires that CS, DS, and SS
還不斷提醒自己，F-PC 需要 CS、DS、SS
all point to the Code Segment, and that ES points to the List Segment.
都指向代碼段，而該 ES 指向列表段。
If you do not restore them to this state, NEXT will certainly crash the
如果您不將它們恢復到此狀態，NEXT 肯定會使
system to verify the fact. However, you should not fear crashing the
系統來驗證事實。但是，您不應該擔心崩潰
system. It is the daily portion which keeps a Forth programmer alert and
系統。這是讓 Forth 程序員保持警覺的每日部分，並且
nourished. It also helps to remind the computer who is the master lest
滋養。它還有助於提醒計算機誰是主人，以免
it forgets, which it often does.
它忘記了，而且經常會這樣。


8.10. DEBUGGING CODE WORDS
8.10. 偵錯碼字


Debugging large code words is very difficult. You are encouraged to
調試大型碼字非常困難。我們鼓勵您
avoid writing large code words for this reason. The best way to optimize
因此，避免編寫大型碼字。最佳優化方式
your Forth application is first writing everything in high level colon
您的 Forth 應用程序首先在高級冒號中寫入所有內容
words. After you have debugged the application and have a working
言。在您偵錯應用程式並運作
system, examine the colon words carefully to identify the 'critical
系統，仔細檢查冒號單詞以確定“關鍵
routines' where the computer spends most of its time. Only these
例程“，計算機花費大部分時間的地方。只有這些
routines need to be converted to code words.
例程需要轉換為碼字。


If a critical routine is a long colon definition, try to break it into
如果關鍵常式是長冒號定義，請嘗試將其分成
small pieces which can be conveniently converted to code words. If the
可以方便地轉換為代碼字的小塊。如果
code words are small, coding and testing them will be easy. If you have
代碼字很小，編碼和測試它們會很容易。如果您有
to build a large code word, code it in small pieces anyway. It is easy
要構建一個大型代碼字，無論如何都要將其編碼成小塊。這很容易
to merge small code words into a large code word.
將小碼字合併為大碼字。


If you take every precaution in writing a code word but it still fails to
如果你在編寫一個代碼字時採取了一切預防措施，但它仍然失敗
work, you have a last chance. Because F-PC has the capability to spawn a
工作，你還有最後的機會。因為 F-PC 有能力生成一個
DOS shell, using the command SYS and ` (back tick), you can invoke the
DOS shell，使用命令 SYS 和 '（反引號），您可以調用
DEBUG program in DOS to step through a code word. For example, if you
DOS 中的 DEBUG 程式來逐步執行程式碼字。例如，如果您
want to debug the code word GIZZMO, load and assemble it into your
想要調試碼字 GIZZMO，載入並組裝到你的
dictionary and execute:
字典並執行：


' GIZZMO HEX U.
' 吉茲莫十六進制 U。


to find its address in the dictionary. You can find the code segment of
在字典中找到它的地址。您可以找到
your dictionary by
您的詞典依據


?CS: U.
？CS：美國。


Write these numbers on a piece of paper so that you can find the code
將這些數字寫在一張紙上，以便找到代碼
after you are in DOS DEBUG. To invoke DOS DEBUG, type:
在您進入 DOS DEBUG 之後。若要叫用 DOS DEBUG，請鍵入：


SYS DEBUG or ` DEBUG
SYS DEBUG 或 ' DEBUG


You have to make sure that you have COMMAND.COM and DEBUG.COM in your
您必須確保您的 COMMAND.COM 和 DEBUG.COM
current directory or in the PATH before you execute the SYS word. If
目前目錄或 PATH 中，然後再執行 SYS 字。如果
these files are accessible, you will see the DEBUG prompt '-'. Now you
這些檔案是可存取的，您將看到 DEBUG 提示符「-」。現在你
can use the DEBUG commands to set up registers, disassemble code to see
可以使用 DEBUG 指令來設定暫存器，反彙編程式碼以查看
if the code was assembled correctly, and also step through the code one
如果代碼組合正確，並逐步執行代碼一
instruction at a time. Go find and dust off your DOS manual.
一次指導。去找你的 DOS 手冊並撣掉灰塵。


The only other thing you have to be careful about is that DEBUG
您唯一需要注意的另一件事是 DEBUG
initializes the segment registers, the stack pointers, and the CPU
初始化區段暫存器、堆疊指標和 CPU
registers in its own way, very different from the way F-PC sets them up.
以自己的方式註冊，與 F-PC 設置它們的方式非常不同。
You must initialize all the registers used by F-PC correctly. If GISSMO
您必須正確初始化 F-PC 使用的所有暫存器。如果 GISSMO
needs parameters from the data stack, you must push them on the data
需要資料堆疊中的參數，您必須將它們推送到資料上
stack before stepping through GIZZMO.
堆疊，然後再逐步通過 GIZZMO。


DEBUG does not provide the most friendly interface to its user. You
DEBUG 沒有為其用戶提供最友好的界面。你
have to be prepared to pay the price before dipping into assembly coding.
在投入彙編編碼之前，必須準備好付出代價。
Try to minimize the pain by staying in the friendly environment in F-PC
盡量通過留在 F-PC 的友好環境中來最大程度地減少痛苦
as long as possible, where the interpreter, the compiler, the editor, and
儘可能，其中解釋器、編譯器、編輯器、
the high level debugger are ready and eager to render their best
高階偵錯工具已準備好，並渴望呈現其最佳狀態
services.
服務。

