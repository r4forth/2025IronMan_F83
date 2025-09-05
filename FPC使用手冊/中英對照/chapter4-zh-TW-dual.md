# CHAPTER 4. PROGRAMMING TOOLS 第 4 章。程式設計工具

In this chapter we will discussed the most useful utility words which are
在本章中，我們將討論最有用的實用詞，它們是
either unique in F-PC or have different behavior than those in F83. We
在 F-PC 中獨一無二，或與 F83 中的行為不同。我們
assume that the user is familiar with F83 so that those words adopted
假設使用者熟悉 F83，以便採用這些詞語
unmodified from F83 are not presented. Reference material such as Inside
未從 F83 修改。參考資料，例如內部
F83 and F83 Reference Manual by C. H. Ting are useful in obtaining an
C. H. Ting 的 F83 和 F83 參考手冊有助於獲得
overview on F83. Dr. Ting's companion F-PC Technical Reference Manual is
F83 概述。丁博士的配套 F-PC 技術參考手冊是
is devoted to the internal structure of F- PC.
致力於 F-PC 的內部結構。

## 4.1. DUMP 4.1. 轉儲

The dump utility gives you a formatted hex dump with the ASCII text
傾印公用程式會提供具有 ASCII 文字的格式化十六進位傾出
corresponding to the bytes on the right hand side of the screen. Data
對應於螢幕右側的位元組。資料
and addresses are displayed in hex, with 16 bytes to a line. Both the
位址以十六進位表示，每行有 16 個位元組。兩者的
segment and offset addresses are displayed for easy reference.
會顯示線段和偏移位址，以便於參考。

DUMP displays memory in the Code Segment, where code, strings, and other
DUMP 會在程式碼區段中顯示記憶體，其中程式碼、字串和其他
data are stored. XDUMP displays memory in the List Segment, where colon
資料會儲存。XDUMP 會在「清單區段」中顯示記憶體，其中冒號
definitions are stored. YDUMP displays memory in the Head Segment.
定義會儲存。YDUMP 會在「磁頭區段」中顯示記憶體。
These dump utilities are derived from the generic dump function LDUMP,
這些傾出公用程式衍生自一般傾出函數 LDUMP，
which displays a range of memory from a memory segment whose segment
它顯示來自記憶體區段的記憶體範圍，其區段
address is given on the stack with an offset address and byte count.
地址在堆棧上給出，具有偏移地址和位元組計數。
DUMP, XDUMP, and YDUMP set DUMPSEG to the corresponding segment and then
DUMP、XDUMP 及 YDUMP 將 DUMPSEG 設為對應的區段，然後
do LDUMP.
執行 LDUMP。

DUMP, XDUMP and YDUMP change DUMPSEG to cs:, es:, and ys:, respectively.
DUMP、XDUMP 及 YDUMP 會分別將 DUMPSEG 變更為 cs：、es： 及 ys：。
Their behavior takes a little bit of getting use to, but they allow you
他們的行為需要一點時間來適應，但他們允許你
to navigate through the entire segmented memory space. XDUMP is unique
以瀏覽整個分段記憶體空間。XDUMP 是唯一的
in that it takes a segment pointer and a count as parameters. It is made
因為它採用區段指標和計數作為參數。它是製成的
so that you will able to dump colon definitions beyond the 64K boundary.
這樣您就可以將冒號定義轉儲到 64K 邊界之外。

```
DUMP ( address length -- ) Dump Code segment
LDUMP ( segment offset length -- ) Dump any segment
XDUMP ( relative-segment length -- ) Dump List segment
YDUMP ( offset length -- ) Dump Head segment
```

DU displays 64 bytes in the dump segment and increments the memory
DU 在傾印區段中顯示 64 個位元組，並遞增記憶體
address by 64 so that you can continue dumping the next 64 bytes with
位址為 64，以便您可以繼續轉儲接下來的 64 個位元組，並使用
another DU.
另一個 DU。


## 4.2. THE DEBUGGER 4.2. 偵錯器

The F-PC debugger is very similar to the F83 debugger. Some features
F-PC 偵錯器與 F83 偵錯器非常相似。一些功能
have been added to enhance its operation. The decompiled source for the
已添加以增強其操作。的反編譯原始碼
current definition being debugged is displayed while debugging. A
偵錯時會顯示目前正在偵錯的定義。一個
typical command sequence might be as follows:
一般指令順序可能如下：

```
DEBUG WORDS <return>
```

which sets up the debugger so that WORDS will be debugged as soon as it
它設置了調試器，以便 WORDS 將在它
is executed. DEBUG only sets the debugger up to debug a word. The
被執行。DEBUG 只會將偵錯工具設定為偵錯單字。這
debugging process does not start until the word is executed. A new
偵錯程序在執行字之前不會開始。一個新的
debugging command DBG is added, which caused the following word to be
debugg 指令 DBG 的新增，導致以下單字為
executed and debugged immediately. The command sequence is:
立即執行和調試。命令順序為：

```
DBG <word_name> <return>
```

It is much easier to use and makes much of the intricate behavior of the
它更容易使用，並且具有許多複雜的行為
F83 DEBUG transparent to the user.
F83 DEBUG 對使用者透明。

Once in the debugger, you will be shown a special debugger display. The
進入偵錯工具之後，您會看到特殊的偵錯工具顯示。這
decompiled source code is shown in the top half of the screen. The
反編譯的原始程式碼會顯示在畫面的上半部。這
debugging information is shown in the bottom window. At this point,
偵錯資訊會顯示在底部視窗中。在這一點上，
pressing return will cause the word highlighted to be executed, and the
按 Return 會導致突出顯示的單詞被執行，並且
debugger will print the stack after execution, and step to the next word
debugger 會在執行後列印堆疊，並逐步執行到下一個字
in the list and wait for a command.
並等待命令。

Notice the fields in the bottom debugging window. The number on the left
請注意底部偵錯視窗中的欄位。左邊的數字
is the address in memory where the debugger is currently working. The
是偵錯工具目前運作的記憶體位址。這
next field is the word the debugger is about to execute. The next symbol
Next 欄位是偵錯工具即將執行的單字。下一個符號
"?>" is a marker pointing to what will be the printed stack contents
“？>” 是一個標記，指向打印的堆棧內容
after we press <return>. The bar of text shown in the middle of screen
在我們按下 <return> 之後。顯示在畫面中間的文字列
is the command menu:
是命令功能表：

```
C-cont, D-done, F-forth, N-nest, Q-quit, S-skipto, U-unnest, X-source-on/off
```

These are the commands you can use in the debugger. Their detailed
這些是您可以在偵錯工具中使用的命令。他們的詳細
functions are as follows:
功能如下：


C-cont Trace continuously until a key is pressed.
C-cont 連續追蹤，直到按下按鍵為止。
D-done Stop debugging and enter the browser. Press F10
D-done 停止調試，進入瀏覽器。按 F10
to return.
返回。
F-forth Allow entry of Forth command lines until <return>
F-forth 允許輸入 Forth 命令列，直到<return>
is pressed on an empty line.
被壓在一條空線上。
N-nest Nest into the ":" definition we were about to
N-nest Nest 放入我們即將要的 “：” 定義中
execute. Only works on ":" definitions, and
誅。僅適用於 “：” 定義，並且
deferred words.
延期詞。
Q-quit Quit the debugger, and unpatch next.
Q-退出 退出偵錯工具，然後取消修補。
S-skipto Using + or - to skip to the desired word. Press
S-skip 至 使用 + 或 - 跳至所需的單字。壓
<return> to continue debugging from there.
<return> 從那裡繼續偵錯。
U-Unnest Unnest the current definition to the next higher
U-Unnest 將當前定義解嵌到下一個更高的定義
level.
平。
X-source-on/off Toggle on and off the source code display and
X-source-on/off 打開和關閉源代碼顯示和
devote the whole screen for debugging.
將整個螢幕用於調試。

You will have noticed that the upper portion of the screen is filled with
您會注意到螢幕的上部充滿了
the source code of the word you are currently debugging. This is to make
您目前正在偵錯的字的原始碼。這是要讓
it easier to follow the debug process. You may want to turn off the
遵循偵錯程序更容易。您可能想要關閉
source display, if it interferes the debugging process, by using the X
來源顯示，如果它干擾偵錯程式，請使用 X
command while debugging or used SRCOFF before debugging:
調試時或在調試前使用 SRCOFF 時命令：

SRCOFF Turn off the source display
SRCOFF 關閉來源顯示
SRCON Turn on the source display
SRCON 開啟來源顯示器

The default state is SRCON.
預設狀態為 SRCON。

During debugging, only the topmost 4 numbers on the data stack are
在調試過程中，只有資料堆疊上最頂層的4個數字是
displayed, with the total depth of stack shown in square brackets. This
顯示，並以方括號顯示堆疊總深度。這
is designed so that all debugging text fits in one line. As .S is used
的設計目的是讓所有偵錯文字都適合一行。如。使用 S
to display the stack contents, its behavior is modified from the .S in
若要顯示堆疊內容，其行為會從 .S 在
F83, which displays all items on the data stack. Sometimes it is
F83，顯示資料堆疊上的所有項目。有時是
inconvenient to have the bottom of the stack hidden from you, you can
不方便隱藏堆疊底部，您可以
change the contents of variable MAX.S to the desired number of stack
變更變數 MAX 的內容。S 到所需的堆疊數
items to be shown. MAX.S has a default value of 4.
要顯示的項目。最大。S 的預設值為 4。


## 4.3. VALUES: CONSTANTS AS VARIABLES 4.3. 值：常數作為變數

"Constants aren't; variables won't".
「常數不是;變數不會」。

A set of operators has been included for manipulating data values stored
已包含一組運算子，用於操作儲存的資料值
in the parameter fields in constants and variables. Constants are faster
在常數和變數的參數欄位中。常數更快
at run time than variables. You can improve performance in critical
在執行階段比變數。您可以改善關鍵
operations taking advantage of them. Since variables are more often
利用它們的操作。由於變數更頻繁
fetched than stored, using a constant to store a variable provides a
fetched 比 stored，使用常數來儲存變數會提供
somewhat more readable source by eliminating lots of @'s. In order to
通過消除大量 @ 來增加可讀性。為了
preserve the appearance of constants with their values not modifiable,
保留常數的外觀，其值不可修改，
F-PC defines a new type of data called VALUE. VALUE is an alias of
F-PC 定義了一種稱為 VALUE 的新資料類型。VALUE 是
CONSTANT, with the stated intention that their values are to be changed
CONSTANT，並聲明其值將被更改
at run-time.
在執行階段。

Here is a list of words which manipulate the contents of a value from the
以下是操作值內容的單字清單，這些單字會從
keyboard or in colon words:
鍵盤或冒號詞：

```
=: <name> ( n -- ) Store integer to value. It looks nice.
=： <name> （ n -- ） 將整數儲存為值。看起來不錯。
!> <name> ( n -- ) Store integer into value. Identical to =:
！> <name> （ n -- ） 將整數儲存為值。與 = 相同：
@> <name> ( -- n ) Return contents of a value.
@> <name> （ -- n ） 傳回值的內容。
+!> <name> Increment value-name by integer
+！> <name> 以整數遞增值名稱
INCR> <name> Increment value-name by one
INCR> <name> 將 value-name 遞增 1
DECR> <name> Decrement value-name by one
DECR> <name> 遞減 value-name 一
ON> <name> Store -1 into value-name
ON>將 <name> -1 儲存到 value-name 中
OFF> <name> Store 0 into value-name
OFF> <name> 將 0 儲存到 value-name 中
```

These operators are written in assembly, so they are very fast. The name
這些運算子是用組合語言編寫的，所以它們非常快。名稱
following these value operators should be defined with VALUE. However,
這些值運算子後面應該使用 VALUE 定義。但
these operators will work on constants, variables, and even deferred
這些運算子將處理常數、變數，甚至延遲
words, but you will have to take responsibility of the consequences.
話，但你必須對後果負責。

Variable-constants or VALUE's are very useful in passing data among many
變數常數或 VALUE 在許多變數之間傳遞資料非常有用
program modules. One module sets the value in a constant or VALUE and
程式模組。一個模組在常數或 VALUE 中設定值，並且
many other modules can use it. As VALUE's, constants and variables are
許多其他模組可以使用它。作為 VALUE，常數和變數是
global in Forth, you have to watch them very carefully in a large
全球的，你必須非常仔細地觀察它們
program. Changing the value of a constant can be deadly if you are not
程序。如果您不這樣做，更改常數的值可能是致命的
aware of its consequences. Use this tool with caution.
意識到其後果。請謹慎使用此工具。

The constants -1, 0, 1, 2, and 3 defined in F83 are eliminated in F-PC
F83 中定義的常數 -1、0、1、2 和 3 在 F-PC 中被消除
because in F-PC literals are much faster than constants. In-line
因為在 F-PC 中，文字比常數快得多。在線
literals are faster than constants and values in F-PC, because (LIT) is
文字比 F-PC 中的常數和值更快，因為 （LIT） 是
simply:
只是：

```
CODE (LIT) LODSW ES: 1PUSH END-CODE
```

However, excessive use of literal numbers will make code very difficult
然而，過度使用文字數字會使程式碼變得非常困難
to understand. It is much preferred to name the constants and values to
去理解。最好將常數和值命名為
help documenting your intentions.
幫助記錄您的意圖。


## 4.4. HELP WORDS 4.4. 幫助詞

F-PC provides the standard F83 decompiler command SEE. SEE has been
F-PC 提供標準 F83 反編譯器命令 SEE。SEE 一直
modified to display a decompiled source that is in most cases very
修改為顯示反編譯的源代碼，該源代碼在大多數情況下非常
similar to the original source on disk. This capability does not come
類似於磁碟上的原始來源。這個能力沒有來
free. The price we pay in F-PC is that every word must have a unique
放。我們在 F-PC 中付出的代價是每個單詞都必須有一個獨特的
address in the Code segment, even when the words have identical code,
address 的 address，即使單字具有相同的代碼，
such as IF, UNTIL, and WHILE, which all compile the same ?BRANCH. The
例如 IF、UNTIL 和 WHILE，它們編譯的都是相同的？支。這
unique code addresses enable the decompiler to identify and recover the
唯一的程式碼位址可讓反編譯器識別並復原
proper names to be displayed. The debugger DEBUG and DBG also uses this
要顯示的專有名稱。偵錯工具 DEBUG 和 DBG 也使用
decompiler to display the definition under examination.
反編譯器以顯示正在檢查的定義。


REF is the inverse of SEE.
REF 是 SEE 的逆數。

REF <wordname>

searches through all colon words defined in the dictionary and displays
搜尋字典中定義的所有冒號單字並顯示
the names of words which contains <wordname>. This tool is very useful
包含 的單詞名稱 <wordname>。這個工具非常有用
in analyzing where a word is used and how often it is used in any
分析一個詞的使用位置以及該詞在任何單詞中的使用頻率
application.
應用。

The help mechanism in F-PC 3.5 is much more polished and powerful than
F-PC 3.5 中的幫助機制比
that in F83 and F-PC 2.25, because of the hypertext based browser.
F83 和 F-PC 2.25 中，因為基於超文本的瀏覽器。
Whenever help is requested, the editor is invoked and the system is put
每當請求幫助時，都會調用編輯器並放置系統
into the browsing mode. If a word name is given after a HELP word, a
進入瀏覽模式。如果在 HELP 單字之後給出單字名稱，則
.HLP text file is opened and the text about the word is display in the
.HLP 文字檔案會開啟，且有關該單字的文字會顯示在
editor window. The user can then use the browser to move around looking
編輯器視窗。然後，用戶可以使用瀏覽器四處移動尋找
at source code or help text.
在源代碼或幫助文本中。

The principal help command in F-PC 3.5 is BROWSE. VIEW is made an alias
F-PC 3.5 中的主要幫助命令是 BROWSE。VIEW 會變成別名
of BROWSE to maintain F83 compatibility. B and V are also aliases of
的 BROWSE 以保持 F83 相容性。B 和 V 也是
BROWSE for convenience.
為了方便起見，瀏覽。

```
BROWSE <wordname>
```

opens the .SEQ file in which <wordname> was defined and displays the
開啟 。SEQ 檔案 <wordname>，並顯示
source code of <wordname>.
的原始碼 <wordname>。

```
HELP <wordname>
```

opens the companion .HLP file to the .SEQ file in which a word is defined
開啟小夥伴 。HLP 檔案新增至 .SEQ 檔案，其中定義了單字
and displays the help message in the HLP file associated with <wordname>.
，並在與 相關聯的 HLP 檔案中顯示說明訊息 <wordname>。
It assumes that the help file exists; otherwise, an error message will be
它假設說明檔案存在;否則，錯誤訊息將是
displayed.
顯示。

Used without a word name, HELP enters the editor's browsing mode and
不帶字名使用，HELP 進入編輯器的瀏覽模式，並
displays the root help screen of the hypertext help system to assist you
顯示超文本幫助系統的根幫助畫面，為您提供協助
start ing the investigation of F-PC. While you are browsing a file,
開始調查 F-PC。當您瀏覽檔案時，
position the cursor on any word and press <return> or F9. The source
將游標放在任何字上，然後按 <return> 或 F9。來源
code of this word will be displayed. If you want to see the help text
將顯示該字的代碼。如果您想查看說明文字
about a word, press Alt-H.
關於一個單詞，按 Alt-H。

WORDS behaves identically to that in F83 when used normally to display
WORDS 在正常使用時的行為與 F83 中的行為相同，以顯示
the names of definitions in the context vocabulary. It is enhanced in
上下文詞彙中的定義名稱。它在
F-PC such that if the following string is not a valid name in the context
F-PC，因此如果下列字串在內容中不是有效名稱
vocabulary, it will use the string as a substring template and prints the
詞彙，它會使用字串作為子字串模板，並列印
names of all definitions in all vocabularies, whose name contains the
所有詞彙中所有定義的名稱，其名稱包含
substring. Two substrings can be attached to WORDS. Many special strings
子字串。兩個子字串可以附加至 WORDS。許多特殊琴弦
can be used after WORDS to show different classes of Forth words. For
可以在 WORDS 之後使用，以顯示不同類別的 Forth 單字。為
example, WORDS *.* causes all words in all vocabularies to be
例如，WORDS *.* 會導致所有詞彙中的所有單字
displayed.
顯示。

The behavior of these very useful help words is summarized as follows:
這些非常有用的幫助詞的行為總結如下：

```
BROWSE <wordname> Drop into the browsing mode in editor and display the
瀏覽 在<wordname>編輯器中拖放到瀏覽模式並顯示
source of <wordname>.
的來源 <wordname>。
B Shorthand for BROWSE.
B 瀏覽的簡寫。
ED <wordname> Drop into the editing mode in editor, display the
ED 在<wordname>編輯器中進入編輯模式，顯示
source of <wordname> and ready for editing.
來源<wordname>並準備好編輯。
E Shorthand for ED.
E ED 的簡寫。
HELP Drop into the editor and display system help message.
HELP 拖入編輯器並顯示系統說明訊息。
HELP <wordname> Display help message associated with <wordname>.
說明 <wordname> 顯示與 相關聯的說明訊息 <wordname>。
H Shorthand for HELP.
H HELP 的簡寫。
REF <wordname> Display all words which compile ,wordname>.
REF <wordname> 顯示所有編譯 ，wordname> 的單詞。
SEE <wordname> Decompile <wordname>.
參見 <wordname> 反編譯 <wordname>。
VIEW <wordname> Alias of BROWSE.
查看瀏覽<wordname>的別名。
V Shorthand for VIEW.
V VIEW 的簡寫。
WORDS Display words in the context vocabulary.
單詞 在上下文詞彙中顯示單詞。
WORDS xyz Display all words containing the substring 'xyz'.
WORDS xyz 顯示包含子字串 'xyz' 的所有單字。
WORDS xy ab Display all words containing both 'xy' and 'ab'.
單詞 xy ab 顯示所有同時包含 'xy' 和 'ab' 的單詞。
WORDS *.* Display all words in F-PC.
單詞 *.* 顯示 F-PC 中的所有單詞。
WORDS :.* Display all colon words.
單詞 ：.* 顯示所有冒號單詞。
WORDS code.* Display all code words.
WORDS code.* 顯示所有代碼字。
WORDS constant.* Display all constants.
WORDS 常數。* 顯示所有常數。
WORDS defer.* Display all deferred words.
WORDS defer.* 顯示所有延遲的字詞。
WORDS total.* Display number of words.
總字數。* 顯示字數。
WORDS udefer.* Display all user deferred words.
WORDS udefer.* 顯示所有用戶延遲的單詞。
WORDS uvariable.* Display all user variables.
WORDS uvariable.* 顯示所有使用者變數。
WORDS value.* Display all value words.
WORDS 值。* 顯示所有值字。
WORDS variable.* Display all variables.
WORDS 變數。* 顯示所有變數。
```

## 4.5. DATE AND TIME 4.5. 日期和時間

A complete set of time and date manipulation words has been included in
一套完整的時間和日期操作詞已包含在
F-PC. They call appropriate DOS service functions to provide the
F-PC。它們會呼叫適當的 DOS 服務函式，以提供
requested services. The words for getting and setting the date and time
請求的服務。用於獲取和設置日期和時間的單詞
are as follows:
如下：

```
GETDATE ( -- d1 ) Return d1 a 32 bit binary date
GETDATE （ -- d1 ） 傳回 d1 一個 32 位元二進位日期
from the operating system. Bytes
從作業系統。位元組
in d1 are arranged as
在 d1 中，被安排為
year/month/day/day-of-week.
年/月/日/星期幾。
SETDATE ( d1 -- ) Given the binary date d1, set the
SETDATE （ d1 -- ） 給定二進位日期 d1，將
system clock to that date.
系統時鐘到該日期。
GETTIME ( -- d1 ) Return d1 with bytes arranged in
GETTIME （ -- d1 ） 傳回 d1，位元組排列在
the order hr/min/sec/100th- sec
順序 hr/min/sec/100th- sec
from the operating system.
從作業系統。
SETTIME ( d1 -- ) Given the binary time d1, set the
SETTIME （ d1 -- ） 給定二進位時間 d1，將
system clock to that time.
系統時鐘到那個時間。
.DATE ( -- ) Print to the screen the current date, in the
.DATE （ -- ） 將目前日期列印到螢幕上，在
format MM/DD/YY, where MM is
格式 MM/DD/YY，其中 MM 是
month, DD is day, and YY is year.
月，DD 是日，YY 是年。
Y-M-D sets the format to
Y-M-D 將格式設定為
YY-MM-DD, and D.M.Y sets it to
YY-MM-DD，而 D.M.Y 將其設定為
DD.MM.YY.
DD.MM.YY。
.TIME ( -- ) Print to the screen the current
.時間 （ -- ） 將當前
time, in the format HH:MM:SS.HR,
time，格式為 HH：MM：SS.HR，
where HH is in hours, MM in
其中 HH 以小時為單位，MM 以小時為單位
minutes, SS in seconds, and HR
分鐘、SS （以秒為單位） 和 HR
in hundredths of a second.
在百分之一秒內。
```

A special word set is defined in F-PC for measuring elapsed time for real
F-PC 中定義了一個特殊的字集，用於測量實際經過的時間
time experiments and for characterization of program performance.
時間實驗和程序性能的表徵。

TIMER <name> TIMER performs the Forth words following on the
TIMER <name> TIMER 執行
same command line, and when they finish
相同的命令列，以及當它們完成時
execution, TIMER prints the elapsed time required
執行時，TIMER 會列印所需的經過時間
for their execution.
為了執行他們的處決。
TIME-RESET Reset the accumulated time value in the double
TIME-RESET 重置雙精度中的累積時間值
variable STIME to zero, in effect resetting the
變數 STIME 設為零，實際上會將
current elapsed time to zero.
電流經過時間為零。
.ELAPSED Print the time elapsed since the last TIME_RESET.
.ELAPSED 列印自上次 TIME_RESET 以來經過的時間。

TIMER-RESET is used at the beginning of a sequence of operations you want
TIMER-RESET 用於您想要的一系列操作的開頭
to time. The word .ELAPSED is used at the end of the operations to print
到時間。這個詞。ELAPSED 用於列印作業結束時
the elapsed time since the last TIME- RESET.
自上次 TIME- RESET 以來經過的時間。


The following words are used to change different fields in the timer:
下列字詞可用來變更計時器中的不同欄位：

```
TENTHS ( tenths_of_a_second -- )
SECONDS ( seconds -- )
MINUTES ( minutes -- )
HOURS ( hours -- )
```

Time delay words use the DOS time function to obtain very accurate time
延時詞使用 DOS 時間函數來獲得非常準確的時間
delays. Background processing continues, as pause is called in the wait
延誤。背景處理會繼續，因為在等待期間呼叫暫停
loop. Another deferred word, PAUSE-FUNC, is also in the loop, which can
圈。另一個延遲詞 PAUSE-FUNC 也在循環中，它可以
be re-assigned to perform any function you want done while the delay is
被重新分配以在延遲期間執行您想要完成的任何功能
occurring.
發生。


## 4.6. COMMENTS  4.6. 註解

All comment words in F83, like (, .(, \, \S are preserved and they behave
F83 中的所有註解字，例如 （、.（、\、\S） 都會保留，並且它們的行為
identically in F-PC. However, a file in F-PC is similar to a block in F83
在 F-PC 中也是如此。但是，F-PC 中的檔案類似於 F83 中的區塊
and \S stops the compilation of the rest of the file. To accommodate
\S 會停止檔案其餘部分的編譯。為了適應
documentation which spans over many lines, additional comment words are
跨越多行的文件，附加註釋詞是
defined in F-PC. Multiple line comment in F-PC starts with COMMENT: and
在 F-PC 中定義。F-PC 中的多行註解以 COMMENT： 和
terminates at COMMENT; . It looks like:
終止於 COMMENT; 。它看起來像：


COMMENT:
註解：
<text>
<more text>
<更多文字>
...
<even more text>
<更多文字>
COMMENT;
註解;
To print multiple line comments during compiling,
若要在編譯期間列印多行註解，


.COMMENT:
.註解：
...
...
COMMENT;
註解;


.COMMENT: starts a group of lines that are to be printed to the terminal,
.COMMENT：啟動一組要列印到終端機的行，
until a terminating COMMENT; is found.
直到終止 COMMENT;被發現。


/* and */ pair can be used to enclose comments similar to the COMMENT:
/* 和 */ 對可用於括住類似於 COMMENT 的註釋：
and COMMENT; pair. They make the source code look even closer to C code.
和評論;雙。它們使原始程式碼看起來更接近 C 程式碼。


Plenty of documentation tools are provided in F-PC. There is no excuse
F-PC 中提供了大量文檔工具。沒有任何藉口
not using them to beautify your program.
不要用它們來美化你的程序。


## 4.7. SCREEN CONTROL WORDS IN F-PC 4.7. F-PC 中的螢幕控制詞

F-PC allows you to control the CRT screen to generate very fancy text
F-PC 允許您控制 CRT 屏幕以生成非常精美的文本
displays.
顯示。

FAST Select the fast screen output routines
快速 選擇快速螢幕輸出常式
that are very hardware dependent.
非常依賴硬體。

The fast mode of screen display is much faster than what BDOS can do, but
屏幕顯示的快速模式比 BDOS 能做到的要快得多，但是
requires very compatible hardware. As FAST stores characters directly
需要非常相容的硬體。由於 FAST 直接儲存字元
into the hardware screen buffer, you have to make sure that a carriage
進入硬體螢幕緩衝區，您必須確保一個托架
return is inserted before a line runs over the 79'th column. If you want
在第 79 欄的行之前插入 return。如果你想要
line wrap, use:
換行，使用：

SLOW Select the SLOW screen output routines.
慢速 選取慢速螢幕輸出常式。

The BDOS display routines are less hardware dependent than FAST.
BDOS 顯示常式比 FAST 少相依於硬體。

When F-PC is loaded into PC, it asks DOS what kind of video board is in
當 F-PC 加載到 PC 中時，它會詢問 DOS 中裝有哪種視頻板
the PC and sets the video display mode accordingly. It also allows you
並相應地設置視頻顯示模式。它還允許您
to change the attributes of displayed characters very conveniently.
非常方便地更改顯示字符的屬性。

In the monochrome mode, you can select from the following list different
在單色模式下，您可以從以下列表中選擇不同的
types of characters to be displayed on the screen:
要在螢幕上顯示的字元類型：

```
>NONE Normal character display
>無 正常字元顯示
>UL Underlined
>UL 下劃線
>BOLD Bold
>粗體
>REV Reversed. Black character on white background.
>REV 撤銷。白底黑字。
>BOLDUL Bold underlined
>粗體下劃線
>BOLDBLNK Bold blinking
>BOLDBLNK 粗體閃爍
>REVBLNK Reversed blinking
>REVBLNK 反向閃爍
```

Characters EMITed to the screen are not affected by the attribute
發出到螢幕的字元不受屬性的影響
selection. To show characters with the selected attribute, used FEMIT or
選擇。若要顯示具有所選屬性的字元，請使用 FEMIT 或
TYPE.
型。

F-PC also supports color cards. It asks DOS which card is installed and
F-PC 也支援色卡。它詢問 DOS 安裝了哪張卡，以及
configures the output routines accordingly. In color mode, F-PC gives
相應地配置輸出常式。在彩色模式下，F-PC 給出了
you the following choices:
您有下列選擇：

```
>BUGN Blue background, green foreground
>BUGN 藍色背景，綠色前景
>RDWT Red background, white foreground
>RDWT 紅色背景，白色前景
>GNWT Green background, white foreground
>GNWT 綠色背景，白色前景
```

There are many other choices of background/foreground combinations. The
背景/前景組合還有許多其他選擇。這
following word set allows you to specified any combination of foreground
下列字組可讓您指定前景的任意組合
and background colors:
和背景顏色：

```
>FG ( n1 -- ) Select foreground
>FG （ n1 -- ） 選取前景
>BG ( n1 -- ) Select background
>BG （ n1 -- ） 選擇背景
```

Words from the COLOR.SEQ file that allow setting the foreground and
來自 COLOR.SEQ 檔案，允許設定前景和
background colors on a color monitor are:
色彩監視器上的背景色彩包括：

```
>ATTRIB1 to >ATTRIB8 ( -- )
```

They are deferred words to allow selection of the various display
它們是延遲字，以允許選擇各種顯示
attributes for the current display board. They default to the following
目前顯示板的屬性。它們預設為下列
attributes for Monochrome or Color Card:
單色或色卡的屬性：

```
MONOCHROME COLOR
Word bkgrnd frgrnd
```

```
>ATTRIB1 UNDERLINE BLUE GREEN
>ATTRIB1 下劃線 藍綠色
>ATTRIB2 BOLD UNDERLINE RED WHITE
>ATTRIB2 粗體下劃線 紅色 白色
>ATTRIB3 BOLD BLUE WHITE
>ATTRIB3 大膽的藍白
>ATTRIB4 REVERSE RED WHITE
>ATTRIB4 反轉紅白
```

These values can be changed by changing either COLOR.SEQ, or MONOCROM.SEQ
這些值可以透過變更任一 COLOR.SEQ，或單線。序
and re- generating the system with EXTEND.BAT.
並用 EXTEND.BAT 再生系統。

```
SAVESCR ( -- ) Save screen
RESTSCR ( -- ) Restore screen
RECOVERSCR ( -- ) Copy rather than pop the screen stack.
RECOVERLINE ( n -- ) Copy a line from saved screen stack.
```

These words give you the ability to save the screen contents and later
這些詞使您能夠保存屏幕內容和以後的內容
restore the screen to its original appearance in a simple way. SAVESCR
以簡單的方式將螢幕恢復到原來的外觀。SAVESCR
may be used and nested up to three times before RESTSCR needs to be done.
在需要完成 RESTSCR 之前，最多可以使用和巢狀 3 次。
That is, three screens can be saved and sequentially restored.
也就是說，可以保存三個屏幕並依序還原。

## 4.8. COMPILATION CONTROL WORDS 4.8. 編譯控制詞

To load a source file, the most convenient way is to use the command
要載入原始檔，最方便的方法是使用命令
FLOAD or its alias INCLUDE:
FLOAD 或其別名包括：

```
FLOAD <file-name> <return>
INCLUDE <file-name> <return>
```

will open the file and compile the source code starting at the beginning.
將開啟檔案，從頭開始編譯原始碼。
After the file is compiled, FLOAD closes the file so that other files can
編譯檔案之後，FLOAD 會關閉檔案，讓其他檔案可以
be loaded.
被加載。


If a file is opened by the editor or by the OPEN command,
如果編輯器或 OPEN 指令開啟檔案，

```
OK <return>
```

compiles the currently open file, starting at the beginning, and
編譯目前開啟的檔案，從頭開始，以及
continuing through the end of the file or until an error is encountered.
一直持續到檔案結尾或直到遇到錯誤為止。

```
<line-number> LOAD <return>
```

Start loading the current file starting at the <line_number> specified.
從指定的開始載入目前檔案 <line_number>。
If the stack is empty (no line- number specifier), it starts at line 1.
如果堆疊是空的 （沒有行號指定元） ，則會從第 1 行開始。
It loads through the end of the file or until an error or an \S is
它會載入檔案結尾，或直到錯誤或 \S 為止
encountered. OK is defined as 1 LOAD.
遇到了。OK 定義為 1 LOAD。

The names of all files loaded into the F-PC system are stored in a
載入到 F-PC 系統中的所有檔案名稱都儲存在
vocabulary FILES. The word .LOADED displays their names.
詞彙文件。這個詞。LOADED 會顯示其名稱。

The word #IF has been added, which accepts a Boolean flag, and determines
已新增單字 #IF，它接受布林旗標，並決定
if the lines following #IF are compiled up until the #ENDIF. A TRUE flag
如果後面的行 #IF 編譯到 #ENDIF。TRUE 旗標
causes the lines to be compiled. A FALSE flag causes the lines to be
導致編譯行。FALSE 旗標會導致行為
skipped.
跳過了。

```
TRUE #IF
.( This message will be printed.)
#ENDIF
```

## 4.9. PRINTING SOURCE FILES IN F-PC 4.9. 在 F-PC 中列印原始檔案

Files can of course be printed while in the editor, but you can also
當然，可以在編輯器中列印檔案，但您也可以
print files from a Forth command line as follows:
從 Forth 命令列列印檔案，如下所示：

```
OPEN <filename> <return> \ Open a file
LISTING <return> \ Print the file
```

The print format is the same as the default format for the editor. Every
列印格式與編輯器的預設格式相同。每
page is printed with a header and a footer, suitable for framing. The
頁面印有頁眉和頁腳，適合裝裱。這
header is taken from the first line in the file. You can thus customize
header 取自檔案中的第一行。因此，您可以自訂
the header according to your taste by carefully designing the text in the
根據您的喜好精心設計文本的標題
first line. The footer provides the file name, page number, date and
第一行。頁尾提供檔案名稱、頁碼、日期和
time. A command which combines the two commands above is:
時間。結合上述兩個命令的命令是：

```
FPRINT <filespec> <return>
```

It opens the file and performs a LISTING. Wildcard characters can be
它會開啟檔案並執行 LISTING。萬用字元可以是
used in the file specification so that many files are printed with a
在檔案規格中使用，以便許多檔案以
single FPRINT command.
單一 FPRINT 指令。

```
INDEX <filespec> <return>
```

behaves similarly to FPRINT. However, it displays only the first line of
其行為類似於 FPRINT。不過，它只會顯示
each file specified and thus produces a nice table of contents for the
每個指定的檔案都會為
files selected.
選取的檔案。

Another very useful word is PRINT. PRINT turns on the printer and
另一個非常有用的詞是 PRINT。PRINT 開啟印表機，然後
interprets the commands following it. All the characters sent to the
解譯後面的命令。所有傳送至
screen are now sent to the printer.
螢幕現在會傳送到印表機。

## 4.10. GLOBAL SEARCH  4.10. 全域搜尋

One of the neat additions to F-PC is EDITALL. EDITALL is used as
F-PC 的巧妙補充之一是 EDITALL。EDITALL 用作
follows:
如下：

```
EDITALL <string> <filespecs> ... <return>
```

All files specified are searched for <string>. If the string is found,
會搜尋所有指定的檔案 <string>。如果找到字串，
the editor is entered on that line in the file, ready for you to perform
編輯器會輸入到檔案中的該行，可供您執行
an edit or replace on the string. If you use F8, the replacement is made
對字串進行編輯或替換。如果您使用 F8，則會進行替換
and the next occurrence is found. Otherwise, only the first occurrence
並找到下一個出現。否則，只有第一次出現
of string is located, and repeated Alt-F6 commands can locate additional
的字串，重複的 Alt-F6 指令可以找到其他
occurrences of string in the file. Shift-F8 Replace-All can also be used
檔案中字串的出現次數。也可以使用 Shift-F8 全部替換
while in a file to replace all occurrences of a string with another
while 在檔案中，將字串的所有出現項目替換為另一個字串
string. When you are done editing, press ESC to terminate edit, and the
繩子。完成編輯後，按 ESC 終止編輯，然後
search will continue through the filespecs specified for additional
搜尋將繼續透過指定給其他
occurrences of string, until all files have been searched through. This
字串的出現，直到搜尋完所有檔案為止。這
has been very valuable in maintaining a system by making global changes
通過進行全局更改來維護系統非常有價值
to all occurrences of a Forth word.
對 Forth 單詞的所有出現。


If you want to search a string containing spaces, just type EDITALL
如果要搜尋包含空格的字串，只需鍵入 EDITALL
<return> and you will be prompted for a string to search for.
<return> 系統會提示您輸入要搜尋的字串。

Another interesting addition to F-PC is:
F-PC 的另一個有趣的新增功能是：

FLOOK <name> <filespecs> <return>

It performs similarly to EDITALL in searching for a string through many
它的執行方式類似於 EDITALL 在透過許多
files, but it just displays the line number and the line contents of all
文件，但它只顯示所有
occurrences found without doing anything to the strings found. It is
找到的出現次數，但沒有對找到的字串執行任何操作。這是
very useful to print a report on where a particular string occurred in a
對於列印特定字串在
set of files.
檔案集。


## 4.11. ALIAS 4.11. 別名

In many occasions, there is a need to shorten the name of a word which we
在許多情況下，需要縮短一個詞的名稱，我們
expect the user to use very often, like BROWSE, HELP, etc. It is
期望用戶經常使用，例如 BROWSE、HELP 等。這是
wasteful to redefine the function using a short name. ALIAS is a defining
使用簡短名稱重新定義函數是浪費的。ALIAS 是一個定義
word which generates a new definition with a head only. Its
單詞，它生成一個僅帶有頭部的新定義。它的
code-pointer- field points to the code field of an existing word. It
code-pointer- 欄位指向現有單字的程式碼欄位。它
does not need its own code field at all. Examples of its uses are:
完全不需要自己的程式碼欄位。其用途範例包括：

```
' BROWSE ALIAS B
' HELP ALIAS H
```

The code field address returned by ' is then stored in the head of the
然後，' 傳回的代碼欄位位址會儲存在
new word, forcing it to perform the function of a word already defined in
new word，強制它執行
the dictionary.
字典。

## 4.12. BROWSING A LARGE FILE  4.12. 瀏覽大檔案

F-PC generally reads an entire file into the editor buffer for editing
F-PC 一般將整個檔案讀取到編輯器緩衝區中進行編輯
and browsing. It can handle a file up to about 120K bytes on a 640K byte
和瀏覽。它可以在 640K 位元組上處理高達 120K 位元組的檔案
machine. However, if you have to examine a file larger than what the
機。不過，如果您必須檢查檔案大於
memory can hold, you can read in a part of it and browsing through that
記憶體可以保存，你可以讀取其中的一部分並瀏覽它
part. VIEWFROM and its alias VF is included to allow viewing very large
部分。VIEWFROM 及其別名 VF 包含在內，以允許查看非常大的
files from a specified starting line number. It is used in the form:
指定起始行號中的檔案。它以以下形式使用：

```
OPEN FPCGLOS.TXT \ A very large file
300 VIEWFROM <return>
```

The above commands skip the first 300 lines of the file and starts
上述命令會跳過檔案的前 300 行，並啟動
reading at line 300. This is useful for examining very large files. You
閱讀第 300 行。這對於檢查非常大的檔案很有用。你
should of course be careful not to switch to editing mode and change such
當然應該注意不要切換到編輯模式並更改
a file lest it get written back to the original file on disk. You can use
一個檔案，以免它寫回磁碟上的原始檔案。您可以使用
Alt-W to write the read portion of the file out to a new file.
Alt-W 將檔案的讀取部分寫入新檔案。

## 4.13. THE NEWZ EDITOR  4.13. NEWZ 編輯器

This is Tom Zimmer's new and improved editor. The execution file and its
這是 Tom Zimmer 的全新改進編輯器。執行檔案及其
documentation files are put in the NEWZ directory, separated from F-PC.
文檔文件放在 NEWZ 目錄中，與 F-PC 分開。
This NEWZ editor includes some additional features that make it very
這個 NEWZ 編輯器包含一些附加功能，使其非常
useful when examining someone else's source code for a program you have
在檢查您擁有的程式的其他人原始碼時很有用
been given. Tom had experienced the pain associated with taking over
被給予。湯姆經歷過接管帶來的痛苦
another person's program for maintenance and change. It can be very
另一個人的維護和變更計劃。它可以非常
painful if the program is large and consists of many files. NEWZ can now
如果程序很大並且由許多文件組成，則會很痛苦。NEWZ 現在可以
compile an index file of all symbols in your source files. It then
編譯原始檔中所有符號的索引檔。然後它
provides a hypertext browsing environment where you can easily view,
提供超文本瀏覽環境，方便查看，
change, and explore a multitude of source files. You can nest file
更改並探索大量源文件。您可以巢狀檔案
searches and return to where you were. Locating any symbol in a
搜索並返回您原來的位置。在
multi-thousand symbol index file on an 80286 machine takes less than one
80286 機器上的數千個符號索引檔案需要少於一個
second. This version of NEWZ supports Forth type words, and assembly
秒。此版本的 NEWZ 支援 Forth 類型 word，以及組合語言
symbols. Support for additional languages will be provided shortly on an
符號。對其他語言的支持將很快在
as requested basis. See NEWZ's hypertext help under configuration for
根據要求的基礎。請參閱 NEWZ 的超文本說明 在配置下
details of how to setup and build an index file of your source files.
詳細說明如何設定和建置來源檔案的索引檔案。


NEWZ includes many new features, here is a brief summary:
NEWZ 包含許多新功能，以下是簡要總結：


1. Work with up to 20 files at one time. (Only one file is in memory
2. 一次最多處理 20 個文件。（記憶體中只有一個檔案
but switching between files with a hard disk is very quick, and
但是使用硬碟在檔案之間切換非常快，並且
requires only a single keystroke.)
只需要一次按鍵。


2. Searching is supported within a file, and across multiple files,
2. 支持在一個文件內和多個文件之間進行搜索，
to help find any file that contains a particular character
以協助尋找包含特定字元的任何檔案
sequence.
序。


3. You can set the default file extension to any three characters.
3. 您可以將默認文件擴展名設置為任意三個字符。
The specified extension will be applied to a file when no
當沒有
extension is specified.
副檔名。


4. Maximum file size is limited by available memory, and will
4. 最大檔案大小受可用記憶體限制，並且會
typically be greater than 250k on a 640k machine.
在 640k 機器上通常大於 250k。


5. EGA/VGA high resolution text modes are supported, NEWZ will
5. 支援 EGA/VGA 高解析度文字模式，NEWZ 將
automatically adjust to whatever screen size your display is set
自動調整為顯示器設定的任何螢幕尺寸
for up to 132 columns by 60 lines.
最多可容納 132 欄 x 60 行。


6. You can create your own hypertext systems for training.
6、可以創建自己的超文本系統進行訓練。


7. NEWZ is very fast, moving around a document, or from one end to
7. NEWZ 速度非常快，可以在文件周圍移動，或從一端移動到
the other, is limited by the repeat rate of your keyboard, not
另一個，受鍵盤重複率的限制，而不是
NEWZ's redisplay speed. On a 4.7 MHZ 8088 machine, NEWZ can
NEWZ 的重新顯示速度。在 4.7 MHZ 8088 機器上，NEWZ 可以
redisplay more than ten full (80x24) screens per second.
每秒重新顯示十個以上的完整 （80x24） 螢幕。


8. NEWZ automatically recognizes and supports a mouse when a driver
8. NEWZ 在驅動程序時自動識別並支持鼠標
is present. The mouse can be used with pulldown menus, cursor
存在。鼠標可以與下拉菜單、光標一起使用
positioning, scanning through a document, and text line selection
定位、掃描文件和文字行選取
for Cut and Copy operations.
用於剪下和複製作業。


9. You can specify in the NEWZ.CFG configuration file whether you
9. 您可以在 NEWZ.CFG 組態檔，無論您
want backup copies kept of your edits.
想要保留您編輯的備份副本。


The NEWZ editor is shareware. If you find NEWZ useful in your daily work,
NEWZ 編輯器是共享軟件。如果您發現 NEWZ 在您的日常工作中很有用，
join other satisfied users and register your copy by sending a check for
加入其他滿意的用戶並通過發送支票來註冊您的副本
$50.00 to the address below.
50.00 美元至以下地址。


Tom Zimmer, 292 Falcato Drive, Milpitas, CA 95035,
湯姆·季默，292 Falcato Drive，米爾皮塔斯，CA 95035，
Tel. (408) 263-8859.
電話：（408） 263-8859。


You will receive the next upgrade free, and you will be notified of new
您將免費收到下一次升級，並且您將收到新的通知
releases about twice a year. Each upgrade will be about $25.00. Be sure
大約每年發布兩次。每次升級約為 25.00 美元。確定
to send your NEWZ revision date (displayed in the upper right hand corner
發送您的 NEWZ 修訂日期（顯示在右上角
after you leave NEWZ).
在您離開 NEWZ 之後）。


## 4.14. THE SZ EDITOR 4.14. SZ 編輯器

This is another one of Tom Zimmer's new and improved editors. The major
這是 Tom Zimmer 的另一位新的和改進的編輯器。專業
improvement is its size, only 18K bytes! It is produced by Tom's new
改進是它的大小，只有 18K 字節！它是由湯姆的新
target compiler, which is designed to generate tight and secure
目標編譯器，其設計目的是產生緊密且安全的
application programs from F-PC source. It only compiles what is needed
來自 F-PC 來源的應用程式。它只編譯需要的內容
in the application and discards Forth words which are not used by the
並丟棄未被
application.
應用。


SZ is very simple to use. Type:
SZ 使用起來非常簡單。型：

```
SZ <filename> <return>
```

and you can edit the file immediately. Press F1 or ESC pops up and help
您可以立即編輯該文件。按 F1 或 ESC 彈出並幫助
screen showing all the commands available. It has the general look and
顯示所有可用命令的屏幕。它具有整體外觀和
feel of SED, without the complications. It is quite sufficient for
SED 的感覺，沒有並發症。對於
writing programs and research papers.
撰寫程序和研究論文。


SZ is a public domain program. You can distribute it freely. Contact
SZ 是一個公共領域程序。您可以自由分發它。㨟
Tom if you need a customized editor, or if you are interested in his
湯姆，如果您需要定制編輯器，或者您對他的編輯器感興趣
target compiler.
目標編譯器。

