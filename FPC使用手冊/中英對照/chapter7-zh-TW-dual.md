CHAPTER 7. DOS INTERFACE
第 7 章。DOS 介面



Forth is a language with an operating system packed in. It provides a
Forth 是一種包含作業系統的語言。它提供了一個
complete programming environment so that a user can write, test and debug
完整的編程環境，以便用戶可以編寫、測試和調試
substantial programs completely inside of this environment. When Chuck
完全在這種環境中進行大量程序。當查克
Moore started developing Forth, the operating systems were primitive, and
摩爾開始開發 Forth，操作系統很原始，並且
often got in the way, preventing the user from exploiting the full
經常妨礙用戶充分利用
capability of the hardware underneath the operating system. His
作業系統底下硬體的功能。他的
solution, adopted by most earlier Forth implementations, was to eliminate
大多數早期的 Forth 實現所採用的解決方案是消除
the operating system completely and incorporate all essential functions
操作系統完整並包含所有基本功能
of the operating system into Forth. BLOCK was invented to access mass
操作系統進入 Forth。BLOCK 的發明是為了獲取質量
storage directly, and it allows Forth to use different magnetic storage
存儲，它允許 Forth 使用不同的磁存儲
media very efficiently and quite transparently to the user.
媒體對用戶非常高效且相當透明。


However, using blocks imposes many restrictions on the style of
然而，使用區塊對
programming in Forth. The most apparent restriction is on the editor,
在福斯進行編程。最明顯的限制是編輯者，
which handles text in fixed 1024 byte chunks. It also makes Forth
它處理固定 1024 位元組區塊中的文字。它還使 Forth
incompatible with other programming environments.
與其他程式設計環境不相容。


In the good old days of minicomputers and mainframes, compatibility was
在小型計算機和大型機的美好時光中，兼容性是
among the least of concerns because there were so many of them. None of
這是最不令人擔憂的，因為他們太多了。都不是
them were compatible in hardware or in software. In the confusion, Forth
它們在硬件或軟件上兼容。在混亂中，福斯
was able to offer an universal solution, and was ported easily to every
能夠提供通用的解決方案，並且可以輕鬆移植到每個
machine in sight. It is very sad that these bygone days are no more. In
機器就在眼前。這些過去的日子已經不復存在，這是非常可悲的。在
the field of microcomputers and personal computers, Big Blue and
微型電腦和個人電腦領域，藍色巨人和
Not-So-Big Red have established certain common practices, if not
Not-So-Big Red 已經建立了某些常見的做法，如果不是的話
standards. Whether we like them or not, DOS and MAC prevail as the
標準。無論我們喜歡與否，DOS 和 MAC 都佔上風，因為
environments we are condemned to live in for the next few years. After
我們注定要在未來幾年生活在這樣的環境中。後
that, we will all be sentenced for life under UNIX if we can ever escape
如果我們能逃脫，我們都會在 UNIX 下被判處終身監禁
from C.
從 C.


It is thus very important that Forth should take advantage of these
因此，福斯應該利用這些非常重要
less-than-optimized operating systems in areas where convenience and
在方便和
compatibility are useful and cost effective. Forth can be then further
相容性是有用且具有成本效益的。然後可以更進一步
refined to arrive at the optimized solutions which demand the best of
經過改進，以達到需要最佳效果的最佳解決方案
performance and code compacting. F-PC tries to exploit the DOS
效能和程式碼壓縮。F-PC 試圖利用 DOS
environment to its practical limit in adopting the sequential file
環境達到採用順序檔案的實際極限
structure for mass storage and providing a smooth and convenient path to
用於大規模存儲的結構，並提供順暢便捷的路徑
all the utility in DOS and OS2. All DOS and BIOS calls are readily
DOS 和 OS2 中的所有實用程序。所有 DOS 和 BIOS 調用都很容易
accessible from F-PC. You can even spawn a DOS shell within F-PC to use
可從 F-PC 訪問。您甚至可以在 F-PC 中生成一個 DOS shell 來使用
DOS utilities.
DOS 實用程式。


7.1. SYSTEM INTERRUPTS AND BIOS CALLS
7.1.系統中斷和 BIOS 呼叫


BIOS (Basic Input Output System) is a set of subroutines stored in the
BIOS（基本輸入輸出系統）是一組儲存在
Read-Only Memory (ROM) in the PC. These subroutines provide the most
PC 中的唯讀記憶體 （ROM）。這些子常式提供最多的
elementary services for the operating system to access the resources in
基本服務，供作業系統存取
PC, such as the keyboard, the display, the disk drives, and the printer.
PC，例如鍵盤、顯示器、磁碟機和印表機。


To invoke any of these service subroutines, a software interrupt
若要呼叫任何這些服務子常式，軟體岔斷
instruction INT must be executed at the machine level. This interrupt
指令 INT 必須在機器層級執行。此中斷
instruction transfers the control to the proper service routine via an
指令會透過
interrupt vector table in the memory area 0:0 to 0:3FFH. Parameters are
內存區域 0：0 至 0：3FFH 中的中斷向量表。參數為
sent to the service routine in one or more registers in the CPU.
傳送至 CPU 中一或多個暫存器中的服務常式。
Results, if any, are returned in the registers or as flags. For
結果 （如果有的話） 會在暫存器中傳回，或作為旗標傳回。為
available BIOS services and their functional specifications, one must
可用的 BIOS 服務及其功能規格，必須
consult the IBM Hardware Reference Manual for the specific model or any
請參閱 IBM 硬體參考手冊 以取得特定型號或任何
reasonably good book on MS-DOS. See some references in the Preface to
關於 MS-DOS 的相當不錯的書。請參閱前言中的一些參考文獻
this Manual.
本手冊。


F-PC itself does not provide high level tools to do software interrupts.
F-PC 本身不提供高級工具來進行軟件中斷。
However, it does use BIOS service to handle keyboard input, screen and
但是，它確實使用 BIOS 服務來處理鍵盤輸入、螢幕和
printer output. Since most of these words were coded in assembly, they
印表機輸出。由於這些單字大部分都是在組合中編碼的，因此它們
invoke INT instructions directly. For example, to receive a character
直接呼叫 INT 指令。例如，接收一個角色
from the keyboard through BIOS:
從鍵盤到 BIOS：


CODE BIOSKEY ( -- char )
代碼 BIOSKEY （ -- char ）
BEGIN
開始
MOV AH, # 0
莫夫 AH，#0
INT 16
智力 16
CMP AX, # 0
CMP AX，#0
0<> UNTIL
0<> 直到
MOV BIOSKEYVAL AX
1PUSH
1 推
END-CODE
結束代碼


Other important software interrupts are:
其他重要的軟體中斷包括：


INT 5 printer
INT 5 印表機
INT 6 video display
INT 6 視頻顯示
INT 19 diskette drive
INT 19 磁片驅動器
INT 33 DOS services
INT 33 DOS 服務


If you intend to use any of the software interrupts, you can find lots of
如果您打算使用任何軟件中斷，您可以找到很多
good examples in the source files of F-PC. Use them as models and modify
F-PC 源文件中的好例子。將它們用作模型並修改
them to suit your own need.
它們以滿足您自己的需求。


7.2. DOS SERVICE CALLS
7.2. DOS 服務呼叫


INT 33 invokes the DOS services which cover a wide range of very
INT 33 調用 DOS 服務，涵蓋廣泛的非常
interesting functions which are not in the BIOS ROM, but loaded into the
有趣的功能不在 BIOS ROM 中，而是載入到
RAM memory when DOS is booted. F-PC uses the DOS services extensively
DOS 啟動時的 RAM 記憶體。F-PC 廣泛使用 DOS 服務
and a set of words is defined to facilitate their uses.
並定義了一組單詞以方便它們的使用。


BDOS ( data function -- n )
BDOS（數據函數 -- n）


This service emulates the CP/M BDOS call protocol, which requires a
此服務模擬 CP/M BDOS 呼叫通訊協定，這需要
function number and some data. The number returned on the stack is zero
函數編號和一些數據。堆疊上傳回的數字為零
always, so that it is compatible with the BDOS function implemented in
總是，使其與
F83.


When a service call requires more input and/or output parameters, F-PC
當服務呼叫需要更多輸入和/或輸出參數時，F-PC
gives you the following choices:
為您提供以下選擇：


BDOS2 ( CX DX AX -- CX DX AX )
BDOS2 （ CX DX AX -- CX DX AX ）


Pop the top three items on the data stack and then do an INT 33. The
彈出數據堆棧上的前三個項目，然後執行 INT 33。這
contents of CX, DX, and AX, at the completion of the DOS service is
CX、DX 和 AX 的內容，在 DOS 服務完成後是
returned on the stack. Most status information is returned in these
在堆疊上傳回。大部分狀態資訊都會在這些
registers by DOS. You have to consult a DOS manual for detailed
DOS 的登記冊。您必須查閱 DOS 手冊以了解詳細信息
specifications on registers.
寄存器上的規範。


OS2 ( CX DX AX -- CX DX AX )
作業系統 2 （ CX DX AX -- CX DX AX ）


OS2 is identical to BDOS2. Its sole purpose is to please people in the
OS2 與 BDOS2 相同。它的唯一目的是取悅人們
three piece suits. The last item from AX register is masked to an 8 bit
三件套西裝。AX 暫存器中的最後一個項目被遮罩為 8 位
number.
數。


XFDOS ( DX CX BX AX ES DS -- CX BX AX Carry )
XFDOS （ DX CX BX AX ES DS -- CX BX AX 進位 ）


XFDOS is needed to allow DOS services to access memory above the 64K byte
需要 XFDOS 才能允許 DOS 服務存取 64K 位元組以上的記憶體
Code/Data Segment.
程式碼/資料區段。


DOS 33 Interrupt Services provides more than 30 different types of
DOS 33 中斷服務提供 30 多種不同類型的
services. It is not possible to cover them here even to a very small
服務。即使是非常小的，也不可能在這裡涵蓋它們
extent. If you are interested, please consult the MS-DOS systems manual
程度。如果您有興趣，請查閱 MS-DOS 系統手冊
or books. In F-PC, the file handles, time/date, directory path, some
或書籍。在 F-PC 中，檔案句柄、時間/日期、目錄路徑、一些
keyboard and screen functions are all done through this interrupt
鍵盤和螢幕功能都是透過這個中斷完成的
service.
服務。


7.3. THE DOS SHELL
7.3. DOS 外殼


The interface from F-PC to DOS occurs at several levels. In this section
從 F-PC 到 DOS 的介面發生在多個層次上。本節內容
we will discuss the interface to the DOS commands as opposed to the DOS
我們將討論 DOS 命令的介面，而不是 DOS
system calls. DOS is a language, with its own syntax rules and
系統呼叫。DOS 是一種語言，有自己的語法規則和
functions. By providing a bridge to DOS, F-PC encompasses two powerful
事。透過提供通往 DOS 的橋樑，F-PC 包含兩個強大的
languages at a very small cost.
以非常低的成本學習語言。


It is convenient to be able to issue DOS commands from within F-PC. This
能夠從 F-PC 內發出 DOS 命令很方便。這
avoids having to leave F-PC to do the normal housekeeping works that are
避免了不得不離開 F-PC 來做正常的內務工作，這些工作是
regular occurrences in a DOS based computer. In line with this, F-PC
在基於 DOS 的計算機中經常發生。與此一致，F-PC
implements several commands:
實作數個指令：


$SYS ( counted-string -- f1 )
$SYS （ 計數字串 -- f1 ）


Pass the counted string to COMMAND.COM as a command line. A shell is
將計數的字串作為命令列傳遞給 COMMAND.COM。殼是
spawned in the process with the "/c" parameter included so that
在包含“/c”參數的過程中生成，以便
COMMAND.COM terminates on completion of the command line. If a NULL
COMMAND.COM 會在指令行完成時終止。如果 NULL
string is passed then the DOS shell will be spawned for you to enter one
string 的 String ，則會產生 DOS shell 供您輸入一個
or several command lines. You can then return to Forth by typing EXIT
或數個命令列。然後，您可以鍵入 EXIT 返回 Forth
<return>.
<return>。


SYS <commands> ( -- )
系統 <commands> （ -- ）


Accept a command line following SYS and executes the commands as a DOS
接受 SYS 後面的命令列，並以 DOS 身分執行命令
command line.
命令列。


` <commands> ( -- )
' <commands> （ -- ）


Pronounced 'back tick'. A pseudonym for SYS.
發音為“反勾”。SYS 的化名。


These words allow performing almost any DOS command line operation you
這些詞允許執行幾乎任何 DOS 命令行操作
would want to do. To make things even more convenient, several FORTH
會想做的。為了讓事情更加方便，幾個 FORTH
words have been defined which use the $SYS for specific DOS functions.
已定義使用特定 DOS 函數$SYS 的單字。
They are as follows:
它們如下：


DIR DEL CHDIR CD COPY REN RENAME


A: B: C: D:
A：B：C：D：


These commands may be used exactly as they are used in DOS. If you press
這些命令的使用方式可以與 DOS 中使用的完全相同。如果您按
Control-C, or Control-Break during the execution of any of the above
Control-C 或 Control-Break 在執行上述任何操作期間
words, the operation will abort and control will be returned back to
words，則作業會中止，控制權會傳回給
Forth.
第四。


SYS or ` can be given without a DOS command. In this case you return the
SYS 或 ' 可以在沒有 DOS 命令的情況下給出。在此情況下，您會傳回
COMMAND.COM shell and you will see the familiar C> or equivalent DOS
COMMAND.COM shell，你會看到熟悉的 C> 或等效的 DOS
prompt. You can execute any DOS commands or other COM and EXE files.
速。您可以執行任何 DOS 命令或其他 COM 和 EXE 檔案。
After you are through with DOS, EXIT will return you back to F-PC. You
完成 DOS 後，EXIT 會將您返回 F-PC。你
can switch very conveniently back and forth among Forth, DOS and any
可以在 Forth、DOS 和任何
other application.
其他應用。


7.4. BATCH COMMANDS
7.4. 批次命令


F-PC allows commands to be passed to Forth on the DOS command line in the
F-PC 允許將命令傳遞到 DOS 命令列上的 Forth
following manner:
以下方式：


C> F-PC <filename> <forth words> <return>
C> F-PC <filename> <第四個詞> <return>


This illustrates how you can start F-PC with a specified file name, and
這說明了如何使用指定的檔案名稱啟動 F-PC，並且
perform commands on the file. An example of how this might be used is as
對檔案執行命令。如何使用此專案的範例如下
follows:
如下：


C> F-PC BANNER LOAD <return>
C> F-PC 橫幅載入<return>


Here we are starting F-PC with the file BANNER.SEQ, and then performing
在這裡，我們使用檔案 BANNER 啟動 F-PC。SEQ，然後執行
LOAD to compile the file. Another way to use command line parameters is:
LOAD 來編譯檔案。使用命令列參數的另一種方法是：


C> F-PC - <forth words> <return>
C> F-PC - <第四個詞> <return>


Here we are starting F-PC, followed by a dash "-" to tell F-PC we are not
在這裡，我們開始 F-PC，然後加上破折號“-”，告訴 F-PC 我們不是
opening a file, then telling F-PC to perform the Forth words following
打開一個文件，然後告訴 F-PC 執行以下的第四個單詞
the "-". Here is an example:
“-”。這是一個例子：


C> F-PC - REPAIR DIR <return>
C> F-PC - 維修目錄<return>


This example starts up F-PC without a file and tells F-PC we want to
此範例啟動沒有檔案的 F-PC，並告訴 F-PC 我們想要
repair the word DIR. It will locate the word DIR and start up the editor
修復 DIR 一詞。它將找到單詞 DIR 並啟動編輯器
with the cursor located on the first line of the DIR definition.
游標位於 DIR 定義的第一行。


We can build batch files this way. As you can see, many types of
我們可以透過這種方式建立批次檔案。如您所見，許多類型的
commands could be given to F- PC on the command line. Here are the
命令可以在命令列上下達給 F-PC。以下是
contents of the FMETA.BAT:
FMETA.BAT 內容：


F-PC - FLOAD META86
F-PC - FLOAD 元 86


This single line batch file meta-compiles the F-PC kernel file and
這個單行批次檔案元編譯了 F-PC 核心檔案，並且
creates the KERNEL.COM file. A similar batch file EXTEND.BAT is provided
建立 KERNEL.COM 檔案。提供類似的批次檔案 EXTEND.BAT
to extend the the kernel into a full featured F-PC system. There are a
將核心擴展到功能齊全的 F-PC 系統。有一個
number of batch files in the F-PC system and they are good examples of
F-PC 系統中的批次檔案數量，它們是很好的範例
how to call F-PC to perform various tasks in the DOS environment and then
如何在 DOS 環境下呼叫 F-PC 執行各種任務，然後
return automatically to DOS. It is a valuable tool for building
自動返回 DOS。它是構建的寶貴工具
customized applications.
客製化應用程式。


The only caution on batch files is that you must not place commands on
批次檔的唯一注意事項是，您不得將命令放在
the command line which cause the command line to be interpreted again.
導致命令行再次解譯的命令列。
The words HELLO and COLD are such words. They should not be used since
HELLO 和 COLD 這兩個詞就是這樣的詞。它們不應該被使用，因為
infinite recursion will crash the system.
無限遞歸會使系統崩潰。


7.5. DOS MEMORY MAP OF F-PC
7.5. F-PC 的 DOS 記憶體映射


F-PC was built to handle a class of programming problems that requires
F-PC 旨在處理一類需要的程式設計問題
very large memory and cannot be handled well on any normal 64K
內存非常大，在任何正常的 64K 上都無法很好地處理
implementation of Forth because of space constraints. Careful analysis
由於空間限制，Forth 的實施。仔細分析
showed that in a large Forth system most memory space is consumed by
表明在大型 Forth 系統中，大部分記憶體空間被
colon definitions. This is quite natural because Forth is a virtual
冒號定義。這是很自然的，因為 Forth 是一個虛擬的
machine. The virtual machine is built upon a small kernel which has to
機。虛擬機建置在一個小型內核之上，該內核必須
be implemented in code definitions. However, once the basic mechanism is
在程式碼定義中實作。然而，一旦基本機制是
in place, utilities and applications are constructed in high level using
就位時，公用程式和應用程式是使用
colon definitions. Therefore, F-PC struggled to give the user as much
冒號定義。因此，F-PC 努力為用戶提供盡可能多的東西
space as he will need to store colon definitions, while reserving only
空間，因為他需要儲存冒號定義，同時僅保留
64K bytes for code, constants, variables, and arrays, and 64K bytes for
64K 位元組用於程式碼、常數、變數和陣列，以及 64K 位元組
heads which may or may not be needed in an application. F-PC also
應用程序中可能需要也可能不需要的頭部。F-PC 也
includes words with which you can ask the operating system for more
包括您可以向操作系統詢問更多信息的單詞
memory when needed and release it back to DOS when you have finished
內存並在完成後將其釋放回 DOS
using it.
使用它。


F-PC allows the List (colon space) Segment to be much larger than 64K
F-PC 允許列表（冒號空間）段遠大於 64K
bytes. In fact the only real limitation in system size comes from the
位元組。事實上，系統大小唯一真正的限制來自於
fact that there are only 64k available for heads. Calculations indicate
事實上，只有 64k 可用於頭部。計算表明
there is room for about 2300 definitions on top of the current system of
在當前系統之上還有大約 2300 個定義的空間
about 3000 words. This calculation is based on an average name length of
大約3000字。此計算是根據
5 characters, with an average head length of 12 bytes. With 5300 total
5個字元，平均頭長為12個位元組。總數為 5300
definitions, less than 30k of code segment would be used for code fields
定義，少於 30k 的程式碼區段將用於程式碼欄位
of colon definitions, leaving the remaining 30+K of Code Segment for
冒號定義，留下剩餘的 30+K 代碼段
variables and arrays. Not enough for an infinitely large application
變數和陣列。對於無限大的應用程序來說是不夠的
obviously, but probably large enough for most applications.
顯然，但對於大多數應用程序來說可能足夠大。


F-PC places a segment (ES) and and offset (IP) on the return stack for
F-PC 在返回堆棧上放置一個段 （ES） 和偏移量 （IP），以用於
each nest operation. Only the relative segment offset is compiled into
每個巢狀作業。只有相對區段偏移量被編譯為
the code field, and the conversion to absolute segment is performed by
程式碼欄位，而轉換為絕對區段是由
NEST. This makes the code fully relocatable as is required by the DOS
巢。這使得程式碼可以完全按照 DOS 的要求重新定位
environment. Some performance could be gained by using absolute segment
環境。使用絕對區段可以獲得一些性能
addressing, and performing a conversion at save and load time to and from
定址，並在儲存和載入時執行轉換
relative and absolute. The performance gain would come from having a
相對的和絕對的。效能提升將來自於擁有
simpler NEST, which would not have to perform the relative to absolute
更簡單的 NEST，它不必執行相對於絕對的
conversion at run-time.
執行階段的轉換。


CS, SS, and DS always point to the Code Segment, so that all assembly
CS、SS 和 DS 一律指向程式碼區段，讓所有元件
language operations work with data in the Code Segment unless a special
語言作業會使用程式碼區段中的資料，除非特殊
operator like @L or !L is used to reach an external memory area. This
運算子，例如 @L 或 ！L 用於到達外部記憶體區域。這
means there is no penalty to be paid for most Forth operations and very
意味著大多數 Forth 操作無需支付罰款，並且非常
high compatibility to F83 is maintained.
保持與 F83 的高相容性。


The header of every word contains a view field for locating the source
每個單詞的標題都包含一個用於查找源的視圖字段
code, a link field to maintain the vocabulary thread, a name field, and a
code、用於維護詞彙執行緒的連結欄位、名稱欄位和
code pointer field. The code pointer field contains a code field address
程式碼指標欄位。程式碼指標欄位包含程式碼欄位位址
which points to the executable code of this word in the Code Segment.
它指向代碼段中該單詞的可執行代碼。
The machine code in the Code Segment is executed when this word is
當此字組為
invoked. For a colon definition, the code starts with a JMP NEST, which
被調用。對於冒號定義，程式碼以 JMP NEST 開頭，該
saves the current ES and IP registers, adds the next two bytes to XSEG
保存當前的 ES 和 IP 暫存器，將接下來的兩個位元組添加到 XSEG
and moves them into ES and clears IP to zero. When the NEST routine is
並將它們移至 ES 並清除 IP 為零。當 NEST 常式為
executed to completion, NEXT obtains the next instruction in the List
執行至完成時，NEXT 會取得清單中的下一個指令
Segment pointed to by ES register and starts processing the address list
ES 暫存器指向的區段，並開始處理位址清單
in this colon definition.
在這個冒號定義中。


In a code definition, the code pointer field in the header points to its
在程式碼定義中，標頭中的程式碼指標欄位會指向其
machine code in the Code Segment. For other types of words, like
機器碼。對於其他類型的單字，例如
CONSTANTs, VARIABLEs, and other executable structures, the first
CONSTANT、VARIABLE 和其他可執行結構，第一個
instruction in the code field is always a CALL to the appropriate inner
code 欄位中的指令一律是對適當內部的 CALL
interpreter which carries out the task assigned to the specific type of
解釋器，執行分配給特定類型的任務
word.
字。


This manual is not the proper place to discuss the inner mechanism of
本手冊不是討論內部機制的適當場所
F-PC. If the above discussion seems to be too abstract, please don't
F-PC。如果上述討論看起來過於抽象，請不要
worry. F-PC behaves just like any other Forth system. You can be very
擔心。F-PC 的行為與任何其他 Forth 系統一樣。你可以非常
productive without any knowledge about how or why the Forth virtual
高效，無需了解 Forth 虛擬如何或為何
machine works. However, it is very comforting to know where things are
機器工作。然而，知道東西在哪裡是非常令人欣慰的
stored, just in case you need to find them.
存儲，以防萬一您需要找到它們。



The memory segments in F-PC
F-PC 中的記憶體區段


























Data structures in a colon definition
冒號定義中的資料結構























7.6. LONG MEMORY WORD SET
7.6. 長記憶體字集


A complete set of words is defined in F-PC to let the user accessing the
在 F-PC 中定義了一組完整的單字，讓使用者存取
DOS memory very conveniently. The standard Forth memory accessing words
DOS 內存非常方便。標準的 Forth 記憶體存取字
are retained for addressing the Code/Data Segment in the memory. Generic
保留用於尋址記憶體中的程式碼/資料段。一般的
extended memory words are appended (or prepended) with the letter L, and
擴展記憶單字附加（或前置）字母 L，並且
they require address specifications in segment:offset pairs. Words
它們需要 Segment：Offset 對中的位址規格。言
addressing the List Segment have X prefix and words addressing the Head
尋址列表段有 X 前綴和單詞，稱呼 Head
Segment have Y prefix.
區段具有 Y 前綴。


Generic Long Memory Words are those which require an explicit segment
通用長記憶詞是那些需要明確段的詞
address with a 16 bit address offset. They are the basic word set from
位址具有 16 位元位址偏移。它們是來自
which other segment specific memory words are derived. This word set
衍生出哪些其他區段特定記憶詞。這個詞集
includes the following words:
包括以下詞語：


@L ( seg addr -- n ) Fetch 16 bit integer.
@L （ seg addr -- n ） 取得 16 位元整數。
!L ( n seg addr -- ) Store 16 bit integer.
!L （ n seg addr -- ） 儲存 16 位元整數。
C@L ( seg addr -- b ) Fetch a byte.
C@L （ seg addr -- b ） 取得一個位元組。
C!L ( b seg addr -- ) Store a byte.
C！L （ b seg addr -- ） 儲存一個位元組。
CMOVEL ( seg addr seg' addr' n -- ) Move n bytes from seg:addr to seg':addr'.
CMOVEL （ seg addr seg' addr' n -- ） 將 n 個位元組從 seg：addr 移至 seg'：addr'。
CMOVEL> ( seg addr seg' addr' n -- ) Move n bytes in reversed order.
CMOVEL> （ seg addr seg' addr' n -- ） 以相反的順序移動 n 個位元組。
LFILL ( seg addr n b -- ) Fill n bytes from seg:addr with b.
LFILL （ seg addr n b -- ） 用 b 填入 seg：addr 中的 n 個位元組。
LDUMP ( seg addr n -- ) Dump n bytes from seg:addr.
LDUMP （ seg addr n -- ） 從 seg：addr 傾出 n 個位元組。
Seg is stored into DUMPSEG.
Seg 儲存在 DUMPSEG 中。


Following are words addressing the List Segment:
以下是針對列表區段的詞語：


X, ( n -- ) Compile integer to top of the list dictionary.
X， （ n -- ） 將整數編譯到列表字典的頂部。
XC, ( b -- ) Compile byte to the list dictionary.
XC， （ b -- ） 將位元組編譯到清單字典中。
XDUMP ( rel-seg n -- ) Dump n bytes in the list segment starting at XSEG.
XDUMP （ rel-seg n -- ） 從 XSEG 開始傾出清單區段中的 n 個位元組。
XDP ( -- addr ) Offset to top of list dictionary.
XDP （ -- addr ） 位移至清單字典頂端。
XDPSEG ( -- seg ) Segment to top of list dictionary.
XDPSEG （ -- seg ） 區段至清單字典頂端。
XHERE ( -- seg addr ) Seg:addr to top of list dictionary.
XHERE （ -- seg addr ） Seg：addr 到列表字典的頂部。
XSEG ( -- seg ) Segment base of List Space.
XSEG （ -- seg ） 清單空間的區段基數。


The corresponding words addressing into the Head Segment are:
進入 Head Segment 的相應詞語是：


Y@ ( addr -- n ) Fetch integer from head segment.
Y@ （ addr -- n ） 從頭段擷取整數。
Y! ( n addr -- ) Store integer to head segment.
Y!（ n 地址 -- ）將整數儲存到頭段。
YC@ ( addr -- b ) Fetch byte.
YC@ （ addr -- b ） 取得位元組。
YC! ( b addr -- ) Store byte.
YC！（ b 地址 -- ）存放區位元組。
Y, ( n -- ) Compile integer to head dictionary.
Y， （ n -- ） 將整數編譯到頭字典。
YCSET ( b addr -- ) Set bits in a byte.
YCSET （ b addr -- ） 在位元組中設定位元。
YDUMP ( addr n -- ) Dump n bytes from addr in the head segment.
YDUMP （ addr n -- ） 從 head 區段中的 addr 傾出 n 個位元組。
YDP ( -- addr ) Pointer to top of head dictionary.
YDP （ -- addr ） 指向頭頂字典的指標。
YHERE ( -- addr ) Address of top of head dictionary.
YHERE （ -- addr ） 頭頂字典的地址。
YSEG ( -- seg ) Segment base of Head Space.
YSEG （ -- seg ） 頂空的段基數。


7.7. DOS MEMORY ALLOCATION
7.7. DOS 記憶體配置


The following words allow you to request, adjust and discard memory
以下單字允許您請求、調整和丟棄記憶體
blocks from DOS for your program to use.
DOS 中的區塊供您的程式使用。


ALLOC ( size -- seg2 seg flag )
ALLOC （ 大小 -- seg2 seg 旗標 ）


Request size segments of free memory from DOS. Flag=0 if ok, 8 if not
向 DOS 請求可用記憶體的大小段。如果正常，則旗幟=0，如果不正常，則為 8
enough memory. Seg is the segment base of the allocated memory. seg2 is
足夠的記憶體。Seg 是已配置記憶體的區段基數。seg2 是
maximum number of segments available that will not cause an error 8,
不會導致錯誤的可用區段數目上限 8，
insufficient memory.
記憶體不足。


DEALLOC ( seg -- flag )
DEALLOC （ seg -- 旗標 ）


Release a block of memory to DOS. Seg must be the same as the segment
釋放一個記憶體區塊到 DOS。Seg 必須與區段相同
base returned by ALLOC as the base of the allocated memory. Flag=0 if
base 作為配置記憶體的基礎 ALLOC 傳回。Flag=0 如果
ok, 9 if seg is not valid.
好的，如果 seg 無效，則為 9。


SETBLOCK ( seg size --- flag )
SETBLOCK （ seg 大小 --- 旗標 ）


Re-adjust the memory block specified by seg to a new size in segments.
將 seg 指定的記憶體區塊重新調整為以段為單位的新大小。
SEG is the absolute segment address that was returned by ALLOC. 'Size' is
SEG 是 ALLOC 傳回的絕對區段位址。“尺寸”是
the size of the array in 16 byte units. Typically you would take the BYTE
陣列的大小（以 16 個位元組單位為單位）。通常，您會採用 BYTE
size needed and use the word SEGMENTS to convert that to the number of
size 需要，並使用單詞 SEGMENTS 將其轉換為
segments needed.
需要的段。


These words are useful if you need an extra large space to store large
如果您需要超大的空間來存放大件物品，這些詞很有用
arrays of data. F-PC in its default configuration uses about 400K bytes
數據陣列。預設配置中的 F-PC 使用大約 400K 位元組
of memory. The DOS still has about 200K bytes held in reserve, if you
記憶。DOS 仍有大約 200K 位元組保留，如果您
have not loaded any TSR software programs. This free memory can be
尚未載入任何 TSR 軟體程式。這個空閒記憶體可以是
allocated for your use. With the extended memory words, you can address
分配給您使用。使用擴展記憶字，您可以將
any memory whether DOS allows it or not. However, if you are building a
任何內存，無論 DOS 是否允許。不過，如果您正在建置
system which will coexist with other software, it is prudent to be polite
系統，將與其他軟件共存，謹慎行事
to Ms. DOS and observe her protocol when it is also convenient to do so.
向 DOS 女士致函，並在方便的時候遵守她的協議。
You make her happy. She will make you happy.
你讓她開心。她會讓你快樂的。

