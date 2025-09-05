OBþ
奧布茲
OþþBþþ . . . . . . . . . . . . . . . Word Glossary of the F-PC Forth Vocabulary by Tom Zimmer
OþþBþþ . . .湯姆·季默 （Tom Zimmer） 的 F-PC Forth 詞彙表


****************************** Notice *************************************
啟事*************************************
* 10/16/89 T. Zimmer *
* 10/16/89 T. 齊默 *
* As of this release, this glossary contains all of the words that are *
* 從此版本開始，此詞彙表包含所有單字 *
* going to be documented in F-PC, BUT! Not all of the words have glossary *
* 將記錄在 F-PC 中，但是！並非所有單詞都有詞彙表 *
* entries entered, so you will find some words that specify only a word *
* 輸入的條目，因此您會發現一些僅指定一個單詞的單詞 *
* name, followed by a vocabulary name. This file is still in the process *
* name，後面接著詞彙名稱。此檔案仍在處理中 *
* of being updated. *
* 正在更新。*
* *
***************************************************************************


Forward
前


This glossary contains entries for all of the words in F-PC's FORTH
此詞彙表包含 F-PC 的 FORTH 中所有單詞的條目
vocabulary, broken into two major sections. The first section contains
詞彙，分為兩個主要部分。第一節包含
lists of words broken into catagories. The second section contains the
分成類別的單詞列表。第二個區段包含
same words grouped in a single alphabetized list. The alphabetized
相同的單詞分組在一個按字母順序排列的列表中。按字母順序排列的
list includes a stack picuture, the filename where the words source can
列表包含一個堆棧 picuture，即單詞 source 可以
be found, and descriptive text explaining the function of each word in
被找到，並解釋每個單詞功能的描述性文本
the list. The catagory section contains only a list of words in a
名單。類別區段僅包含
catagory, and a stack picture for each word.
類別，以及每個單字的堆疊圖片。


Glossary Format
詞彙表格式


The format of this glossary uses abreviated character sequences to
此詞彙表的格式使用縮寫字元序列來
describe a series of words, this is done primarily for brevity. Here
描述一系列單詞，這樣做主要是為了簡潔。這裏
is a list of the abreviations used in this glossary.
是本詞彙表中使用的縮寫清單。


Symbol definitions used in this Glossary
本詞彙表中使用的符號定義


n1 16 bit signed number
n1 16 位元有符號數
d1 32 bit signed number
d1 32 位元有符號數
u1 16 bit unsigned number
u1 16 位元無正負號
ud1 32 bit unsigned number
ud1 32 位元無正負號
f1 boolean flag
f1 布林旗標
c1 8 bit character
C1 8 位元字元
nfa Name field address
nfa 名稱欄位位址
cfa code field address
CFA 代碼欄位位址
lfa link field address
LFA 連結欄位位址
seg 16 bit absolute segment number
SEG 16 位絕對段號
offset 16 bit offset into a segment
偏移 16 位偏移到區段中
<char> A character from the input stream.
<char> 輸入資料流程中的字元。
<name> A Forth word, comes from the input stream.
<name> 第四個字來自輸入流。
<string> A sequence of ascii characters, comes from the
<string> ASCII 字元序列，來自
input stream.
輸入串流。
<filespec> Standard DOS file specification
<filespec> 標準 DOS 檔案規格
| seperator for stack parameters and input stream
|堆疊參數和輸入串流的分隔符號
parameters.
參數。


Glossary entries in the alphabetized section are in the following format:
按字母順序排列的區段中的詞彙表項目採用以下格式：


Example:
例：


WORD ( c1 | <string> --- a1 ) FILE_WHERE_FOUND
WORD （ c1 |<string> --- a1 ）FILE_WHERE_FOUND
DESCRIPTIVE_TEXT: The character c1 is passed into WORD on the data
DESCRIPTIVE_TEXT：字元 c1 在資料上傳遞到 WORD 中
stack, <string> is passed to WORD from the input stream, and a1 is
stack， <string> 從輸入流傳遞給 WORD，a1 是
returned by WORD on the data stack.
由資料堆疊上的 WORD 傳回。




---------------------- Operators by Catagory -------------------------
---------------------- 分類運營商 -------------------------


This section contains the list of available word separated into catagory
本節包含按類別劃分的可用單字清單
or use. This section is most useful when you know what you want to do but
或使用。當您知道自己想做什麼但
don't know what the word name is that does the function you want. the
不知道名字這個詞是什麼，可以發揮你想要的功能。這
words of F-PC have been broken into catagories, here is a list of those
F-PC 的詞已被分解為類別，以下是這些類別的列表
catagories:
類別：


Catagory Titles
類別標題


Compiling and Allocation words
編譯和分配字詞
Conditional Test & Compilation words
條件測試和編譯詞
Defining and Related Words
定義詞和相關詞
Dictionary Field Manipulation words
字典欄位操作單字
DOS Interface words
DOS 介面詞
File Manipulation words
檔案操作詞
Math words
數學單字
Memory words for VARIABLES and ARRAYS in CODE space
CODE 空間中 VARIABLES 和 ARRAYS 的記憶體字
Memory words for VALUES
VALUES 的記憶字
Memory Manipulation words for External memory and Ports
外部記憶體和連接埠的記憶體操作字
Menu Building words
菜單構建詞
Mode Control and Associated words
模式控制和關聯字
Number Conversion & Output words
數字轉換和輸出單詞
Printing Related words
列印相關詞彙
Stack Manipulation words
堆疊操作字詞
Status Testing and Error Condition Handling words
狀態測試和錯誤條件處理字
String Manipulation and Output words
字串操作和輸出字
System words
系統詞
Terminal Input & Output words
終端輸入和輸出字
Timing Related words
時機相關詞
Utility words
實用詞
VIEW Manipulation words
VIEW 操作詞
Window Control words
視窗控制單字











Here then is the words contained in each catagory along with their stack
以下是每個類別中包含的單詞及其堆棧
picture. For detailed information on a particular function examine its
圖。如需特定函式的詳細資訊，請檢查其
entry in the alphabetized section.
按字母順序排列的部分中的條目。


Compiling and Allocation words
編譯和分配字詞


ALIGN ( --- )
對齊 （ --- ）
ALLOT ( n1 --- ) ASCII ( | <char> --- c1 )
分配 （ n1 --- ） ASCII （ |<char> --- c1 ）
C, ( c1 --- ) DEFERS ( <name> --- )
C， （ c1 --- ） 延期 （ <name> --- ）
DLITERAL ( d# -- ) DP ( --- a1 )
DLITERAL （ d# -- ） DP （ --- a1 ）
LITERAL ( n1 -- )
字面意思 （ n1 -- ）
X, ( n1 --- ) X," ( | <string>" --- )
X， （ n1 --- ） X，“ （ |<string>“ --- ）
X>"BUF ( --- "BUF ) XC, ( n1 --- )
X>“BUF （ --- ”BUF ） XC， （ n1 --- ）
XDP ( --- a1 ) XDPSEG ( --- a1 )
XDP （ --- a1 ） XDPSEG （ --- a1 ）
XHERE ( --- seg n1 ) Y! ( n1 a1 --- )
XHERE （ --- seg n1 ） Y！（ n1 a1 --- ）
Y, ( n1 --- ) Y@ ( a1 --- n1 )
Y， （ n1 --- ） Y@ （ a1 --- n1 ）
YC! ( n1 a1 --- ) YC@ ( a1 --- n1 )
YC！（ n1 a1 --- ）YC@ （ A1 --- N1 ）
YCOUNT ( a1 --- a2 n1 ) YCSET ( byte a1 --- )
YCOUNT （ a1 --- a2 n1 ） YCSET （ 位元組 a1 --- ）
YDP ( --- a1 ) YHASH ( yname vocaddr --- thread )
YDP （ --- a1 ） YHASH （ yname vocaddr --- thread ）
YHERE ( --- a1 ) YS: ( a1 --- yseg a1 )
YHERE （ --- a1 ） YS： （ a1 --- yseg a1 ）
YSEG ( -- a1 ) YSTART ( --- a1 )
YSEG （ -- a1 ） YSTART （ --- a1 ）
[ ( -- ) ['] ( | <name> -- )
[ ( -- ) ['] ( |<name> -- ）
[COMPILE] ( | <name> -- ) \ ( -- )
[編譯]( |<name> -- ） \ （ -- ）
\S ( n1 --- ) \UNLESS ( | <name> --- )
\S （ n1 --- ） \除非 （ |<name> --- ）
] ( -- ) ` ( command --- )
] （ -- ） ' （ 命令 --- ）


Conditional Test & Compilation words
條件測試和編譯詞


#ELSE ( --- ) #ENDIF ( --- )
#ELSE （ --- ） #ENDIF （ --- ）
#THEN ( --- ) #IF ( f1 --- )
#THEN （ --- ） #IF （ f1 --- ）
+LOOP ( n1 --- ) 0< ( n1 --- f1 )
+循環 （ n1 --- ） 0< （ n1 --- f1 ）
0<= ( n1 --- f1 ) 0<> ( n1 --- f1 )
0<= （ n1 --- f1 ） 0<> （ n1 --- f1 ）
0= ( n1 --- f1 ) 0> ( n1 --- f1 )
0= （ n1 --- f1 ） 0> （ n1 --- f1 ）
0>= ( n1 --- f1 ) < ( n1 n2 --- f1 )
0>= （ n1 --- f1 ） < （ n1 n2 --- f1 ）
<= ( n1 n2 --- f1 ) <> ( n1 n2 --- f1 )
<= （ n1 n2 --- f1 ） <> （ n1 n2 --- f1 ）
= ( n1 n2 --- f1 ) > ( n1 n2 --- f1 )
= （ n1 n2 --- f1 ） > （ n1 n2 --- f1 ）
>= ( n1 n2 --- f1 ) >MARK ( --- a1 )
>= （ n1 n2 --- f1 ） >馬克 （ --- a1 ）
>RESOLVE ( a1 --- ) ?<MARK ( --- f1 a1 )
>解決 （ a1 --- ） ？<MARK （ --- f1 a1 ）
?<RESOLVE ( f1 a1 --- ) ?>MARK ( --- f1 a1 )
?<解決 （ f1 a1 --- ） ？>MARK （ --- f1 a1 ）
?>RESOLVE ( f1 a1 --- ) ?BRANCH ( f1 --- )
？>解決 （ f1 a1 --- ） ？分支 （ f1 --- ）
?DO ( limit start --- ) ?EXIT ( f1 --- )
?DO（限制起始---）？退出 （ f1 --- ）
?LEAVE ( f1 --- ) ?UNTIL ( f1 --- )
?離開 （ f1 --- ） ？直到 （ f1 --- ）
?WHILE ( f1 --- ) AGAIN ( --- )
?而 （ f1 --- ） 再次 （ --- ）
AND ( n1 n2 --- n3 ) BEGIN ( --- )
和 （ n1 n2 --- n3 ） 開始 （ --- ）
BETWEEN ( n1 n2 n3 --- f1 ) BOUNDS ( a1 n1 --- a2 a3 )
之間 （ n1 n2 n3 --- f1 ） 邊界 （ a1 n1 --- a2 a3 ）
BRANCH ( --- ) CASE ( -- )
分支 （ --- ） 案例 （ -- ）
D0= ( d1 --- f1 ) D< ( d1 d2 --- f1 )
D0= （ d1 --- f1 ） D< （ d1 d2 --- f1 ）
D= ( d1 d2 --- f1 ) D> ( d1 d2 --- f1 )
D= （ d1 d2 --- f1 ） D> （ d1 d2 --- f1 ）
DMAX ( d1 d2 --- d3 ) DMIN ( d1 d2 --- d3 )
DMAX （ d1 d2 --- d3 ） DMIN （ d1 d2 --- d3 ）
DNEGATE ( d1 d2 --- d3 ) DO ( limit start -- )
DNEGATE （ d1 d2 --- d3 ） DO （ 限制開始 -- ）
DU< ( d1 d2 --- f1 ) ELSE ( --- )
DU< （ d1 d2 --- f1 ） ELSE （ --- ）
ENDCASE ( -- ) ENDOF ( -- )
尾例 （ -- ） 結尾 （ -- ）
EXIT ( --- ) FALSE ( --- f1 )
退出 （ --- ） 錯誤 （ --- f1 ）
I ( --- n1 ) IF ( f1 -- )
我 （ --- n1 ） 如果 （ f1 -- ）
J ( --- n1 ) LEAVE ( -- )
J （ --- n1 ） 離開 （ -- ）
LOOP ( -- ) NOT ( n1 --- n2 )
循環 （ -- ） 不是 （ n1 --- n2 ）
NRESOLVE ( 0 n1 n2 ... n -- ) OF ( n1 n2 -- n1 ) ( n1 n1 -- )
NRESOLVE （ 0 n1 n2 ...n -- ） 的 （ n1 n2 -- n1 ） （ n1 n1 -- ）
OR ( n1 n2 --- n3 ) RECURSE ( -- )
或 （ n1 n2 --- n3 ） 遞歸 （ -- ）
RECURSIVE ( -- ) immediate REPEAT ( -- )
遞迴 （ -- ） 立即重複 （ -- ）
THEN ( -- ) TRUE ( --- f1 )
那麼 （ -- ） 真 （ --- f1 ）
U< ( n1 n2 --- f1 ) U<= ( un1 un2 --- f1 )
U< （ n1 n2 --- f1 ） U<= （ un1 un2 --- f1 ）
U> ( n1 n2 --- f1 ) U>= ( n1 n2 --- f1 )
U> （ n1 n2 --- f1 ） U>= （ n1 n2 --- f1 ）
UNDO ( --- ) UNNEST ( --- )
撤消 （ --- ） 取消巢 （ --- ）
UNTIL ( f1 -- ) WHILE ( f1 -- )
直到 （ f1 -- ） 而 （ f1 -- ）
WITHIN ( n1 n2 --- f1 ) XOR ( n1 n2 --- n3 )
在 （ n1 n2 --- f1 ） 內 （ n1 n2 --- n3 ）


Defining and Related Words
定義詞和相關詞


2CONSTANT ( d1 | <name> --- ) 2VARIABLE ( | <name> --- )
2 常數 （ d1 |<name> --- ） 2 變數 （ |<name> --- ）
: ( | <name> ... ; --- ) ; ( --- )
: ( |<name> ... ; --- ） ;( --- )
;CODE ( --- ) ;USES ( --- )
;代碼 （ --- ） ;用途 （ --- ）
ALIAS ( a1 | <name> --- ) ANEW ( | <name> --- )
別名 （ a1 |<name> --- ）新 （ |<name> --- ）
CODE ( | <name> --- ) CONSTANT ( n1 | <name> -- )
代碼 （ |<name> --- ）常數 （ n1 |<name> -- ）
CREATE ( | <name> -- ) DEFER ( | <name> -- )
創建 （ |<name> -- ）延遲 （ |<name> -- ）
DEFINED ( -- here 0 | a1 true ) DEFINITIONS ( -- )
定義 （ -- 這裡 0 | a1 true ） 定義 （ -- ）
DOES> ( -- ) EXEC: ( n1 -- )
確實> （ -- ） 執行官： （ n1 -- ）
EXECUTE ( a1 --- ) HEADER ( | <name> -- )
EXECUTE （ a1 --- ） 標頭 （ |<name> -- ）
HIDE ( -- ) IMMEDIATE ( -- )
隱藏 （ -- ） 立即 （ -- ）
IS ( cfa -- ) LABEL ( --- a1 )
IS （ cfa -- ） 標籤 （ --- a1 ）
PERFORM ( a1 --- ) REVEAL ( -- )
執行 （ a1 --- ） 揭示 （ -- ）
VALUE ( n1 | <name> --- ) VARIABLE ( | <name> -- )
值 （ n1 |<name> --- ）可變 （ |<name> -- ）
WIDTH ( --- a1 )
寬度 （ --- a1 ）


Dictionary Field Manipulation words
字典欄位操作單字


.ID ( nfa --- ) >BODY ( cfa --- pfa )
.ID （ nfa --- ） >BODY （ cfa --- pfa ）
>LINK ( cfa --- lfa ) >NAME ( cfa --- nfa )
>鏈接 （ cfa --- lfa ） >名稱 （ cfa --- nfa ）
>VIEW ( cfa --- vfa ) BODY> ( cfa --- cfa )
>視圖 （ CFA --- VFA ） BODY> （ CFA --- CFA ）
L>NAME ( lfa -- nfa ) LINK> ( lfa -- cfa )
L>名稱 （ lfa -- nfa ） 連結> （ lfa -- cfa ）
N>LINK ( nfa -- lfa) NAME> ( nfa -- cfa )
N>LINK （ nfa -- lfa） 名稱> （ nfa -- cfa ）
NAME>PAD ( A1 --- PAD ) TRAVERSE ( a1 direction -- addr' )
NAME>PAD （ A1 --- PAD ） TRAVERSE （ A1 方向 -- 地址' ）
VIEW> ( vfa -- cfa )
視圖> （ vfa -- cfa ）


DOS Interface words
DOS 介面詞


A: ( --- ) B: ( --- )
A：（ --- ） B：（ --- ）
C: ( --- ) ALLOC ( n1 --- n2 n3 n4 )
C：（ --- ） 分配 （ n1 --- n2 n3 n4 ）
CD ( | <filespec> --- )
光碟 （ |<filespec> --- ）
CHDIR ( | <filespec> --- ) COMSPEC$ ( --- a1 )
CHDIR （ |<filespec> --- ）COMSPEC$ （ --- a1 ）
COMSPEC@ ( --- ) COPY ( <filespec> --- )
COMSPEC@ （ --- ） 複製 （ <filespec> --- ）
D: ( --- ) DEALLOC ( n1 --- f1 )
D： （ --- ） DEALLOC （ n1 --- f1 ）
DEL ( <filespec> --- ) DIR ( <filespec> --- )
DEL （ <filespec> --- ） DIR （ <filespec> --- ）
DOS-LINE ( --- a1 ) DOS>TIB ( --- )
DOS-LINE （ --- a1 ） DOS>TIB （ --- ）
DOSVER ( --- n1 ) DRIVE? ( --- n1 )
DOSVER （ --- n1 ） 驅動器？（ --- n1 ）
ENVSIZE ( --- n1 ) EVSEG ( --- n1 )
環境尺寸 （ --- n1 ） EVSEG （ --- n1 ）
FINDFIRST ( string --- f1 ) FINDNEXT ( --- f1 )
FINDFIRST （ 字串 --- f1 ） FINDNEXT （ --- f1 ）
ME$ ( --- a1 ) ME@ ( --- )
ME$ （ --- a1 ） ME@ （ --- ）
PATH$ ( --- a1 ) PATH@ ( --- )
路徑$ （ --- a1 ） PATH@ （ --- ）
PATHHNDL ( --- a1 ) PATHSET ( handle --- f1 )
PATHHNDL （ --- a1 ） PATHSET （ 句柄 --- f1 ）
REN ( <filespec> --- ) RENAME ( | <filespec> --- )
REN （ <filespec> --- ） 重新命名 （ |<filespec> --- ）
SELECT ( n1 --- ) SET-DTA ( a1 --- )
SELECT （ n1 --- ） SET-DTA （ a1 --- ）
SETBLOCK ( seg size --- f1 ) SYS ( | command --- )
SETBLOCK （ seg size --- f1 ） SYS （ | command --- ）


File Manipulation words
檔案操作詞


!HCB ( a1 | <name> --- ) $>HANDLE ( a1 handle --- )
!HCB （ a1 |<name> --- ） $>HANDLE （ a1 手柄 --- ）
$HOPEN ( a1 --- f1 ) $PFILE ( a1 --- f1 )
$HOPEN （ A1 --- F1 ） $PFILE （ A1 --- F1 ）
$FLOAD ( a1 --- f1 ) .CURFILE ( --- )
$FLOAD （ A1 --- F1 ） 。CURFILE （ --- ）
.FILE ( --- ) .FILES ( --- )
.文件 （ --- ） 。檔案 （ --- ）
.LOADED ( --- ) .SEQHANDLE ( --- )
.已加載 （ --- ） 。序列手柄 （ --- ）
>ATTRIB ( handle --- attrib-a1 )
>ATTRIB （ 手柄 --- attrib-a1 ）
>LINE ( n1 --- )
>線路 （ n1 --- ）
>NAM ( handle --- name-string-a1 )
>NAM （ 句柄 --- name-string-a1 ）
>HNDLE ( handle --- handle-a1 )
>HNDLE（手柄---手柄-a1）
?DRIVE.EXTRACT ( handle --- drive-n1 )
?開。EXTRACT （ 手柄 --- drive-n1 ）
?DRIVE.PREPEND ( drive-n1 handle --- )
?開。PREPEND （ drive-n1 手柄 --- ）
?FILEOPEN ( --- )
?檔案開啟 （ --- ）
?PREPEND.VPATH ( a1 --- a1 ) B/HCB ( --- n1 )
?預備。VPATH （ a1 --- a1 ） B/HCB （ --- n1 ）
CHARREAD ( --- c1 ) CLOSE ( --- )
查爾德 （ --- c1 ） 關閉 （ --- ）
CLR-HCB ( a1 --- ) CURPOINTER ( handle --- d1-current )
CLR-HCB （ a1 --- ） CURPOINTER （ 手柄 --- d1-current ）
DEFEXT ( --- a1 )
DEFEXT （ --- a1 ）
ENDFILE ( handle --- double-end )
ENDFILE （ 雙端---處理 ）
EXHREAD ( a1 n1 hndl seg1 --- n2 )
EXHREAD （ a1 n1 hndl seg1 --- n2 ）
EXHWRITE ( a1 n1 hndl seg1 --- )
EXHWRITE （ a1 n1 hndl seg1 --- ）
FCB>HANDLE ( a1 a2 --- ) FILE ( | <name> --- )
FCB>HANDLE （ a1 a2 --- ） 檔案 （ |<name> --- ）
FILE>TIB ( a1 --- ) FILEPOINTER ( --- a1 )
FILE>TIB （ a1 --- ） 檔案指標 （ --- a1 ）
FILES ( --- ) FILLBUFF ( --- )
檔案 （ --- ） FILLBUFF （ --- ）
FILLTIB ( --- ) FL ( | <name> --- )
菲爾蒂布 （ --- ） 佛羅里達州 （ |<name> --- ）
FLHNDL ( --- a1 ) FLOAD ( | <name> --- )
FLHNDL （ --- a1 ） FLOAD （ |<name> --- ）
GET_ALINE ( --- ) GFL ( | <name> --- )
GET_ALINE （ --- ） GFL （ |<name> --- ）
HANDLE ( | <name> --- ) HANDLE>EXT ( a1 --- a2 )
手柄 （ |<name> --- ）手柄>伸線 （ a1 --- a2 ）
HCLOSE ( handle --- f1 ) HCREATE ( handle --- error-code )
HCLOSE （ 處理碼 --- f1 ） HCREATE （ 處理碼 --- 錯誤碼 ）
HDELETE ( handle --- f1 )
HDELETE （ 句柄 --- f1 ）
HNDLS ( --- a1 )
HNDLS （ --- a1 ）
HOPEN ( handle --- error-code )
HOPEN（處理錯誤代碼---）
HREAD ( a1 n1 handle --- n2 )
HREAD（ a1 n1 手柄 --- n2 ）
HRENAME ( handle1 handle2 --- return-code )
HRENAME （ handle1 handle2 --- 回覆碼 ）
HWRITE ( a1 n1 handle --- n2 )
HWRITE （ a1 n1 句柄 --- n2 ）
IBLEN ( --- n1 ) IBRESET ( --- )
IBLEN （ --- n1 ） IBRESET （ --- ）
INCLUDE ( | <name> --- ) LINEREAD ( --- a1 )
包括 （ |<name> --- ）線讀 （ --- a1 ）
LOAD ( n1 --- ) LOADED, ( --- )
負載 （ n1 --- ） 已加載， （ --- ）
LOADER ( --- ) LOADING ( --- a1 )
裝載機 （ --- ） 裝載 （ --- A1 ）
LOADSTAT ( --- ) MOVEPOINTER ( d1-offset handle --- )
LOADSTAT （ --- ） MOVEPOINTER （ d1 偏移控點 --- ）
NEEDS ( | <name> --- ) NEWFILE ( | <name> --- )
需求 （ |<name> --- ）新檔案 （ |<name> --- ）
OBLEN ( --- n1 ) OK ( --- )
OBLEN （ --- n1 ） OK （ --- ）
OPEN ( | <name> --- ) OUTBUF ( --- a1 )
OPEN （ |<name> --- ）OUTBUF （ --- a1 ）
PREPEND.PATH( handle --- f1 ) RWERR ( --- a1 )
預備。PATH（ 句柄 --- f1 ） RWERR （ --- a1 ）
RWMODE ( --- a1 ) SAVEPOINTER ( --- )
RWMODE （ --- a1 ） 保存指標 （ --- ）
SEEK ( d1 --- ) SEQDOWN ( --- )
SEEK （ d1 --- ） 排序 （ --- ）
SEQHANDLE+ ( --- a1 ) SEQHANDLE ( --- a1 )
SEQHANDLE+ （ --- a1 ） SEQHANDLE （ --- a1 ）
SEQUP ( --- )
序列 （ --- ）


Math words
數學單字


* ( n1 n2 --- n3 ) */ ( n1 n2 n3 --- quotient )
* （ n1 n2 --- n3 ） */ （ n1 n2 n3 ---商 ）
*/MOD ( n1 n2 n3 --- n4 n5 )
*/MOD（ n1 n2 n3 --- n4 n5 ）
*D ( n1 n2 --- d1 ) + ( n1 n2 --- n3 )
*D （ n1 n2 --- d1 ） + （ n1 n2 --- n3 ）
/ ( n1 n2 --- n3 ) /MOD ( n1 n2 --- n3 n4 )
/ （ n1 n2 --- n3 ） /MOD （ n1 n2 --- n3 n4 ）
1+ ( n1 --- n2 ) 1- ( n1 --- n2 )
1+ （ n1 --- n2 ） 1- （ n1 --- n2 ）
2* ( n1 --- n2 ) 2+ ( n1 --- n2 )
2* （ n1 --- n2 ） 2+ （ n1 --- n2 ）
2- ( n1 --- n2 ) 2/ ( n1 --- n2 )
2- （ n1 --- n2 ） 2/ （ n1 --- n2 ）
8* ( n1 --- n2 ) D+ ( d1 d2 --- d3 )
8* （ n1 --- n2 ） D+ （ d1 d2 --- d3 ）
D- ( d1 d2 --- d3 ) D2* ( d1 --- d2 )
D- （ d1 d2 --- d3 ） D2* （ d1 --- d2 ）
D2/ ( d1 --- d2 ) DABS ( d1 --- d2 )
D2/ （ d1 --- d2 ） DABS （ d1 --- d2 ）
M/MOD ( d1 n1 --- rem quot ) MAX ( n1 n2 --- n3 )
M/MOD （ d1 n1 --- 對物報價 ） MAX （ n1 n2 --- n3 ）
MIN ( n1 n2 --- n3 ) MOD ( num den -- modulus )
MIN （ n1 n2 --- n3 ） MOD （ num den -- 模數 ）
MU/MOD ( d1 n1 --- rem dquot ) NEGATE ( n1 --- n2 )
MU/MOD （ d1 n1 --- rem dquot ） 否定 （ n1 --- n2 ）
U16/ ( n1 --- n2 ) U2/ ( n1 --- n2 )
U16/ （ n1 --- n2 ） U2/ （ n1 --- n2 ）
UM* ( un1 un2 -- ud ) UM/MOD ( ud un --- urem uquot )
UM* （ un1 un2 -- ud ） UM/MOD （ ud un --- urem uquot ）


Memory words for VARIABLES and ARRAYS in CODE space
CODE 空間中 VARIABLES 和 ARRAYS 的記憶體字


! ( n1 a1 --- ) +! ( n1 a1 --- )
!（ n1 a1 --- ） +！（ n1 a1 --- ）
, ( n1 --- ) - ( n1 n2 --- n3 )
， （ n1 --- ） - （ n1 n2 --- n3 ）
-1! ( a1 --- ) 0! ( a1 --- )
-1!（ a1 --- ） 0！（ A1 --- ）
2! ( d1 a1 --- ) 2+! ( d1 a1 --- )
2!（ d1 a1 --- ） 2+！（ d1 a1 --- ）
2@ ( a1 --- d1 ) @ ( a1 --- n1 )
2@ （ a1 --- d1 ） @ （ a1 --- n1 ）
@L ( seg a1 --- n1 ) @REL>ABS ( cfa --- a1 )
@L （ seg a1 --- n1 ） @REL>ABS （ cfa --- a1 ）
BLANK ( a1 n1 --- ) C! ( c1 a1 --- )
空白 （ a1 n1 --- ） C！（ C1 A1 --- ）
C+! ( c1 a1 --- ) C@ ( a1 --- c1 )
C+！（ C1 A1 --- ）C@ （ A1 --- C1 ）
CAPS-COMP ( a1 a2 n1 --- f1 ) CMOVE ( a1 a2 n1 --- )
CAPS-COMP （ a1 a2 n1 --- f1 ） CMOVE （ a1 a2 n1 --- ）
CMOVE> ( a1 a2 n1 --- ) COMP ( a1 a2 n1 --- f1 )
CMOVE> （ a1 a2 n1 --- ） COMP （ a1 a2 n1 --- f1 ）
COMPARE ( a1 a2 n1 --- f1 ) COUNT ( a1 --- a2 n1 )
比較 （ a1 a2 n1 --- f1 ） 計數 （ a1 --- a2 n1 ）
CRESET ( n1 a1 --- ) CSET ( n1 a1 --- )
CRESET （ n1 a1 --- ） CSET （ n1 a1 --- ）
CTOGGLE ( a1 n1 --- ) DECR ( a1 -- )
CTOGGLE （ a1 n1 --- ） DECR （ a1 -- ）
ERASE ( a1 n1 --- ) EVEN ( -- )
擦除 （ a1 n1 --- ） 偶數 （ -- ）
FILL ( a1 n1 c1 --- ) INCR ( a1 -- )
填充 （ a1 n1 c1 --- ） INCR （ a1 -- ）
LARGEST ( a1 n1 --- a2 n2 ) LENGTH ( a1 --- a2 n1 )
最大 （ a1 n1 --- a2 n2 ） 長度 （ a1 --- a2 n1 ）
MOVE ( a1 a2 n1 --- ) OFF ( a1 --- )
移動 （ a1 a2 n1 --- ） 關閉 （ a1 --- ）
ON ( a1 --- ) SCAN ( a1 n1 c1 --- )
開啟 （ a1 --- ） 掃描 （ a1 n1 c1 --- ）
SCANW ( a1 w1 w2 --- a2 w3 )
掃描 （ a1 w1 w2 --- a2 w3 ）
SEARCH ( sadr slen badr blen -- n1 f1 )
搜尋 （ sadr slen badr blen -- n1 f1 ）
SKIP ( a1 n1 c1 --- )
跳過 （ a1 n1 c1 --- ）
SSEG ( --- a1 ) UPC ( char --- char' )
SSEG （ --- a1 ） UPC （ char --- char' ）
UPPER ( a1 length --- )
鞋面（a1 長度---）


Memory words for VALUES
VALUES 的記憶字


!> ( n1 | <name> --- ) +!> ( n1 | <name> --- )
！> （ n1 |<name> --- ） +！> （ n1 |<name> --- ）
=: ( n1 | <name> --- ) IS ( cfa --- data-address )
=： （ n1 |<name> --- ）IS（ cfa --- 資料位址 ）
@> ( | <name> --- n1 ) DECR> ( | <name> -- )
@> ( |<name> --- n1 ）12 月> （ |<name> -- ）
INCR> ( | <name> -- ) OFF> ( | <name> --- )
增加> （ |<name> -- ）關閉> （ |<name> --- ）
ON> ( | <name> --- )
開啟> （ |<name> --- ）


Memory Manipulation words for External memory and Ports
外部記憶體和連接埠的記憶體操作字


!L ( n1 seg a1 --- )
!L （ n1 seg a1 --- ）
C!L ( c1 seg a1 --- )
C！L （ c1 seg a1 --- ）
CMOVEL ( sseg sptr dseg dptr cnt -- )
CMOVEL （ sseg sptr dseg dptr cnt -- ）
CMOVEL> ( from-seg from-offset to-seg to-offset length --- )
CMOVEL> （ from-seg from-offset to-seg to-offset length --- ）
LFILL ( a1 len value --- )
LFILL （ a1 len 值 --- ）
LFILLW ( seg offset byte-len WORD --- )
LFILLW （ seg offset byte-len WORD --- ）
P! ( n1 port# --- )
P!（ n1 連接埠# --- ）
P@ ( port# -- n1 )
P@ （ 連接埠# -- n1 ）
PARAGRAPH ( offset --- paragraph-in )
PARAGRAPH （ 偏移 --- 段落 ）
PC! ( n1 port# --- )
電腦！（ n1 連接埠# --- ）
PC@ ( port# -- n1 )
PC@ （ 連接埠# -- n1 ）
XALIGN ( --- )
XALIGN （ --- ）
XEVEN ( a1 --- a2 )
XEVEN（ a1 --- a2 ）


Menu Building words
菜單構建詞


ENDMENU ( a1 n1 --- )
結束菜單 （ a1 n1 --- ）
MENU ( --- a1 n1 )
菜單 （ --- a1 n1 ）
MENULINE" ( n1 | <string> <func> --- n1+1 )
菜單線“ （ n1 |<string> <func> --- n1+1 ）
NEWMENU ( | <name> --- )
新菜單 （ |<name> --- ）
NEWMENUBAR ( | <name> --- )
新選單列 （ |<name> --- ）


Mode Control and Associated words
模式控制和關聯字


AUTOEDITOFF ( --- ) AUTOEDITON ( --- )
自動編輯關閉 （ --- ） 自動編輯關閉 （ --- ）
AUTOSAVEOFF ( --- ) AUTOSAVEON ( --- )
自動儲存 （ --- ） 自動儲存 （ --- ）
BACKUPOFF ( --- ) BACKUPON ( --- )
BACKUPOFF （ --- ） BACKUPON （ --- ）
BLANKOFF ( --- ) BLANKON ( --- )
布蘭克 （ --- ） 布蘭肯 （ --- ）
HELPOFF ( --- ) HELPON ( --- )
幫助 （ --- ） 幫助 （ --- ）
HIDELINES ( --- ) INITCOLOR ( --- )
隱藏線 （ --- ） 初始顏色 （ --- ）
INITMONO ( --- ) NOBACKUP ( --- )
初始 （ --- ） 無備份 （ --- ）
RESTORESTATE( --- ) RESTORE_VECTORS ( -- )
RESTORESTATE（ --- ） RESTORE_VECTORS （ -- ）
SAVESTATE ( --- ) SET_VECTORS ( -- )
薩維特 （ --- ） SET_VECTORS （ -- ）
SHOWLINES ( --- ) SRCOFF ( --- )
展線 （ --- ） SRCOFF （ --- ）
SRCON ( --- ) STATOFF ( --- )
SRCON （ --- ） STATOFF （ --- ）
STATON ( --- ) WITHPATH ( --- f1 )
STATON （ --- ） WITHPATH （ --- f1 ）


Number Conversion & Output words
數字轉換和輸出單詞


# ( d1 --- d2 ) #> ( d1 --- a1 n1 )
# （ d1 --- d2 ） #> （ d1 --- a1 n1 ）
#S ( d1 --- d2=0 ) (D.) ( d1 --- a1 n1 )
#S （ d1 --- d2=0 ） （ d.） （ d1 --- a1 n1 ）
(U.) ( n1 --- a1 n2 ) (UD.) ( d1 --- a1 n1 )
（美國。（ n1 --- a1 n2 ）（UD.）（ D1 --- A1 N1 ）
. ( n1 --- ) .R ( n1 n2 --- )
.（ n1 --- ） 。R （ n1 n2 --- ）
<# ( d1 --- d1 ) ? ( a1 --- )
<# （ d1 --- d1 ） ？（ A1 --- ）
BASE ( --- a1 ) CONVERT ( +d1 a1 --- +d2 a2 )
基數 （ --- a1 ） 轉換 （ +d1 a1 --- +d2 a2 ）
D. ( d1 --- ) D.M.Y ( --- )
D. （ d1 --- ） D.M.Y （ --- ）
D.R ( d1 n1 --- ) DECIMAL ( --- )
D.R （ d1 n1 --- ） 小數 （ --- ）
DIGIT ( char base --- n1 f1 ) DOUBLE? ( --- f1 )
數字（字元基--- n1 f1）雙精度？（ --- f1 ）
DPL ( --- a1 ) H. ( u -- )
DPL （ --- a1 ） H. （ u -- ）
HEX ( --- ) HLD ( --- a1 )
十六進制 （ --- ） HLD （ --- a1 ）
HOLD ( c1 --- ) M/D/Y ( --- )
保持 （ C1 --- ） M/D/Y （ --- ）
NUMBER ( a1 --- d1 ) NUMBER? ( a1 --- d1 f1 )
數字 （ a1 --- d1 ） 數字？（ A1 --- D1 F1 ）
OCTAL ( --- ) S>D ( n1 --- d1 )
八角 （ --- ） S>D （ n1 --- d1 ）
SIGN ( n1 --- ) U*D ( n1 n2 --- d1 )
符號 （ n1 --- ） U*D （ n1 n2 --- d1 ）
U. ( n1 --- ) U.R ( n1 n2 --- )
美國 （ n1 --- ） 美國 （ n1 n2 --- ）
UD. ( d1 --- ) UD.R ( d1 n1 --- )
烏德。（ d1 --- ）烏德。R （ d1 n1 --- ）
Y-M-D ( --- )
Y-M-D （ --- ）


Printing Related words
列印相關詞彙


FILEPRINT ( | <name> --- ) FPRINT ( file_specs --- )
檔案列印 （ |<name> --- ）FPRINT （ file_specs --- ）
IBM-PROPRINT ( --- ) PCLOSE ( --- )
IBM-PROPRINT （ --- ） PCLOSE （ --- ）
PDOS ( a1 drive# --- f1 ) PEMIT ( c1 --- )
PDOS （ a1 磁碟機# --- f1 ） PEMIT （ c1 --- ）
PFILE ( | <name> --- ) PR-STATUS ( n1 --- n2 )
PFILE （ |<name> --- ）PR-STATUS （ n1 --- n2 ）
PRINT ( | <command-line> -- ) PRINTING ( --- a1 )
列印 （ |<command-line> -- ）印刷 （ --- a1 ）
PRNHNDL ( --- a1 ) TELETYPE ( --- )
PRNHNDL （ --- a1 ） 電傳打字機 （ --- ）
TOPRINTER ( --- )
TOPRINTER （ --- ）


Stack Manipulation words
堆疊操作字詞


-ROT ( n1 n2 n3 --- n3 n1 n2 )
-腐爛 （ n1 n2 n3 --- n3 n1 n2 ）
.S ( --- )
2>R ( n1 n2 --- )
2>R （ n1 n2 --- ）
2DROP ( d1 --- ) 2DUP ( d1 --- d1 d1 )
2DROP （ d1 --- ） 2DUP （ d1 --- d1 d1 ）
2OVER ( d1 d2 --- d1 d2 d1 ) 2R> ( --- n1 n2 )
2OVER （ d1 d2 --- d1 d2 d1 ） 2R> （ --- n1 n2 ）
2R@ ( --- n1 n2 ) 2ROT ( d1 d2 d3 --- d2 d3 d1 )
2R@ （ --- n1 n2 ） 2ROT （ d1 d2 d3 --- d2 d3 d1 ）
2SWAP ( d1 d2 --- d2 d1 )
2SWAP （ d1 d2 --- d2 d1 ）
3DROP ( n1 n2 n3 --- )
3DROP （ n1 n2 n3 --- ）
3DUP ( n1 n2 n3 --- n1 n2 n3 n1 n2 n3 )
3DUP （ n1 n2 n3 --- n1 n2 n3 n1 n2 n3 ）
4DUP ( d1 d2 --- d1 d2 d1 d2 )
4DUP （ d1 d2 --- d1 d2 d1 d2 ）
>R ( n1 --- )
>R （ n1 --- ）
?DNEGATE ( d1 d2 --- d3 ) ?DUP ( n1 --- n1 n1<>0 | n1=0)
?DNEGATE （ d1 d2 --- d3 ） ？DUP （ n1 --- n1 n1<>0 | n1=0）
?NEGATE ( n1 n2 --- n3 ) ABS ( n1 --- n2 )
?負 （ n1 n2 --- n3 ） ABS （ n1 --- n2 ）
DEPTH ( -- n1 )
深度 （ -- n1 ）
DROP ( n1 --- ) DUP ( n1 --- n1 n1 )
DROP （ n1 --- ） DUP （ n1 --- n1 n1 ）
DUP>R ( n1 --- n1 ) FLIP ( n1 --- n2 )
DUP>R （ n1 --- n1 ） 翻轉 （ n1 --- n2 ）
NIP ( n1 n2 --- n2 ) OVER ( n1 n2 --- n1 n2 n1 )
NIP （ n1 n2 --- n2 ） 超過 （ n1 n2 --- n1 n2 n1 ）
PICK ( n1 --- n2 ) R> ( --- n1 )
選擇 （ n1 --- n2 ） R> （ --- n1 ）
R>DROP ( --- ) R@ ( --- n1 )
R>DROP （ --- ） R@ （ --- n1 ）
RESTORE> ( --- )
恢復> （ --- ）
ROLL ( n1 --- n2 )
滾動 （ n1 --- n2 ）
ROT ( n1 n2 n3 --- n2 n3 n1 )
腐爛 （ n1 n2 n3 --- n2 n3 n1 ）
RP! ( a1 --- )
RP！（ A1 --- ）
RP0 ( --- a1 ) RP@ ( --- a1 )
RP0 （ --- a1 ） RP@ （ --- a1 ）
SAVE!> ( n1 --- ) SAVE> ( --- )
SAVE！> （ n1 --- ） SAVE> （ --- ）
SP! ( a1 --- ) SP0 ( --- a1 )
SP！（ A1 --- ）SP0 （ --- a1 ）
SP@ ( --- a1 ) SPLIT ( n1 --- n2 n3 )
SP@ （ --- a1 ） 分體式 （ n1 --- n2 n3 ）
SWAP ( n1 n2 --- n2 n1 ) TUCK ( n1 n2 --- n2 n1 n2 )
交換 （ n1 n2 --- n2 n1 ） TUCK （ n1 n2 --- n2 n1 n2 ）


Status Testing and Error Condition Handling words
狀態測試和錯誤條件處理字


?COMP ( --- ) ?CONDITION ( f1 --- )
?補償 （ --- ） ？條件 （ f1 --- ）
?CSP ( --- ) ?DOINGMAC ( --- f1 )
?CSP （ --- ） ？DOINGMAC （ --- f1 ）
?DOSIO ( --- f1 ) ?ENOUGH ( n1 --- )
?DOSIO （ --- f1 ） ？夠了 （ n1 --- ）
?ERROR ( a1 n1 f1 --- ) ?EXEC ( --- )
?錯誤 （ a1 n1 f1 --- ） ？執行委員會 （ --- ）
?LOADED ( | <filename> --- ) ?MISSING ( f1 --- )
?已加載 （ |<filename> --- ） ？失蹤 （ f1 --- ）
?STACK ( --- ) ABORT ( --- )
?堆疊 （ --- ） 中止 （ --- ）
ABORT" ( f1 | <message>" --- ) CSP ( --- a1 )
ABORT“ （ f1 |<message>“ --- ）CSP （ --- a1 ）
STATUS ( -- )
狀態 （ -- ）


String Manipulation and Output words
字串操作和輸出字


" ( | <string>" --- ) "" ( | <string>" --- )
" ( |<string>“ --- ）"" ( |<string>“ --- ）
">$ ( a1 n1 --- a2 ) "BUF ( --- a1 )
“>$ （ a1 n1 --- a2 ） ”BUF （ --- a1 ）
"ENVFIND ( a1 n1 --- n2 f1 ) "HEADER ( a1 --- )
“ENVFIND （ a1 n1 --- n2 f1 ） ”標頭 （ a1 --- ）
$>EXT ( a1 n1 a2 --- ) $>HANDLE ( a1 handle --- )
$>EXT （ a1 n1 a2 --- ） $>HANDLE （ a1 句柄 --- ）
$>TIB ( a1 --- ) ," ( | <string> --- )
$>TIB （ a1 --- ） ，“ （ |<string> --- ）
-TRAILING ( a1 n1 --- a2 n2 ) ." ( | <string>" --- )
-尾部 （ a1 n1 --- a2 n2 ） 。」( |<string>“ --- ）
.( ( | <string>) --- )
.( ( |<string>） --- ）
.BOX" ( | <string>" --- )
.盒子」（ |<string>“ --- ）
.COMMENT: ( | ....COMMENT; --- )
.評論：（ | ....註解;--- )
/STRING ( a1 len n1 --- addr' len' )
/STRING （ a1 len n1 --- addr' len' ）
?CR ( --- )
?CR （ --- ）
?LINE ( n1 --- )
?線路 （ n1 --- ）
?PAGE ( --- ) ?UPPERCASE ( a1 --- a1 )
?頁 （ --- ） ？大寫 （ a1 --- a1 ）
COMMENT: ( --- ) PAD ( --- a1 )
評論：（ --- ） PAD （ --- A1 ）
PAGE ( --- ) PARSE ( a1 --- a2 n1 )
頁 （ --- ） 解析 （ a1 --- a2 n1 ）
PLACE ( from count to --- )
PLACE（從計數到---）


System words
系統詞


!CSP ( --- ) !USED ( --- )
!CSP （ --- ） ！二手 （ --- ）
#CODESEGS ( --- n1 ) #HEADSEGS ( --- n1 )
#CODESEGS （ --- n1 ） #HEADSEGS （ --- n1 ）
#LISTSEGS ( --- n1 ) #THREADS ( --- n1 )
#LISTSEGS （ --- n1 ） #THREADS （ --- n1 ）
#TIB ( --- a1 ) #USER ( --- a1 )
#TIB （ --- A1 ） #USER （ --- A1 ）
#VOCS ( --- a1 ) ' ( | <name> --- cfa )
#VOCS （ --- a1 ） ' （ |<name> --- CFA ）
'DOCOL ( --- a1 ) 'TIB ( --- a1 )
'DOCOL （ --- a1 ） 'TIB （ --- a1 ）
'WORD ( --- a1 )
'WORD （ --- a1 ）
( ( --- )
(FIND) ( here lfa --- cfa flag | here flase )
（尋找）（這裡是 lfa --- CFA 旗幟 | 這裡是 flase ）
(FRGET) ( code-addr relative-link-addr --- )
（弗吉特）（ 代碼-地址 relative-link-addr --- ）
,CALL ( --- )
，呼叫 （ --- ）
,JUMP ( --- )
，跳躍 （ --- ）
,VIEW ( --- ) .COMPSTAT ( --- )
，視圖 （ --- ） 。康普斯塔特 （ --- ）
.COMSPEC ( --- ) .DATE ( --- )
.COMSPEC （ --- ） 。日期 （ --- ）
.ELAPSED ( --- ) .ENV ( --- )
.已消逝 （ --- ） 。環境 （ --- ）
.FREE ( --- ) .HELLO ( --- )
.免費 （ --- ） 。您好 （ --- ）
.ME ( --- ) .PATH ( --- )
.我 （ --- ） 。路徑 （ --- ）
.STATUS ( --- ) .TIME ( --- )
.狀態 （ --- ） 。時間 （ --- ）
.USED ( --- ) .VOCWORDS ( --- )
.二手 （ --- ） 。VOCWORDS （ --- ）
/* ( | ... */ --- ) 0COMPILER ( --- )
/* （ | ... */ --- ） 0編譯器 （ --- ）
>NEST ( --- a1 ) >NEXT ( --- a1 )
>內側 （ --- a1 ） >下一個 （ --- a1 ）
>PRE ( --- ) ?CS: ( --- seg )
>PRE （ --- ） ？CS： （ --- seg ）
?ES: ( --- seg ) ?FILLBUFF ( --- )
？ES：（ --- seg ） ？填充增益 （ --- ）
?VMODE ( --- ) A; ( --- )
?VMODE （ --- ） A;( --- )
ADEBUG ( a1 --- ) ASSEMBLER ( --- )
ADEBUG （ a1 --- ） 彙編器 （ --- ）
ATBL ( --- a1 ) AUTOSAVE-MINUTES ( --- n1 )
ATBL （ --- a1 ） 自動儲存分鐘 （ --- n1 ）
BDOS ( n1 func# --- a1 ) BGSTUFF ( --- )
BDOS （ n1 func# --- a1 ） BGSTUFF （ --- ）
BOOT ( --- ) BUG ( --- )
啟動 （ --- ） 錯誤 （ --- ）
BYE ( --- ) BYTFUNC ( --- )
再見 （ --- ） BYTFUNC （ --- ）
CNHASH ( cfa -- ya ) CNSRCH ( cfa ya maxya -- nfa failf )
CNHASH （ cfa -- ya ） CNSRCH （ cfa ya maxya -- nfa failf ）
CNT ( --- a1 ) COLD ( -- )
碳納米管 （ --- a1 ） 冷 （ -- ）
COMPILE ( | <name> -- ) CONHNDL ( --- a1 )
編譯 （ |<name> -- ）CONHNDL （ --- a1 ）
CONTEXT ( --- a1 ) CONTROL ( <char> -- n1 )
上下文 （ --- a1 ） 控制 （ <char> -- n1 ）
CRASH ( -- ) CURRENT ( --- a1 )
崩潰 （ -- ） 電流 （ --- a1 ）
DBG ( | <name> --- ) DEFAULT ( --- )
DBG （ |<name> --- ）預設 （ --- ）
DEFAULTSTATE( --- ) DIV0FUNC ( -- )
DEFAULTSTATE（ --- ） DIV0FUNC （ -- ）
DIV0STRT ( -- )
DIV0STRT （ -- ）
DIVIDE0 ( status_reg CS IP AX BX CX DX SI BP -- )
DIVIDE0 （ status_reg CS IP AX BX CX DX SI BP -- ）
DLN ( a1 --- )
DLN （ a1 --- ）
DONE? ( n1 -- f1 ) EDITOR ( --- )
熟？（ n1 -- f1 ）編輯 （ --- ）
EMIT. ( char -- ) END? ( --- a1 )
發。（ char -- ）端？（ --- A1 ）
ENTRY ( --- a1 ) ES0 ( --- a1 )
入口 （ --- a1 ） ES0 （ --- a1 ）
EXEHCB ( --- a1 ) FIRST ( --- a1 )
EXEHCB （ --- a1 ） 第一 （ --- a1 ）
FORTH ( --- ) FUDGE ( --- a1 )
第四 （ --- ） 軟糖 （ --- a1 ）
GO ( a1 --- ) HASH ( str-addr voc-ptr -- thread )
GO （ a1 --- ） HASH （ str-addr voc-ptr -- 執行緒 ）
HDEFAULT ( -- )
HDEFAULT （ -- ）
HDOS1 ( cx dx fun -- ax cf | err-code 1 )
HDOS1 （ cx dx fun -- ax cf | 錯誤代碼 1 ）
HERE ( --- a1 )
這裡（--- A1 ）
HIDDEN ( --- )
隱藏 （ --- ）
INITSTUFF ( --- ) INSTALLSTUFF( --- )
初始內容 （ --- ） 安裝內容 （ --- ）
INTERPRET ( -- ) LAST ( --- a1 )
解釋 （ -- ） 最後 （ --- a1 ）
LIMIT ( --- a1 ) LINK ( --- a1 )
限制 （ --- a1 ） 連結 （ --- a1 ）
MAKEDUMMY ( | <name> -- ) MAX.S ( --- a1 )
MAKEDUMMY （ |<name> -- ）最大。S （ --- a1 ）
MAXNEST ( --- n1 ) MEMCHK ( f1 --- )
MAXNEST （ --- n1 ） MEMCHK （ f1 --- ）
NO-NAME ( --- ) NOOP ( --- )
無名 （ --- ） NOOP （ --- ）
OSF ( --- a1 ) OUTPAUSE ( --- )
OSF （ --- a1 ） 暫停 （ --- ）
PAUSE ( --- ) PAUSE-FUNC ( --- )
暫停 （ --- ） 暫停功能 （ --- ）
PRE> ( --- ) PRIOR ( --- a1 )
前> （ --- ） 先驗 （ --- a1 ）
ROOT ( --- ) RUN ( --- )
根 （ --- ） 運行 （ --- ）
SEGSET ( --- ) SEQINIT ( --- )
SEGSET （ --- ） SEQINIT （ --- ）
SETTIB ( a1 --- ) SETYSEG ( --- )
SETTIB （ a1 --- ） SETYSEG （ --- ）
SOURCE ( --- a1 n1 ) SOURCE-PARSE-WRD ( C1 --- A1 N1 )
來源 （ --- A1 n1 ） 來源解析-WRD （ C1 --- A1 N1 ）
START ( --- ) STATE ( --- a1 )
啟動 （ --- ） 狀態 （ --- a1 ）
SVINIT ( --- ) SVSEG ( --- seg1 )
SVINIT （ --- ） SVSEG （ --- seg1 ）
TOS ( --- a1 ) TOTALWORDS ( --- a1 )
TOS （ --- a1 ） 總字數 （ --- a1 ）
TRIM ( faddr voc-addr -- ) UNBUG ( -- )
修剪 （ faddr voc-addr -- ） UNBUG （ -- ）
UNINSTALLSTUFF ( --- ) UP ( --- a1 )
UNINSTALLSTUFF （ --- ） UP （ --- a1 ）
USER ( --- ) VMODE-VAR ( --- a1 )
用戶 （ --- ） VMODE-VAR （ --- a1 ）
VMODE.SET ( --- ) VOC-LINK ( --- a1 )
VMODE。設置 （ --- ） VOC-LINK （ --- A1 ）
VOCABULARY ( | <name> -- ) W.NAME ( NFA --- )
詞彙 （ |<name> -- ）W.NAME （ NFA --- ）
WARM ( -- ) WARNING ( --- a1 )
溫暖 （ -- ） 警告 （ --- a1 ）
WORD ( C1 --- A1 ) XSEG ( --- a1 )
WORD （ C1 --- A1 ） XSEG （ --- A1 ）


Terminal Input & Output words
終端輸入和輸出字


#LINE ( --- a1 ) #OUT ( --- a1 )
#LINE （ --- A1 ） #OUT （ --- A1 ）
#PAGE ( --- a1 ) (EMIT) ( c1 --- )
#PAGE （ --- a1 ） （ 發射） （ c1 --- ）
(EXPECT) ( a1 n1 --- ) (KEY) ( --- c1 )
（預期）（ A1 N1 --- ）（關鍵）（ --- c1 ）
(KEY?) ( --- f1 ) -LINE ( --- )
（關鍵？（ --- f1 ） -線 （ --- ）
-TAB ( --- ) >ATTRIB1-8 ( --- )
-TAB （ --- ） >ATTRIB1-8 （ --- ）
>BG ( n1 --- ) >BOLD ( --- )
>BG （ n1 --- ） >粗體 （ --- ）
>BOLDBLNK ( --- ) >BOLDUL ( --- )
>BOLDBLNK （ --- --->）
>BUGN ( --- ) >BUWT ( --- )
>布恩 （ --- ） >布特 （ --- ）
>COLOR ( --- ) >FG ( n1 --- )
>顏色 （ --- ） >FG （ n1 --- ）
>IBM ( --- ) >IN ( --- a1 )
>IBM （ --- ） >IN （ --- a1 ）
>LCD ( --- ) >MONO ( --- )
>LCD （ --- ） >單聲道 （ --- ）
>NONE ( --- ) >NORM ( --- )
>無 （ --- ） >規範 （ --- ）
>RDWT ( --- ) >REV ( --- )
>RDWT （ --- ） >REV （ --- ）
>REVBLNK ( --- ) >TYPE ( a1 n1 --- )
>REVBLNK （ --- ） >類型 （ a1 n1 --- ）
>UL ( --- ) ?DARK ( --- )
>UL （ --- ） ？深色 （ --- ）
?KEYPAUSE ( --- ) ?PRINTER.READY ( --- f1 )
?按鍵暫停 （ --- ） ？印刷者。就緒 （ --- f1 ）
AT ( col row --- ) ATTRIB ( --- a1 )
AT （ 列行 --- ） ATTRIB （ --- a1 ）
BACKSPACES ( n1 --- ) BEEP ( --- )
退格鍵 （ n1 --- ） 嗶聲 （ --- ）
BELL ( --- c1 ) BIG-CURSOR ( --- )
鈴鐺 （ --- c1 ） 大紅旗 （ --- ）
BIOSCHAR ( --- a1 ) BIOSKEY ( --- n1 )
BIOSCHAR （ --- a1 ） BIOSKEY （ --- n1 ）
BIOSKEY? ( --- f1 ) BIOSKEYVAL ( --- a1 )
生物鍵？（ --- f1 ）BIOSKEYVAL （ --- a1 ）
BL ( --- c1 ) BLACK ( --- n1 )
BL （ --- c1 ） 黑色 （ --- n1 ）
BLACK-ON-WHITE ( --- ) BLUE ( --- n1 )
白底黑字 （ --- ） 藍色 （ --- N1 ）
BROWN ( --- n1 ) BS ( --- c1 )
布朗 （ --- n1 ） 學士 （ --- c1 ）
CLS ( --- ) COLS ( --- n1 )
CLS （ --- ） COLS （ --- n1 ）
CONSOLE ( c1 --- ) CR ( --- )
控制台 （ c1 --- ） CR （ --- ）
CRLF ( --- ) CROWS ( --- n1 )
CRLF （ --- ） 烏鴉 （ --- n1 ）
CRTAB ( --- ) CURSOR-ON ( --- )
CRTAB （ --- ） CURSOR-ON （ --- ）
CURSOR-OFF ( --- ) CYAN ( --- n1 )
CURSOR-OFF （ --- ） 青色 （ --- n1 ）
DARK ( --- ) DKGRAY ( --- n1 )
黑暗 （ --- ） DKGRAY （ --- n1 ）
DTBUF ( --- a1 ) EEOL ( --- )
DTBUF （ --- a1 ） EEOL （ --- ）
EMIT ( c1 -- ) EXPECT ( a1 n1 --- )
發出 （ c1 -- ） 預期 （ a1 n1 --- ）
EXTYPE ( seg a1 n1 --- ) FEMIT ( c1 --- )
EXTYPE （ seg a1 n1 --- ） FEMIT （ c1 --- ）
FORM-FEED ( --- ) GET-CURSOR ( --- SHAPE )
FORM-FEED （ --- ） GET-CURSOR （ --- 形狀 ）
GREEN ( --- n1 ) IBM--LINE ( -- )
綠色 （ --- n1 ） IBM--線 （ -- ）
IBM-AT ( col row -- ) IBM-AT? ( --- col row )
IBM-AT （ 列行 -- ） IBM-AT？（ 列行--- ）
KEY ( --- c1 ) KEY? ( --- f1 )
鑰匙（---c1）鑰匙？（ --- f1 ）
LDUMP ( seg offset len --- ) LMARGIN ( -- a1 )
LDUMP （ seg 偏移 len --- ） LMARGIN （ -- a1 ）
LTBLUE ( --- n1 ) LTCYAN ( --- n1 )
LTBLUE （ --- n1 ） LTCYAN （ --- n1 ）
LTGRAY ( --- n1 ) LTGREEN ( --- n1 )
LTGRAY （ --- n1 ） LTGREEN （ --- n1 ）
LTMAGENTA ( --- n1 ) LTRED ( --- n1 )
LTMAGENTA （ --- n1 ） LTRED （ --- n1 ）
MAGENTA ( --- n1 ) MED-CURSOR ( --- )
洋紅色 （ --- n1 ） MED-CURSOR （ --- ）
NORM-CURSOR ( --- ) QTYPE ( A1 N1 --- )
NORM-CURSOR （ --- ） QTYPE （ A1 N1 --- ）
QUERY ( --- ) RED ( --- n1 )
查詢 （ --- ） 紅色 （ --- n1 ）
RMARGIN ( -- a1 ) ROWS ( --- n1 )
RMARGIN （ -- a1 ） 列 （ --- n1 ）
SET-CURSOR ( N1 --- ) SLOW ( --- )
SET-CURSOR （ N1 --- ） 慢速 （ --- ）
SPACE ( --- ) SPACES ( n1 --- )
空格 （ --- ） 空格 （ n1 --- ）
SPAN ( --- a1 ) SPCS ( --- a1 )
跨度 （ --- a1 ） SPCS （ --- a1 ）
TAB ( -- ) TABSIZE ( --- a1 )
TAB （ -- ） TABSIZE （ --- a1 ）
TIB ( --- a1 ) TILLKEY ( n1 --- )
TIB （ --- a1 ） TILLKEY （ n1 --- ）
TYPE ( a1 n1 --- ) TYPESEG ( --- a1 )
類型 （ a1 n1 --- ） 類型例如 （ --- a1 ）
VIDEO-SEG ( --- a1 ) VIDEO-TYPE ( a1 n1 --- )
視訊格式 （ --- a1 ） 視訊類型 （ a1 n1 --- ）
WHITE ( --- n1 ) WHITE-ON-BLACK ( --- )
白色 （ --- n1 ） 黑底白字 （ --- ）
YELLOW ( --- n1 )
黃色 （ --- n1 ）


Timing Related words
時機相關詞


10TH-ELAPSED ( --- n1 ) B>SEC ( d1 --- n1 )
10TH-ELAPSED （ --- n1 ） B>SEC （ d1 --- n1 ）
B>T ( d1 --- d2 ) FORM-DATE ( d1 --- a1 )
B>T （ d1 --- d2 ） 表格日期 （ d1 --- a1 ）
FORM-TIME ( d1 --- a1 ) GETDATE ( --- Y MD )
FORM-TIME （ d1 --- a1 ） GETDATE （ --- Y MD ）
GETTIME ( --- HM Sh ) HOURS ( N1 --- )
GETTIME （ --- HM Sh ） 小時 （ N1 --- ）
MINUTES ( N1 --- ) MS ( n1 --- )
分鐘 （ N1 --- ） MS （ n1 --- ）
SEC-ELAPSED ( --- N1 ) SECONDS ( N1 --- )
秒耗盡 （ --- N1 ） 秒 （ N1 --- ）
SETDATE ( NM Y --- ) SETTIME ( HM Sh --- )
SETDATE （ NM Y --- ） SETTIME （ HM Sh --- ）
STIME ( --- a1 ) T>B ( d1 --- d2 )
STIME （ --- a1 ） T>B （ d1 --- d2 ）
TENTHS ( N1 --- ) TIME-ELAPSED( --- d1 )
十分之一 （ N1 --- ） 時間耗盡 （ --- d1 ）
TIME-RESET ( --- ) TIMER ( | forth_commands --- )
時間重置 （ --- ） 定時器 （ | forth_commands --- ）
TTIME ( --- a1 )
TTIME （ --- a1 ）


Utility words
實用詞


DEBUG ( | <name> --- ) DEBUGABLE ( --- )
偵錯 （ |<name> --- ）可調試 （ --- ）
DLN ( a1 --- ) DONE ( --- )
DLN （ a1 --- ） 完成 （ --- ）
DU ( a1 -- addr+64 ) DUMP ( a1 len -- )
DU （ a1 -- addr+64 ） 轉儲 （ a1 len -- ）
ED ( --- ) EDIT ( n1 --- )
ED （ --- ） 編輯 （ n1 --- ）
EMPTY ( --- ) FALLOF ( func | fl_specs --- )
空 （ --- ） FALLOF （ func | fl_specs --- ）
FAST ( --- ) FENCE ( --- a1 )
快速 （ --- ） 圍欄 （ --- a1 ）
FIND ( a1 -- cfa flag | a1 false )
查找 （ a1 -- cfa 標誌 | a1 false ）
FLOOK ( | <string> <fl_specs> --- )
FLOOK （ |<string> <fl_specs> --- ）
FORGET ( | <name> -- )
忘記 （ |<name> -- ）
FSAVE ( | <name> --- ) INDEX ( file_spec --- )
FSAVE （ |<name> --- ）目錄 （ file_spec --- ）
INLINE ( --- ) INSTALL ( --- )
內聯 （ --- ） 安裝 （ --- ）
LINEEDITOR ( x y a1 n1 --- f1 ) LISTING ( --- )
LINEEDITOR （ x y a1 n1 --- f1 ） 列表 （ --- ）
MANY ( -- ) MARK ( | <name> -- )
許多 （ -- ） 馬克 （ |<name> -- ）
POSTFIX ( --- ) PREFIX ( --- )
前綴 （ --- ） 前綴 （ --- ）
QUIT ( -- ) REF ( | <name> --- )
退出 （ -- ） REF （ |<name> --- ）
REPAIR ( | <name> --- ) SAVE-EXE ( | <name> --- )
維修 （ |<name> --- ）保存-EXE （ |<name> --- ）
SED ( | filename --- ) SEE ( <name> --- )
SED （ | 檔案名稱 --- ） 參見 （ <name> --- ）
THESE ( --- ) TIMES ( N1 -- )
這些 （ --- ） 次 （ N1 -- ）
TOTALLINES ( --- a1 ) TURNKEY ( | <name> --- )
TOTALLINES （ --- a1 ） 交鑰匙 （ |<name> --- ）
UNDEFER ( | <name> -- ) UNEDIT ( --- )
UNDEFER （ |<name> -- ）取消編輯 （ --- ）
UNINSTALL ( --- ) USED ( | <command_line> --- )
解除安裝 （ --- ） 已使用 （ |<command_line> --- ）
USEDIN ( | <name> --- ) WORDS ( | <text> <text> -- )
使用於 （ |<name> --- ）文字 （ |<text> <text> -- ）
XDUMP ( a1 n1 --- ) XREF ( | <name> --- )
XDUMP （ a1 n1 --- ） XREF （ |<name> --- ）
YDUMP ( A1 N1 --- )
YDUMP （ A1 N1 --- ）


VIEW Manipulation words
VIEW 操作詞


+LINES ( n1 --- ) -1LINE ( --- )
+行 （ n1 --- ） -1 行 （ --- ）
-LINES ( n1 --- ) >VIEWFILE ( cfa --- offset a1 )
-LINES （ n1 --- ） >VIEWFILE （ cfa --- 偏移量 a1 ）
>VIEWLINE ( n1 --- ) B ( --- )
>視線 （ n1 --- ） B （ --- ）
HELLO ( --- ) HELP ( | <name> --- )
您好 （ --- ） 幫助 （ |<name> --- ）
HELPVIEW ( | <name> --- ) L ( --- )
幫助視圖 （ |<name> --- ）L ( --- )
LIST ( n1 --- ) LL ( | <name> --- )
清單 （ n1 --- ） LL （ |<name> --- ）
N ( --- ) SETVIEW ( | <path> --- )
N （ --- ） SETVIEW （ |<path> --- ）
VIEW ( | <name> --- ) VIEWLINES ( n1 n2 --- )
查看 （ |<name> --- ）視線 （ n1 n2 --- ）
VIEWPATH ( --- a1 )
檢視路徑 （ --- a1 ）


Window Control words
視窗控制單字


BCR ( --- )
BCR （ --- ）
BOX ( left top right bottom --- )
BOX（左上右下---）
BOX&FILL ( left top right bottom --- )
BOX&FILL（左上右下---）
RECOVERLINE ( n1 --- )
恢復線 （ n1 --- ）
RECOVERSCR ( --- )
恢復 （ --- ）
RESTSCR ( --- )
RESTSCR （ --- ）
SAVESCR ( --- )
SAVESCR （ --- ）











-------------------- Function Glossary Aplphabetic -------------------
-------------------- 功能詞彙表 Aplphabetic -------------------


! ( n1 a1 --- ) KERNEL1
!（ n1 a1 --- ）KERNEL1
Store a 16 bit value N1 into the address a1 in the CODE
將 16 位值 N1 儲存到 CODE 中的位址 a1 中
segment.
瓣。


!> ( n1 | <name> -- ) EQUCOLON
！> （ n1 |<name> -- ）埃科隆
Store the value n1 on the stack into the body field of <name>.
將堆疊上的值 n1 儲存到 的 body 欄位中 <name>。
Typically used to modify a VALUE or VARIABLE. May be used on
通常用來修改 VALUE 或 VARIABLE。可用於
the command line. Used in the form: 10 !> XX where XX is a
命令列。以以下形式使用：10 ！> XX 其中 XX 是
VALUE or VARIABLE.
VALUE 或 VARIABLE 的 VALUE 或 VARIABLE。


!CSP ( -- ) KERNEL3
!CSP （ -- ） KERNEL3
Save the current stack level for later error checking by ?CSP.
儲存目前的堆疊層級，以便稍後透過？CSP。


!HCB ( a1 | <name> --- ) HANDLES
!HCB （ a1 |<name> --- ）手柄
Get <name> from the input stream and move it into the handle
<name> 從輸入資料流程取得，並將其移至控制碼中
a1.
答：1.


!L ( n1 seg a1 -- ) KERNEL2
!L （ n1 seg a1 -- ） KERNEL2
Store the 16 bit value N1 into the FAR address specified by SEG
將 16 位值 N1 存儲到 SEG 指定的 FAR 地址中
and ADDR.
和 ADDR。


!USED ( --- ) UTILS
!已使用 （ --- ） UTILS
Stores away the current values of the various segments in F-PC
存儲 F-PC 中各個段的當前值
for later comparison with the same values after a compile.
以便稍後在編譯後與相同值進行比較。
Used to determine dictionary space usage.
用來判斷字典空間使用情況。


" ( | <string>" -- ) compile time KERNEL3
" ( |<string>“ -- ） 編譯時間 KERNEL3
( --- a1 n1 ) runtime
（ --- a1 n1 ） 執行階段
Compile <string> terminated by a ", into CODE space. Return the
將<string>以 “ 結尾的編譯為 CODE 空間。傳回
address and length of the string at runtime.
執行階段字串的位址和長度。


"" ( | <string>" -- ) compile time KERNEL3
"" ( |<string>“ -- ） 編譯時間 KERNEL3
( --- a1 n1 ) runtime
（ --- a1 n1 ） 執行階段
Compile <string> terminated by a ", into LIST space. The
將<string>以 “ 結尾的編譯為 LIST 空間。這
string is moved into a CODE space buffer at runtime, the
string 在執行階段移至 CODE 空間緩衝區，則
address and length of the buffer are subsequently returned.
緩衝區的位址和長度隨後會傳回。
Only a single buffer is used for these strings, so each ""
這些字串只會使用單一緩衝區，因此每個「”
string must be used before the next "" string is executed.
string 必須在執行下一個 “” 字串之前使用。


"+ ( a1 n1 -- ) TIMER
“+ （ a1 n1 -- ） 計時器
Append string a1,n1 to the date/time buffer DTBUF ;
將字串 a1，n1 附加至日期/時間緩衝區 DTBUF ;


".ERRMSG ( a1 n1 -- ) SEDSHELL
".ERRMSG （ a1 n1 -- ） SEDSHELL
Display mesage a1,n1 in a 32 character wide box and wait for
在 32 個字元寬的方塊中顯示訊息 a1，n1 並等待
a key to be pressed.
一個要按下的鍵。


">$ ( a1 len -- a2 ) KERNEL3
“>$ （ a1 len -- a2 ） KERNEL3
Convert address a1 and length len of a string created with "
轉換使用”
into a counted string address a2. This word relys on the fact
轉換為計數字串位址 a2。這個詞依賴於事實
that " really creates counted strings, but converts them to
該“確實創建了計數字符串，但將它們轉換為
address and length on execution.
地址和執行時的長度。


"BUF ( --- a1 ) KERNEL3
“BUF （ --- a1 ） KERNEL3
The buffer that is used when returning a "" string at runtime.
在執行階段傳回 “” 字串時所使用的緩衝區。
See also the "" definition above.
另請參閱上面的“”定義。


"CREATE ( a1 -- ) KERNEL3
“CREATE （ a1 -- ） KERNEL3
Create a definition in the dictionary from the counted string a1.
從計數字串 a1 在字典中建立定義。
The definition will behave like CREATEed definitions.
定義的行為類似於 CREATE 定義。


"EMIT ( -- ) PERTYPE
“發出 （ -- ） PERTYPE
Emit a " character to the screen using the fast FEMIT word.
使用快速 FEMIT 單字向螢幕發出「字元」。


"ENVFIND ( a1 n1 --- n2 f1 ) ENVIRON
“ENVFIND （ a1 n1 --- n2 f1 ） 環境
Search the environment for the string specified by a1, n1 where
在環境中搜尋 a1、n1 所指定的字串，其中
A1 is the address of the first character to find, and N1 is the
A1 是第一個要找到的字元的位址，N1 是
length of the string being searched for. Return a boolean flag
所搜尋字串的長度。傳回布林旗標
TRUE if found, and N2 the offset into the environment where the
TRUE 如果找到，則 N2 偏移到環境中，其中
match occured.
匹配發生。


"HEADER ( a1 --- ) KERNEL3
“標題 （ a1 --- ） KERNEL3
Use the string specified by a1 to make a header, and initialize
使用 a1 指定的字串做標頭，並初始化
the code field. First we check for duplicates. Then we make
代碼欄位。首先，我們檢查重複項。然後我們讓
entry in >NAME hash table if appropriate. Next lay down the
如果適用，則在>NAME 雜湊表中輸入條目。接下來，放下
view field. Then we hook in to the correct thread an make the
檢視欄位。然後我們掛接正確的線程，使
link field. We set up LAST so that it points to our name
link 欄位。我們設定了 LAST，以便它指向我們的名字
field. Then we copy the name to YSEG and delimit the name
田。然後我們將名稱複製到 YSEG 並分隔名稱
field bits. Then we make the pointer in the YSEG to the CFA.
字段位。然後我們在 YSEG 中將指標指向 CFA。
Then we add a stopper entry to >NAME hash table in case of a
然後我們在 >NAME 雜湊表中新增一個終止符條目，以防出現
large ALLOT or end of dictionary. All of the work is done in
大 ALLOT 或字典末尾。所有的工作都在
HEAD space, "HEADER has no effect on CODE space whatsoever.
HEAD 空間，“HEADER 對 CODE 空間沒有任何影響。


"SYSCOMMAND ( a1 n1 c1 -- ) EXEC
“SYSCOMMAND （ a1 n1 c1 -- ） 執行
Pass the string a1,n1 to DOS with the Forth line following the
將字串 a1，n1 傳遞給 DOS，第四行後面的
command up to character c1 appended to string a1,n1.
命令，最多字符 C1 附加到字符串 A1，N1。


# ( d1 --- d2 ) KERNEL2
# （ d1 --- d2 ） KERNEL2
Convert a single digit of D1 into the number conversion buffer
將 D1 的個位數轉換為數字轉換緩衝區
below PAD in the current base. Return D2 the remainder for
低於當前基礎的 PAD。傳回 D2 的剩餘數
further conversion.
進一步轉換。


##+ ( n1 -- ) TIMER
##+ （ n1 -- ） 計時器
Append the two lower digits of n1 in the current base to DTBUF.
將當前基數中 n1 的兩個小數字附加到 DTBUF。


#> ( d1 --- a1 len ) KERNEL2
#> （ d1 --- a1 len ） KERNEL2
Complete the numeric conversion of D1, discarding the double
完成 D1 的數字轉換，丟棄雙精度
ZERO and returning the address and count of the converted
ZERO 並傳回轉換後的位址和計數
string located below PAD.
位於 PAD 下方的字串。


#CODESEGS ( --- n1 ) KERNEL2
#CODESEGS （ --- n1 ） KERNEL2
A VALUE which returns the number of 16 byte segments assigned
傳回指派的 16 位元組區段數目的 VALUE
to be used for CODE (assembly language), CONSTANTS and
用於 CODE（彙編語言）、CONSTANTS 和
VARIABLES. Limited to 64k, which is the value 4096 decimal.
變數。限制為 64k，即十進制後 4096 的值。


#DIRSEGS ( -- n1 ) WFL HIDDEN
#DIRSEGS （ -- n1 ） WFL 隱藏
A constant that returns the number of segments (16 byte
傳回區段數目的常數 （16 位元組
paragraphs) allocated to the directory save buffer.
段落）分配給目錄儲存緩衝區。


#ELSE ( --- ) COMMENT
#ELSE （ --- ） 評論
The optional ELSE portion of an interpreted conditional
解譯條件的選擇性 ELSE 部分
structure started with #IF, and completed with #THEN. See
結構始於 #IF，完成於 #THEN。看
also #IF.
也 #IF。


#EMPTY ( -- n1 ) DECOM HIDDEN
#EMPTY （ -- n1 ） DECOM 隱藏
An internal word used by the decompiler. It allows the decompiler
反編譯器使用的內部單字。它允許反編譯器
to know how many blank lines are between the word being
知道單詞之間有多少行空行
decompiled, and the split screen line. Used to know when to
反編譯，以及分割畫面行。以前知道什麼時候
scroll the decompilers lines.
捲動反編譯器行。


#ENDIF
#THEN ( --- ) COMMENT
#THEN （ --- ） 評論
Ends a multi-line Compiler directive. See #IF.
結束多行編譯器指示詞。參見 #IF。


#FLS ( -- n1 ) WFL HIDDEN
#FLS （ -- n1 ） WFL 隱藏
A VALUE that holds the number of directory entries read when the
一個 VALUE，它保存了在
pop up file selection tool is used.
彈出式檔案選擇工具。


#HEADSEGS ( --- n1 ) KERNEL2
#HEADSEGS （ --- n1 ） KERNEL2
A VALUE which returns the number of 16 byte segments assigned
傳回指派的 16 位元組區段數目的 VALUE
to be used for Forth HEADERS. Limited to 64k, which is the
用於 Forth HEADERS。限制為 64k，這是
value 4096 decimal.
值 4096 小數點。


#IF ( f1 --- ) COMMENT
#IF （ f1 --- ） 評論
Starts a multi-line compiler directive. If the boolean passed
啟動多行編譯器指引。如果布林值通過
to #IF is true, then the lines following #IF will be executed.
如果 #IF 為 true，則將執行 #IF 後面的行。
If the boolean is false, then the lines following #IF up to the
如果布林值為 false，則後面的行 #IF 到
#ENDIF or #THEN, will be ignored. An optional #ELSE may be
#ENDIF 或 #THEN，將被忽略。可選 #ELSE 可能是
inserted after #IF, and before #THEN. Used in the following
在 #IF 之後和 #THEN 之前插入。用於以下
form: <boolean> #IF TRUE portion to perform
形式： <boolean> #IF 要執行的 TRUE 部分
#ELSE optional else portion
#ELSE 選用的 else 部分
#THEN operation continues here.
#THEN 操作在這裡繼續。


#LINE ( --- a1 ) KERNEL2
#LINE （ --- A1 ） KERNEL2
A variable that holds the line number of the current line on
保留目前行行號的變數
which text is being typed. Incremented by CR.
正在鍵入的文字。以 CR 遞增。


#LISTSEGS ( --- n1 ) KERNEL2
#LISTSEGS （ --- n1 ） KERNEL2
A VALUE which returns the number of 16 byte segments assigned
傳回指派的 16 位元組區段數目的 VALUE
to be used for bodys of Forth colon definitions. Limited by
用於 Forth 冒號定義的主體。受限
the memory of your computer.
電腦的記憶體。


#MACROS ( -- n1 ) MACROS HIDDEN
#MACROS （ -- n1 ） 隱藏的巨集
A CONSTANT that specifies how many keyboard macros we can have
一個 CONSTANT，指定我們可以擁有多少個鍵盤巨集
defined at one time.
一次定義。


#NUM ( a1 -- d1 f1 ) KERNEL2
#NUM （ A1 -- D1 F1 ） KERNEL2
A DEFERed word that is used by %NUMBER to process normal number
%NUMBER 用來處理一般數字的 DEFERed 字
conversions. Normally contains NUMBER?.
轉換。通常包含 NUMBER？。


#OUT ( --- a1 ) KERNEL2
#OUT （ --- A1 ） KERNEL2
A variable that holds the column number of the most recent type
保存最新類型資料行編號的變數
or emit to the display. Incremented by EMIT or TYPE.
或發射到顯示器。依 EMIT 或 TYPE 遞增。


#PAGE ( --- a1 ) UTILS
#PAGE （ --- a1 ） UTILS
A VARIABLE that contains the number of the current page. #PAGE
包含目前頁面編號的變數。#PAGE
is incremented by PAGE, but must be reset manually.
由 PAGE 遞增，但必須手動重設。


#PRLINES ( -- n1 ) BROWSE HIDDEN
#PRLINES （ -- n1 ） 瀏覽隱藏
A VALUE that counts the times ?.PRLINES is called between actually
計算次數的值？PRLINES 實際上是在
showing an update message on the screen while doing >BROWSE.
在執行>BROWSE 時在螢幕上顯示更新訊息。


#S ( d1 --- d2=0 ) KERNEL2
#S （ d1 --- d2=0 ） KERNEL2
Convert the double number D1 into ascii characters stored below
將雙數 D1 轉換為下面儲存的 ASCII 字元
PAD until D1 is reduced to a double ZERO.
PAD 直到 D1 減少到雙零。


#THREADS ( -- n1 ) KERNEL1
#THREADS （ -- n1 ） KERNEL1
Return the CONSTANT number of vocabulary threads used in the
傳回
dictionary. In F-PC this number can vary in binary multiples
字典。在 F-PC 中，這個數字可以以二進制倍數變化
from 2 to 128, it is normally set to 64.
從 2 到 128，通常設置為 64。


#TIB ( --- a1 ) KERNEL2
#TIB （ --- A1 ） KERNEL2
Used by WORD to hold the number of characters in the terminal
WORD 用來保存終端機中的字元數
input buffer when interpreting from the keyboard.
從鍵盤解譯時的輸入緩衝區。


#TIMES ( -- a1 ) UTILS
#TIMES （ -- a1 ） UTILS
Used by TIMES in performing a Forth command line repeatedly.
TIMES 在重複執行 Forth 命令行時使用。


#USER ( --- a1 ) KERNEL4
#USER （ --- A1 ） KERNEL4
A VARIABLE that holds the count of how many user variables are
一個 VARIABLE，它保存了使用者變數的數量
allocated.
分配。


#VOCS ( --- n1 ) KERNEL2
#VOCS （ --- n1 ） KERNEL2
The maximum number of vocabularies that can be active at one
一個詞彙表中可以作用中的詞彙數目上限
time in the vocabulary search order array.
詞彙搜尋順序陣列中的時間。


$.L ( a1 n1 n2 -- ) UTILS
$.L （ a1 n1 n2 -- ） 效用
Display string a1,n1 left justified in a field of n2 characters.
在 n2 個字元的欄位中顯示字串 a1，n1 左對齊。


$.R ( a1 n1 n2 -- ) UTILS
$.R （ a1 n1 n2 -- ） 效用
Display string a1,n1 right justified in a field of n2 characters.
在 n2 個字元的欄位中顯示字串 a1，n1 右對齊。


$>EXT ( a1 n1 a2 --- ) HANDLES
$>EXT （ a1 n1 a2 --- ） 句柄
Move the specified string a1,n1 to the extension field of the
將指定的字串 a1，n1 移至
handle a2.
處理 A2。


$>HANDLE ( a1 a2 --- ) HANDLES
$>HANDLE （ a1 a2 --- ） 句柄
Move a counted filename string a1 into handle a2 for use by
將計數的檔案名稱字串 a1 移至控制碼 a2 中，供
the following words.
下面的話。


$>TIB ( a1 --- ) UTILS
$>TIB （ a1 --- ） 公用程式
Move the counted string A1 into the Terminal Input Buffer for
將計數字串 A1 移至 終端機輸入緩衝區
immediate interpretation or access with WORD. Any contents of
立即解釋或使用 WORD 存取。任何內容
TIB is overwritten.
TIB 會被覆寫。


$DIR ( a1 -- ) EXEC HIDDEN]
$DIR （ a1 -- ） EXEC 隱藏]
Display a directory for the drive and path counted string a1.
顯示磁碟機和路徑計數字串 a1 的目錄。


$FILE ( a1 -- f1 ) FPATH
$FILE （ a1 -- f1 ） FPATH
Open the file specified by the counted string a1. Return f1
開啟計數字串 a1 指定的檔案。返回 f1
false if the file opened properly. Searches the Forth PATH in
false，如果檔案已正確開啟。在
trying to open the file.
嘗試開啟檔案。


$FLOAD ( a1 --- f1 ) SEQREAD
$FLOAD （ a1 --- f1 ） 序列
the file specified by counted string a1, return f1 true
計數字串 a1 指定的檔案，傳回 f1 true
if the file did not exist. Will abort if a compile error
如果檔案不存在。如果編譯錯誤，將中止
occurs while compiling the file.
在編譯檔案時發生。


$GETDIR ( a1 -- ) WFL HIDDEN
$GETDIR （ a1 -- ） WFL 隱藏
Read the directory using the filespec in counted string a1.
使用計數字串 a1 中的 filespec 讀取目錄。
The directory entries are read into the external segment
目錄項目會讀入外部區段
directory buffer. See the file WFL.SEQ for usage.
目錄緩衝區。請參閱檔案 WFL。SEQ 的使用。


$HOPEN ( a1 --- f1 ) SEQREAD
$HOPEN （ a1 --- f1 ） 序列讀取
Open the file specified by the counted string a1. Return
開啟計數字串 a1 指定的檔案。回
boolean f1 false if the open was succesful.
如果開局成功，則布林 f1 為假。


$NUM ( a1 -- d1 f1 ) KERNEL2
$NUM （ A1 -- D1 F1 ） KERNEL2
A DEFERed word that is used by %NUMBER to process HEXDECIMAL
%NUMBER 用來處理 HEXDECIMAL 的 DEFERed 字組
numbers, that is number starting with the $ symbol.
數字，即以 $ 符號開頭的數字。


$PFILE ( a1 --- f1 ) PRINT
$PFILE （ a1 --- f1 ） 列印
Select a print file as specified by the counted string a1.
選取計數字串 a1 所指定的列印檔案。
Return F1 a boolean error flag true if the print file could not
如果列印檔案無法傳回 F1 布林錯誤旗標 true
be created.
被創建。


$SYS ( a1 -- f1 ) EXEC HIDDEN
$SYS （ a1 -- f1 ） EXEC 隱藏
Spawn a DOS shell and perform the DOS command specified in the
產生 DOS shell 並執行
counted string a1. Return f1 true is an error occured.
計數字串 A1。傳回 f1 true 是發生錯誤。


%NUMBER ( a1 -- d1 f1 )
%數字 （ a1 -- d1 f1 ）
Convert count delimited string at a1 into double number.
將 a1 處的計數分隔字串轉換為雙精度。
Special prefixes allowed.
允許使用特殊前綴。


&> ( t1 --- a1 )
&> （ t1 --- a1 ）
Return the BODY address a1 of word t1, a VALUE of VARIABLE.
傳回單字 t1 的 BODY 位址 a1，即 VARIABLE 的 VALUE。


' ( | <name> -- cfa ) pronounced "tick" KERNEL3
' ( |<name> -- CFA ）發音為“tick”KERNEL3
Return the CFA (code field address) of the next word in the
傳回下一個單字的 CFA（代碼欄位位址）
input stream, <name>.
輸入流， <name>.


'DOCOL ( --- a1 ) UTILS
'DOCOL （ --- a1 ） UTILS
A CONSTANT that returns the execution address of NEST, or
傳回 NEST 執行位址的 CONSTANT，或
DOCOLON at it is sometimes known.
DOCOLON 有時是眾所周知的。


'NUM ( a1 -- d1 f1 ) KERNEL2
'NUM （ a1 -- d1 f1 ） KERNEL2
A defered word that processes 'A' byte in-line literal numbers
處理 'A' 位元組行內文字數字的延遲字
when compiling. See aso ^NUM, #NUM and $NUM.
編譯時。參見 aso ^NUM、#NUM 和 $NUM。


'TIB ( --- a1 ) KERNEL2
'TIB （ --- a1 ） KERNEL2
A VARIABLE that contains an address that points to the location
包含指向位置的位址的 VARIABLE
in memory where characters are entered by user.
在用戶輸入字符的內存中。


( ( -- ) KERNEL3
（ （ -- ） KERNEL3
The Forth comment character. The input stream of the current
第四個註解字元。目前的輸入串流
line is skipped until a ) is encountered. Terminates at line
跳過行，直到遇到 a ） 為止。終止於線路
end.
端。


(") ( | <string> -- a1 len )KERNEL3
(")( |<string> -- a1 len ）KERNEL3
Return the address and length of the inline string, and
傳回內嵌字串的位址和長度，以及
continue execution after the string.
在字串之後繼續執行。


(+LOOP) ( n1 --- ) KERNEL1
（+循環）（ n1 --- ）KERNEL1
Increment the loop counter by the value on the stack and decide
將迴圈計數器遞增堆疊上的值，並決定
whether or not to loop again. Due to the wierdness of the
是否再次循環。由於
8080, you have to stand on your head to determine the
8080，你得倒立才能確定
conditions under which you loop or exit.
您迴圈或退出的條件。


(.") ( --- ) KERNEL3
(.")( --- )KERNEL3
Type the inline string, and continue execution after the
輸入內嵌字串，並在
string. Compiled by ." , not used from the keyboard.
繩子。編譯者 “，不從鍵盤上使用。


(.) ( n1 --- a1 n2 ) KERNEL2
(.)（ n1 --- a1 n2 ）KERNEL2
Convert a signed 16 bit number to a string.
將帶正負號的 16 位數字轉換為字串。


(?DO) ( n1 n2 --- ) KERNEL1
(?做） （ n1 n2 --- ） KERNEL1
The runtime code compiled by ?DO. The difference between ?DO
由 ？DO 編譯的執行階段程式碼。之間的區別？做
and DO is that ?DO will not perform any iterations if the
那是嗎？如果
initial index is equal to the final index.
初始索引等於最終索引。


(?ERROR) ( a1 n1 f1 --- ) KERNEL3
(?錯誤） （ a1 n1 f1 --- ） KERNEL3
Default for ?ERROR. If boolean f1 is true then type the message
預設值為 ？錯。如果布林值 f1 為真，則鍵入訊息
specified by a1,n1 and QUIT. Else discard the message a1,n1.
由 a1，n1 和 QUIT 指定。否則，捨棄訊息 a1，n1。


(?LEAVE) ( f1 --- ) KERNEL1
(?離開） （ f1 --- ） KERNEL1
Compiled function emplaced by ?LEAVE. Leaves if the flag on the
由 ？ 置入的編譯函數離。如果旗幟上的旗幟會離開
stack is true. Continues if not.
stack 為 true。如果沒有，請繼續。


(?SERROR) ( a1 n1 f1 --- ) SEQREAD
(?SERROR） （ a1 n1 f1 --- ） 序列讀取
If boolean is true, then print message addr1,n1 and show the
如果布林值為 true，則列印訊息 addr1，n1 並顯示
line in the current file where the error occured.
發生錯誤的目前檔案中的行。


(?STACK) ( -- ) KERNEL3
(?堆疊） （ -- ） KERNEL3
An assembly primitive that checks for stack underflow, stack
檢查堆疊底層的元件基本類型，stack
overflow, and the nearly out of memory condition.
溢位，以及幾乎記憶體不足的情況。


(ABORT") ( f1 -- ) KERNEL3
（中止“）（ f1 -- ）KERNEL3
The Runtime code compiled by ABORT". Uses ERROR, and updates
由 ABORT 編譯的運行時代碼“。使用 ERROR，並更新
return stack.
返回堆疊。


(CHAR) ( a1 n1 c1 -- a1 n1+1 c1 )
（查爾）（ a1 n1 c1 -- a1 n1+1 c1 ）
A primitive used by the "kernel" EXPECT that saves character c1
「核心」EXPECT 使用的基本類型，可儲存字元 c1
into the current EXPECT buffer.
進入目前的 EXPECT 緩衝區。


(CONSOLE) ( c1 -- ) SEQREAD
（主機）（ c1 -- ）序列
Send character c1 to the console using a handle write to device
使用控制碼寫入裝置將字元 c1 傳送至主控台
CON:. See aso CONSOLEL, (PRINT) and PRINTL.
缺點：。參見 aso CONSOLEL、（PRINT） 和 PRINTL。


(D.) ( d1 --- a1 n1 ) KERNEL2
（四。（ D1 --- A1 N1 ）KERNEL2
Convert a signed double number to a string.
將帶正負號的雙精度轉換為字串。


(DO) ( n1 n2 --- ) KERNEL1
（做）（ n1 n2 --- ）KERNEL1
The runtime code compiled by DO. Pushes the inline address onto
DO 編譯的執行階段程式碼。將內嵌位址推送到
the return stack along with values needed by (LOOP).
傳回堆疊以及 （LOOP） 所需的值。


(DOERROR) FORTH
（錯誤）第四


(EDITERR) FORTH
（編輯）第四


(EMIT) ( c1 --- ) KERNEL2
（發射）（ c1 --- ）KERNEL2
Sends a character to both the console and optionally to the
將角色傳送至控制台，並選擇性地傳送至
printer.
印刷者。


(ESC-IN) FORTH
（電調輸入）第四


(EXPECT) ( a1 n1 --- ) KERNEL2
（預期）（ A1 N1 --- ）KERNEL2
Wait for n1 characters to be typed at the keyboard, and place
等待在鍵盤上鍵入 n1 個字元，然後將
those characters in the buffer starting at a1.
緩衝區中從 A1 開始的字元。


(FIND) ( here lfa --- cfa flag | here false ) KERNEL3
（尋找）（這裡是 lfa --- CFA 標誌 | 這裡是錯誤的）KERNEL3
Does a search of the dictionary based on a pointer to a
根據指向
vocabulary thread and a string. If it finds the string in the
詞彙線程和一個字串。如果它在
chain, it returns a pointer to the CFA field inside the header.
chain，則會傳回標頭內 CFA 欄位的指標。
This field contains the code field address of the body. If it
此欄位包含內文的代碼欄位位址。如果是
was an immediate word the flag returned is a 1. If it is
是一個立即的單詞，返回的標誌是 1。如果是
non-immediate the flag returned is a -1. If the name was not
non-immediate 時，傳回的旗標是 -1。如果名稱不是
found, the string address is returned along with a flag of
found，則會傳回字串位址以及
zero. Note that links point to links, and are absolute
零。請注意，連結指向連結，而且是絕對的
addresses.
地址。


(FRGET) ( code-addr relative-link-addr ) KERNEL3
（弗吉特）（ 代碼-addr relative-link-addr ）KERNEL3
Forgets part of the dictionary. Both the code address and the
忘記了字典的一部分。代碼位址和
header address are specified, and may be independent. (FRGET)
標頭位址，而且可以是獨立的。（弗吉特）
resets all of the links and releases the space.
重置所有鏈結並釋放空間。


(IS) ( cfa -- ) KERNEL4
（是）（ 特許金融分析師 -- ）KERNEL4
The code compiled by IS. Sets the following DEFERred word to the
The code compiled by IS.將下列 DEFERred 字設定為
address on the parameter stack.
位址。


(KEY) ( --- c1 ) KERNEL2
（關鍵）（ --- c1 ）KERNEL2
Pauses until a key is ready, and returns it on the stack.
暫停，直到金鑰準備就緒，並將它傳回堆疊上。


(KEY?) ( --- f1 ) KERNEL2
（關鍵？（ --- f1 ）KERNEL2
Returns true if the user has already pressed a key, otherwise
如果使用者已按下按鍵，則傳回 true，否則
false.
偽。


(LEAVE) ( --- ) KERNEL1
（離開）( --- )KERNEL1
Compiled function emplace by LEAVE. Does an immediate exit of a
由 LEAVE 編譯的函數 emplace。立即結束
DO ... LOOP structure. Unlike FIG Forth which waits until the
做。。。LOOP 結構。與 FIG Forth 不同，它等到
next LOOP is executed.
下一個 LOOP 被執行。


(LIT) ( --- n1 ) KERNEL1
（點亮）（ --- n1 ）KERNEL1
The runtime code for literals. Pushes the following two bytes
常值的執行階段程式碼。推送下列兩個位元組
onto the parameter stack and moves the IP over them. It is
到參數堆疊上，並將 IP 移到它們上。這是
compiled by the word LITERAL.
由單詞 LIRAL 編譯。


(LIT+) HIDDEN
（LIT+）潛


(LOOP) ( --- ) KERNEL1
（循環）( --- )KERNEL1
the runtime procedure for LOOP. Branches back to the beginning
LOOP 的執行階段程序。分支回到起點
of the loop if there are more iterations to do. Otherwise it
如果有更多迭代要做，則迴圈的迴圈。否則
exits. The loop counter is incremented.
退出。迴圈計數器會遞增。


(NUMBER) ( a1 --- d1 f1 ) KERNEL2
（數字）（ A1 --- D1 F1 ）KERNEL2
Convert the count delimited string at a1 to a double number.
將 a1 處的計數分隔字串轉換為雙精度。
(NUMBER) takes into account a leading minus sign, and stores a
（NUMBER） 會考量前導減號，並儲存
pointer to the last period in DPL. Note the string must end
指向 DPL 中最後一個句點的指標。請注意，字串必須結尾
with a blank or an error message is issued.
發出空白或錯誤訊息。


(NUMBER?) ( a1 --- d1 f1 ) KERNEL2
（數字？（ A1 --- D1 F1 ）KERNEL2
Given a string containing at least one digit, convert it to a
給定一個包含至少一個數字的字串，將其轉換為
number.
數。


(OF) ( n1 n2 -- n1 ) ( or ) ( n1 n1 -- ) KERNEL1
（的）（ n1 n2 -- n1 ）（ 或 ）（ n1 n1 -- ）KERNEL1
The run-time code compiled of OF . If the top two stack
編譯的執行階段程式碼 OF .如果前兩個堆疊
elements are the same, the two items will be dropped from the
元素相同，則這兩個項目將從
stack and the code following OF will be executed. Otherwise,
堆疊，並將執行 OF 後面的程式碼。否則
only the top item is dropped from the stack, and a branch is
只有最頂層的項目會從堆疊中捨棄，而分支是
taken from the literal following the in-line (OF) .
取自內聯 （OF） 後面的文字。


(PRINT) ( c1 -- ) SEQREAD
（列印）（ c1 -- ）序列
Send character c1 to the current print device using a handle
使用句柄將字元 c1 傳送至目前的列印裝置
write. See also PRINTL, (CONSOLE) and CONSOLEL.
寫。另請參閱 PRINTL、（CONSOLE） 及 CONSOLEL。


(REF) HIDDEN
（參考文獻）潛


(SEE) FORTH
（見）第四


(TYPE) FORTH
（類型）第四


(TYPEL) FORTH
（類型）第四


(U.) ( n1 --- a1 n2 ) KERNEL2
（美國。（ n1 --- a1 n2 ）KERNEL2
Convert an unsigned 16 bit number to a string.
將無符號的 16 位數字轉換為字串。


(UD.) ( d1 --- a1 n1 ) KERNEL2
（UD.）（ D1 --- A1 N1 ）KERNEL2
Convert an unsigned double number to a string.
將無符號雙精度轉換為字串。


(X") FORTH
（X）第四


(\.") FORTH
(\.")第四


(]) FORTH
（]） 向前


* ( n1 n2 -- n3 ) KERNEL1
* （ n1 n2 -- n3 ） KERNEL1
Returns a product of two numbers. The numbers may be either
傳回兩個數字的乘積。數字可以是
signed or unsigned. The product will be correct as long as it
簽名或未簽名。只要產品是正確的
may be properly represented in 16 bits!
可以用 16 位正確表示！


*/ ( n1 n2 n3 -- quot ) KERNEL1
*/ （ n1 n2 n3 -- quot ） KERNEL1
is a particularly useful operator, as it allows you to do
是一個特別有用的運算子，因為它允許您執行
accurate arithmetic on fractional quantities. Think of it as
分數的精確算術。把它想像成
multiplying n1 by the fraction n2/n3. The intermediate result
將 n1 乘以分數 n2/n3。中間結果
is kept to full accuracy. Notice that this is not the same as
保持完全準確。請注意，這與
* followed by /. See Starting Forth for more examples.
* 後面接著 /。有關更多示例，請參閱 Starting Forth。


*/MOD ( n1 n2 n3 -- mod quot )KERNEL1
*/MOD （ n1 n2 n3 -- mod quot ）KERNEL1
This returns the floored quotient and modulus of a 32 bit
這會傳回 32 位元的底商和模數
numerator and a 16 bit denominator n3 . The numerator is an
分子和 16 位分母 n3 。分子是
intermediate 32 bit product of the 16 bit quantities n1 and n2
16 位量 N1 和 N2 的中間 32 位乘積
. Note that the sign of the modulus is the same as the sign of
.請注意，模數的符號與 的符號相同
the denominator.
分母。


*BIG-CURSOR HIDDEN
*隱藏大光標


*D ( n1 n2 --- d1 ) KERNEL1
*D （ n1 n2 --- d1 ） KERNEL1
multiplys two singles and leaves a double.
乘以兩個單倍並留下一個雙倍。


*MED-CURSOR HIDDEN
*隱藏的 MED-遊標


*NORM-CURSOR HIDDEN
*隱藏的規範遊標


+ ( n1 n2 --- n3 ) KERNEL1
+ （ n1 n2 --- n3 ） KERNEL1
Add the top two numbers on the stack and return the result.
將堆疊上的前兩個數字相加並傳回結果。


+! ( n1 a1 --- ) KERNEL1
+!（ n1 a1 --- ）KERNEL1
Increment the value at a1 by n1. This is equivalent to the
將 a1 處的值遞增 n1。這相當於
following: DUP @ ROT + SWAP ! but much faster.
以下：DUP @ ROT + SWAP ！但要快得多。


+!> ( n1 | <name> -- ) EQUCOLON
+！> （ n1 |<name> -- ）埃科隆
Increment the body field of <name> by value n1 on the stack.
將 的 body 欄位遞增堆<name>疊上的值 n1。
Typically used to modify a VALUE or VARIABLE.
通常用來修改 VALUE 或 VARIABLE。


+," FORTH
+，“ FORTH


+A.? HIDDEN
+一個。潛


+LOOP ( n1 -- ) KERNEL3
+循環 （ n1 -- ） KERNEL3
Terminate a loop structure. Increment loop index by n1 and
終止迴圈結構。將迴圈索引遞增 n1 和
repeat <loop-body> until loop index crosses the boundary
重複<loop-body>直到迴圈索引越過邊界
between limit and limit - 1. Used in the following form: DO
在極限和極限之間 - 1.以以下形式使用：DO
<loop-body> LOOP.
<loop-body> 圈。


+TAB ( --- ) DECOM
+TAB （ --- ） DECOM
Bump the left margin up by 8 characters. used by the
將左邊距向上增加 8 個字元。由
decompiler to display nested conditional structures.
反編譯器來顯示巢狀條件結構。


+XSEG FORTH
+XSEG 前進
, ( n1 -- ) pronounced "comma" KERNEL3
， （ n1 -- ） 發音為“逗號”KERNEL3
Set the contents of the dictionary to the arbitrary 16-bit
將字典的內容設定為任意 16 位元
value on the stack.
堆疊上的值。


," ( | <string> -- ) KERNEL3
," ( |<string> -- ）KERNEL3
Add the following text string till a " to the dictionary in
將以下文本字符串添加到字典中，直到 ”
CODE space.
CODE 空間。


,CALL ( -- ) KERNEL3
，呼叫 （ -- ） KERNEL3
Compiles a CALL to address ZERO, the actual branch address is
編譯一個 CALL 到位址 ZERO，實際分支位址為
set later by ;USES or ;CODE.
後來由 ;用途或 ;法典。
See CREATE, VARIABLE, CONSTANT & :
請參閱 CREATE、VARIABLE、CONSTANT & ：


,JUMP ( --- ) KERNEL3
，跳躍 （ --- ） KERNEL3
Compiles a JMP to address ZERO, the actual jump address is set
編譯 JMP 以定址 ZERO，設定實際跳轉位址
later by ;USES or ;CODE. See CREATE, VARIABLE, CONSTANT & :
後來被 ;用途或 ;法典。請參閱 CREATE、VARIABLE、CONSTANT & ：


,VIEW ( -- ) KERNEL3
，檢視 （ -- ） KERNEL3
Calculate and compile the VIEW field into the header.
計算 VIEW 欄位並將其編譯到標頭中。


- ( n1 n2 --- n3 ) KERNEL1
- （ n1 n2 --- n3 ） KERNEL1
Subtracts n2 from n1 leaving the result on the stack.
從 n1 中減去 n2，將結果留在堆疊上。


-1! ( a1 -- ) KERNEL1
-1!（ a1 -- ）KERNEL1
Set the contents of the 16 bit quantity at a1 to -1 (all bits
將 a1 的 16 位元數量的內容設定為 -1 （所有位元
set).
設定）。


-LINE ( --- ) UTILS
-線路 （ --- ） 公用事業
A DEFERed word that deletes one line on the display at the
一個 DEFERed 字，在顯示器上刪除一行
cursor line. Lines below the cursor line are scrolled up one
游標線。游標線下方的線向上捲動一
line.
線。


-ROT ( n1 n2 n3 --- n3 n1 n2 ) KERNEL1
-腐爛 （ n1 n2 n3 --- n3 n1 n2 ） KERNEL1
The inverse of ROT. Rotates the top element to third place.
ROT 的反面。將頂端元素旋轉到第三位。


-SCAN FORTH
-向前掃描


-TAB ( --- ) DECOM
-TAB （ --- ） DECOM
Decrement the left margin up by 8 characters. Used by the
將左邊距遞減 8 個字元。由
decompiler to display nested conditional structures.
反編譯器來顯示巢狀條件結構。


-TRAILING ( a1 n1 --- a2 n2 ) KERNEL2
-尾隨 （ a1 n1 --- a2 n2 ） KERNEL2
Return the address and length of the given string ignoring
傳回給定字串的位址和長度，忽略
trailing blanks.
尾隨空白。


. ( n1 --- ) KERNEL2
.（ n1 --- ）KERNEL2
Display n1 as a signed 16 bit number with a trailing space.
將 n1 顯示為帶有尾端空格的帶正負號 16 位數字。


." ( | <string> -- ) KERNEL3
."( |<string> -- ）KERNEL3
Compile the string till a " to be typed out later. These
編譯字串，直到稍後輸入的 “。這些
strings are compiled into LIST space to conserve CODE room.
字串被編譯成 LIST 空間，以節省 CODE 空間。


."X$" HIDDEN
."X$」隱藏


.( ( -- ) KERNEL3
.（ （ -- ） KERNEL3
Type the following string on the terminal.
在終端機上鍵入下列字串。


.(;CODE) HIDDEN
.(;代碼）隱藏


.+LOOP HIDDEN
.+循環隱藏


.2W FORTH
.2W 向前


.: HIDDEN
。：潛


.?DO HIDDEN
.?做隱藏


.ABORT" HIDDEN
.中止」隱藏


.AGAIN HIDDEN
.再次隱藏


.ASKMACRO HIDDEN
.ASKMACRO 隱藏


.BASE FORTH
.基地


.BEGIN HIDDEN
.隱藏開始


.BOX" ( X Y | <string> --- ) BOXTEXT
.盒子」（X Y |<string> --- ）方塊文字
Used while compiling, followed by <string> which is compiled
編譯時使用，後面是<string>編譯的
into the current definition. Displays <string> inside a box on
進入當前定義。顯示在<string>方塊內
the screen whose upper left corner is at X, Y. Used in a COLON
左上角位於 X、Y 的螢幕。用於冒號
definitions as Follows: : TEXT 10 10 .BOX" This is a test" ;
定義如下： ： 文本 10 10 .BOX“這是一個測試”;


.CASE HIDDEN
.案件隱藏


.COMMENT: ( --- ) COMMENT
.評論：（---）評論
Starts a multi-line print statment. All lines following the
開始多行列印陳述式。所有行後面的
".comment:" line will be printed to the display until a
“.comment：” 行將列印到顯示器上，直到
"comment;" is encountered.
“comment;”。


.COMPSTAT ( --- ) TIMESTUF
.COMPSTAT （ --- ） TIMESTUF
Display the compiler status since the most recent 0COMPILER was
顯示編譯器狀態，因為最近的 0COMPILER 是
performed. Used to keep track of the performance of the
執行。用來追蹤
compiler on various hardware. See also 0COMPILER
各種硬體上的編譯器。另請參閱 0編譯器


.COMSPEC ( --- ) ENVIRON
.COMSPEC （ --- ） 環境
Print the current command specification including the drive and
列印目前的命令規格，包括磁碟機和
path.
路。


.CONSTANT HIDDEN
.常數隱藏


.CURFILE ( --- ) HELLO
.CURFILE （ --- ） 你好
Display the full file path and size of the currently open file.
顯示目前開啟檔案的完整檔案路徑和大小。


.DATE ( --- ) TIMER
.日期 （ --- ） 計時器
Get and display the DOS date.
取得並顯示 DOS 日期。


.DEFER HIDDEN
.延遲隱藏


.DEFINITION-CLASS HIDDEN
.定義類別隱藏


.DEFSRC FORTH


.DO HIDDEN
.做隱藏


.DOES> HIDDEN
.確實>隱藏


.ECURSOR HIDDEN
.ECURSOR 隱藏


.ELAPSED ( --- ) TIMER
.已耗盡 （ --- ） 計時器
Display the elapsed time in Houres, minutes, seconds, and
以小時、分鐘、秒和
hundredths since the last TIME-RESET was performed. Overflows
自上次執行時間重置以來的百分之一。溢位
at 18 hours.
在 18 小時。


.ELINE HIDDEN
.艾琳隱藏


.ELSE HIDDEN
.否則隱藏


.ENDCASE HIDDEN
.隱藏的尾箱


.ENDOF HIDDEN
.隱藏的結尾


.ENV ( --- ) ENVIRON
.環境 （ --- ） 環境
Display the current contents of the environment string.
顯示環境字串的目前內容。


.EXECUTION-CLASS HIDDEN
.執行類別隱藏


.FILE ( --- ) HELLO
.檔案 （ --- ） 你好
Display the name of the currently open file.
顯示目前開啟的檔案名稱。


.FILE-ONCE HIDDEN
.檔案 - 隱藏一次


.FILES ( --- ) FILSTAT
.文件 （ --- ） FILSTAT
Print the contents of the file system handle stack.
列印檔案系統控制碼堆疊的內容。


.FINISH HIDDEN
.完成隱藏


.FIRSTLINE HIDDEN
.第一線隱藏


.FOOT FORTH
.腳向前


.FPATH FORTH
.FPATH 向前


.FREE ( --- ) UTILS
.免費 （ --- ） 實用程式
Display the amount of dictionary space available at the
顯示可用的字典空間量
current time.
當前時間。


.HEAD FORTH
.前進


.HELLO ( --- ) HELLO
.你好（ --- ） 你好
Defered word, that displays the startup message when F-PC
延遲字，在 F-PC 時顯示啟動訊息
begins execution. Performs .<hello> by default.
開始執行。執行 。<hello> 預設情況下。


.HORIZONTAL FORTH
.水平向前


.ID ( nfa -- ) KERNEL4
.ID （ nfa -- ） KERNEL4
Display the variable length name whose name field address is on
顯示名稱欄位位址為
the stack. If it is shorter than its count, it is padded with
堆疊。如果它短於其計數，則填充
underscores. Only valid Ascii is typed.
下劃線。只會輸入有效的 Ascii。


.IF HIDDEN
.如果隱藏


.IMMEDIATE HIDDEN
.立即隱藏


.INST FORTH
.研究所


.IS HIDDEN
.是隱藏的


.LIT HIDDEN
.點燈隱藏


.LOADED ( --- ) FILSTAT
.加載 （ --- ） FILSTAT
Print a list of all files that have been loaded.
列印已載入的所有檔案清單。


.LOADLINE FORTH
.負載線向前


.LOOP HIDDEN
.迴圈隱藏


.ME ( --- ) ENVIRON
.我 （ --- ） 周邊地區
Print the name of the program currently executing. This only
列印目前執行的程式名稱。這只是
works on DOS 3.0 and higher. If it is used on DOS 2.x no name
適用於 DOS 3.0 及更高版本。如果在 DOS 2.x 上使用，則沒有名稱
will be printed. See also ME@.
將被列印。另請參閱 ME@。


.MENU FORTH
.菜單第四


.MENUBAR FORTH
.選單列向前


.NAM HIDDEN
.NAM 隱藏


.OF HIDDEN
.隱藏的


.OTHER HIDDEN
.其他隱藏


.PATH ( --- ) ENVIRON
.路徑 （ --- ） 環境
Print the current directory search PATH.
列印目前目錄搜尋 PATH。


.PFA HIDDEN
.PFA 隱藏


.QUOTE HIDDEN
.報價隱藏


.R ( n1 n2 --- ) KERNEL2
.R （ n1 n2 --- ） KERNEL2
Display n1 as a signed 16 bit number right justified in a field
將 n1 顯示為在欄位中右對齊的帶正負義 16 位元數字
of n2 spaces.
的 n2 空間。


.REPEAT HIDDEN
.重複隱藏


.REPMAC HIDDEN
.REPMAC 隱藏


.RVOCWORDS HIDDEN
.RVOCWORDS 隱藏


.S ( -- ) KERNEL4
.S （ -- ） KERNEL4
Displays the contents of the parameter stack non destructively.
以非破壞性方式顯示參數堆疊的內容。
Very useful when debugging.
調試時非常有用。


.SEQHANDLE ( --- ) SEQREAD
.序列手柄 （ --- ） 序列讀取
Display the filename in the current sequential file handle.
在目前的循序檔案控點中顯示檔案名稱。


.SRCCR FORTH
.SRCCR 福斯


.SRCDEF FORTH
.SRCDEF 前進


.STATUS ( -- ) STATUS
.狀態 （ -- ） 狀態
Test STATV, if it is on, then display the status line at the
測試 STATV，如果它已開啟，則在
top of the screen.
螢幕頂部。


.STRING"" HIDDEN
.STRING“” 隱藏


.STRING" HIDDEN
.STRING」隱藏


.STRING." HIDDEN
.字符串。潛


.THEN HIDDEN
.然後隱藏


.TIME ( --- ) TIMER
.時間 （ --- ） 計時器
Get the time from DOS, and display it.
從 DOS 獲取時間並顯示它。


.UNNEST HIDDEN
.隱藏的巢穴


.UNTIL HIDDEN
.直到隱藏


.USED ( --- ) UTILS
.已使用 （ --- ） UTILS
Display the amount of dictionary space used since the last
顯示自上次以來使用的字典空間量
!USED was executed.
!USED 已執行。


.USER-DEFER HIDDEN
.使用者延遲隱藏


.USER-VARIABLE HIDDEN
.隱藏使用者變數


.VALUE HIDDEN
.隱藏的價值


.VARIABLE HIDDEN
.變數隱藏


.VERTICAL FORTH
.垂直向前


.VOCWORDS ( A1 --- ) WORDS
.VOCWORDS （ A1 --- ） 單詞
Display the words matching, from a vocabulary. See the source
顯示詞彙表中的單詞匹配。查看來源
for WORDS for usage information.
用於 WORDS 的使用信息。


.VYET FORTH
.前進


.WHILE HIDDEN
.隱藏時


.WORD HIDDEN
.隱藏的單詞


.['] HIDDEN
.[']潛


/ ( num den -- quot ) KERNEL1
/ （ num den -- quot ） KERNEL1
Divide two signed single precision numbers and return the
除以兩個有符號的單精度數字，並傳回
floored quotient. Note that -5 2 / returns a value of -3 .
底商。請注意，-5 2 / 傳回值 -3 。


/* ( | <text> --- ) COMMENT
/* ( |<text> --- ）註解
Start a group of comments until a terminating */ is
開始一組註解，直到終止 */ 為止
encountered.
遇到了。


/LISTING FORTH
/上市前


/MOD ( num den -- rem quot ) KERNEL1
/MOD （ num den -- rem quot ） KERNEL1
Divide two signed single precision numbers and return the
除以兩個有符號的單精度數字，並傳回
floored quotient and modulus (remainder). Note that this
底商和模數（餘數）。請注意，這個
function is designed to return a modulus which has the same
函數旨在返回具有相同
sign as the denominator (usually positive), independent of the
符號作為分母（通常是正數），獨立於
sign of the denominator.
分母的標誌。


/NOLISTING FORTH


/STRING ( a1 len n1 --- addr' len' ) KERNEL2
/STRING （ a1 len n1 --- addr' len' ） KERNEL2
Index into the string addr, len, by n1. Returns addr+n and
索引字串 addr， len， by n1。傳回 addr+n 和
len-n.
倫恩。


0! ( a1 -- ) KERNEL1
0!（ a1 -- ）KERNEL1
Clear all 16 bits at the specified address.
清除指定位址的所有 16 位元。


0< ( n1 --- f1 ) KERNEL1
0< （ n1 --- f1 ） KERNEL1
Returns true if top is negative, ie sign bit is on.
如果 top 為負數，則傳回 true，即符號位元開啟。


0<= ( n1 --- f1 ) UTILS
0<= （ n1 --- f1 ） 效用
Return a boolean flag true if n1 is less than or equal to zero.
如果 n1 小於或等於零，則傳回布林旗標 true。


0<> ( n1 --- f1 ) KERNEL1
0<> （ n1 --- f1 ） KERNEL1
Returns true if the top is non-zero, False otherwise.
如果頂部非零，則傳回 true，否則傳回 False。


0= ( n1 --- f1 ) KERNEL1
0= （ n1 --- f1 ） KERNEL1
Returns True if top is zero, False otherwise.
如果 top 為零，則傳回 True，否則傳回 False。


0> ( n1 --- f1 ) KERNEL1
0> （ n1 --- f1 ） KERNEL1
Returns true if top is positive.
如果 top 為正數，則傳回 true。


0>= ( n1 --- f1 ) UTILS
0>= （ n1 --- f1 ） 效用
Return a boolean flag true if n1 is greater than or equal to
如果 n1 大於或等於
zero.
零。


0COMPILER ( --- ) TIMESTUF
0 編譯器 （ --- ） TIMESTUF
Initialize the compiler performance monitoring tool, in
起始設定編譯器效能監視工具，在
preperation for loading a quantity of source code. The word
為載入大量原始程式碼做好準備。這個詞
.COMPSTAT when later executed will inform you of the number of
.COMPSTAT 稍後執行時會通知您
lines compiled, and the rate at which linew were compiled. See
編譯的行，以及編譯 Linew 的速度。看
also .COMPSTAT.
亦。康普斯塔特。


0DECR FORTH
012月以後


0FL HIDDEN
0FL 隱藏


0ISTK HIDDEN
0ISTK 隱藏


0MAX FORTH
0 最大前進


1+ ( n1 --- n2 ) KERNEL1
1+ （ n1 --- n2 ） KERNEL1
Increment the top of the stack by one.
將堆疊頂端遞增 1。


1- ( n1 --- n2 ) KERNEL1
1- （ n1 --- n2 ） KERNEL1
Decrement the top of the stack by one.
將堆疊頂部遞減 1。


10TH-ELAPSED ( --- N1 ) TIMESTUF
10TH-ELAPSED （ --- N1 ） TIMESTUF
Return n1 the tenths of a second that have elapsed since the
傳回 n1 自
last TIME-RESET was performed.
上次執行 TIME-RESET 。


1FILE HIDDEN
1檔案隱藏


1ST-ROWCHAR FORTH
第一行


1STCOLD FORTH


2! ( d1 a1 --- ) KERNEL1
2!（ d1 a1 --- ）KERNEL1
Store a 32 bit value at addr.
在 addr 儲存 32 位元值。


2* ( n1 --- n2 ) KERNEL1
2* （ n1 --- n2 ） KERNEL1
Double the number on the Stack.
堆疊上的數字加倍。


2+ ( n1 --- n2 ) KERNEL1
2+ （ n1 --- n2 ） KERNEL1
Increment the top of the stack by two.
將堆疊頂端遞增 2。


2+! ( d1 a1 -- ) KERNEL1
2+!（ d1 a1 -- ）KERNEL1
Add the double number to the contents of the double word at
將雙精度數字添加到雙精度單詞的內容中
the specified address.
指定的位址。


2- ( n1 --- n2 ) KERNEL1
2- （ n1 --- n2 ） KERNEL1
Decrement the top of the stack by two.
將堆疊頂部遞減 2。


2/ ( n1 --- n2 ) KERNEL1
2/ （ n1 --- n2 ） KERNEL1
Shift the number on the stack right one bit. Equivalent to
將堆疊上的數字向右移動一點。相當於
division by 2 for positive numbers.
除以 2 為正數。


2>R ( n1 n2 --- ) KERNEL1
2>R （ n1 n2 --- ） KERNEL1
Pops two values off of the parameter stack and pushes them onto
從參數堆疊中彈出兩個值，並將它們推送到
the return stack. It is dangerous to use this randomly! This
返回堆棧。隨意使用這個很危險！這
word is equivalent to: "SWAP >R >R" that is the order of the
單詞相當於：“SWAP >R >R”，即
operator on the parameter stack is maintained when they are
參數堆疊上的運算子會在
placed on the return stack.
放置在返回堆棧上。


2@ ( a1 --- d1 ) KERNEL1
2@ （ a1 --- d1 ） KERNEL1
Fetch a 32 bit value from addr.
從 addr 取得 32 位元值。


2CONSTANT ( d1 | <name> -- ) compile time KERNEL3
2 常數 （ d1 |<name> -- ） 編譯時間 KERNEL3
( --- d1 ) run time
（ --- d1 ） 運行時間
Create a double number constant.
建立雙數常數。


2DROP ( n1 n2 --- ) KERNEL1
2DROP （ n1 n2 --- ） KERNEL1
( d1 --- )
（ d1 --- ）
Drop the top two elements of the data stack.
捨棄資料堆疊的前兩個元素。


2DUP ( n1 n2 --- n1 n2 n1 n2 ) KERNEL1
2DUP （ n1 n2 --- n1 n2 n1 n2 ） KERNEL1
( d1 --- d1 d1 )
（ d1 --- d1 d1 ）
Duplicate the top two elements of the data stack.
複製資料堆疊的前兩個元素。


2OVER ( n1 n2 n3 n4 --- n1 n2 n3 n4 1n 2n ) KERNEL1
2OVER （ n1 n2 n3 n4 --- n1 n2 n3 n4 1n 2n ） KERNEL1
( d1 d2 --- d1 d2 d1 )
（ D1 D2 --- D1 D2 D1 ）
Copy the second pair of numbers over the top pair. Behaves
將第二對數字複製到頂部對上。行為
like 2SWAP for 32 bit integers.
就像 2SWAP 一樣，用於 32 位整數。


2R> ( --- n1 n2 ) KERNEL1
2R> （ --- n1 n2 ） KERNEL1
Pops two values off of the return stack and pushes them onto
從傳回堆疊中彈出兩個值，並將它們推送到
the parameter stack. It is dangerous to use this randomly!
參數堆疊。隨意使用這個很危險！
This word is equivalent to: R> R> SWAP that is the order of the
這個詞相當於：R> R> SWAP，即
operator on the return stack is maintained when they are placed
返回堆疊上的運算子在放置時會保持不變
on the parameter stack.
在參數堆疊上。


2R@ ( --- n1 n2 ) KERNEL1
2R@ （ --- n1 n2 ） KERNEL1
Copies the two top values from the return stack to the
將返回堆疊中的兩個頂值複製到
parameter stack. Same as "R> R> 2DUP >R >R SWAP" that is the
參數堆疊。與「R> R> 2DUP >R >R SWAP」相同，即
order of the operator on the return stack is maintained when
當
they are placed on the parameter stack.
它們會放置在參數堆疊上。


2ROT ( n1 n2 n3 n4 n5 n6 --- n3 n4 n5 n6 n1 n2 ) KERNEL1
2ROT （ n1 n2 n3 n4 n5 n6 --- n3 n4 n5 n6 n1 n2 ） KERNEL1
( d1 d2 d3 --- d2 d3 d1 )
（ d1 d2 d3 --- d2 d3 d1 ）
Rotates top three double numbers.
輪換前三個雙數字。


2SWAP ( n1 n2 n3 n4 --- n3 n4 1n 2n ) KERNEL1
2SWAP （ n1 n2 n3 n4 --- n3 n4 1n 2n ） KERNEL1
( d1 d2 --- d2 d1 )
（ D1 D2 --- D2 D1 ）
Swap the top two pairs of numbers on the stack. You can use this
交換堆疊上前兩對數字。您可以使用這個
operator to swap two 32 bit integers and preserve their meaning as
運算子交換兩個 32 位整數，並保留其含義為
double numbers.
雙倍數字。


2VARIABLE ( | <name> -- ) compile time KERNEL3
2 變數 （ |<name> -- ） 編譯時間 KERNEL3
( --- a1 ) runtime
（ --- a1 ） 執行階段
Create a double length variable.
建立雙倍長度變數。


3DROP ( n1 n2 n3 --- ) KERNEL1
3DROP （ n1 n2 n3 --- ） KERNEL1
Drop the top three elements of the data stack.
捨棄資料堆疊的前三個元素。


3DUP ( n1 n2 n3 --- n1 n2 n3 n1 n2 n3 ) KERNEL1
3DUP （ n1 n2 n3 --- n1 n2 n3 n1 n2 n3 ） KERNEL1
Duplicate the top three elements of the data stack.
複製資料堆疊的前三個元素。


4DUP ( n1 n2 n3 n4 --- n1 n2 n3 n4 n1 n2 n3 n4 ) KERNEL1
4DUP （ n1 n2 n3 n4 --- n1 n2 n3 n4 n1 n2 n3 n4 ） KERNEL1
( d1 d2 --- d1 d2 d1 d2 )
（ d1 d2 --- d1 d2 d1 d2 ）
Duplicate the top four 16 bit elements of the stack.
複製堆疊的前四個 16 位元元素。


8* ( n1 --- n2 ) KERNEL1
8* （ n1 --- n2 ） KERNEL1
Multiply the top of the stack by 8.
將堆疊頂部乘以 8。


: ( -- ) KERNEL3
： （ -- ） KERNEL3
Defines a colon definition. The definition is hidden until it
定義冒號定義。定義是隱藏的，直到它
is completed, or the user desires recursion. The runtime for :
已完成，或使用者想要遞迴。執行階段：
adds a nesting level.
新增巢狀層級。


; ( -- ) KERNEL3
;( -- )KERNEL3
Terminates a colon definition. Compiles the runtime code to
終止冒號定義。將執行階段程式碼編譯為
remove a nesting level, and changes STATE so that compilation
移除巢狀層級，並變更 STATE 以編譯
will terminate.
將終止。


;CODE ( -- ) KERNEL3
;代碼 （ -- ） KERNEL3
Used for defining the run time portion of a defining word in
用於定義定義單字的執行時間部分
low level code.
低階程式碼。


;USES ( -- ) KERNEL3
;用途 （ -- ） KERNEL3
Similar to the traditional ;CODE except used when run time
與傳統相似;CODE （執行階段使用時除外）
code has been previously defined.
程式碼已預先定義。


< ( n1 n2 --- f1 ) KERNEL1
< （ n1 n2 --- f1 ） KERNEL1
Compare the top two elements on the stack as signed integers
將堆疊上的前兩個元素比較為有符號的整數
and return true if n1 < n2.
如果 n1 < n2，則傳回 true。


<# ( d1 --- d1 ) KERNEL2
<# （ d1 --- d1 ） KERNEL2
Start numeric conversion. Sets the variable HLD to PAD.
開始數值轉換。將變數 HLD 設定為 PAD。


<#IF> FORTH
<#IF>向前


<$FILE> FORTH
<$FILE>向前


<'> FORTH
<>


<.COMMENT:> FORTH
<.評論：>


<.CURFILE> FORTH
<.CUR檔案> FORTH


<.ELAPSED> FORTH
<.消失>第四


<.HELLO> FORTH
<.你好>福斯


<.STAT> FORTH


<= ( n1 n2 --- f1 ) UTILS
<= （ n1 n2 --- f1 ） 效用
Less than or equal.
小於或等於。


<> ( n1 n2 --- f1 ) KERNEL1
<> （ n1 n2 --- f1 ） KERNEL1
Returns true if the two element are not equal, else false.
如果兩個元素不相等，則傳回 true，否則傳回 false。


<?PTR.READY> FORTH
<？PTR.READY> 向前


<BDOS> FORTH
<BDOS> 第四


<BOX> HIDDEN
<BOX> 潛


<COMMENT:> FORTH
<評論：> FORTH


<D.M.Y> FORTH
<DMY>福斯


<DOLDEL> HIDDEN
<DOLDEL> 潛


<ED> ( --- ) TOPEDIT
<ED> （ --- ） 托佩迪特
Re-Enter the editor on the current file at the most recent edit
在最近編輯時重新進入目前檔案的編輯器
line. Reads the file into memory if needed.
線。如有需要，將檔案讀入記憶體。


<EDONE> HIDDEN
<EDONE> 潛


<EQUIT> HIDDEN
<EQUIT> 潛


<EXEC> HIDDEN
<EXEC> 潛


<FLOAD> ( --- ) SEQREAD
<FLOAD> （ --- ） 順序
Primitive word that loads the file just opened.
載入剛開啟檔案的原始字。


<FPATH+> FORTH
<FPATH+>向前


<GETFILE> FORTH
<GETFILE> 第四


<GETTIME> ( --- hm sh ) TIMER
<GETTIME> （ --- hm sh ） 定時器
Get the system time in DOS format, HM=hours,minutes and
以 DOS 格式獲取系統時間，HM=小時、分鐘和
SH=seconds,hundreths. See also .TIME, .DATE
SH=秒，百秒。另請參閱 。時間。日期


<GRAPHDUMMY> FORTH
<GRAPHDUMMY> 第四


<HEADER> FORTH
<HEADER> 第四


<HRENAME> ( handle1 handle2 --- return-code ) HANDLES
<HRENAME> （ handle1 handle2 --- return-code ） 句柄
Code primitive for the HRENAME. See also HRENAME.
HRENAME 的程式碼基本類型。另請參閱 HRENAME。


<ICHAR> HIDDEN
<ICHAR> 潛


<LEDIT> HIDDEN
<LEDIT> 潛


<LOAD> ( --- ) SEQREAD
<LOAD> （ --- ） 順序
Load the current file starting at the current file offset.
從目前檔案偏移開始載入目前檔案。


<LRUN> FORTH
<LRUN> 第四


<M/D/Y> FORTH
<月/日/年>第四


<MARK ( -- a1 ) KERNEL3
<馬克 （ -- a1 ） KERNEL3
Set up for a Backwards Branch.
設定向後分支。


<RED> FORTH
<RED> 第四


<RESOLVE ( a1 -- ) KERNEL3
<解決 （ a1 -- ） KERNEL3
Resolve a Backwards Branch.
解析向後分支。


<RUN> FORTH
<RUN> 第四


<SAVE-EXE> FORTH
<SAVE-EXE> 第四


<TO<>BL HIDDEN
<到<>BL 隱藏


<TO=BL+1 HIDDEN
<TO=BL+1 隱藏


<W.NAME> FORTH
<W.NAME>向前


<Y-M-D> FORTH
<Y-M-D> 第四


= ( n1 n2 --- f1 ) KERNEL1
= （ n1 n2 --- f1 ） KERNEL1
Returns true if the two elements on the stack are equal, False
如果堆疊上的兩個元素相等，則傳回 true，False
otherwise.
否則。


=: ( n1 | <name> -- ) EQUCOLON
=： （ n1 |<name> -- ）埃科隆
Used to assign values into the body of <name>, like VARIABLEs
用於將值賦值到 的主體中，<name> 例如 VARIABLEs
or VALUEs. May be used on the command line. Typical usage is as
或 VALUE。可在命令列上使用。典型用法是
follows: 34 VALUE MYVAL \ create a VALUE
以下： 34 VALUE MYVAL \ 建立 VALUE
: CHANGE_MYVAL ( --- ) \ define a word to
： CHANGE_MYVAL （ --- ） \ 定義一個詞
23 =: MYVAL ; \ change MYVAL
23 =：邁瓦爾;\ 更改 MYVAL


> ( n1 n2 --- f1 ) KERNEL1
> （ n1 n2 --- f1 ） KERNEL1
Compare the top two elements on the stack as signed integers
將堆疊上的前兩個元素比較為有符號的整數
and return true if n1 > n2.
如果 n1 > n2，則傳回 true。


>.ID FORTH
>.第四個


>= ( n1 n2 --- f1 ) UTILS
>= （ n1 n2 --- f1 ） 效用
Compare n1 and n2, return a true if n1 is greater than or
比較 n1 和 n2，如果 n1 大於或
equal to n2.
等於 n2。


>ATTRIB ( handle --- attrib-a1 )HANDLES
>ATTRIB（手柄--- attrib-a1）手柄
Step to the attribute field of the handle
控制碼屬性欄位的步驟


>ATTRIB8
>ATTRIB7
>ATTRIB6
>ATTRIB5
>ATTRIB4
>ATTRIB3
>ATTRIB2
>ATTRIB1 ( --- ) UTILS
>ATTRIB1 （ --- ） UTILS
Select a display attribute for the display you are using.
選取您正在使用的顯示的顯示屬性。
These are DEFERed words that are setup at COLD start time to
這些是在 COLD 啟動時設定的 DEFERed 字，以
perform the proper function for the display card you are using.
為您正在使用的顯示卡執行正確的功能。


>ATTRIB8 FORTH
>ATTRIB8 向前


>B FORTH
> B 前進


>BG ( N1 --- ) COLOR
>BG （ N1 --- ） 顏色
Set the Background color to value n1.
將 背景色彩 設定為值 n1。


>BODY ( cfa -- pfa ) KERNEL3
>BODY （ cfa -- pfa ） KERNEL3
Go from code field address cfa to body address pfa.
從代碼字段地址 cfa 轉到正文地址 pfa。


>BOLD ( --- ) MONOCROM
>粗體 （ --- ） 單色
Set the display attribute to bold.
將 display 屬性設定為粗體。


>BOLDBLNK ( --- ) MONOCROM
>BOLDBLNK （ --- ） 單色
Set the display attribute to bold blink.
將顯示屬性設定為粗體閃爍。


>BOLDUL ( --- ) MONOCROM
>粗體 （ --- ） 單色
Set the display attribute to bold underline.
將顯示屬性設定為粗體底線。


>BOX FORTH
>盒子第四


>BROWSER FORTH
>瀏覽器


>BUGN ( --- ) COLOR
>BUGN （ --- ） 顏色
Set the Backgound to BLUE, and Forground to Green.
將 Backgound 設定為 BLUE，並將 Forground 設定為 Green。


>BUWT ( --- ) COLOR
>BUWT （ --- ） 顏色
Set the Background to Green, and Forground to WHITE.
將背景設定為綠色，並將 Forground 設定為白色。


>COLOR ( --- ) COLOR
>顏色 （ --- ） 顏色
Select hilighting for color monitor.
為彩色顯示器選擇高光。


>EDATTRIB HIDDEN
>EDATTRIB 隱藏


>FADR HIDDEN
>法德爾隱藏


>FG ( N1 --- ) COLOR
>FG （ N1 --- ） 顏色
Set the Forground color to value n1.
將 Forground 顏色設定為值 n1。


>HNDLE ( handle --- handle-a1 )HANDLES
>HNDLE （ handle --- handle-a1 ）HANDLES
Step to the handel storage field of the handle array.
逐步移至手柄陣列的手感儲存欄位。


>IBM ( -- ) IBMCURSR
>IBM （ -- ） IBMCURSR
Select the IBM display as the default display.
選取 IBM 顯示畫面作為預設顯示畫面。


>IN ( --- a1 ) KERNEL2
>IN （ --- A1 ） KERNEL2
Number of characters interpreted so far.
到目前為止解譯的字元數。


>IS ( cfa -- data-address ) KERNEL4
>IS （ cfa -- 資料位址 ） KERNEL4
Maps a code field into a data field. If the word is in the USER
將程式碼欄位對應至資料欄位。如果該單字位於 USER
class of words, then the data address must be calculated
類別，則必須計算資料位址
relative to the current user pointer. Otherwise it is just the
相對於目前的使用者指標。否則，它只是
parameter field.
參數欄位。


>ISTK HIDDEN
>隱藏


>KEYS1 HIDDEN
>KEYS1 隱藏


>KEYS2 HIDDEN
>KEYS2 隱藏


>LCD ( --- ) COLOR
>LCD（---）彩色
Select the LCD display mode, that is only minimal display
選擇 LCD 顯示模式，即僅最小顯示
attributes are used, REVERSE only.
屬性，僅使用 REVERSE 。


>LINE ( n1 --- ) SEQREAD
>線 （ n1 --- ） 順序
Step to line n1 in the current file.
步驟到目前檔案中的 n1 行。


>LINK ( cfa -- lfa ) KERNEL3
>LINK （ CFA -- lfa ） KERNEL3
Go from code field address cfa to link field address lfa.
從代碼欄位位址 cfa 移至連結欄位位址 lfa。


>MARK ( -- a1 ) KERNEL3
>馬克 （ -- a1 ） KERNEL3
Set up for a Forward Branch.
設定前向分支。


>MENU FORTH
>菜單第四


>MONO ( --- ) MONOCROM
>單聲道 （ --- ） 單色
Set the ATTRIB words to select various monochrome attributes.
設定 ATTRIB 單字以選取各種單色屬性。


>NAM ( handle --- name-string-a1 ) HANDLES
>NAM （ handle --- name-string-a1 ） 句柄
Step to the null terminated name field of the handle
逐步移至控句的 Null 終止名稱欄位


>NAME ( cfa -- nfa ) KERNEL3
>名稱 （ CFA -- nfa ） KERNEL3
Go from code field address cfa to name field address nfa.
從代碼字段地址 cfa 轉到名稱字段地址 nfa。


>NAME.ID FORTH
>NAME.ID 向前


>NEST ( --- a1 ) KERNEL1
>內斯特 （ --- a1 ） KERNEL1
The address of the NEST routine.
NEST 常式的位址。


>NEXT ( --- a1 ) KERNEL1
>下一頁 （ --- A1 ） KERNEL1
Label of the NEXT sequence. This is the location we jump to
NEXT 序列的標籤。這是我們跳到的位置
when we are NOT using in-line NEXT.
當我們不使用內聯 NEXT 時。


>NONE
>無


>NONEBG FORTH
>沒有出現


>NORM ( --- ) MONOCROM
>NORM （ --- ） 單色
Set display attributes to none, or normal.
將顯示屬性設定為無或正常。


>NORMBG FORTH


>PATHEND-1 HIDDEN
>PATHEND-1 隱藏


>PATHEND HIDDEN
>路徑隱藏


>PATHEND" HIDDEN
>PATHEND」隱藏


>PRE ( --- ) PASM
>PRE （ --- ） PASM
Select the PREFIX assembler mode, and saves the previous prefix
選取 PREFIX 組譯器模式，並儲存前一個字首
flag on the return stack for later restoral by PRE>.
旗標，以便稍後由 PRE> 恢復。


>R ( n1 --- ) KERNEL1
>R （ n1 --- ） KERNEL1
Pops a value off of the parameter stack and pushes it onto
從參數堆疊中彈出值，並將其推送到
return stack. It is dangerous to use this randomly!
返回堆疊。隨意使用這個很危險！


>RDWT ( --- ) COLOR
>RDWT （ --- ） 顏色
Set the Background to RED, and Forground to WHITE.
將背景設定為紅色，並將「前地面」設定為白色。


>RESOLVE ( a1 -- ) KERNEL3
>解決 （ a1 -- ） KERNEL3
Resolve a Forward Branch.
解析轉向分支。


>REV ( --- ) UTILS
>REV （ --- ） UTILS
Set the display attribute to reverse.
將顯示屬性設定為反轉。


>REVBLNK ( --- ) MONOCROM
>REVBLNK （ --- ） 單色
Set the display attribute to reverse blink.
將 display 屬性設定為反向閃爍。


>REVERSE FORTH
>反向前進


>TO<>BL HIDDEN
>到 <>BL 隱藏


>TO=BL HIDDEN
>TO=BL 隱藏


>TYPE ( a1 len -- ) KERNEL3
>類型 （ a1 len -- ） KERNEL3
TYPE for multitasking systems.
TYPE 用於多任務處理系統。


>UL ( --- ) MONOCROM
>UL （ --- ） 單色
Set the display attribute to underline.
將顯示屬性設定為底線。


>VIEW ( cfa -- vfa ) KERNEL3
>VIEW （ CFA -- VFA ） KERNEL3
Go from code field address cfa to view field address vfa.
從代碼欄位位址 cfa 移至檢視欄位位址 vfa。


>VIEWFILE ( cfa --- offset a1 ) VIEW
>VIEWFILE （ cfa ---偏移量 a1 ） 檢視
Locate the file which was used to compile word CFA, and return
找到用來編譯單字 CFA 的檔案，然後傳回
its string in PAD as A1 a counted string, and OFFSET the offset
其在 PAD 中的字串為 A1 一個計數字串，並 OFFSET 偏移量
into the file where the word definition starts.
到單字定義開始的檔案中。


>XBUF HIDDEN
>XBUF 隱藏


? ( a1 --- ) UTILS
?（ A1 --- ）公用事業
Display the contents of the 16 bit memory location a1 as a
將 16 位元記憶體位置 a1 的內容顯示為
signed value.
signed 值。


?.LOADLINE FORTH
?.負載線向前


?.PRLINES HIDDEN
?.隱藏的 PRLINES


?<MARK ( -- f1 a1 ) KERNEL3
？<馬克 （ -- f1 a1 ） KERNEL3
Set up for a Backwards Branch with Error Checking.
設定具有錯誤檢查的向後分支。


?<RESOLVE ( f1 a1 -- ) KERNEL3
？<解決 （ f1 a1 -- ） KERNEL3
Resolve a backwards Branch with Error Checking.
使用錯誤檢查解決向後分支。


?>MARK ( -- f1 a1 ) KERNEL3
？>馬克 （ -- f1 a1 ） KERNEL3
Set up a forward Branch with Error Checking.
設定具有錯誤檢查功能的轉發分支。


?>RESOLVE ( f1 a1 -- ) KERNEL3
？>解決 （ f1 a1 -- ） KERNEL3
Resolve a forward Branch with Error Checking.
使用錯誤檢查解決轉發分支。


?ADDMAC HIDDEN
?ADDMAC 隱藏


?ALREADY_DEF FORTH
?ALREADY_DEF 向前


?BASE_RESTORE FORTH
?BASE_RESTORE 向前


?BRANCH ( f1 --- ) KERNEL1
?分支 （ f1 --- ） KERNEL1
Performs a conditional branch. If the top of the parameter
執行條件式分支。如果參數的頂部
stack in True, take the branch. If not, skip over the branch
stack in True，則取分支。如果沒有，請略過分支
address which is inline.
內嵌地址。


?CHAR HIDDEN
?隱藏字符


?CODENAME FORTH
?代號 FORTH


?COLORIZE FORTH
?著色


?COMP ( --- ) SAVEREST
?補償 （ --- ） 最節省
Verify F-PC is in COMPILE state. Issue an error message if
驗證 F-PC 是否處於 COMPILE 狀態。如果出現以下情況，請發出錯誤訊息
Forth is not in COMPILE state.
Forth 不處於 COMPILE 狀態。


?CONDITION ( f1 -- ) KERNEL3
?條件 （ f1 -- ） KERNEL3
Simple compile time error checking. Usually adequate.
簡單的編譯時錯誤檢查。通常足夠了。


?CONSTANT.* FORTH
?常數。


?CONTROL HIDDEN
?控制隱藏


?CR ( -- ) KERNEL4
?CR （ -- ） KERNEL4
Break the line at the cursor, if we have reached the right
如果我們到達右側，請在光標處劃斷線
margin as specified by RMARGIN.
margin 由 RMARGIN 指定。


?CS: ( --- seg ) KERNEL2
？CS：（ --- seg ） KERNEL2
leave Forths Code Segment on the stack.
將 Forths Code Segment 保留在堆疊上。


?CSP ( -- ) KERNEL3
?CSP （ -- ） KERNEL3
Issue error message if stack has changed since the most recent
如果堆疊自最近一次以來已變更，則會發出錯誤訊息
!CSP.
!CSP。


?CURSOR-MOVE HIDDEN
?游標移動隱藏


?DARK ( --- ) UTILS
?深色 （ --- ） 實用程式
Conditionally perform a DARK if no key is waiting at the
如果沒有金鑰在等待，則有條件地執行 DARK
keyboard.
鍵盤。


?DEBUG HIDDEN
?偵錯隱藏


?DEF.EXT ( --- ) HANDLES
?防禦。EXT （ --- ） 控點
If the specified file name has no "." indicating the extension,
如果指定的檔案名稱沒有表示副檔名的「.」，
then supply one from the default.
然後從預設值中提供一個。


?DEFATTRIB FORTH
?德法特里布·福斯


?DEFER.* FORTH
?推遲。


?DIR-DOWN HIDDEN
?DIR-DOWN 隱藏


?DIR-UP HIDDEN
?DIR-UP 隱藏


?DIR-WINDOW HIDDEN
?DIR 視窗隱藏


?DNEGATE ( d1 d2 --- d3 ) KERNEL1
?DNEGATE （ d1 d2 --- d3 ） KERNEL1
Negate the double number if the top is negative.
如果頂部為負數，則否定雙倍數字。


?DO ( limit start -- ) KERNEL3
?DO （ 限制開始 -- ） KERNEL3
Same as DO except that the loop will not be executed if start =
與 DO 相同，只是如果 start =
limit.
限。


?DOINGMAC ( --- f1 ) UTILS
?DOINGMAC （ --- f1 ） 實用程式
Return a boolean flag TRUE if a macro is in the process of
如果巨集正在處理中，則傳回布林旗標 TRUE
being executed, else return FALSE.
正在執行，否則傳回 FALSE。


?DOMAC HIDDEN
?DOMAC 隱藏


?DOMAC1 HIDDEN
?DOMAC1 隱藏


?DOMKEY FORTH
?多姆基·福斯


?DOSIO ( --- f1 ) UTILS
?DOSIO （ --- f1 ） UTILS
Return a boolean flag TRUE if we are currently using DOS for
如果我們目前使用 DOS 來傳回布林標誌 TRUE
all I/O, rather than direct screen output.
所有 I/O，而不是直接螢幕輸出。


?DOSTOP FORTH
?前進


?DRIVE.EXTRACT ( handle --- drive-value ) PATHSET
?開。EXTRACT （ 處理 --- 驅動值 ） PATHSET
Given handle, return drive-value, the drive specified in
給定控制碼，傳回磁碟機值，中指定的磁碟機
handle, or return the current drive if no drive was specified
處理，或傳回現行磁碟機 （如果未指定磁碟機）
in handle.
在手柄中。


?DRIVE.PREPEND ( drive-value handle --- ) PATHSET
?開。PREPEND （ 磁碟機值控制碼 --- ） 路徑集
Given drive-value and handle, prepend the drive-value into
給定 drive-value 和句柄，將 drive-value 置於前面
handle, as letter followed by ":".
handle，後面跟著“：”。


?DROP FORTH
?掉下來


?DUP ( n1 --- n1 n1<>0 | n1=0 ) KERNEL1
?DUP （ n1 --- n1 n1<>0 | n1=0 ） KERNEL1
Duplicate the top of the stack if it is non-zero.
如果堆疊頂端不是零，請複製它。


?ENOUGH ( n1 --- ) UTILS
?足夠 （ n1 --- ） UTILS
Test the number of items on the data stack, if there are more
測試資料堆疊上的專案數目 （如果有更多）
than n1 items then continue. If there are less than n1 items,
然後繼續 n1 項目。如果少於 n1 個項目，
abort with an error.
中止並出現錯誤。


?ERROR ( a1 n1 f1 --- ) KERNEL3
?錯誤 （ a1 n1 f1 --- ） KERNEL3
Maybe indicate an error. If f1 is true then display the error
也許表示錯誤。如果 f1 為 true，則顯示錯誤
message a1,n1, else discard a1,n1. Change this to alter ABORT".
訊息 a1，n1，否則捨棄 a1，n1。更改此值以更改 ABORT“。


?ES: ( --- ) KERNEL2
？ES：（ --- ） KERNEL2
Return the current value of the ES register on the stack.
傳回堆疊上 ES 暫存器的目前值。


?EXEC ( --- ) COMMENT
?執行委員會 （ --- ） 評論
ABORT if Forth is not currently in EXECUTION STATE with an
如果 Forth 目前未處於 EXECUTION STATE 且
error message.
錯誤訊息。


?EXIT ( f1 --- ) KERNEL1
?退出 （ f1 --- ） KERNEL1
If boolean f1 is true then perform EXIT above else continue
如果布林值 f1 為真，則執行 EXIT 以上繼續
executing the current definition.
執行目前的定義。


?FILEOPEN ( --- ) VIEW
?FILEOPEN （ --- ） 檢視
Verify a file is open, give an error message if no file is
驗證檔案是否已開啟，如果沒有檔案，則顯示錯誤訊息
open.
開。


?FILLBUFF ( --- ) SEQREAD
?FILLBUFF （ --- ） 序列
Re-fill the input buffer if it needs it.
如果需要，請重新填充輸入緩衝區。


?FIX-CURSOR FORTH
?修復游標向前


?FUNC HIDDEN
?功能隱藏


?GETEXPFILE FORTH
?GETEXP 檔案


?HELP-DO HIDDEN
?幫助-執行隱藏


?IN-EMPTY FORTH
?空空的


?INNAME FORTH
?名義


?INSERT-TOGGLE HIDDEN
?插入-切換隱藏


?KEYPAUSE ( --- ) UTILS
?KEYPAUSE （ --- ） 公用程式
Wait for a key to be pressed at the keyboard. If the key is an
等待按下鍵盤上的按鍵。如果金鑰是
ESC, abort. If the key is any other key, wait for an additional
ESC，中止。如果金鑰是任何其他金鑰，請等待額外的
key. If the additional key is anything but an ESC, continue
鑰匙。如果附加鍵不是 ESC，請繼續
execution. If the second key is an ESC, then abort.
死刑。如果第二個鍵是 ESC，則中止。


?LDONE HIDDEN
?LDONE 隱藏


?LEAVE ( f1 -- ) KERNEL3
?離開 （ f1 -- ） KERNEL3
Immediately exit a DO-LOOP if the flag is true; else continue
如果旗標為真，請立即退出 DO-LOOP;否則繼續
looping.
循環。


?LINE ( n1 -- ) KERNEL4
?線 （ n1 -- ） KERNEL4
Break the line at the cursor if there are less than n1
如果游標處的線小於 n1
characters till RMARGIN is encountered.
字符，直到遇到 RMARGIN。


?LISTING FORTH
?上市


?LMATCH HIDDEN
?LMATCH 隱藏


?LOADED ( | <name> --- f1 ) NEEDS
?已加載 （ |<name> --- f1 ）需要
Have we already loaded the file specified by NAME? Return a
我們是否已經載入了 NAME 指定的檔案？傳回
boolean F1 true if we have.
布林值 F1 true 如果我們有的話。


?LOADED, FORTH
?裝上，向前


?LOADING FORTH
?載入中


?MENU-DO HIDDEN
?選單-執行隱藏


?MENUBAR# HIDDEN
?選單列# 隱藏


?MENUKEY FORTH
?菜單鍵向前


?MISSING ( f1 -- ) KERNEL3
?遺失 （ f1 -- ） KERNEL3
Tell user the word does not exist.
告訴使用者該詞不存在。


?MOUSEINIT HIDDEN
?MOUSEINIT 隱藏


?NEGATE ( n1 n2 --- n3 ) KERNEL1
?否定 （ n1 n2 --- n3 ） KERNEL1
Negate the second element if the top is negative.
如果頂部為負數，則否定第二個元素。


?NOLOADED, FORTH
?空載，向前


?NOUSER FORTH
?沒有人前進


?OPEN.ERROR FORTH
?開。錯誤


?PAGE ( --- ) UTILS
?頁面 （ --- ） 實用程式
Output a page command if we are not already on the top of a new
如果我們尚未在新的頂部，請輸出頁面命令
page.
頁。


?PAGE-DOWN HIDDEN
?向下翻頁隱藏


?PAGE-UP HIDDEN
?頁面隱藏


?PATH-WINDOW HIDDEN
?路徑視窗隱藏


?PREPEND.VPATH ( a1 --- a1 ) PATHSET
?預備。VPATH（ a1 --- a1 ）路徑集
Given a handle a1, prepend to the name in the handle, the
給定一個控制碼 a1，在控制碼中的名稱前面加上，
current VIEW directory path.
目前的 VIEW 目錄路徑。


?PRINTER.READY ( --- f1 ) KERNEL2
?印刷者。就緒 （ --- f1 ） KERNEL2
A DEFERed word that returns a boolean flag true if the system
如果系統
printer is online and ready for printing. This word gets
印表機已上線並準備好列印。這個詞得到
defered to TRUE if we are printing to a disk file.
如果我們要列印到磁碟檔案，則延遲為 TRUE。


?REPMAC HIDDEN
?REPMAC 隱藏


?REPMAC1 HIDDEN
?REPMAC1 隱藏


?SCROLL-LEFT HIDDEN
?向左捲動隱藏


?SCROLL-RIGHT HIDDEN
?向右捲動隱藏


?SCROLL-DN HIDDEN
?SCROLL-DN 隱藏


?SCROLL-UP HIDDEN
?向上捲動隱藏


?SELECT-MENU HIDDEN
?選擇選單隱藏


?SEQRANGE FORTH
?後續


?SET-CURSOR FORTH
?設定游標向前


?SETDIR HIDDEN
?塞特迪爾隱藏


?SHOWSTACK FORTH
?展示堆棧


?STACK ( -- ) KERNEL3
?堆疊 （ -- ） KERNEL3
Check for parameter stack underflow or overflow and issue
檢查參數堆疊下溢或溢位，並發出問題
appropriate error message if detected.
如果偵測到適當的錯誤訊息。


?START/STOPMAC HIDDEN
?啟動/停止 MAC 隱藏


?SYSERROR HIDDEN
?隱藏的系統錯誤


?TOTAL.*
?總。*
?UDEFER.*
?烏德弗。
?DEFER.*
?延。*
?CONSTANT.*
?恆。*
?UDEFER.* FORTH
?烏德弗。
?UVARIABLE.*
?不可變量。
?VARIABLE.*
?不定的。*
?VALUE.*
?價。*
?:.*
?CODE.*
?法典。*
?*.* ( --- ) WORDS
？*.* （ --- ） 字
Test words used by WORDS to recognize a group of words to
測試 WORDS 用來識別一組要識別的單字
display. These are not used by you the user, they are only
獻。這些不是由您用戶使用的，它們只是
available to show you the classes of words you can look at with
可用於向您展示可以查看的單詞類別
WORDS.
言。


?TOTALWORDS FORTH
?總詞


?UNLINK HIDDEN
?取消連結隱藏


?UNTIL ( f1 --- ) KERNEL1
?直到 （ f1 --- ） KERNEL1
A special version of ?BRANCH that is used to mark a return
的特殊版本？BRANCH 的 BRANCH，用來標示傳回
point for the decompiler.
反編譯器的點。


?UPPERCASE ( a1 --- a1 ) KERNEL2
?大寫 （ a1 --- a1 ） KERNEL2
Convert the counted string at a1 to uppercase if CAPS is TRUE.
如果 CAPS 為 TRUE，則將 a1 處的計數字串轉換為大寫。


?USER FORTH
?用戶前進


?VMODE ( --- n1 ) VIDEO
?VMODE （ --- n1 ） 視頻
Read the current video mode from the BIOS. A value of 7 is
從 BIOS 讀取目前的視訊模式。值 7 是
normal for monochrome, and a value of 2 is a CGA board. Also
單色為正常值，值為 2 為 CGA 板。亦
sets the number of columns in the COLS VALUE and the number of
設定 COLS VALUE 中的欄數和
rows in the ROWS VALUE.
ROWS VALUE 中的列。


?W.NAME FORTH
?W.NAME 向前


?W.TEST FORTH
?W.測試前進


?WHILE ( f1 --- ) KERNEL1
?而 （ f1 --- ） KERNEL1
A special version of ?BRANCH that is used to mark a return
的特殊版本？BRANCH 的 BRANCH，用來標示傳回
point for the decompiler.
反編譯器的點。


?WORDTYPE FORTH
?字型第四


@ ( a1 --- n1 ) KERNEL1
@ （ a1 --- n1 ） KERNEL1
Fetch a 16 bit value from addr.
從 addr 取得 16 位元值。


@> ( | <name> -- n1) EQUCOLON
@> ( |<name> -- n1）埃科隆
Fetch the value n1 from the body field of <name> to the stack.
從 的 body 欄位擷取值 n1 <name> 到堆疊。
Typically used to modify a VALUE or VARIABLE. May be used on
通常用來修改 VALUE 或 VARIABLE。可用於
the command line.
命令列。


@L ( seg adr - n1 ) KERNEL2
@L （ seg adr - n1 ） KERNEL2
load word long from seg and adr.
從 SEG 和 ADR 加載 Word long。


@REL>ABS ( CFA --- a1 ) KERNEL4
@REL>ABS（CFA --- a1）KERNEL4
Given CFA the CODE FILED ADDRESS of an F-PC definition, return
給定 CFA F-PC 定義的 CODE FILED ADDRESS，返回
the address a1 of the code function used to perform the
用於執行
definition. This word is normally NOT used on CODE words, it is
定義。這個詞通常不用於 CODE 詞，它是
instead used on COLON definitions, VARIABLES, CONSTANTS,
而是用於 COLON 定義、VARIABLES、CONSTANTS、
VALUES, etc. to locate the actual code function used to perform
VALUES 等來定位用於執行的實際程式碼函數
the selected class of words. This word assumes the first byte
選取的單字類別。此字假設第一個位元組
of the cfa is a JMP or CALL instrunction and is followed
CFA 是 JMP 或 CALL 的規定，並被遵循
immediately by two bytes of RELATIVE address which @REL>ABS
立即由兩個位元組的 RELATIVE 位址，@REL>ABS
converts to an absolute address.
轉換為絕對位址。


A: B: C: D: ( --- ) KERNEL4
A：B：C：D：（ --- ） KERNEL4
Select drive A:, B:, C:, or D: as the default drive.
選取磁碟機 A：、B：、C： 或 D： 作為預設磁碟機。


A; ( ---- ) PASM
一個;( ---- )帕斯姆
Complete the compiling of the current line of assembly
完成當前裝配線的編譯
instructions. This word is normally executed automatically at
說明。這個字通常在
the end of a line of assembly language. The user need only use
彙編語言行的結尾。用戶只需使用
this word when creating MACROS. See PASM for an example of
創建宏指令時這個詞。請參閱 PASM 以取得以下範例
a macro for NEXT.
NEXT 的巨集。


A;! FORTH
一個;！第四


ABORT ( -- ) KERNEL3
中止 （ -- ） KERNEL3
Clear the data stack and QUIT; no message is displayed.
清除資料堆疊並退出;不會顯示任何訊息。


ABORT" ( f1 | <message>" -- ) KERNEL3
ABORT“ （ f1 |<message>“ -- ）KERNEL3
If the flag is true, issue <message> and ABORT.
如果旗標為 true，則發出<message>並中止。


ABS ( n1 --- n2 ) KERNEL1
ABS（ n1 --- n2 ）KERNEL1
Return the absolute value of the 16 bit integer on the stack
傳回堆疊上 16 位整數的絕對值


ADEBUG ( A1 --- ) DEBUG
ADEBUG （ A1 --- ） 調試
Set the CFA=a1 as the current word to be debugged.
將 CFA=a1 設定為要除錯的當前字。


AFT FORTH
向前


AGAIN ( -- ) KERNEL3
再次 （ -- ） KERNEL3
Unconditional jump to just after BEGIN in a BEGIN ... AGAIN
無條件跳到 BEGIN 中 BEGIN 之後......再
loop.
圈。


ALETTER HIDDEN
一個隱藏的字母


ALIAS ( a1 | <name> --- ) UTILS
別名 （ a1 |<name> --- ）公用事業
Define a new header whose CODE FIELD POINTER points to a1. This
定義其 CODE FIELD POINTER 指向 a1 的新標頭。這
word has the effect of creating another name for an existing
Word 具有為現有的
definition, both names will compile the same OLDER word when
定義時，兩個名稱都會編譯相同的 OLDER 單字
compiling. This word has NO EFFECT on CODE space or LIST
編譯。此字對 CODE 空間或 LIST 沒有影響
space.
間。


ALIGN ( -- ) KERNEL3
對齊 （ -- ） KERNEL3
Used to force even addresses. A noop on the 8086.
用於強制偶數地址。8086 上的一個 noop。


ALLOC ( n1 --- n2 n3 n4 ) KERNEL2
分配 （ n1 --- n2 n3 n4 ） KERNEL2
Allocate n1 16 byte units from DOS. Returns n2 the physical
從 DOS 分配 n1 個 16 位元組單位。傳回 n2 實體
segment number of the start of the space allocated, but only if
已配置空間開頭的區段編號，但前提是
the allocate succeeds. returns n3 the largest number of 16
配置成功。傳回 n3 的最大數 16
byte segments that could have been allocated, and n4=8 if the
位元組區段，如果
ALLOC FAILED. If n4 is not 8, then discard n3 and use n2 to
分配失敗。如果 n4 不是 8，則丟棄 n3 並使用 n2 來
point to the allocated space. This space must be accessed with
指向分配的空間。此空間必須透過
the L@, L!, LFILL, CMOVEL> and CMOVEL operators. the returned
L@、L！、LFILL、CMOVEL>和 CMOVEL 運算子。傳回的
value n2 can later be used to DEALLOCate the space back to DOS
值 n2 稍後可用於將空間 DEALLOC 回 DOS
when you are done using it.
當你用完它時。


ALLOT ( n1 -- ) KERNEL3
分配 （ n1 -- ） KERNEL3
Allocate more space in the dictionary.
在字典中分配更多空間。


AND ( n1 n2 --- n3 ) KERNEL1
和 （ n1 n2 --- n3 ） KERNEL1
Returns the bitwise AND of n1 and n2 on the stack.
傳回堆疊上 n1 和 n2 的位元 AND。


ANEW ( | <name> -- ) KERNEL3
新 （ |<name> -- ）KERNEL3
Define A NEW definition <name>. If <name> already exists, then
定義 一個新的定義 <name>。如果<name>已經存在，則
we FORGET it before making the new one. A nice utility to
我們在製作新之前就忘記了它。一個不錯的實用程序
allow re-loading a file again and again for debugging purposes.
允許一次又一次地重新載入檔案以進行偵錯。
I don't know where this first originated, but I learned of it
我不知道這最初起源於哪裡，但我知道了它
from RAY ISAAC at CALOS, a real neat trick.
來自 CALOS 的 RAY ISAAC，這是一個真正巧妙的技巧。


ARRAY FORTH
陣列向前


ARUNSAVE FORTH
阿倫薩維·福斯


ASCII ( | <char> -- n1 ) KERNEL3
ASCII （ |<char> -- n1 ）KERNEL3
Compile the next character in the input stream as a literal
將輸入資料流程中的下一個字元編譯為文字
ASCII integer.
ASCII 整數。


ASSEMBLER ( --- ) KERNEL3
彙編器 （ --- ） KERNEL3
The VOCABULARY that contains all of the assembler definitions.
包含所有組譯器定義的詞彙。


ASSOCIATIVE: HIDDEN
關聯：隱藏


AT ( col row --- ) UTILS
AT （ 列 行 --- ） UTILS
A special defered word that moves the display cursor to the COL
將顯示游標移至 COL 的特殊延遲字組
and ROW specified in preperation for displaying text. The
以及 ROW 在準備中指定以顯示文字。這
system variables #OUT and #LINE are automatically adjusted by
系統變數 #OUT 和 #LINE 會自動調整
this word without your defered function having to keep track of
這個詞無需您的延遲函數
them.
他們。


AT." HIDDEN
在。潛


AT? FORTH
在？第四


ATBL ( --- a1 ) KERNEL2
ATBL （ --- a1 ） KERNEL2
A table of character values 256 bytes in size. The UPC and
字元值的表格大小為 256 個位元組。UPC 和
UPPERCASE words use this table when performing case conversion.
執行大小寫轉換時，大寫單字會使用此表格。
The values in this table can be changed if you want to do some
如果您想要執行一些動作，可以變更此表格中的值
special type of character translation.
特殊類型的字元翻譯。


ATTRIB ( --- a1 ) VIDEO
ATTRIB （ --- a1 ） 視頻
A variable that holds the value of the current display
保存目前顯示值的變數
attributes. The value 7 is the default for normal video.
屬性。值 7 是一般視訊的預設值。


AUTOCLEAR HIDDEN
自動清除隱藏


AUTOEDITOFF ( --- ) EDITERR
AUTOEDITOFF （ --- ） 編輯者
Disable automatic entry into the editor when a compile error
在編譯錯誤時停用自動進入編輯器
occurs. The error message is displayed on the screen but the
發生。錯誤訊息會顯示在畫面上，但
editor is not invoked.
編輯器。


AUTOEDITON ( --- ) EDITERR
AUTOEDITON （ --- ） 編輯者
Turn on the automatic entry into the editor when a compile
在編譯時開啟編輯器的自動輸入
error is detected. The edit cursor is placed in the editor at
偵測到錯誤。編輯游標放置在編輯器中，位於
the error point.
誤差點。


AUTOSAVEON ( --- ) SEDITOR
自動保存 （ --- ） 編輯器
Enable the automatic save of changes to a file after ten
啟用十點後自動儲存檔案變更
minutes of keyboard in-activity. The ten minute delay is
鍵盤活動分鐘數。十分鐘的延遲是
configurable with the VALUE AUTOSAVE-MINUTES. The default mode
可設定值 AUTOSAVE-MINUTES。預設模式
is AUTOSAVEON. See also AUTOSAVEOFF.
是 AUTOSAVEON。另請參閱 AUTOSAVEOFF。


AUTOSAVEOFF ( --- ) SEDITOR
自動保存 （ --- ） 編輯器
Disable the automatic saving of changes after a period of
停用一段時間後自動儲存變更
keyboard in-activity. You can walk away from the keyboard
鍵盤活動中。您可以離開鍵盤
forever and the editor will NEVER automatically save your
永遠，編輯器永遠不會自動保存您的
changes.
變化。


AUTOSAVE-MINUTES ( --- n1 ) SEDITOR
自動保存分鐘數 （ --- n1 ） 編輯器
A VALUE which returns the number of minutes SED will wait after
傳回 SED 等待的分鐘數的 VALUE
the last keystroke before automatically saving any changes you
自動儲存任何變更之前的最後一次擊鍵
may have made to the current edit file.
可能已對目前的編輯檔案進行。


B ( --- ) VIEW
B （ --- ） 檢視
Backup 16 lines in current file and display a section of the
備份目前檔案中的 16 行，並顯示
file.
檔案。


B/FNAM HIDDEN
B/FNAM 隱藏


B/HCB ( --- n1 ) pronounced bytes per handle control block
B/HCB （ --- n1 ） 每個句柄控制區塊的發音位元組
HANDLES
手柄
A CONSTANT that returns the number of byte used to make a
傳回用於製作
handle with the HANDLE word.
handle 與 HANDLE 字組。


B>SEC ( D1 - N1 ) TIMER
B>SEC （ D1 - N1 ） 計時器
Convert the BINARY time d1 to seconds. Overflows at 18 hours.
將 BINARY 時間 d1 轉換為秒。18 小時溢出。


B>T ( d1 --- d2 ) TIMER
B>T （ d1 --- d2 ） 定時器
Convert the d1 BINARY time value to d2 the DOS time format.
將 d1 BINARY 時間值轉換為 d2 DOS 時間格式。


BACK-UP FORTH
後備


BACKSPACES ( n1 --- ) KERNEL2
退格鍵 （ n1 --- ） KERNEL2
Send a set of Backspaces to the terminal.
將一組退格鍵傳送到終端機。


BACKUPOFF ( --- ) EDITSTUF
BACKUPOFF （ --- ） 編輯
Turn off the feature of SED to automatically create backup
關閉 SED 功能以自動建立備份
copies of your files when you start an edit. You will be
開始編輯時的檔案副本。你會是
editing the original and ONLY copy of your file, and will NOT
編輯檔案的原始和唯一副本，並且不會
be able to go back to the previous edited version of a file you
能夠返回您之前編輯的文件版本
change. This switch is normally used only when working on
變。此開關通常僅在工作時使用
floppys where there is no room for a backup copy.
沒有空間放置備份副本的軟碟。


BACKUPON ( --- ) EDITSTUF
BACKUPON （ --- ） 編輯
Enable the feature of SED to automatically create backup copies
啟用 SED 的功能以自動建立備份副本
of your files when you start an edit. This is the normal mode,
開始編輯時的檔案。這是正常模式，
and allows you to go back to the previous edited version of a
並允許您返回到先前編輯的版本
changed file if a serious error occurs.
如果發生嚴重錯誤，則已更改檔案。


BADMOUSE HIDDEN
壞老鼠隱藏


BASE ( --- a1 ) KERNEL2
基礎 （ --- a1 ） KERNEL2
The current numeric base for number input output.
數字輸入輸出的目前數值基數。


BCR ( --- ) BOXTEXT
BCR （ --- ） 方框文字
pronounced box carraige return.
發音為盒式卡拉格返回。
After creating a box on the screen with BOX&FILL, the cursor is
使用 BOX&FILL 在螢幕上建立方塊後，游標為
placed automatically on the first empty line inside the box.
自動放置在框內的第一行空行上。
This word places the cursor down one line and to the left edge
這個字會將游標向下一行放置到左邊緣
inside the box once for each time it is performed. here is an
每次執行時在盒子內一次。這裡有一個
example:
例：
: TESTBOX ( --- ) 20 06
： 測試箱 （ --- ） 20 06
40 10 BOX&FILL
40 10 盒裝和填充
." This is displayed on the first line." BCR
."這顯示在第一行。BCR 的
." This is on the second line." BCR
."這是在第二行。BCR 的
." This is on the third line of the box." ;
."這是在盒子的第三行。


BDOS ( n1 func# --- al ) KERNEL2
BDOS （ n1 func# --- al ） KERNEL2
Load up the registers and do a DOS system call. return the
加載暫存器並執行 DOS 系統調用。傳回
result placed in the A register on the stack.
結果放置在堆疊上的 A 暫存器中。


BDOS2 FORTH
BDOS2 第四


BEEP ( --- ) KERNEL2
嗶嗶聲 （ --- ） KERNEL2
Ring the bell on the terminal by emiting the value 7.
通過發射值 7 來敲響終端上的鈴聲。


BEEPDURATION FORTH
嗶嗶聲持續時間


BEEPFREQ FORTH
嗶嗶聲


BEGIN ( -- ) KERNEL3
開始 （ -- ） KERNEL3
Used in the form BEGIN ... AGAIN,
以 BEGIN ...再
or BEGIN ... flag UNTIL,
或 BEGIN ...標記直到，
or BEGIN ... flag WHILE ... REPEAT
或 BEGIN ...標誌 WHILE ...重


BEHEAD FORTH
斬首


BEHEADABLE FORTH
可斬首


BELL ( --- c1 ) KERNEL2
貝爾 （ --- c1 ） KERNEL2
Return the value 7, an Ascii BELL char.
傳回值 7，一個 Ascii BELL 字元。


BETWEEN ( n1 n2 n3 --- f1 ) KERNEL1
之間 （ n1 n2 n3 --- f1 ） KERNEL1
Return true if n2 <= n1 <= n3, otherwise false.
如果 n2 <= n1 <= n3，則傳回 true，否則傳回 false。


BGSTUFF ( --- ) KERNEL2
BGSTUFF （ --- ） KERNEL2
A DEFERed word chain, that contains operations that need to be
DEFERed 字鏈，其中包含需要
performed periodically while waiting for a key from the
在等待來自
keyboard. Words included in the chain must preserve and restore
鍵盤。鏈中包含的單詞必須保存和恢復
the stacks to the state they found them prior to their
堆疊到他們之前發現它們的狀態
execution. Words in the chain must also return quickly to
死刑。鏈條中的單詞也必須快速返回
prevent excessive delays in user response.
防止使用者回應過度延遲。


BIG-CURSOR ( --- ) IBMCURSR
BIG-CURSOR （ --- ） IBMCURSR
Set the cursor to a block cursor.
將游標設定為區塊游標。


BIOSBKSAVE FORTH
BIOSBKSAVE 前進


BIOSCHAR ( --- a1 ) KERNEL2
BIOSCHAR （ --- a1 ） KERNEL2
A VARIABLE that holds the keycode and scancode of the most
一個 VARIABLE，它保存了大多數的密鑰碼和掃描碼
recent BIOSKEY?.
最近的生物？


BIOSKEY ( --- n1 ) KERNEL2
BIOSKEY （ --- n1 ） KERNEL2
Wait for a key to be pressed on the keyboard, and return the
等待鍵盤上的按鍵被按下，然後返回
key as n1 containing the ascii code in the lower byte and the
key 作為 n1，包含下部位元組中的 ASCII 代碼，而
scan clde in the upper byte.
掃描 clde 在上位元組中。


BIOSKEY? ( --- f1 ) KERNEL2
生物鍵？（ --- f1 ）KERNEL2
Returns a true flag if a key has been pressed and is waiting to
如果已按下按鍵並等待
be picked up. You can in effect look ahead at the key by
被撿起來。實際上，您可以通過以下方式向前看鑰匙
looking at the variable BIOSCHAR which holds the scanned key
查看保存掃描密鑰的變量 BIOSCHAR
that is waiting.
那就是等待。


BIOSKEYVAL ( --- a1 ) KERNEL2
BIOSKEYVAL （ --- a1 ） KERNEL2
A VARIABLE that holds the actual bois key value returned on the
一個 VARIABLE，它保存在
most recent BIOSKEY operation. This value contains both the
最近的 BIOSKEY 操作。此值包含
ascii value and the scancode for the key.
ASCII 值和金鑰的掃描碼。


BL ( --- c1 ) KERNEL2
BL （ --- c1 ） KERNEL2
Return hex 20, decimal 32 the value of an Ascii space.
傳回十六進位 20，十進制 32 Ascii 空間的值。


BLACK ( --- n1 ) COLOR
黑色 （ --- n1 ） 顏色
A CONSTANT that returns the value for color black used on a
一個 CONSTANT，傳回用於
color monitor.
彩色顯示器。


BLACK-ON-WHITE ( --- ) MONOCROM
白底黑字 （ --- ） 單色
Select BLACK characters on a WHITE background rather than the
選取白色背景上的黑色字元，而不是
normal WHITE on BLACK. This is mostly useful for true white
黑底白字正常。這對於純白色最有用
phosphor monitors.
熒光粉監視器。


BLANK ( a1 n1 --- ) KERNEL2
空白 （ a1 n1 --- ） KERNEL2
Fill the string with blanks
用空白填滿字串


BLANK.COLOR FORTH
空白的。色彩四射


BLANKING FORTH
空白前進


BLANKOFF ( --- ) SAVESCR
BLANKOFF （ --- ） SAVESCR
Disable blanking when typing to the display in fast mode on a
在快速模式下對顯示器鍵入時禁用空白
color monitor. The CGA board needs blanking to reduce the snow
彩色顯示器。CGA 板需要下料以減少積雪
effect, but EGA/VGA do not.
效果，但 EGA/VGA 沒有。


BLANKON ( --- ) SAVESCR
布蘭孔 （ --- ） SAVESCR
Enable blanking when typing to the display in fast mode on a
在快速模式下對顯示器鍵入時啟用空白
color monitor. The CGA board needs this to reduce the snow
彩色顯示器。CGA 董事會需要它來減少降雪
effect, but EGA/VGA do not.
效果，但 EGA/VGA 沒有。


BLINE HIDDEN
布萊恩隱藏


BLUE ( --- n1 ) COLOR
藍色 （ --- n1 ） 顏色
Return the color value for BLUE.
傳回 BLUE 的色彩值。


BODY> ( pfa -- cfa ) KERNEL3
身體> （ pfa -- cfa ） KERNEL3
Go from body address pfa to code field address cfa.
從正文地址 pfa 轉到代碼字段地址 cfa。


BOOT ( --- ) KERNEL4
啟動 （ --- ） KERNEL4
The very first high level word executed during cold start.
在冷啟動期間執行的第一個高階字。


BOUNDS ( a1 n1 --- a2 a3 ) KERNEL1
邊界 （ a1 n1 --- a2 a3 ） KERNEL1
Given address a1 and length n1, return a2 and a3 the boundry
給定位址 a1 和長度 n1，傳回 a2 和 a3 邊界
addresses for DO ... LOOP.
DO 的地址 ...圈。


BOX ( x y x' y' --- ) BOXTEXT
BOX （ x y x' y' --- ） BOXTEXT
Draws a box like BOX&FILL, but does not fill the box with
繪製像 BOX&FILL 這樣的方塊，但不會以
blanks. See also BOX&FILL.
空白。另請參閱 BOX&FILL。


BOX&FILL ( x y x' y' --- ) BOXTEXT
BOX&FILL （ x y x' y' --- ） BOXTEXT
Draw a box on the screen from x,y the top left, to x',y' the
在螢幕上從左上角的 x，y 到 x'，y' 畫一個框
lower right and clear the inside to blanks. the cursor is then
右下角，將內部清理成空白。然後游標是
placed in the upper left corner of the box in preperation for a
放置在盒子的左上角，以準備一個
." . Use BCR to perform a BOX CR down and to the left edge of
." .使用 BCR 向下和左邊緣執行 BOX CR
the box for the next line.
下一行的方框。


BRANCH ( --- ) KERNEL1
分行 （ --- ） KERNEL1
Performs an unconditional branch. Notice that we are using
執行無條件分支。請注意，我們正在使用
absolute addresses insead of relative ones. (fast)
絕對地址 insead 的相對地址。（快）


BREAK FORTH
突破


BROWN ( --- n1 ) COLOR
棕色 （ --- n1 ） 顏色
Return the color value for BROWN.
傳回 BROWN 的色彩值。


BROWSE FORTH
瀏覽


BS ( --- c1 ) KERNEL2
學士 （ --- c1 ） KERNEL2
Return the value 8, an Ascii Back Space.
傳回值 8，即 ASCII 退格空間。


BS-IN FORTH
第二步


BUFSIZE-INIT FORTH
BUFSIZE-初始化


BUG ( --- ) VOCABS
BUG （ --- ） 詞彙
vocabulary stack -> ( voc1 voc2 -- bug voc2 | current = ? )
詞彙堆疊 -> （ voc1 voc2 -- bug voc2 | current = ？ ）
The BUG vocabulary, sets CONTEXT to BUG when executed.
BUG 詞彙在執行時將 CONTEXT 設定為 BUG。


BUILD-DATE FORTH
構建日期


BUILD-HM FORTH
構建-HM FORTH


BUILD-SH FORTH
向前建造


BUILD-TIME FORTH
構建時間


BX HIDDEN
BX 隱藏


BY HIDDEN
由 HIDDEN


BYE ( -- ) KERNEL4
再見 （ -- ） KERNEL4
Returns control to DOS. Performs the defered word BYEFUNC
將控制權傳回給 DOS。執行延遲的單字 BYEFUNC
before actually leaving.
在真正離開之前。


BYEFUNC ( --- ) KERNEL4
BYEFUNC （ --- ） KERNEL4
A defered word which normally contains NOOP, provided wo you
一個通常包含 NOOP 的延遲詞，前提是你
can specify a function to be performed before leaving back to
可以指定在離開回來之前要執行的功能
DOS.
做。


BYTES_SRCH HIDDEN
BYTES_SRCH 隱藏


C! ( b1 a1 --- ) KERNEL1
C!（ b1 a1 --- ）KERNEL1
Store 8 bit value b1 at address a1.
在位址 a1 儲存 8 位元值 b1。


C!L ( b1 seg a1 --- ) KERNEL2
C！L （ b1 seg a1 --- ） KERNEL2
Store the 8 bit value b1 into the long address specified by seg
將 8 位元值 b1 儲存到 seg 指定的長位址中
and a1.
和 a1。


C+! ( b1 a1 --- ) KERNEL1
C+！（ b1 a1 --- ）KERNEL1
Increment the byte value at a1 by n1. This is equivalent the
將 a1 的位元組值遞增 n1。這相當於
following: "DUP C@ ROT + SWAP C!" but much faster.
以下：“DUP C@ ROT + SWAP C！”，但速度要快得多。


C, ( char -- ) KERNEL3
C， （ char -- ） KERNEL3
Compile the 8 bit value char into the CODE area. The next
將 8 位值 char 編譯到 CODE 區域中。下一個
available byte location is used as specified by DP, and DP is
可用的位元組位置會依 DP 所指定使用，而 DP 是
then incremented. Same as , except uses an 8-bit value.
然後遞增。與 相同，但使用 8 位值。


C.ID FORTH
C.ID 向前


C@ ( a1 --- b1 ) KERNEL1
Fetch the 8 bit value b1 from addrress a1.
從 addrress a1 取得 8 位元值 b1。


C@L ( seg a1 - b1 ) KERNEL2
C@L （ seg a1 - b1 ） KERNEL2
Push the 8 bit value b1 located at the long address specified
推送位於指定長位址的 8 位元值 b1
by seg and a1.
由 SEG 和 A1 提供。


CALLS ( | <name> --- ) REF
通話 （ |<name> --- ）參考文獻
An ALIAS for REF.
REF 的別名。


CAPS ( --- a1 ) KERNEL2
大寫 （ --- a1 ） KERNEL2
If true, then convert names to upper case
如果為 true，則將名稱轉換為大寫


CAPS-COMP ( a1 a2 n1 --- f1 ) KERNEL2
CAPS-COMP （ a1 a2 n1 --- f1 ） KERNEL2
The code on this screen handles the case where case is not
此畫面上的程式碼會處理大小寫不是的情況
significant. Each character is converted to upper case before
有意思的。每個字元都會在之前轉換為大寫
the comparison is made. Thus, lower case a and upper case A
進行了比較。因此，小寫 a 和大寫 A
are considered identical.
被認為是相同的。


CASE ( -- ) CASE
案例 （ -- ） 案例
Start a CASE statment, as follows:
啟動 CASE 陳述式，如下所示：


CC-REST HIDDEN
CC-REST 隱藏


CC-SAVE HIDDEN
CC-SAVE 隱藏


CCR FORTH
CCR 福斯


CD ( | <filespec> --- ) EXEC
光碟 （ |<filespec> --- ）執行委員會
A pseudonym for CHDIR. See also CHDIR.
CHDIR 的化名。另見 CHDIR。


CDATE FORTH
凱達特·福斯


CFA_VIEW FORTH
CFA_VIEW 向前


CFGHNDL FORTH
CFGHNDL 福斯


CHAR FORTH
查爾福斯


CHARBUTTON FORTH
查爾巴頓前進


CHARCOL FORTH
查科爾·福斯


CHARLINE FORTH
查琳·福斯


CHARREAD ( --- c1 ) SEQREAD
CHARREAD （ --- c1 ） 後續
Read a character c1 from the current file.
從目前檔案讀取字元 c1。


CHCOL FORTH
奇科爾·福斯


CHDIR ( | <filespec> --- ) EXEC
CHDIR （ |<filespec> --- ）執行委員會
Change the directory to the directory specified by filespec.
將目錄變更為 filespec 指定的目錄。


CHROW FORTH


CLEARMEM HIDDEN
CLEARMEM 隱藏


CLEAR_LABELS FORTH
CLEAR_LABELS 向前


CLOSE ( --- ) SEQREAD
關閉 （ --- ） 順序
A pseudonym for SEQDOWN. See also SEQDOWN.
SEQDOWN 的化名。另請參閱 SEQDOWN。


CLOSEALL FORTH
關閉全部向前


CLR-COLON HIDDEN
CLR-COLON 隱藏


CLR-CONSTANT HIDDEN
CLR-常數隱藏


CLR-DEFER HIDDEN
CLR-延遲隱藏


CLR-HCB ( a1 --- ) HANDLES
CLR-HCB （ a1 --- ） 控點
Clear the handle a1 to empty, it is erased and marked as a
清除手柄 a1 清空，它被擦除並標記為
closed file.
已關閉的檔案。


CLR-OTHER HIDDEN
CLR-其他隱藏


CLR-UDEFER HIDDEN
CLR-UDEFER 隱藏


CLR-UVARIABLE HIDDEN
CLR-U 變數隱藏


CLR-VALUE HIDDEN
CLR-值隱藏


CLR-VARIABLE HIDDEN
CLR-變數隱藏


CLS ( --- ) UTILS
CLS （ --- ） 公用事業
An ALIAS for DARK.
DARK 的別名。


CMDBUF HIDDEN
CMDBUF 隱藏


CMDLEN HIDDEN
CMDLEN 隱藏


CMDPATH HIDDEN
CMDPATH 隱藏


CMOVE ( a1 a2 n1 --- ) KERNEL1
CMOVE （ a1 a2 n1 --- ） KERNEL1
Move a set of bytes from the from address to the to address.
將一組位元組從 from 位址移至 to 位址。
The number of bytes to be moved is count. The bytes are moved
要移動的位元組數是 count。位元組會移動
from low address to high address, so overlap is possible and in
從低位址到高位址，因此重疊是可能的，並且在
fact sometimes desired.
事實有時是需要的。


CMOVE> ( a1 a2 n1 --- ) KERNEL1
CMOVE> （ a1 a2 n1 --- ） KERNEL1
The same as CMOVE above except that bytes are moved in the
與上面的 CMOVE 相同，只是位元組在
opposite direction, ie from high addresses to low addresses.
相反的方向，即從高地址到低地址。


CMOVEL ( sseg sptr dseg dptr cnt -- ) KERNEL2
CMOVEL （ sseg sptr dseg dptr cnt -- ） KERNEL2
Move the character block long from source seg sseg and sptr, to
將字元區塊從來源 seg sseg 和 sptr 移至
destination seg dseg and dptr for length count.
目標 seg dseg 和 dptr 用於長度計數。


CMOVEL> ( from-seg from-offset to-seg to-offset length --- ) KERNEL2
CMOVEL> （ from-seg from-offset to-seg to-offset length --- ） KERNEL2
Move length of data from from-seg and from-offset to to-seg and
將資料長度從 from-seg 和 from-offset 移至 to-seg 和
to-offset. If the move crosses a 64k segment boundry the
抵消。如果移動越過 64k 區段邊界，則
results are UN-PREDICTABLE.
結果是不可預測的。


CNHASH ( cfa -- ya ) KERNEL3
CNHASH （ cfa -- ya ） KERNEL3
Given CFA, get pointer into >NAME hash table in YSEG.
給定 CFA，取得指向 YSEG 中 >NAME 雜湊表的指標。


CNSRCH ( cfa ya maxya -- nfa failf ) KERNEL3
CNSRCH （ cfa ya maxya -- nfa failf ） KERNEL3
Search for CFA between YA and MAXYA in YSEG. Return NFA and
在 YSEG 中搜尋 YA 和 MAXYA 之間的 CFA。傳回 NFA 和
failure flag.
失敗旗標。


CNT ( --- a1 ) DEBUG
CNT （ --- a1 ） 調試
How many times thru debug next
接下來通過調試多少次


CODE ( | <name> --- ) PASM
代碼 （ |<name> --- ）帕斯姆
Define <name> as a new code definition. Assembly language
定義<name>為新的程式碼定義。組合語言
follows, terminated by END-CODE.
後面，以 END-CODE 終止。


CODECOLOR HIDDEN
CODECOLOR 隱藏


COLD ( -- ) KERNEL4
冷 （ -- ） KERNEL4
The high level cold start code. For ordinary forth, BOOT should
高階冷啟動程式碼。對於普通的 forth，BOOT 應該
initialize and pass control to QUIT.
初始化並將控制權傳遞給 QUIT。


COLONCOLOR HIDDEN
冒號顏色隱藏


COLOR-CLASS HIDDEN
顏色類別隱藏


COLOR-INFO FORTH
顏色信息


COLORIZEON FORTH
著色在前


COLORIZEOFF FORTH
著色離開


COLORIZE-INIT FORTH
著色-初始化


COLORIZE FORTH
著色


COLORSET FORTH
顏色設定


COLS ( --- n1 ) VIDEO
COLS （ --- n1 ） 視頻
A VALUE initialized at boot time that returns the number of
在開機時初始化的 VALUE，傳回
screen columns on the current display, typically in the range
目前顯示上的螢幕欄，通常在
40 to 132. Normally 80, but you should use this value along
40 至 132。通常為 80，但您應該同時使用此值
with ROWS to make your applications forgiving of other display
使用 ROWS 使您的應用程序能夠容忍其他顯示
modes.
模式。


COLSEG HIDDEN
COLSEG 隱藏


COMMAND.BUF FORTH
令。布夫·福斯


COMMENT$ FORTH
評論$ FORTH


COMMENT: ( --- ) COMMENT
評論：（---）評論
Start a multi-line comment. Patches <comment:> into RUN, it
開始多行註解。修補程式 <comment：> 到 RUN 中，它
then reads and throws away lines until "comment;" is
然後閱讀並丟棄行，直到“評論”;
encountered.
遇到了。


COMP ( a1 a2 n1 --- f1 ) KERNEL2
COMP （ a1 a2 n1 --- f1 ） KERNEL2
This performs a string compare. If the two strings are equal,
這會執行字串比較。如果兩個字串相等，
then COMPARE returns 0. If the two strings differ, then
則 COMPARE 傳回 0。如果兩個字串不同，則
COMPARE returns -1 or +1. -1 is returned if string 1 is less
COMPARE 傳回 -1 或 +1。如果字串 1 較小，則傳回 -1
than string 2. +1 is returned if string 1 is greater than
比字符串 2。如果字串 1 大於
string 2. All comparisons are relative to ASCII order.
字串 2.所有比較都是相對於 ASCII 順序的。


COMPARE ( a1 a2 n1 --- f1 ) KERNEL2
比較 （ a1 a2 n1 --- f1 ） KERNEL2
Performs a string compare. If CAPS is true, characters from
執行字串比較。如果 CAPS 為 true，則來自
both strings are converted to upper case before comparing.
在比較之前，這兩個字串都會轉換為大寫。


COMPILE ( | <name> -- ) KERNEL3
編譯 （ |<name> -- ）KERNEL3
Compile the (typically not-immediate) following word <name>
編譯後面的單字 <name>（通常不是立即的）
when this definition executes. Name is later compiled into the
執行此定義時。名稱稍後會編譯成
LIST dictionary space.
LIST 字典空間。


COMSPEC$ ( --- a1 ) ENVIRON
COMSPEC$ （ --- a1 ） 環境
The handle used to hold the COMSPEC string. I.e. COMMAND.COM
用來保存 COMSPEC 字串的控制碼。即 COMMAND.COM


COMSPEC@ ( --- ) ENVIRON
COMSPEC@ （ --- ） 環境
Read the environment string, and extrac the COMSPEC parameter.
讀取環境字串，並移出 COMSPEC 參數。
the COMSPEC is inserted in the COMSPEC$ handle.
COMSPEC 會插入 COMSPEC$ 控點中。


CONHNDL ( --- a1 ) SEQREAD
CONHNDL （ --- a1 ） 後續
The handle used to send characters to the console when DOS I/O
DOS I/O 時用來將字元傳送至主控台的句柄
is being used.
正在使用。


CONSOLE ( c1 --- ) KERNEL2
控制台 （ c1 --- ） KERNEL2
Send character c1 to the console display.
將字元 c1 傳送至主控台顯示畫面。


CONSOLEL FORTH
控制台前進


CONSTANT ( n1 | <name> -- ) KERNEL3
常數 （ n1 |<name> -- ）KERNEL3
A defining word that creates constants. At runtime the value of
一個創建常數的定義詞。在執行階段，的值
the constant is placed on the stack.
常數會放置在堆疊上。


CONSTANTCOLOR HIDDEN
恆定顏色隱藏


CONTEXT ( --- a1 ) KERNEL2
上下文 （ --- a1 ） KERNEL2
The array specifying the search order.
指定搜尋順序的陣列。


CONTEXTONLY FORTH
上下文僅向前


CONTINUE FORTH
繼續前進


CONTROL ( <char> -- n1 ) KERNEL3
控制 （ <char> -- n1 ） KERNEL3
Compile the next character in the input stream as a literal
將輸入資料流程中的下一個字元編譯為文字
ASCII Control Character.
ASCII 控制字元。


CONTYPEL FORTH


CONVERT ( +d1 a1 --- +d2 a2 ) KERNEL2
轉換 （ +d1 a1 --- +d2 a2 ） KERNEL2
Starting with the unsigned double number ud1 and the string at
從無符號雙精度 ud1 和
adr1, convert the string to a number in the current base. Leave
adr1，則將字串轉換為目前基數中的數字。離
result and address of unconvertable digit on stack.
堆疊上不可轉換數字的結果和位址。


COPY ( <filespec> --- ) EXEC
複製 （ <filespec> --- ） 執行
Perform a DOS COPY with the filespec following the COPY
使用 COPY 後面的 filespec 執行 DOS COPY
command.
令。


COUNT ( a1 --- a2 n1 ) KERNEL2
計數 （ a1 --- a2 n1 ） KERNEL2
Given the address on the stack, returns the address plus one
給定堆疊上的位址，傳回位址加 1
and the byte at that address. Useful for strings.
以及該位址的位元組。對字串很有用。


COUNTL FORTH
數到這裡


CR ( --- ) KERNEL2
CR （ --- ） KERNEL2
Typically set to CRLF, above. PR-STAT Return printer status, if
通常設定為 CRLF，如上所示。PR-STAT 傳回印表機狀態，如果
implemented, else TRUE (PRINT) The value of the DEFERRED word
implemented，否則 TRUE （PRINT） DEFERRED 字的值
EMIT when you want to send a character to the printer.
當您想要將字元傳送至印表機時發出。


CR-IN FORTH
CR-第四


CRASH ( -- ) KERNEL3
崩潰 （ -- ） KERNEL3
Default routine called by execution vectors.
執行向量呼叫的預設常式。


CREATE ( | <name> -- ) KERNEL3
創建 （ |<name> -- ）KERNEL3
Make a header for the next word in the input stream.
為輸入流中的下一個單詞製作標頭。


CRESET ( n1 a1 --- ) KERNEL1
CRESET （ n1 a1 --- ） KERNEL1
Set the contents of a1 so the the bits that are 1 in n1 are
設定 a1 的內容，以便 n1 中 1 的位元
zero in addr. Equivalent to DUP C@ ROT NOT AND SWAP C!
地址為零。相當於 DUP C@ ROT NOT 和 SWAP C！


CRLF ( --- ) KERNEL2
CRLF （ --- ） KERNEL2
Sends a carriage return line feed sequence.
傳送回車換行順序。


CRLF>BL'S FORTH
CRLF>BL 的第四個


CROWS ( --- n1 ) VIDEO
烏鴉 （ --- n1 ） 視頻
A VALUE initialized at boot time that returns the number of
在開機時初始化的 VALUE，傳回
cursor rows for a character. Used by the system when setting
游標列。系統在設定時使用
the NORMAL or BIG cursor.
NORMAL 或 BIG 游標。


CRTAB ( --- ) DECOM
CRTAB （ --- ） DECOM
Do a carraige return and a TAB of the current TABSIZE.
執行 carraige 返回和當前 TABSIZE 的 TAB。


CRUNSAVE FORTH
克倫塞福斯


CSET ( n1 a1 --- ) KERNEL1
CSET （ n1 a1 --- ） KERNEL1
Set the contents of a1 so that the bits that are 1 in n1 are
設定 a1 的內容，讓 n1 中 1 的位元
also 1 in addr. Equivalent to DUP C@ ROT OR SWAP C!
還有 1 個在 addr。相當於 DUP C@ ROT 或 SWAP C！


CSP ( --- a1 ) KERNEL2
CSP （ --- a1 ） KERNEL2
Used for compile time error checking.
用於編譯時錯誤檢查。


CTIME FORTH
CTIME 福斯


CTOGGLE ( a1 n1 --- ) KERNEL1
CTOGGLE （ a1 n1 --- ） KERNEL1
Flip the bits in a1 by the value n. Equivalent to DUP C@ ROT
將 a1 中的位翻轉值 n。相當於 DUP C@ ROT
XOR SWAP C!
異或交換 C！


CTRLBKSAVE FORTH
CTRLBK 儲存


CURFL HIDDEN
CURFL 隱藏


CURFLSAVE HIDDEN
隱藏的 CURFLSAVE


CURMAC HIDDEN
庫爾馬克隱藏


CURPOINTER ( handle --- double-current ) SEQREAD
CURPOINTER （ handle --- double-current ） SEQREAD
Return the double-current offset into file handle.
將雙電流位移傳回檔案句柄。


CURRENT ( --- a1 ) KERNEL2
電流 （ --- a1 ） KERNEL2
New words are added to the CURRENT vocabulary.
新單詞被添加到當前詞彙表中。


CURSOR-ON ( --- ) IBMCURSR
CURSOR-ON （ --- ） IBMCURSR
Turn the cursor back on.
重新開啟游標。


CURSOR-OFF ( --- ) IBMCURSR
CURSOR-OFF （ --- ） IBMCURSR
Turn off the cursor.
關閉游標。


CURSORSET FORTH
柯索塞特·福斯


CURSOR_POS_INIT FORTH


CUT/COPY_FILE FORTH
切/COPY_FILE 向前


CYAN ( --- n1 ) COLOR
青色 （ --- n1 ） 顏色
Return the color value of CYAN.
傳回 CYAN 的色彩值。


D+ ( d1 d2 --- d3 ) KERNEL1
D+ （ d1 d2 --- d3 ） KERNEL1
Add the two double precision numbers on the stack and return
將堆疊上的兩個雙精度數字相加並傳回
the result as a double precision number.
結果為雙精度數字。


D+! FORTH
D+！第四


D- ( d1 d2 --- d3 ) KERNEL1
D- （ d1 d2 --- d3 ） KERNEL1
Subtract the two double precision numbers.
減去兩個雙精度數字。


D. ( d1 --- ) KERNEL2
D. （ d1 --- ） KERNEL2
Output as a signed double number with a trailing space.
輸出為帶有尾端空格的帶正負號雙精度。


D.2W FORTH
D.2W 第四


D.M.Y ( --- ) TIMER
D.M.Y（---）計時器
Select the date format Day.Month.Year for all calendar
選取所有行事曆的日期格式 Day.Month.Year
operations.
操作。


D.R ( d1 n1 --- ) KERNEL2
D.R （ d1 n1 --- ） KERNEL2
Output as a signed double number right justified.
輸出為右對齊的帶正號雙對齊。


D0= ( d1 --- f1 ) KERNEL1
D0= （ d1 --- f1 ） KERNEL1
Compare the top double number to zero. True if d = 0
將頂部的雙倍數字與零進行比較。如果 d = 0 則為 True


D2* ( d1 --- d2 ) KERNEL1
D2* （ d1 --- d2 ） KERNEL1
32 bit left shift.
32 位左移。


D2/ ( d1 --- d2 ) KERNEL1
D2/ （ d1 --- d2 ） KERNEL1
32 bit arithmetic right shift. Equivalent to divide by 2.
32 位算術右移。相當於除以 2。


D: ( --- ) KERNEL4
D：（ --- ） KERNEL4
Select drive A:, B:, C:, or D: as the default drive.
選取磁碟機 A：、B：、C： 或 D： 作為預設磁碟機。


D< ( d1 d2 --- f1 ) KERNEL1
D< （ d1 d2 --- f1 ） KERNEL1
Compare the top two double numbers. True if d1 < d2
比較前兩個雙倍數字。如果 d1 < d2 為 True


D= ( d1 d2 --- f1 ) KERNEL1
D= （ d1 d2 --- f1 ） KERNEL1
Compare the top two double numbers. True if d1 = d2
比較前兩個雙倍數字。如果 d1 = d2 則為 True


D> ( d1 d2 --- f1 ) KERNEL1
D> （ d1 d2 --- f1 ） KERNEL1
Compare the top two double numbers. True if d1 > d2
比較前兩個雙倍數字。如果 d1 > d2 為 True


DABS ( d1 --- d2 ) KERNEL1
DABS （ d1 --- d2 ） KERNEL1
Return the absolute value of the 32 bit integer on the stack
傳回堆疊上32位元整數的絕對值


DARK ( --- ) UTILS
深色 （ --- ） 實用程式
Clear the screen to black or white depending on the display
根據顯示器將螢幕清除為黑色或白色
mode. See also BLACK-ON-WHITE, and WHITE-ON-BLACK.
方式。另請參閱 BLACK-ON-WHITE 和 WHITE-ON-BLACK。


DBG ( | <name> --- ) DEBUG
DBG （ |<name> --- ）偵錯
Start debugging the word following DBG immediately. See also
立即開始偵錯 DBG 後面的單字。另請參閱
DEBUG.
偵錯。


DBG.S FORTH
DBG。S FORTH


DBGBL HIDDEN
DBGBL 隱藏


DBOFF FORTH
DBOFF 福斯


DBSEG FORTH


DEALLOC ( n1 --- f1 ) KERNEL2
DEALLOC （ n1 --- f1 ） KERNEL2
De-allocate the DOS memory area specified by absolute segment
取消分配絕對段指定的 DOS 記憶體區域
n1. Returns f1 false if all went well, else f1 is an error
註 1.如果一切順利，則傳回 f1 false，否則 f1 是錯誤
code. N1 must be the value passed to Forth when the memory
法典。N1 必須是記憶體
array was originally allocated.
陣列最初已配置。


DEBNEXT FORTH
德布下一個福斯


DEBUG ( | <name> --- ) DEBUG
偵錯 （ |<name> --- ）偵錯
Look up the word following DEBUG, and make it the next word to
查詢 DEBUG 後面的單字，並將其設為下一個單字
be debugged.
被調試。


DEBUGABLE ( --- ) DBGFIX
可調試 （ --- ） DBGFIX
Convert the kernel from inline NEXT to a central NEXT right now
立即將內核從內聯 NEXT 轉換為中央 NEXT
at runtime. This is done in preperation for running the
在運行時。這是為執行
debugger, and is made possible by using a simple form of
debugger，並透過使用簡單的形式
pattern recognition.
模式識別。


DECIMAL ( --- ) KERNEL2
小數 （ --- ） KERNEL2
All subsequent numeric IO will be in Decimal.
所有後續的數字 IO 都會以十進位為單位。


DECIMALBASE FORTH
十進制基數


DECOMSEG@ HIDDEN
DECOMSEG@隱藏


DECOMSEG HIDDEN
DECOMSEG 隱藏


DECR ( a1 -- ) KERNEL1
DECR （ a1 -- ） KERNEL1
Decrement the word at the specified address by 1.
將指定位址的單字遞減 1。


DECR> ( | <name> -- ) EQUCOLON
12 月> （ |<name> -- ）埃科隆
Decrement the body of <name> by one, used to modify the
將主體遞減<name>一，用於修改
following VALUE or VARIABLE.
VALUE 或 VARIABLE 之後。


DEF-RWMODE FORTH
DEF-RW 模式向前


DEFAULT ( --- ) KERNEL2
預設 （ --- ） KERNEL2
Opens the default file per the execute line. This does nothing
按執行行開啟預設檔案。這沒有任何作用
if no file was given.
如果沒有提供文件。


DEFAULT-LIST FORTH
預設清單


DEFAULT-BAR FORTH
預設列


DEFAULT-MCOLUMN FORTH
DEFAULT-M 直欄


DEFAULT-MLINE FORTH
預設-MLINE 向前


DEFAULTSTATE ( --- ) UTILS
DEFAULTSTATE （ --- ） 公用程式
Set the system state to the default values. The effected
將系統狀態設定為預設值。受影響的
variables are BASE, CAPS, TABSIZE, LMARGIN, and RMARGIN.
變數為 BASE、CAPS、TABSIZE、LMARGIN 及 RMARGIN。


DEFBASE FORTH
向前拆除


DEFBUTTON HIDDEN
隱藏式按鈕


DEFCFA FORTH


DEFDIRSPEC$ HIDDEN
DEFDIRSPEC$ 隱藏


DEFER ( | <name> -- ) KERNEL3
延遲 （ |<name> -- ）KERNEL3
Define a vectored execution word. These are initially set to
定義向量化執行字。這些最初設定為
display an error message. They are initialized with IS.
顯示錯誤訊息。它們會以 IS 初始化。


DEFERCOLOR HIDDEN
DEFERCOLOR 隱藏


DEFERS ( <name> --- ) DEFERS
延期 （ <name> --- ） 延期
installs the contents of a defered word in the current
將延遲字的內容安裝在目前
definition being defined. This is used to build a chain of
定義正在定義。這用於建立一個鏈
words to be performed.
要執行的話。


DEFEXT ( --- a1 ) HANDLES
DEFEXT （ --- a1 ） 控點
An array holding the default extention "SEQ".
保留預設延伸模組「SEQ」的陣列。


DEFINED ( -- here 0 | a1 false )KERNEL3
定義 （ -- 這裡 0 | a1 false ）KERNEL3
Look up the next word in the input stream. Return true if it
在輸入資料流程中尋找下一個單字。如果
exists, otherwise false. Maybe ignore case.
存在，否則是錯誤的。也許忽略案例。


DEFINITION-CLASS HIDDEN
定義類別隱藏


DEFINITIONS ( -- ) KERNEL3
定義 （ -- ） KERNEL3
Subsequent definitions will be placed into CURRENT.
後續定義將放入 CURRENT。


DEFMENU FORTH
德夫梅恩·福斯


DEFSAVE FORTH


DEL ( <filespec> --- ) EXEC
DEL （ <filespec> --- ） 執行
Delete the files specified by filespec.
刪除 filespec 指定的檔案。


DEL-IN FORTH
德林·福斯


DELFL HIDDEN
德爾夫爾隱藏


DELIMITER FORTH
分隔符號


DEPTH ( -- n1 ) KERNEL4
深度 （ -- n1 ） KERNEL4
Returns the number of items on the parameter stack.
傳回參數堆疊上的項目數。


DFILE$ FORTH
DFILE$ 向前


DIDPFA HIDDEN
DIDPFA 隱藏


DIGIT ( ??? ) KERNEL2
數字 （ ??? ）KERNEL2
Returns a flag indicating whether or not the character is a
傳回旗標，指出字元是否為
valid digit in the given base. If so, returns converted value
給定基數中的有效數字。如果是，則傳回轉換後的值
and true, otherwise returns char and false.
和 true，否則會傳回 char 和 false。


DIR ( <filespec> --- ) EXEC
DIR （ <filespec> --- ） 執行委員會
Pass the filespec following DIR to DOS and print a directory of
將 DIR 之後的檔案規格傳遞至 DOS 並列印
the matching filespecs.
相符的檔案規格。


DIR.NAME HIDDEN
DIR.NAME 隱藏


DIR>PAD HIDDEN
DIR>PAD 隱藏


DIRATTRIB HIDDEN
DIRATTRIB 隱藏


DIRHNDL HIDDEN
迪爾恩德爾隱藏


DIRINIT HIDDEN
迪里尼特隱藏


DIRROW HIDDEN
迪羅隱藏


DIRSEG HIDDEN
DIRSEG 隱藏


DIRSPEC$ HIDDEN
DIRSPEC$ 隱藏


DISK-ERROR FORTH
磁碟錯誤


DIV0FUNC ( -- ) KERNEL4
DIV0FUNC （ -- ） KERNEL4
FF traps divide by 0 errors, and calls this defered word when
FF 設陷除以 0 錯誤，並在以下情況下呼叫此延遲字
such an error is detected. You can change the contents of this
偵測到此類錯誤。您可以更改此內容
defered words to handle divide by 0 errors in your own program.
在您自己的程式中處理除以 0 錯誤的延遲字。


DIV0SAVE FORTH
DIV0SAVE 向後


DIV0STRT ( -- ) KERNEL4
DIV0STRT （ -- ） KERNEL4
The default function to perform when a DIVIDE by 0 trap occurs.
發生 DIVIDE by 0 設陷時要執行的預設功能。
This routine aborts. A divide by 0 trap calls DIV0FUNC, which
這個例行公事中止了。除以 0 的設陷會呼叫 DIV0FUNC，而
defers to this routine.
遵循這個例行公事。


DIVIDE0 ( status_reg CS IP AX BX CX DX SI BP -- ) KERNEL4
DIVIDE0 （ status_reg CS IP AX BX CX DX SI BP -- ） KERNEL4
The actual entry point from the divide by 0 trap, this word
實際進入點從除以 0 陷阱，這個詞
just calls the deferd word DIV0FUNC. Normally the registers on
只是稱推遲的詞為 DIV0FUNC。通常，寄存器在
the stack are just discarded, but you can install your own
堆疊只是被丟棄，但您可以安裝自己的
routine into DIV0FUNC to handle the divide by 0 error.
常式轉換為 DIV0FUNC 來處理除以 0 錯誤。


DKGRAY ( --- n1 ) COLOR
DKGRAY （ --- n1 ） 顏色
Returns the color for DARK GRAY. Blinks in Background.
傳回 DARK GRAY 的顏色。在背景中閃爍。


DLEN HIDDEN
DLEN 隱藏


DLITERAL ( d# -- ) KERNEL3
DLITERAL （ d# -- ） KERNEL3
Compile the double integer from the stack as a literal.
將堆疊中的雙整數編譯為文字。


DLN ( a1 --- ) DUMP
DLN （ a1 --- ） 傾出
Dump a line, consisting of 16 bytes of hex data followed by 16
傾出一行，由 16 個位元組的十六進位資料組成，後面接著 16
bytes of ascii data.
ASCII 資料的位元組。


DMAX ( d1 d2 --- d3 ) KERNEL1
DMAX （ d1 d2 --- d3 ） KERNEL1
Return the greater of the the top two double numbers.
傳回前兩個雙精度數字中較大的一個。


DMIN ( d1 d2 --- d3 ) KERNEL1
DMIN （ d1 d2 --- d3 ） KERNEL1
Return the lesser of the top two double numbers.
傳回前兩個雙倍數字中較小的一個。


DNEGATE ( d1 d2 --- d3 ) KERNEL1
DNEGATE （ d1 d2 --- d3 ） KERNEL1
Same as NEGATE except for double precision numbers.
與 NEGATE 相同，但雙精度數字除外。


DNEXT FORTH


DO ( limit start -- ) KERNEL3
DO （ 限制開始 -- ） KERNEL3
Initialize a loop structure with index running from start to
初始化一個循環結構，索引從開始到
limit-1. Used in the form DO ... LOOP or DO ... +LOOP
limit-1 的 LIMIT-1 中。以 DO ...循環或 DO ... +循環


DO-DOS FORTH
該做的事


DOAGAIN FORTH
再做一次


DOANY HIDDEN
做任何隱藏


DOASSEM FORTH
多塞姆前進


DOBDEL HIDDEN
多布德爾隱藏


DOBEGIN FORTH
從前開始


DOBUTTON FORTH
向前做


DOCASE FORTH
做案例


DOCOMPILE FORTH
做編譯


DODOWN HIDDEN
DODOWN 隱藏


DOEND HIDDEN
躲藏


DOENDCASE FORTH
多恩德案例


DOENDOF FORTH
多恩多福斯


DOERROR FORTH
做錯誤


DOES> ( -- ) KERNEL3
做嗎> （ -- ） KERNEL3
Specifies the run time of a defining word in high level Forth.
指定高階 Forth 中定義字的執行時間。


DOES? FORTH
是嗎？第四


DOESCOLOR HIDDEN
做顏色隱藏


DOFDEL HIDDEN
多夫德爾隱藏


DOFHELP FORTH
多夫幫助前


DOFUNC FORTH
多芬克·福斯


DOHOME HIDDEN
DOHOME 隱藏


DOINS HIDDEN
隱藏的


DOKEY HIDDEN
DOKEY 隱藏


DOLDEL HIDDEN
多爾德爾隱藏


DOLEFT HIDDEN
DOLEFT 隱藏


DOLF HIDDEN
多爾夫隱藏


DOLISTING FORTH
向前邁進


DOLWORD HIDDEN
隱藏的多爾沃德


DONE ( --- ) EDITSTUF
完成 （ --- ） 編輯
A word that re-enables full screen scrolling if you have left
如果您離開，則重新啟用全螢幕捲動的單字
the editor with a smaller edit window thereby invoking a
編輯器具有較小的編輯視窗，因此呼叫
sub-screen scroll. If you don't understand this, try making
子螢幕捲動。如果你不明白這一點，請嘗試製作
the edit window several lines smaller with Alt-S-W, then leave
編輯視窗使用 Alt-S-W 縮小幾行，然後離開
the editor and notice that only the area below the editor
編輯器並注意，只有編輯器下方的區域
window scrolls.
視窗捲軸。


DONE? ( n1 -- f1 ) KERNEL3
熟？（ n1 -- f1 ）KERNEL3
True if the input stream is exhaused or state doesn't match.
如果輸入資料流程已輸出或狀態不相符，則為 True。


DONFILE HIDDEN
唐菲爾隱藏


DOOTHER FORTH
向前走


DOPGDN HIDDEN
DOPGDN 隱藏


DOPGUP HIDDEN
多普古普隱藏


DOREPEAT FORTH
重複


DORET HIDDEN
多雷特隱藏


DORIGHT HIDDEN
隱藏的


DORWORD HIDDEN
隱藏的 DORWORD


DOS-LINE ( --- a1 ) DEFAULT
DOS-LINE （ --- a1 ） 預設值
The address of where the DOS command line resides.
DOS 命令列所在的位址。


DOS>TIB ( --- ) DEFAULT
DOS>TIB （ --- ） 預設值
Move the DOS command line to the Terminal Input Buffer.
將 DOS 命令列移至終端機輸入緩衝區。


DOSVER ( --- n1 ) KERNEL2
DOSVER （ --- n1 ） KERNEL2
Get DOS version number from DOS, and return it as N1.
從 DOS 取得 DOS 版本號，並傳回為 N1。


DOTAB HIDDEN
DOTAB 隱藏


DOTHEN FORTH
繼續前進


DOUBLE? ( --- f1 ) KERNEL2
雙？（ --- f1 ）KERNEL2
Returns non-zero if period was encountered.
如果遇到句點，則傳回非零。


DOUP HIDDEN
DOUP 隱藏


DOWDEL HIDDEN
道德爾隱藏


DO\CHAR FORTH
向前邁進


DP ( --- a1 ) KERNEL2
DP （ --- a1 ） KERNEL2
Size of dictionary. Next available location.
字典的大小。下一個可用位置。


DPL ( --- a1 ) KERNEL2
DPL （ --- a1 ） KERNEL2
The decimal point location for number input.
數字輸入的小數點位置。


DPSAVED FORTH
DP 已儲存


DPSTART FORTH


DRIVE? ( --- n1 ) UTILS
開？（ --- n1 ）公用事業
Displays the current disk drive in the form A:, B:, C: etc.
以 A：、B：、C： 等格式顯示目前的磁碟機。


DROP ( n1 --- ) KERNEL1
DROP （ n1 --- ） KERNEL1
Throw away the top element of the stack.
丟棄堆疊的頂端元素。


DROP.CONTEXT.I2*+@DUP FORTH
落。上下文。I2*+@DUP 向前


DSBUF FORTH
DSBUF 福斯


DTBUF ( --- a1 ) TIMER
DTBUF （ --- a1 ） 定時器
A buffer used by .DATE and .TIME to build their messages in,
所使用的緩衝區。DATE 和 .是時候將他們的信息構建在其中了，
prior to displaying them.
在顯示它們之前。


DU ( a1 -- addr+64 ) DUMP
DU （ a1 -- addr+64 ） 轉儲
Dump another 4 lines (64 bytes).
再傾出 4 行 （64 位元組）。


DU< ( d1 d2 --- f1 ) KERNEL1
DU< （ d1 d2 --- f1 ） KERNEL1
Performs unsigned comparison of two double numbers.
執行兩個雙精度數的無符號比較。


DUMMYCRS HIDDEN
隱藏的虛擬人


DUMP ( A1 N1 --- ) DUMP
傾出 （ A1 N1 --- ） 傾出
Dump an area of the Code segment.
傾出 Code 區段的區域。


DUMP ( a1 len -- ) KERNEL4
DUMP （ a1 len -- ） KERNEL4
A primitive little dump routine to help you debug after you have
一個原始的小傾印常式，可協助您在
changed the system source and nothing works any more.
更改了系統源，但不再起作用。


DUMPC@ FORTH
DUMPC@向前


DUMPSEG FORTH
轉儲


DUMY$ FORTH
虛擬$ FORTH


DUP ( n1 --- n1 n1 ) KERNEL1
DUP （ n1 --- n1 n1 ） KERNEL1
Duplicate the top element of the stack.
複製堆疊的頂端元素。


DUP>R ( n1 --- n1 ) KERNEL1
DUP>R （ n1 --- n1 ） KERNEL1
Duplicates the value on the parameter stack and pushes it onto
複製參數堆疊上的值，並將其推送到
return stack. It is dangerous to use this randomly!
返回堆疊。隨意使用這個很危險！


E FORTH
E 前進


ECURSOR HIDDEN
ECURSOR 隱藏


ED ( --- ) TOPEDIT
ED （ --- ） TOPEDIT
Enter the editor on the most recent edit line. See also EDITOR
在最近的編輯行上輸入編輯器。另請參閱編輯器


EDIT ( n1 --- ) TOPEDIT
編輯 （ n1 --- ） TOPEDIT
Enter the editor on the current file at line n1. See also
在第 n1 行的當前文件上輸入編輯器。另請參閱
EDITOR
主筆


EDITAFILE FORTH
編輯檔案 FORTH


EDITALL FORTH
編輯所有內容


EDITBUF HIDDEN
EDITBUF 隱藏


EDITFILE FORTH
編輯檔案


EDITOR ( --- ) EDITSTUF
編輯 （ --- ） 編輯
The vocabulary that contains all of the editor words. Normally
包含所有編輯器單字的詞彙。素
you use "line# EDIT", "SED filename" or just "ED" to start the
您使用“line# EDIT”、“SED 文件名”或僅使用“ED”來啟動
editor.
主筆。


EDONE HIDDEN
伊多內隱藏


EEOL ( --- ) UTILS
EEOL （ --- ） 公用事業
Erase the current line to the end of the line.
將目前行清除到行尾。


EFL HIDDEN
EFL 隱藏


EH512Z FORTH
EH512Z 第四


EHADR FORTH
埃哈德爾·福斯


EHCKSM FORTH
EHCKSM 前進


EHLMRV FORTH
EHLMRV 福斯


EHMT FORTH
EHMT 前進


EHSP FORTH
EHSP 前進


EHZ FORTH
EHZ 前進


ELSE ( --- ) KERNEL3
ELSE （ --- ） KERNEL3
Used in the form: ? IF <true> ELSE <false> THEN. If flag ? is
以以下形式使用：？如果<true>不是的話 <false>。如果旗幟？是
false, branches forward to <false>.
false，則分支轉發為 <false>。


EMIT ( c1 -- ) KERNEL2
發射 （ c1 -- ） KERNEL2
A defered word which sends a character to the output device.
將字元傳送至輸出裝置的延遲字。


EMIT. ( char -- ) DUMP
發。（ char -- ）傾銷
Emit an ascii character char. If the char is not printable then
發出一個 ascii 字元 char。如果字元不可列印，則
print a ".".
列印一個“.”。


EMPTY ( --- ) EDITERR
空 （ --- ） 編輯者
A word defined with MARK, that cleans out the dictionary back
用 MARK 定義的單詞，可清除字典
to when EMPTY was defined. All segments are reset. USE CAUTION
到定義 EMPTY 時。所有區段都會重設。使用謹慎
when changing DEFERed words, as EMPTY does not know about them,
當更改 DEFERRed 單詞時，由於 EMPTY 不知道它們，
and will cause a crash if you empty back to before a needed
如果您清空回需要之前，則會導致崩潰
word used in a DEFERed word.
DEFERed 詞中使用的單詞。


END? ( --- a1 ) KERNEL2
端？（ --- A1 ）KERNEL2
True if input stream exhausted, else false.
如果輸入資料流已耗盡，則為 true，否則為 false。


ENDCASE ( -- ) CASE
尾箱 （ -- ） 案例
See CASE.
參見 CASE。


ENDFILE ( handle --- double-end ) HANDLES
ENDFILE （ handle --- double-end ） HANDLES
Return the double-end pointer for the file open in handle, also
傳回在句柄中開啟的檔案的雙端指標，也
sets the pointer to the end of the file. Useful for finding the
將指標設定為檔案結尾。對於尋找
end of a file, and for appending to the end of a file.
檔案結尾，以及附加至檔案結尾。


ENDMENU ( a1 n1 --- ) MENUS
結束選單 （ a1 n1 --- ） 選單
Resolves the building of a new menu. See NEWMENU.
解決新選單的建置問題。請參閱 NEWMENU。


ENDOF ( -- ) CASE
結束 （ -- ） 案例
See CASE.
參見 CASE。


ENTRY ( --- a1 ) KERNEL2
條目 （ --- a1 ） KERNEL2
Jumped to during multitasking.
在多任務處理期間跳到。


ENVSIZE ( --- n1 ) ENVIRON
環境尺寸 （ --- n1 ） 環境
Calculate n1 the size of the environment in bytes, clipped to
計算 n1 環境大小 （以位元組為單位），裁剪至
about 31k bytes.
大約 31k 位元組。


EQUIT HIDDEN
馬鹿隱藏


ERASE ( a1 n1 --- ) KERNEL2
擦除 （ a1 n1 --- ） KERNEL2
Fill the string with zeros
用零填滿字串


ERRFIX FORTH
錯誤修正


ES0 ( --- a1 ) KERNEL2
ES0 （ --- a1 ） KERNEL2
ES register initial segment.
ES 暫存器起始區段。


ESC-IN FORTH
ESC-輸入第四


EVEN ( -- ) KERNEL3
偶數 （ -- ） KERNEL3
Makes the top of the stack an EVEN number. A noop on the 8086.
使堆疊頂部成為偶數。8086 上的一個 noop。


EVSEG ( --- n1 ) ENVIRON
EVSEG （ --- n1 ） 環境
Return n1 the value of the environment segment.
傳回 n1 環境區段的值。


EX HIDDEN
EX 隱藏


EXCUT FORTH
向前挖出


EXEC.PARAM HIDDEN
執行官。帕拉姆隱藏


EXEC: ( n1 -- ) KERNEL1
執行委員會：（ n1 -- ） KERNEL1
Execute the n-th word following the word EXEC: in a high level
在高階執行 EXEC： 一詞後面的第 n 個字
definition.
定義。


EXECUTE ( a1 --- ) KERNEL1
執行 （ a1 --- ） KERNEL1
Execute the word whose code field is on the stack. Very useful
執行其代碼欄位在堆疊上的單字。非常有用
for passing executable routines to procedures!!!
將可執行常式傳遞至程序!!


EXECUTION-CLASS HIDDEN
執行類別隱藏


EXEHCB ( --- a1 ) SAVEEXE
EXEHCB （ --- a1 ） SAVEEXE
A handle for use while saving an .EXE file.
儲存.EXE 檔案時使用的控制碼。


EXHREAD ( a1 n1 handle seg1 --- n2 ) HANDLES
EXHREAD （ a1 n1 手柄 seg1 --- n2 ） 手柄
Read from the file specified by handle to the extended segment
從句柄指定的檔案讀取至延伸區段
area specified by seg1, a1 for length n1. Returns n2 the length
由 SEG1、A1 指定的長度 n1 的面積。傳回長度 n2
actually read.
實際閱讀。


EXHWRITE ( a1 n1 handle seg1 ---) HANDLES
EXHWRITE （ a1 n1 句柄 seg1 ---） 句柄
Write from memory a1,n1 in segment seg1 to the file specified
從區段 seg1 中的記憶體 a1，n1 寫入指定的檔案
by handle.
按句柄。


EXIT ( --- ) KERNEL1
退出 （ --- ） KERNEL1
Pop an entry off the return stack and place it into the
從傳回堆疊中彈出一個項目，並將其放入
Interpretive Pointer. Terminates a Hi Level definition.
解釋指針。終止高層級定義。


EXPECT ( a1 n1 --- ) KERNEL2
期待 （ a1 n1 --- ） KERNEL2
A DEFERed word. Get a string from the terminal and place it in
一個延期的詞。從終端機取得字串，並將其放入
the buffer provided. Performs a certain amount of line
提供的緩衝區。執行一定數量的線
editing. Saves the number of characters input in the Variable
編輯。儲存變數中輸入的字元數
SPAN. Processes control characters per the array pointed to by
拃。處理每個陣列所指向的字元控制字元
CC.
抄送。


EXPORT FORTH
向前匯出


EXPORT$ FORTH
出口$ FORTH


EXTCHAR@ FORTH
EXTCHAR@向前


EXTCHARSEG FORTH


EXTROWS FORTH
延伸


EY HIDDEN
安永隱藏


F1 FORTH
F1 第四


FALLOF ( func | file_specs --- ) FWORDS
FALLOF （ func | file_specs --- ） FWORDS
A generalized function. By setting the defered word DONFILE, a
廣義函數。透過設定延遲字 DONFILE，一個
function can be performed on all files matching the filespec
函數可以對符合 filespec 的所有檔案執行
the user has given. See FLOOK, INDEX, and FPRINT for examples
用戶已經給出了。如需範例，請參閱 FLOOK、INDEX 和 FPRINT
of how to use this word.
如何使用這個詞。


FALSE ( --- f1 ) KERNEL1
錯誤 （ --- f1 ） KERNEL1
This word was brought to you by CONSTANTS FOR CLARITY.
這個詞是由 CONSTANTS FOR CLARITY 帶給你的。


FAST ( --- ) QVIDEO
快速 （ --- ） QVIDEO
Select the fast screen output routines.
選擇快速螢幕輸出常式。


FBX HIDDEN
FBX 隱藏


FCB>HANDLE ( a1 a2 --- ) HANDLES
FCB>手柄（a1 a2 ---）手柄
Copy the file <name> and extention from the specified FCB a1 to
將檔案<name>和延伸範圍從指定的 FCB a1 複製到
handle a2.
處理 A2。


FEMIT ( c1 --- ) KERNEL2
FEMIT （ c1 --- ） KERNEL2
A FAST EMIT, uses TYPE to display the character c1. FEMIT
FAST EMIT 使用 TYPE 來顯示字元 c1。費米特
weill not respond to control characters such as CR, LF or FF,
weill 不響應 CR、LF 或 FF 等控制字符，
They will be displayed as their graphic character equivelant.
它們將顯示為圖形字符等同物。


FENCE ( --- a1 ) KERNEL3
圍欄 （ --- a1 ） KERNEL3
The limit address for forgetting. Words defined below FENCE
忘記的極限地址。FENCE 下方定義的字詞
may not be forgotten.
可能不會被遺忘。


FHELP FORTH
幫助前進


FILE ( | <name> --- ) SEQREAD
檔案 （ |<name> --- ）序列
Select ,name> as the current file for listing, loading or
選取 ，name> 作為目前檔案，以列出、載入或
editing. Any file already open is closed first.
編輯。任何已開啟的檔案都會先關閉。


FILE-LINE_VIEW FORTH
檔案 LINE_VIEW FORTH


FILE>TIB ( a1 --- ) SEQREAD
FILE>TIB （ a1 --- ） 後續
Move the counted dtring a1 into the terminal input buffer. The
將計數的 dtring a1 移至終端機輸入緩衝區。這
string is checked for an extension, if none is found, an
string 檢查副檔名，如果找不到副檔名，則會檢查副檔名
decimal point is added to the string.
小數點會新增至字串。


FILEPOINTER ( --- a1 ) SEQREAD
FILEPOINTER （ --- a1 ） 序列讀取
32 bit variable holding the file pointer of the most recent
32 位元變數，保存最新檔案指標
1read.
1讀。


FILEPRINT ( | <name> --- ) PRINT
檔案列印 （ |<name> --- ）印
All printing is to goto diskfile <name>. No extention is added
所有列印都是轉到磁碟檔案 <name>。未新增延伸模組
to <name>.
到 <name>。


FILES ( --- ) KERNEL1
檔案 （ --- ） KERNEL1
The vocabulary that contains the names of all files loaded into
包含載入到的所有檔案名稱的詞彙
F-PC.
F-PC。


FILES_SET HIDDEN
FILES_SET 隱藏


FILES_SRCH HIDDEN
FILES_SRCH 隱藏


FILL ( a1 n1 c1 --- ) KERNEL2
填充 （ a1 n1 c1 --- ） KERNEL2
FILL the string starting at a1 for count n1 bytes with the
使用 FILL 從 a1 開始的字串，用於計數 n1 位元組
character c1. Both BLANK and ERASE are special cases of FILL.
字符 C1。BLANK 和 ERASE 都是 FILL 的特殊情況。


FILLBUFF ( --- ) SEQREAD
FILLBUFF （ --- ） 序列
Does an unconditional refill of the disk read buffer. The
無條件地重新填入磁碟讀取緩衝區。這
current buffer contents is not over written, but new data is
目前的緩衝區內容不會被覆蓋，但新資料是
read into the end of the buffer to fill it up if there is more
讀取到緩衝區的末尾以填滿它（如果有更多）
data to read.
要讀取的數據。


FILLTIB ( --- ) SEQREAD
FILLTIB （ --- ） 序列
Does an unconditional refill of the terminal input buffer by
終端機輸入緩衝區的無條件重新填充
reading the next line, and setting up TIB to point to that
讀取下一行，並將 TIB 設定為指向該行
line.
線。


FIND ( a1 -- cfa flag | a1 false ) KERNEL3
FIND （ a1 -- cfa 標誌 | a1 false ） KERNEL3
Run through the vocabulary list searching for the name whose
瀏覽詞彙表，搜尋其名稱
address is supplied on the stack. If the name is found, return
address 會在堆疊上提供。如果找到名稱，請傳回
the code field address of the name and a non-zero flag. The
名稱的代碼欄位位址和非零旗標。這
flag is -1 if the word is non-immediate and 1 if it is
如果單字是非即時的，則旗標為 -1，如果是
immediate. If the name is not found, the string address is
近的。如果找不到名稱，則字串位址為
returned along with a false flag.
與假旗一起返回。


FINDFIRST ( string --- f1 ) HANDLES
FINDFIRST （ 字串 --- f1 ） 控點
Begin a search for files specified by filespec string. String
開始搜尋 filespec 字串所指定的檔案。繩子
is a null terminated un-counted string. F1 returned indicates
是空值結尾的未計數字串。傳回的 F1 表示
whether any files matched. The found file is placed in the Data
是否有任何檔案相符。找到的檔案會放置在「資料」
Transfer Area (DTA). USE CAUTION, not to change either the DTA
轉移區域 （DTA）。請小心，不要更改 DTA
or the buffer filled in by FINDFIRST.
或 FINDFIRST 填入的緩衝區。


FINDINLINE HIDDEN
查找內聯隱藏


FINDNEXT ( --- f1 ) HANDLES
FINDNEXT （ --- f1 ） 控點
Continue the file search for a specified string. Returns the
繼續檔案搜尋指定的字串。傳回
boolean f1 true if another match was found. USE CAUTION, not to
布林值 f1 true 如果找到另一個相符項。請小心使用，不要
change either the DTA or the buffer filled in by FINDFIRST, as
變更 DTA 或 FINDFIRST 填入的緩衝區，作為
this function relys on that information.
此功能依賴於該資訊。


FIND_LETTER HIDDEN
FIND_LETTER 隱藏


FIRST ( --- a1 ) KERNEL2
第一個 （ --- a1 ） KERNEL2
A system constant that retuns a useless value in F-PC. It is
重新調整 F-PC 中無用值的系統常數。這是
useless because it is only 10 bytes lower than LIMIT.
沒用，因為它只比 LIMIT 低 10 個字節。


FIXCUR? HIDDEN
修復？潛


FIXINLINE HIDDEN
FIXINLINE 隱藏


FL ( | <name> --- ) SEQREAD
佛羅里達州 （ |<name> --- ）序列
An ALIAS for FILE.
FILE 的別名。


FLHNDL ( --- a1 ) PATHSET
FLHNDL （ --- a1 ） 路徑集
A VALUE that returns the address of the handle we are working
一個 VALUE，傳回我們正在工作的句柄位址
with.
跟。


FLIP ( n1 --- n2 ) KERNEL1
翻轉 （ n1 --- n2 ） KERNEL1
Exhange the hi and low halves of a word.
交換一個單詞的高和低半部分。


FLITEM HIDDEN
FLITEM 隱藏


FLOAD ( | <name> --- ) SEQREAD
FLOAD （ |<name> --- ）序列
load the file <name>. this is nestable.
載入檔案 <name>。這是可套管的。


FLOOK ( search_string file_specs --- ) FWORDS
FLOOK （ search_string file_specs --- ） FWORDS
Search all files in file_spec for search_string. Print each
在 file_spec 中搜尋所有檔案以尋找 search_string。列印每個
occurance found to the display with a line number.
找到帶有行號的顯示。


FNEXT FORTH
下一步


FOFF HIDDEN
FOFF 隱藏


FOFF+ HIDDEN
FOFF+ 隱藏


FOFFSAVE HIDDEN
FOFFSAVE 隱藏


FOR FORTH
為了福斯


FORGET ( | <name> -- ) KERNEL3
忘記 （ |<name> -- ）KERNEL3
Forget all of the code and headers before <name>. FORGET must
忘記之前的所有程式碼和標頭 <name>。忘記必須
be used with caution, if you are using DEFERS or UDEFERS,
如果您使用 DEFERS 或 UDEFERS，請謹慎使用，
FORGET will not know about these chains, so they must be
FORGET 不會知道這些鏈，所以它們一定是
unlinked before using FORGET or disaster WILL strike.
在使用 FORGET 之前取消鏈接，否則災難將發生。


FORGX HIDDEN
FORGX 隱藏


FORGY HIDDEN
隱藏的福吉


FORM-DATE ( d1 --- a1 ) TIMER
表格日期 （ d1 --- a1 ） 計時器
Build the ascii string of the current DOS DATE d1 in the DTBUF
在 DTBUF 中建立目前 DOS DATE d1 的 ASCII 字串
(Date/Time buffer) and return its address.
（日期/時間緩衝區） 並傳回其位址。


FORM-FEED ( --- ) UTILS
表格饋送 （ --- ） UTILS
Print a form feed character.
列印表單饋送字元。


FORM-TIME ( d1 --- a1 ) TIMER
FORM-TIME （ d1 --- a1 ） 計時器
Build the ascii string of the current DOS TIME d1 in the DTBUF
在 DTBUF 中構建當前 DOS TIME d1 的 ASCII 字符串
(Date/Time buffer) and return its address.
（日期/時間緩衝區） 並傳回其位址。


FORTH ( --- ) KERNEL1
第四 （ --- ） KERNEL1
The FORTH vocabulary, where most user words can be found. All
FORTH 詞彙表，可以找到大多數用戶單詞。都
of the words in this glossary are in the FORTH vocabulary.
本詞彙表中的單詞在 FORTH 詞彙表中。


FORWARD FORTH
向前邁進


FPATH FORTH
FPATH 向前


FPATH$ FORTH
FPATH$ 向前


FPATH+ FORTH
FPATH+ 向前


FPRINT ( file_specs --- ) FWORDS
FPRINT （ file_specs --- ） FWORDS
Print listing files of all files that match the file_specs
列印符合 file_specs 的所有檔案的清單檔案
included on the line following FPRINT.
包含在 FPRINT 之後的行中。


FSAVE ( | <name> --- ) SAVEEXE
FSAVE （ |<name> --- ）拯救
A pseudonym for SAVE-EXE
SAVE-EXE 的筆名


FSAVE$ FORTH
FSAVE$ 向前


FSTIME HIDDEN
FSTIME 隱藏


FUDGE ( --- a1 ) BUFSET
軟糖 （ --- a1 ） BUFSET
A VARIABLE used to determine the speed of MS. Calibrated at
用於確定 MS 速度的變量。校準為
boot time to the speed of your computer.
啟動時間到電腦的速度。


FUNCARRAY HIDDEN
隱藏的 FUNCARRAY


GET-CURSOR ( --- SHAPE ) IBMCURSR
GET-CURSOR （ --- 形狀 ） IBMCURSR
Get the cursor shape mask SHAPE.
取得遊標形狀遮罩 SHAPE。


GET-FILESPECS FORTH


GETDATE ( --- Y MD ) TIMER
GETDATE （ --- Y MD ） 計時器
Get the DOS format double date.
取得 DOS 格式雙日期。


GETDIR HIDDEN
蓋迪爾隱藏


GETFILE FORTH
取得檔案


GETINPFILE FORTH


GETMOUS HIDDEN
隱藏的


GETTIME ( --- HM Sh ) TIMER
GETTIME （ --- HM Sh ） 計時器
Get the DOS format double time.
雙倍獲得 DOS 格式。


GET_ALINE ( --- ) SEQREAD
GET_ALINE （ --- ） 序列
get a line of text from the current file, and place it in the
從目前檔案取得一行文字，並將其放在
output buffer.
輸出緩衝區。


GFL ( | <name> --- ) SEQREAD
GFL （ |<name> --- ）序列
Looks at the input stream, if a name is waiting, then continue,
查看輸入流，如果名稱正在等待，則繼續，
but if no name is waiting, the pop up a window display and
但如果沒有名稱在等待，則彈出視窗會顯示，並且
allow the user to pick from a file in the window.
允許使用者從視窗中的檔案中挑選。


GLOBAL_REF FORTH
GLOBAL_REF 向前


GO ( a1 --- ) KERNEL1
GO （ a1 --- ） KERNEL1
Execute code at the given address.
在給定的地址執行代碼。


GOTO FORTH
前往前


GOTOFL HIDDEN
GOTOFL 隱藏


GRAPHCHAR FORTH
圖形字符 FORTH


GRAPHICCHAR FORTH
圖形 FORTH


GREEN ( --- n1 ) COLOR
綠色 （ --- n1 ） 顏色
Return the color value for GREEN.
傳回 GREEN 的色彩值。


H FORTH
H 福斯


H-PVOC HIDDEN
H-PVOC 隱藏


H-STATE HIDDEN
H-STATE 隱藏


H. ( u -- ) KERNEL4
H. （ u -- ） KERNEL4
Display the unsigned number in hex, with trailing blank. Does
以十六進位顯示無符號數字，尾端空白。確實如此
not change the number base.
不改變數字基礎。


HANDLE ( | <name> --- ) HANDLES
手柄 （ |<name> --- ）手柄
Creates an array/handle for name, which holds the files
建立名稱的陣列/控制碼，以保存檔案
attributes, handle number, and null terminated name.
屬性、句柄號碼和 Null 終止名稱。


HANDLE>EXT ( a1 --- a2 ) HANDLES
HANDLE>EXT （ a1 --- a2 ） 手柄
Moves the address from the handle to the decimal point in the
將位址從控點移至
filename, if it exists. Otherwise it steps to the null
檔案名稱 （如果存在的話）。否則，它會逐步執行 null
immediately following the filename.
緊接在檔案名稱之後。


HASH ( str-addr voc-ptr -- thread ) KERNEL3
HASH （ str-addr voc-ptr -- 執行緒 ） KERNEL3
Using the str-addr and the vocabulary address to determine the
使用 str-addr 和詞彙位址來判斷
address thread in the vocabulary that the name should go into.
address 執行緒。


HAVEMOUSE HIDDEN
隱藏了老鼠


HCLOSE ( handle --- f1 ) HANDLES
HCLOSE （ 手柄 --- f1 ） 手柄
Close the file specified by handle, return boolean f1 non-zero
關閉 handle 指定的文件，傳回布林值 f1 非零
if an error occured.
如果發生錯誤。


HCREATE ( handle --- error-code ) HANDLES
HCREATE （ 處理---錯誤代碼 ） HANDLES
Create the file specified in handle, if the file already
建立 handle 中指定的檔案 （如果檔案已）
exists, then it is ZEROed !! Returns zero if no error occured.
存在，那麼它就歸零了！如果未發生錯誤，則傳回零。


HDEFAULT ( -- ) DEFAULT
HDEFAULT （ -- ） 預設值
Open a file specified on the comand line at startup.
在啟動時開啟 comand 行上指定的檔案。


HDELETE ( handle --- f1 ) HANDLES
HDELETE （ 句柄 --- f1 ） 句柄
Delete the file specified by handle, return boolean f1 non-zero
刪除句柄指定的文件，傳回布林值 f1 非零
if an error occured.
如果發生錯誤。


HDOS1 ( cx dx fun -- ax cf | error-code 1 ) HANDLES
HDOS1 （ cx dx fun -- ax cf | error-code 1 ） 句柄
Define a dos call assembly word, which is later used by HOPEN
定義一個 dos 呼叫組合字，稍後由 HOPEN 使用
and HCREATE.
和 HCREATE。


HDOS3 FORTH
HDOS3 第四


HDOS4 FORTH
HDOS4 第四


HDSTSCHR FORTH


HEADER ( | <name> -- ) KERNEL3
標頭 （ |<name> -- ）KERNEL3
Creates a NAME header in HEAD space, but compiles absolutely
在 HEAD 空間中建立 NAME 標頭，但絕對編譯
nothing in CODE space. The head created, does point at HERE
CODE 空間中沒有任何內容。創建的頭部確實指向這裡
though.
雖然。


HEADERLESS FORTH
無標題向前


HEADERS FORTH
標題向前


HELLO ( --- ) HELLO
你好（ --- ） 你好
Cold start initialization for F-PC.
F-PC 的冷啟動初始化。


HELP ( | <name> --- ) VIEW
幫助 （ |<name> --- ）觀
VIEW is followed on the same line by name. Display a help file
VIEW 後面跟在同一行的名稱。顯示說明檔案
entry for the <name> specified.
指定的條目 <name>。


HERE ( --- a1 ) KERNEL2
這裡（--- a1 ）KERNEL2
Return the address of the top of the dictionary
傳回字典頂部的位址


HEX ( --- ) KERNEL2
十六進制 （ --- ） KERNEL2
All subsequent numeric IO will be in Hexadecimal.
所有後續的數字 IO 都將以十六進位為單位。


HEXBASE FORTH
HEXBASE 第四


HFIND FORTH
H 尋找前


HIDDEN ( --- ) VOCABS
隱藏 （ --- ） 詞彙
vocabulary stack -> ( voc1 voc2 -- hidden voc2 | current = ? )
詞彙堆疊 -> （ voc1 voc2 -- 隱藏 voc2 | current = ？ ）
The HIDDEN vocabulary, sets CONTEXT to HIDDEN when executed.
HIDDEN 詞彙表在執行時將 CONTEXT 設定為 HIDDEN。


HIDE ( -- ) KERNEL3
隱藏 （ -- ） KERNEL3
Removes the Last definition from the Header Dictionary.
從「標頭字典」中移除「最後一個」定義。


HIDE.MOUSE FORTH
藏。鼠標向前


HIDE.MS HIDDEN
HIDE.MS 隱藏


HIDELINES ( --- ) SEQREAD
隱藏線 （ --- ） 序列讀取
Turn off listing of lines while loading.
載入時關閉線路清單。


HLD ( --- a1 ) KERNEL2
HLD （ --- a1 ） KERNEL2
Points to a converted character during numeric output.
在數值輸出期間指向轉換的字元。


HNDLOFFSET FORTH


HNDLS ( --- a1 ) SEQREAD
HNDLS （ --- a1 ） 後續
an array of handles, holds 5 handles in a stack. Used by
控制碼陣列，在堆疊中保留 5 個控制碼。使用者
SEQHANDLE, SEQHANDLE+, and FLOAD.
SEQHANDLE、SEQHANDLE+ 和 FLOAD。


HOLD ( c1 --- ) KERNEL2
按住 （ c1 --- ） KERNEL2
Save the char for numeric output later.
儲存字元以供稍後數值輸出。


HOPEN ( handle --- error-code ) HANDLES
HOPEN（錯誤代碼---句柄）句柄
Open the file specified in handle, return error-code zero if
開啟句柄中指定的檔案，如果
the file was opened properly.
檔案已正確開啟。


HOURS ( N1 --- ) TIMESTUF
小時 （ N1 --- ） TIMESTUF
Wait for n1 hours. Performs PAUSE and PAUSE-FUNC constantly
等待 n1 小時。持續執行 PAUSE 和 PAUSE-FUNC
while its waiting.
在等待的時候。


HREAD ( a1 n1 handle --- n2 ) HANDLES
HREAD（ a1 n1 手柄 --- n2 ） 手柄
Read from a file specified by a handle to a1,n1 in the code
從句柄指定的檔案讀取程式碼中 a1，n1
segment. Returns n2 the length actually read.
瓣。傳回實際讀取的長度 n2。


HRENAME ( handle1 handle2 --- return-code ) HANDLES
HRENAME （ handle1 handle2 --- return-code ） 句柄
Change the name of the file specified in handle1 to the name
將 handle1 中指定的檔案名稱變更為名稱
specified in handle2. Can be used to move a file from one
在 handle2 中指定。可用來將檔案從
directory to another on the same drive. Returns 18 if the
目錄到同一磁碟機上的另一個目錄。如果
rename was good, not zero.
重命名是好的，而不是零。


HSRCSCHR FORTH


HV-INSERT HIDDEN
HV-INSERT 隱藏式


HWORDS+ FORTH
HWORDS+ 前進


HWORDS- FORTH
HWORDS- 第四


HWRITE ( a1 n1 handle --- n2 ) HANDLES
HWRITE （ a1 n1 句柄 --- n2 ） 句柄
Write to a file specified by a handle from a1,n1 in the code
寫入程式碼中 a1，n1 的句柄所指定的檔案
segment. Return n2 the length actually written.
瓣。傳回實際寫入的長度 n2。


HYPERTYPEL FORTH
超類型第四


I ( --- n1 ) KERNEL1
我 （ --- n1 ） KERNEL1
returns the current loop index. It now requires a little more
傳回目前迴圈索引。現在需要更多
calculation to compute it than in FIG Forth but the tradeoff is
計算比圖四中要計算它，但權衡是
a much faster (LOOP). The loop index is stored on the Return
更快 （LOOP）。迴圈索引儲存在 Return
Stack.
堆。


IBFULL FORTH
伊富爾福斯


IBLEN ( --- n1 ) SEQREAD
IBLEN （ --- n1 ） 後續
Input buffer length constant.
輸入緩衝區長度常數。


IBLIMIT FORTH
伊限福斯


IBM--LINE ( -- ) IBMCURSR
IBM--LINE （ -- ） IBMCURSR
Delete the current line on the IBM display, causes all lines
刪除 IBM 顯示畫面上的現行行，導致所有行
lower on the screen to scroll up. This is the defered function
在螢幕下方向上捲動。這是延遲函數
of -LINE. Use -LINE for portability.
的 -LINE。使用 -LINE 實現可移植性。


IBM-AT ( col row -- ) IBMCURSR
IBM-AT （ 列列 -- ） IBMCURSR
Move to the COL and ROW specified on the IBM display screen.
移至 IBM 顯示畫面上指定的 COL 及 ROW。
This is done using a BIOS level interupt. This word is normally
這是使用 BIOS 層級中斷來完成的。這個詞通常是
the defered function of AT, you should use AT for portability.
AT 的延遲功能，為了便攜性，應該使用 AT。


IBM-AT? ( --- col row ) IBMCURSR
IBM-AT？（ 列行--- ）IBMCURSR
Return the ROW and COLUMN of the cursor on the display as it is
按原樣返回顯示上游標的 ROW 和 COLUMN
known by DOS. Used to initialize Forth's #LINE and #OUT
由 DOS 知道。用於初始化 Forth 的 #LINE 和 #OUT
variables.
變數。


IBM-DARK FORTH
IBM-黑暗前來


IBM-PROPRINT ( --- ) PROPRINT
IBM-PROPRINT （ --- ） PROPRINT
Select the IBM Proprinter as the system printer, with BOLD and
選取 IBM Proprinter 作為系統印表機，並使用 BOLD 和
UNDERLINE available.
下劃線可用。


IBRESET ( --- ) SEQREAD
IBRESET （ --- ） 序列讀取
Input Buffer RESET, initializes the LINEREAD function to start
輸入緩衝區 RESET，初始化 LINEREAD 函數以啟動
reading from a new file or a file in which a move POINTER has
從新檔案或移動指標具有的檔案讀取
been done. Flushes the contents of the read buffer.
已經完成了。排清讀取緩衝區的內容。


IF ( f1 -- ) KERNEL3
IF （ f1 -- ） KERNEL3
Used in the form: f1 IF <true> ELSE <false> THEN (ELSE is
以以下形式使用：f1 IF <true> ELSE <false> THEN （ELSE 是
optional). If flag f1 is false, branches forward to <false> or
選用）。如果旗標 f1 為 false，則會向前分支至 <false> 或
after THEN.
之後。


IMMEDIATE ( -- ) KERNEL3
立即 （ -- ） KERNEL3
Mark the last Header as an Immediate word.
將最後一個標頭標示為「即時」單字。


IMP/EXP.INIT FORTH
IMP/EXP。向前啟動


IMPORT FORTH
匯入


INBSEG ( --- n1 ) SEQREAD
INBSEG （ --- n1 ） 序列
The input buffer segment VALUE.
輸入緩衝區段 VALUE.


INCLUDE ( | <name> --- ) SEQREAD
包括 （ |<name> --- ）序列
An ALIAS for FLOAD. See also FLOAD.
FLOAD 的別名。另請參閱 FLOAD。


INCR ( a1 -- ) KERNEL1
INCR （ a1 -- ） KERNEL1
Increment the word at the specified address by 1.
將指定位址的單字遞增 1。


INCR> ( | <name> -- ) EQUCOLON
增加> （ |<name> -- ）埃科隆
Increment the body of <name> by one, used to modify the
將主體遞增<name>一，用於修改
following VALUE or VARIABLE.
VALUE 或 VARIABLE 之後。


INDEX ( file_spec --- ) FWORDS
索引 （ file_spec --- ） FWORDS
display an index of the first line of each file that matches
顯示每個相符檔案第一行的索引
the file_specs included on the line following INDEX.
該 file_specs 包含在 INDEX 之後的行中。


INIT-R0 FORTH
INIT-R0 第四個


INIT-SPLIT HIDDEN
初始分割隱藏


INIT.MOUSE HIDDEN
初始化。鼠標隱藏


INITCMDPATH HIDDEN
INITCMDPATH 隱藏


INITCOLOR ( --- ) VIDEO
INITCOLOR （ --- ） 視頻
A defered word that gets set later, and is used to do the color
稍後設定的延遲單字，用來做顏色
display attribute control initialization ( it sets the >ATTRIBx
display 屬性控制項起始設定 （ 它會設定 >ATTRIBx
words. ). See the file MONOCROM, and COLOR.
言。).請參閱檔案 MONOCROM 和 COLOR。


INITMONO ( --- ) VIDEO
INITMONO （ --- ） 視頻
A defered word that gets set later, and is used to do the
稍後設定的延遲單字，用於執行
monochrome display attribute control initialization ( it sets
單色顯示屬性控制項初始化 （ 它設定
the >ATTRIBx words. ). See the file MONOCROM.
>ATTRIBx 詞。).請參閱檔案 MONOCROM。


INITMOUSE HIDDEN
初始滑鼠隱藏


INITSTUFF ( --- ) KERNEL4
初始內容 （ --- ） KERNEL4
A DEFERed word chain, used by many system utilities that need
一個 DEFERed 字鏈，由許多需要的系統公用程式使用
to specify a function to be performed at cold start time. See
以指定要在冷啟動時執行的功能。看
also DEFERS for more information on how defered word chains
也 DEFERS 以取得有關如何延遲字鏈的更多資訊
work.
工作。


INLEN ( --- a1 ) SEQREAD
INLEN （ --- a1 ） 序列
input text length variable
輸入文字長度變數


INLENGTH FORTH
長度向前


INLINE ( --- ) PASM
內聯 （ --- ） PASM
Starts an assembly language sequence in the middle of a :
在中間啟動彙編語言序列：
(colon) definition. Assembly code instructions follow until the
（冒號）定義。組合程式碼指示遵循，直到
sequence is terminated by END-INLINE. The sequence of assembly
序列由 END-INLINE 終止。組裝順序
instructions normally includes NEXT, 1PUSH, or 2PUSH just prior
指令通常包括 NEXT、1PUSH 或 2PUSH 之前
to the word END-INLINE.
到 END-INLINE 一詞。


INSERTALINE FORTH
插入 FORTH


INSERTMODE HIDDEN
INSERTMODE 隱藏


INSTALL ( --- ) UTILS
安裝 （ --- ） UTILS
A DEFERed word that is used to install user defined options in
用於在
the system when they are initially bringing up the system.
當他們最初啟動系統時。


INSTART FORTH


INTERP FORTH
插補前


INTERPRET ( -- ) KERNEL3
解釋 （ -- ） KERNEL3
The Forth Interpret Loop. If the next word is defined, execute
第四個解釋循環。如果定義了下一個單字，請執行
it, otherwise convert it to a number and push it onto the
它，否則將其轉換為數字並將其推送到
stack.
堆。


INVERT-SCREEN FORTH
反轉屏幕向前


IS ( cfa -- ) KERNEL4
IS （ cfa -- ） KERNEL4
Depending on STATE, either sets the following DEFERred word
根據 STATE，請設定下列 DEFERred 字組
immediatly or compiles the setting for later.
立即或編譯設定以供稍後使用。


ISTK> HIDDEN
ISTK>隱藏


ITEM# HIDDEN
項目# 隱藏


ITEMSTK HIDDEN
ITEMSTK 隱藏


J ( --- n1 ) KERNEL1
J （ --- n1 ） KERNEL1
returns the loop index of the inner loop in nested DO .. LOOPs.
傳回巢狀 DO 中內部迴圈的迴圈索引。迴圈。


JOIN FORTH
加入


K FORTH
K 福斯


KEY ( --- c1 ) KERNEL2
KEY （ --- c1 ） KERNEL2
A defered word to get a key from user.
從使用者取得金鑰的延遲字。


KEY? ( --- f1 ) KERNEL2
鑰匙？（ --- f1 ）KERNEL2
A defered word that returns a true flag if a key waiting.
延遲字組，如果索引鍵正在等待，則會傳回 true 旗標。


KEYFILTER FORTH
按鍵過濾器向前


KEYFUNCS2 HIDDEN
KEYFUNCS2 隱藏


KEYFUNCS1 HIDDEN
KEYFUNCS1 隱藏


KEYSFUNCPTR HIDDEN
KEYSFUNCPTR 隱藏


KEYTABLE FORTH
鍵表向前


KEYTESTS HIDDEN
隱藏的金鑰測試


L ( --- ) VIEW
L （ --- ） 視圖
Display 18 lines starting at the most recently displayed line.
顯示從最近顯示的行開始顯示 18 行。


L>NAME ( lfa -- nfa ) KERNEL3
L>NAME （ lfa -- nfa ） KERNEL3
Go from link field address lfa to name field address lfa.
從連結欄位地址 lfa 移至名稱欄位地址 lfa。


LABEL ( --- a1 ) PASM
標籤 （ --- a1 ） PASM
Create a definition that returns the address of whatever code
建立一個定義，傳回任何程式碼的位址
follows, and enable the assembler. Compiled as a VARIABLE.
後面，並啟用組譯器。編譯為 VARIABLE。


LARGEST ( a1 n1 --- a2 n2 ) LARGEST
最大 （ a1 n1 --- a2 n2 ） 最大
Given a starting address a1 and an array length in bytes,
給定起始位址 a1 和陣列長度（以位元組為單位），
return a2 the address of the largest word element in the array,
傳回 a2 數組中最大 word 元素的位址，
and n2 the largest element itself.
n2 是最大的元素本身。


LAST ( --- a1 ) KERNEL2
最後 （ --- a1 ） KERNEL2
Points to the name of the most recently CREATEd word.
指向最近 CREATEd 字的名稱。


LAST-CURSOR HIDDEN
隱藏的最後一個游標


LASTX HIDDEN
LASTX 隱藏


LASTY HIDDEN
最後隱藏


LCHAR HIDDEN
LCHAR 隱藏


LDUMP ( seg offset len --- ) DUMP
LDUMP （ seg offset len --- ） 傾出
Dump to the display the absolute segment seg, starting at
傾出至顯示畫面的絕對區段 seg，從
offset for length len.
長度 len 的偏移量。


LEAVE ( -- ) KERNEL3
離開 （ -- ） KERNEL3
Immediately exit a DO-LOOP.
立即退出 DO-LOOP。


LEDBUTTON HIDDEN
LED 按鈕隱藏


LEDIT_RESTORE FORTH
LEDIT_RESTORE 向前


LENGTH ( a1 --- a2 n1 ) KERNEL2
長度 （ a1 --- a2 n1 ） KERNEL2
Given the address on the stack, returns the address plus two
給定堆疊上的位址，傳回位址加 2
and the two byte contents of the address.
以及位址的兩個位元組內容。


LENGTH.CHECK FORTH
長度。查看


LENLIMIT HIDDEN
LENLIMIT 隱藏


LFEMIT FORTH


LFILL ( a1 len value --- ) KERNEL2
LFILL （ a1 len 值 --- ） KERNEL2
Fill starting at addr, for length len, with value.
從 addr 開始，長度 len 用值填充。


LFILLW ( seg offset byte-len WORD --- ) IBMCURSR
LFILLW （ seg offset byte-len WORD --- ） IBMCURSR
Fill absolute segment seg starting at offset for length
從長度偏移開始填充絕對線段 seg
byte-len with the value WORD.
byte-len 的值為 WORD。


LIC@ FORTH
LIC@向前


LIHERE FORTH
分明


LIMIT ( --- a1 ) KERNEL2
限價 （ --- a1 ） KERNEL2
A constant that returns the highest address in the CODE segment
傳回 CODE 區段中最高位址的常數
used by Forth. Typically $FFFE.
由福斯使用。通常$FFFE。


LINEEDITOR ( x y a1 n1 --- f1 ) LEDIT
LINEEDITOR （ x y a1 n1 --- f1 ） LEDIT
At location x,y start editing the string specified by a1,n1.
在位置 x，y 開始編輯 a1，n1 指定的字串。
the line editor supports the wordstar key sequences, and if the
行編輯器支援 wordstar 鍵序列，且如果
edit terminates with a <enter>, then the original string will
edit 以 <enter> 終止，則原始字串將
be changed to match the edited string. If the edit is
變更以符合編輯的字串。如果編輯是
terminated with ESC, then the original string will not be
以 ESC 終止，則原始字串將不會
changed. See the file LEDIT for further information on
改變了。請參閱檔案 LEDIT 以取得更多相關資訊
LINEEDITOR.
線編輯器。


LINEREAD ( --- a1 ) SEQREAD
LINEREAD （ --- a1 ） 序列讀取
A defered word that returns a line from the current file.
從目前檔案傳回一行的延遲字。


LINESTRT FORTH
線條向前


LINK ( --- a1 ) KERNEL2
鏈接 （ --- a1 ） KERNEL2
Points to next task in the circular multi tasking queue.
指向循環多工佇列中的下一個任務。


LINK> ( lfa -- cfa ) KERNEL3
鏈接> （ lfa -- CFA ） KERNEL3
Go from link field address lfa to code field address cfa.
從連結欄位位址 lfa 移至程式碼欄位位址 cfa。


LIST ( n1 --- ) VIEW
列表 （ n1 --- ） 檢視
N1 is the line number to list in the current open file.
N1 是要在目前開啟的檔案中列出的行號。


LISTING ( --- ) TOPEDIT
上市 （ --- ） TOPEDIT
Print a formatted listing of the file currently open. The
列印目前開啟之檔案的格式化清單。這
printing is done using the editor, so there must be enough
列印是使用編輯器完成的，所以必須有足夠的
memory for the editor to load the file.
編輯器載入檔案的記憶體。


LISTVAR FORTH


LITERAL ( n1 -- ) KERNEL3
字面 （ n1 -- ） KERNEL3
Compile the single integer from the stack as a literal.
將堆疊中的單一整數編譯為文字。


LKEY! HIDDEN
LKEY！潛


LKEY@ HIDDEN
LKEY@隱藏


LL ( | <name> --- ) VIEW
LL （ |<name> --- ）觀
LL is a pseudonym for VIEW, displays Help and Source for
LL 是 VIEW 的筆名，顯示 Help 和 Source
<name>.
<name>。


LMARGIN ( -- a1 ) KERNEL4
LMARGIN （ -- a1 ） KERNEL4
The left margin setting used by ?LINE, ?CR. When a line wrap
？線，？CR。當換行時
occurs, then LMARGIN specifies how many spaces are printed on
發生，則 LMARGIN 會指定列印的空格數目
the following line. Default value is 0.
接下來的行。預設值為 0。


LOAD ( n1 --- ) VIEW
載入 （ n1 --- ） 檢視
n1 is the line number of where to start loading.
n1 是開始載入位置的行號。


LOADED, ( --- ) SEQREAD
已載入，（ --- ） 順序
Compile the name of the current file as a variable in the FILES
將目前檔案的名稱編譯為 FILES 中的變數
vocabulary. Also links the variable into a list of variables
詞彙。也會將變數連結至變數清單
that represent the files that have been loaded.
代表已載入的檔案。


LOADER ( --- ) SEQREAD
載入器 （ --- ） 順序
A defered word that loads the current file.
載入目前檔案的延遲字。


LOADING ( --- a1 ) SEQREAD
載入中 （ --- a1 ） 順序
A VARIABLE that holds a flag TRUE if we in the process of
一個 VARIABLE，如果我們在處理過程中，則持有標誌 TRUE
loading a file.
載入檔案。


LOADLINE FORTH
負載線向前


LOADMACS HIDDEN
隱藏的 LOADMACS


LOADSTAT ( --- ) SEQREAD
LOADSTAT （ --- ） 序列讀取
load status display defered word. Normally deferd to <.STAT>.
載入狀態顯示延遲字。通常推遲到 <.STAT>。


LOCAL_REF FORTH
LOCAL_REF 向前


LOOP ( -- ) KERNEL3
循環 （ -- ） KERNEL3
Terminate a loop structure. Increment loop index by one and
終止迴圈結構。將迴圈索引遞增 1 和
repeat <loop-body> until loop index crosses the boundary
重複<loop-body>直到迴圈索引越過邊界
between limit and limit - 1. Used in the form DO <loop-body>
在極限和極限之間 - 1.以 DO <loop-body> 的形式使用
LOOP.
圈。


LRUNSAVE FORTH
LRUNSAVE 前進


LTBLUE ( --- n1 ) COLOR
LTBLUE （ --- n1 ） 顏色
Return the color value for LIGHT BLUE. Blinks in Background.
傳回 LIGHT BLUE 的色彩值。在背景中閃爍。


LTCYAN ( --- n1 ) COLOR
LTCYAN （ --- n1 ） 顏色
Return the color value for LIGHT CYAN Blinks in Background.
傳回 LIGHT CYAN Blinks in Background 的顏色值。


LTGRAY ( --- n1 ) COLOR
LTGRAY （ --- n1 ） 顏色
Return the color value for LIGHT GRAY
傳回 LIGHT GRAY 的色彩值


LTGREEN ( --- n1 ) COLOR
LTGREEN （ --- n1 ） 顏色
Return the color value for LIGHT GREEN Blinks in Background.
傳回 LIGHT GREEN Blinks in Background 的顏色值。


LTMAGENTA ( --- n1 ) COLOR
LTMAGENTA （ --- n1 ） 顏色
Return the color value for LIGHT MAGENTA Blinks in Background.
傳回 LIGHT MAGENTA Blinks in Background 的顏色值。


LTRED ( --- n1 ) COLOR
LTRED （ --- n1 ） 顏色
Return the color value for LIGHT RED Blinks in Background.
傳回 LIGHT RED Blinks in Background 的色彩值。


M/D/Y ( --- ) TIMER
M/D/Y （ --- ） 計時器
Select the date format Month/Day/Year for all calender
選擇所有日曆的日期格式月/日/年
functions.
事。


M/MOD ( d1 n1 --- rem quot ) KERNEL1
M/MOD （ d1 n1 --- rem quot ） KERNEL1
Divides a double by a single, leaving a single quotient and a
將雙精度除以單數，留下一個單商和一個
single remainder. Division is floored.
單餘數。分裂被擊倒了。


MACBASE HIDDEN
MACBASE 隱藏


MACFILE HIDDEN
MAC 檔案隱藏


MACINIT HIDDEN
MACINIT 隱藏


MACKEY HIDDEN
麥奇隱藏


MACSEG HIDDEN
MACSEG 隱藏


MACSIZ HIDDEN
MACSIZ 隱藏


MACTIMES HIDDEN
隱藏的 MACTIMES


MAGENTA ( --- n1 ) COLOR
洋紅色 （ --- n1 ） 顏色
A CONSTANT that returns the color value for Magenta on a color
傳回顏色上洋紅色顏色值的 CONSTANT
monitor.
班長。


MAKEAFILE FORTH
MAKEAFILE 前進


MAKEDUMMY ( | <name> -- ) KERNEL3
MAKEDUMMY （ |<name> -- ）KERNEL3
Make a dummy : definitions out of <name>. Effectively a NOOP,
製作一個虛擬人：定義。<name> 實際上是一個 NOOP，
used by ANEW.
由 ANEW 使用。


MAKEFILE FORTH
製作文件


MAKINGMAC HIDDEN
讓 MAC 隱藏


MANY ( -- ) UTILS
許多 （ -- ） UTILS
Re-execute the input stream until the user presses a key.
重新執行輸入資料流程，直到使用者按下按鍵為止。


MARK ( | <name> -- ) HELLO
馬克 （ |<name> -- ）你好
Create a mark, that is define a word <name> that will clear the
建立標記，即定義一個將<name>清除
dictionary back to itself when it is executed.
字典在執行時返回到自身。


MAX ( n1 n2 --- n3 ) KERNEL1
最大值 （ n1 n2 --- n3 ） KERNEL1
Return the maximum of n1 and n2
傳回 n1 和 n2 的最大值


MAX-CLASSES HIDDEN
隱藏的最大類別


MAX.S ( --- a1 ) KERNEL4
最大。S （ --- a1 ） KERNEL4
A VARIABLE that holds the value of how many items to display
一個 VARIABLE，它保存要顯示的項目數值
when a .S is performed, normally set to 4, but can be changed
當一個 .執行 S，通常設定為 4，但可以變更
by the user.
由用戶。


MAXCFA HIDDEN
MAXCFA 隱藏


MAXDIR HIDDEN
MAXDIR 隱藏


MAXEDIT HIDDEN
MAXEDIT 隱藏


MAXNAME HIDDEN
MAXNAME 隱藏


MAXNEST ( --- n1 ) SEQREAD
MAXNEST （ --- n1 ） 序列
Total size in bytes of the system handle stack.
系統句柄堆疊的總大小 （以位元組為單位）。


MBUTTON FORTH
穆紐特福斯


MBYE FORTH
前行


MCOL FORTH
麥科爾·福斯


MCOLUMN FORTH
MCOLUMN 福斯


ME$ ( --- a1 ) ENVIRON
ME$ （ --- a1 ） 環境
Storage space for the execution string used to execute this
用來執行此專案的執行字串儲存空間
forth currently running.
第四個目前正在運行。


ME@ ( --- ) ENVIRON
ME@ （ --- ） 環境
Extract the execution string from the environment, and place it
從環境中擷取執行字串，並將其放置
in the string ME$
在字串 ME$ 中


MED-CURSOR ( --- ) IBMCURSR
MED-CURSOR （ --- ） IBMCURSR
set the cursor to a thick cursor, not line, and not block sort
將游標設定為粗游標，而不是線，而不是區塊排序
of double thick.
雙厚。


MEMCHK ( f1 --- ) KERNEL2
MEMCHK （ f1 --- ） KERNEL2
abort with memory error message if true
如果為 true，則中止並顯示記憶體錯誤訊息


MENU ( --- ) MENUS
選單 （ --- ） 選單
Invode the current menu set, accepts keypad keys to move around
調用當前菜單集，接受鍵盤鍵移動
the menubar, and then to enter a menu command. If you have not
功能表列，然後輸入功能表命令。如果您沒有
setup a menubar, then the default Forth menubar is used.
設定功能表列，然後使用預設的 Forth 功能表列。
See also MENUS
另請參閱菜單


MENUBAR FORTH
選單列向前


MENUBOX FORTH
菜單框第四


MENUKEY FORTH
菜單鍵向前


MENULINE" ( | <menu_text> <menu_func> --- ) MENUS
菜單線“ （ |<menu_text> <menu_func> --- ） 菜單
Define a new pull down menu line, with text <menu_text> to
定義新的下拉式功能表行，並將文字<menu_text>傳送至
perform <menu_func>. All menu lines for a particular menu
執行 <menu_func>。特定菜單的所有菜單行
should have the same <menu_text> length. The first capitalized
應該有相同的<menu_text>長度。第一個大寫
letter in the <menu_text> will be the recognized menu command
字母中的字母<menu_text>將是可識別的菜單命令
letter, and should be unique within the items of a particular
字母，並且在特定項目中應該是唯一的
menu. See MENUS
菜單。查看菜單
Example:
例：
"T" is the command key.
“T”是命令鍵。
/ NOOP is the menu function
/ NOOP 是菜單功能
/ /
MENULINE" This is a test " noop
MENULINE“這是一個測試”noop


MENULIST FORTH
菜單列表


MIN ( n1 n2 --- n3 ) KERNEL1
最小值 （ n1 n2 --- n3 ） KERNEL1
Return the minimum of n1 and n2
傳回最小值 n1 和 n2


MINUTES ( N1 --- ) TIMESTUF
分鐘 （ N1 --- ） TIMESTUF
Wait for n1 minutes. PAUSE and PAUSE-FUNC are performed
等待 n1 分鐘。執行 PAUSE 和 PAUSE-FUNC
continuously while waiting.
等待時不斷。


MLINE FORTH
向前移動


MOD ( num den -- modulus ) KERNEL1
MOD（ num den -- 模數 ）KERNEL1
Return the modulus of the numerator and denominator, where the
傳回分子和分母的模數，其中
quotient is "floored". This is designed to yield a result
商是“地板”。這是為了產生結果
having the same sign as the denominator. Note that if the
與分母具有相同的符號。請注意，如果
denominator is positive, the result is positive, regardless of
分母為正，結果為正，無論
the sign of the numerator.
分子的符號。


MORE? FORTH
更？第四


MOUSE.SCALE HIDDEN
老鼠。縮放隱藏


MOUSEBUTTON FORTH
滑鼠按鈕向前


MOUSECHAR HIDDEN
隱藏的老鼠


MOUSEFLG FORTH
老鼠前進


MOUSEKEY FORTH
滑鼠鍵向前


MOUSEKEY? FORTH
鼠標鍵？第四


MOUSEWASDOWN HIDDEN
MOUSEWASDOWN 隱藏


MOUSEXY FORTH
鼠疫前


MOVE ( a1 a2 n1 --- ) KERNEL2
移動 （ a1 a2 n1 --- ） KERNEL2
Move the specified bytes n1 from address a1 ro address a2. No
將指定的位元組 n1 從位址 a1 ro 位址 a2 移動。不
overlapping of data will occur.
將發生數據重疊。


MOVE>MOUSE HIDDEN
移動>滑鼠隱藏


MOVEPOINTER ( double-offset handle --- ) HANDLES
MOVEPOINTER （ 雙偏移控點 --- ） 控點
Move the file pointer for handle to the position double-offset
將控點的檔案指標移至位置雙偏移
in the file already open in handle.
在已在句柄中開啟的檔案中。


MROW FORTH
默羅福斯


MS ( n1 --- ) BUFSET
MS （ n1 --- ） BUFSET
Delay for n1 milliseconds. This function is system specific,
延遲 n1 毫秒。此功能是系統特定的，
and while it is calibrated at system boot time, it may not
雖然它在系統啟動時進行了校準，但它可能不會
always be very acurate.
總是非常準確。


MS: HIDDEN
MS：隱藏


MSGSAVE FORTH
訊息保存 FORTH


MU/MOD ( d1 n1 --- rem dquotient) KERNEL1
MU/MOD（d1 n1 ---對動商）KERNEL1
divides a double by a single, leaving a double quotient and a
將雙精度除以單值，留下一個雙商和一個
single remainder. Division is floored.
單餘數。分裂被擊倒了。


N ( --- ) VIEW
N （ --- ） 檢視
Go forward 16 lines and display 18 lines.
前進 16 行並顯示 18 行。


N>LINK ( nfa -- lfa) KERNEL3
N>LINK （ nfa -- lfa） KERNEL3
Go from name field address nfa to link field address lfa.
從名稱欄位位址 nfa 移至連結欄位位址 lfa。


NAME> ( nfa -- cfa ) KERNEL3
姓名> （ NFA -- CFA ） KERNEL3
Go from name field address nfa to code field address cfa.
從名稱欄位位址 nfa 移至程式碼欄位位址 cfa。


NAME>BUF HIDDEN
名稱>BUF 隱藏


NAME>PAD ( A1 --- PAD ) VIEW
NAME>PAD （ A1 --- PAD ） 檢視
Move the name field to PAD and filter out the hi bit of the
將名稱欄位移至 PAD 並篩選掉
last character in name. Also clears all but lower 5 bits of
名稱中的最後一個字元。還清除了除較低 5 位之外的所有
name count.
名稱計數。


NDIR HIDDEN
NDIR 隱藏


NEEDS ( | <name> --- ) NEEDS
需求 （ |<name> --- ）需要
Test the file <name> following, if we have not loaded it, then
<name> 測試以下文件，如果我們沒有加載它，那麼
load it else just go on.
加載它，否則繼續。


NEGATE ( n1 --- n2 ) KERNEL1
否定 （ n1 --- n2 ） KERNEL1
Turn the number into its negative. A twos complement op.
將數字變成負數。二人補充操作。


NEWBEEP FORTH
新嗶聲


NEWFILE ( | <name> --- ) NEWFILE
新檔案 （ |<name> --- ）新檔案
Open or CREATE the <name> specified and start editing it. if no
開啟或建立<name>指定的，然後開始編輯它。如果沒有
name is specified, then prompt for a name.
name ，然後提示輸入名稱。


NEWMENU ( | <name> --- a1 0 ) compile time MENUS
新菜單 （ |<name> --- a1 0 ） 編譯時間選單
( --- a1 ) run time
（ --- A1 ） 運行時間
Starts the definition of a new menu <name>, see MENUS for an
啟動新功能表的定義 <name>，請參閱 MENUS 以取得
example of how to make a menu.
如何製作菜單的示例。


NEWMENUBAR ( | <name> --- ) MENUS
新選單列 （ |<name> --- ）菜單
Starts the definition of a new menubar, see MENUS for an
啟動新功能表列的定義，請參閱 MENUS 以取得
example of how to make a menubar.
如何製作選單列的範例。


NEXPECT FORTH
期待前進


NEXT FORTH
接下來


NEXT| FORTH
下一頁|第四


NFL HIDDEN
NFL 隱藏


NIP ( n1 n2 --- n2 ) KERNEL1
NIP （ n1 n2 --- n2 ） KERNEL1
Drop the second element from the stack.
從堆疊中刪除第二個元素。


NLEN FORTH
內倫福斯


NO-NAME ( --- ) KERNEL3
無名 （ --- ） KERNEL3
A dummy name, whose name field address is returned by >NAME
虛擬名稱，其名稱欄位位址由 >NAME 傳回
when the real name field can not be found.
當找不到實名欄位時。


NOBACKUP ( --- ) EDITSTUF
NOBACKUP （ --- ） 編輯
Disable the creation of backup copies of your edit files. This
停用編輯檔案的備份副本的建立。這
is normally only done when you are short of disk space, wo
通常只有在磁碟空間不足時才會執行，wo
allow the editing of larger files in a limited environment.
允許在有限的環境中編輯較大的檔案。


NOBASE FORTH
無基地


NOHEADROOM FORTH
沒有餘量


NOISE HIDDEN
隱藏噪音


NOLISTROOM FORTH
諾利斯特·普魯姆·福斯


NOMOUSE HIDDEN
NOMOUSE 隱藏


NOOP ( --- ) KERNEL1
NOOP （ --- ） KERNEL1
One of the most useful words in Forth. Does nothing.
福斯最有用的詞之一。什麼都不做。


NORM-CURSOR ( --- ) IBMCURSR
NORM-CURSOR （ --- ） IBMCURSR
Set the cursor to the normal underline shape.
將游標設定為一般底線形狀。


NORM-DARK FORTH
規範-黑暗福斯


NORM-KEYTABLE FORTH


NORMALVAL FORTH


NORMVAL FORTH
諾姆瓦爾·福斯


NOSETCUR FORTH
NOSETCUR 前進


NOT ( n1 --- n2 ) KERNEL1
不是 （ n1 --- n2 ） KERNEL1
Does a ones complement of the top. Equivalent to -1 XOR.
做一個補充的頂部。相當於 -1 XOR。


NPATH FORTH


NRESOLVE ( 0 n1 n2 ... n -- ) CASE
NRESOLVE （ 0 n1 n2 ...n -- ） 案例
Primitive used by ENDCASE to resolve the previous case
ENDCASE 用來解決前一個案例的基本類型
references.
參考文獻。


NUMBER ( a1 --- d1 ) KERNEL2
數字 （ a1 --- d1 ） KERNEL2
Convert a string to a number. Normally (NUMBER)
將字串轉換為數字。正常 （NUMBER）


NUMBER? ( a1 --- d1 f1 ) KERNEL2
數？（ A1 --- D1 F1 ）KERNEL2
Convert the count delimited string at a1 to a double number.
將 a1 處的計數分隔字串轉換為雙精度。
NUMBER? takes into account a leading minus sign, and stores a
數？會考量前導減號，並儲存
pointer to the last delimiter in DPL. The string must end with
指向 DPL 中最後一個分隔符號的指標。字串必須以
a blank. Leaves a true flag if successful.
一個空白。如果成功，則留下真正的旗標。


OBLEN ( --- n1 ) SEQREAD
OBLEN （ --- n1 ） 序列
output buffer length constant
輸出緩衝區長度常數


OCCUR_SRCH HIDDEN
OCCUR_SRCH 隱藏


OCTAL ( --- ) KERNEL2
八角 （ --- ） KERNEL2
All subsequent numeric IO will be in Octal.
所有後續的數字 IO 都會以八進制為單位。


OF ( n1 n2 -- n1 ) CASE
的 （ n1 n2 -- n1 ） 案例
( n1 n1 -- )
（ n1 n1 -- ）
See CASE.
參見 CASE。


OFF ( a1 --- ) KERNEL1
關閉 （ a1 --- ） KERNEL1
Set the contents of a1 to FALSE
將 a1 的內容設定為 FALSE


OFF> ( | <name> --- ) EQUCOLON
關閉> （ |<name> --- ）埃科隆
Turn off the VALUE or VARIABLE <name> following. Somewhat
關閉<name>後面的 VALUE 或 VARIABLE。聊
faster than <name> OFF.
比關閉更快 <name>。


OFFSET FORTH
偏移向前


OK ( --- ) SEQREAD
確定 （ --- ） 順序
Load all of the current file. Peforms a 1 LOAD.
載入所有目前檔案。執行 1 負載。


OLDFIX HIDDEN
舊修復隱藏


ON ( a1 --- ) KERNEL1
開啟 （ a1 --- ） KERNEL1
Set the contents of a1 to TRUE
將 a1 的內容設定為 TRUE


ON> ( | <name> --- ) EQUCOLON
開啟> （ |<name> --- ）埃科隆
Turn on the VALUE or VARIABLE <name> following. Somewhat faster
開啟以下 VALUE 或 VARIABLE <name> 。稍微快一些
than <name> ON.
比 <name> ON。


OPEN ( | <name> --- ) SEQREAD
OPEN （ |<name> --- ）序列
Open <name> as the current file for loading, editor etc. This
作為<name>當前文件打開以供加載、編輯器等。這
is a pseudonym for FILE.
是 FILE 的筆名。


OPENFILE FORTH
打開文件


OR ( n1 n2 --- n3 ) KERNEL1
或 （ n1 n2 --- n3 ） KERNEL1
Returns the bitwise OR of n1 and n2 on the stack.
傳回堆疊上 n1 和 n2 的位元 OR。


OS2 FORTH
作業系統 2 FORTH


OUTBUF ( --- a1 ) SEQREAD
OUTBUF （ --- a1 ） 序列
the line output buffer array
線輸出緩衝區陣列


OUTFIX HIDDEN
隱藏的外置


OUTPAUSE ( --- ) KERNEL2
暫停 （ --- ） KERNEL2
A DEFERed word that can be set to PAUSE, but is normally set to
可設定為 PAUSE 的 DEFERed 字，但通常設定為
NOOP, to prevent multi tasking from interfering with typed
NOOP，以防止多工處理干擾類型
output.
產量。


OVER ( n1 n2 --- n1 n2 n1 ) KERNEL1
超過 （ n1 n2 --- n1 n2 n1 ） KERNEL1
Copy the second element to the top.
將第二個元素複製到頂部。


OVER.SWAP.HASH.@ FORTH
過。交易。HASH.@向前


P! ( n1 port# --- ) KERNEL1
P!（ n1 連接埠# --- ）KERNEL1
Write the value n1 to the 16 bit port#.
將值 n1 寫入 16 位埠 #。


P-IN FORTH
P-輸入


P@ ( port# -- n1 ) KERNEL1
P@ （ 連接埠# -- n1 ） KERNEL1
Read the 16 bit port# and return value n1.
讀取 16 位埠 # 並傳回值 n1。


PACKED_ASC># FORTH
PACKED_ASC># 第四


PAD ( --- a1 ) KERNEL2
PAD （ --- a1 ） KERNEL2
Floating Temporary Storage area. DON'T USE THIS, it will be
浮動臨時存儲區。不要用這個，它會
going away in the ANSI standard.
在 ANSI 標準中消失。


PAGE ( --- ) UTILS
頁面 （ --- ） 實用程式
Printer dependent. Get to a new page. Increment the page
取決於印表機。前往新頁面。遞增頁面
number and reset the line number and the column number.
number 並重設行號和欄號。


PARAGRAPH ( offset --- paragraph-in ) KERNEL3
段落 （ 偏移 --- 段落 ） KERNEL3
Convert offset to the next largest paragraph size that will
將偏移轉換為下一個最大的段落大小，這將
contain all of offset. Used to do paragraph alignment.
包含所有偏移量。用於進行段落對齊。


PARSE ( a1 --- a2 n1 ) KERNEL2
解析 （ a1 --- a2 n1 ） KERNEL2
Scan the input stream until char is encountered. Update >IN
掃描輸入流，直到遇到 char。更新 >IN
pointer. Leaves the address and length of the enclosed string.
指標。保留所包含字串的位址和長度。


PATH$ ( --- a1 ) ENVIRON
PATH$ （ --- a1 ） 環境
Storage space for the PATH string.
PATH 字串的儲存空間。


PATH1 FORTH
路徑 1 向前


PATH@ ( --- ) ENVIRON
PATH@ （ --- ） 環境
Extract the PATH from the environment string.
從環境字串擷取 PATH。


PATHBOX HIDDEN
隱藏的路徑框


PATHHNDL ( --- a1 ) PATHSET
PATHHNDL （ --- a1 ） 路徑集
A handle that returns a1 the address of the handle that
傳回 a1 的句柄，即該句柄的位址
contains the default drive path.
包含預設磁碟機路徑。


PATHLEN FORTH
路徑前


PATHPTR FORTH
路徑


PATHSET ( handle --- f1 ) HANDLES
PATHSET （ 句柄 --- f1 ） 句柄
Set the current drive path into handle. returns boolean f1 true
將當前驅動器路徑設置為手柄。傳回布林值 f1 true
if an error occured while performing this operation.
如果在執行此作業時發生錯誤。


PAUSE ( --- ) KERNEL1
暫停 （ --- ） KERNEL1
Used by the Multitasker to switch tasks.
多任務處理者用來切換任務。


PAUSE-FUNC ( --- ) TIMESTUF
暫停功能 （ --- ） TIMESTUF
A defered word to be set to a function that is to be performed
要設定為要執行的函數的延遲字
while waiting for timing words Like TENTHS, SECONDS, MINUTES
在等待計時詞時，如 TENTHS、SECONDS、MINUTES
and HOURS to complete.
和完成時間。


PC! ( n1 port# --- ) KERNEL1
電腦！（ n1 連接埠# --- ）KERNEL1
Write the byte n1 to the 8 bit port#.
將位元組 n1 寫入 8 位元埠 #。


PC@ ( port# -- n1 ) KERNEL1
PC@ （ 連接埠# -- n1 ） KERNEL1
Read the 8 bit port# and return value n1.
讀取 8 位埠 # 並傳回值 n1。


PCLOSE ( --- ) PRINT
PCLOSE （ --- ） 列印
Close the current print file, and restore printing to the PRN
關閉目前的列印檔案，並將列印還原至 PRN
device.
裝置。


PDOS ( a1 drive# --- f1 ) KERNEL1
PDOS（a1 驅動器# --- f1）KERNEL1
Read the current DOS path of drive# into the array at a1. The
將 drive# 的當前 DOS 路徑讀入 a1 的陣列中。這
string returned will be NULL terminated. F1 returns TRUE if an
傳回的字串將會以 NULL 終止。如果 F1 傳回 TRUE
error occured.
發生錯誤。


PEMIT ( c1 --- ) KERNEL2
PEMIT （ c1 --- ） KERNEL2
A DEFERed word that normally contains (PRINT), to print a
通常包含 （PRINT） 的 DEFERed 單字，以列印
character c1 to the printer.
字元 C1 傳送至印表機。


PERFORM ( a1 --- ) KERNEL1
執行 （ a1 --- ） KERNEL1
The word whose code field is stored at the address pointed to
其代碼欄位儲存在指向的位址的單字
by a1, the number on the stack. Same as @ EXECUTE
通過 a1，堆棧上的數字。與@EXECUTE 相同


PFALINE HIDDEN
PFALINE 隱藏


PFASAV FORTH


PFILE ( | <name> --- ) PRINT
PFILE （ |<name> --- ）印
All printing is to goto diskfile <name>. No extention is added
所有列印都是轉到磁碟檔案 <name>。未新增延伸模組
to <name>.
到 <name>。


PFL HIDDEN
PFL 隱藏


PICK ( n1 --- n2 ) KERNEL1
選擇 （ n1 --- n2 ） KERNEL1
Reaches into the stack and grabs an element, copying it to the
伸手進入堆疊並抓取一個元素，將它複製到
top of the stack. For example, if the stack has 1 2 3 Then 0
堆疊頂部。例如，如果堆疊有 1 2 3 則 0
PICK is 3, 1 PICK is 2, and 2 PICK is 1.
PICK 是 3,1 PICK 是 2,2 PICK 是 1。


PLACE ( from count to --- ) KERNEL1
PLACE（從計數到---）KERNEL1
Move the characters at from to to with a preceding length byte
將 from to 處的字元移至，並具有前面的長度位元組
of len.
倫的。


PLUCK FORTH
拔出


PNEXT FORTH
下一步


POSTFIX ( --- ) PASM
後綴 （ --- ） PASM
Switch the assembler to POSTFIX mode, like the F83 postfix
將彙編器切換到 POSTFIX 模式，例如 F83 後綴
assembler. The normal mode is PREFIX. See also PREFIX.
彙編器。正常模式是 PREFIX。另請參閱 PREFIX。


PR-STATUS ( n1 --- n2 ) KERNEL2
PR-STATUS （ n1 --- n2 ） KERNEL2
Return the printer status as n2 from the printer specified by
從指定的印表機傳回印表機狀態為 n2
n1. N1=0 for PRT1, and 1 for PRT2.
註 1.PRT1 的 N1=0，PRT2 的 1。


PRE> ( --- ) PASM
PRE> （ --- ） PASM
Restores the previous assembler mode after using >PRE to select
使用 >PRE 選擇後恢復先前的彙編器模式
PREFIX for a macro. Used in pairs with >PRE.
PREFIX 來表示巨集。與 >PRE 成對使用。


PREFIX ( --- ) PASM
前綴 （ --- ） PASM
Switch the assembler to PREFIX notation mode. This is the
將彙編器切換為 PREFIX 表示法模式。這是
normal mode. See also POSTFIX.
正常模式。另請參閱 POSTFIX。


PREMIT HIDDEN
隱藏前置


PREPEND.PATH FORTH
預備。前進的道路


PREPEND.PATH ( handle --- f1 ) PATHSET
預備。PATH （ 句柄 --- f1 ） PATHSET
Prepend the default drive and path to handle, and return f1 the
在前面加上要處理的預設磁碟機和路徑，並傳回 f1
boolean that tells if we were successful.
布林值，說明我們是否成功。


PREWORDS FORTH
前言


PRINT ( | <words-to-be-interpreted> -- ) KERNEL3
列印 （ |<words-to-be-interpreted> -- ）KERNEL3
Interpret the following words, and output to printer.
解譯以下單字，並輸出到印表機。


PRINTING ( --- a1 ) KERNEL2
打印 （ --- a1 ） KERNEL2
A variable which holds a flag that Indicates whether printing
一個變數，它持有一個旗標，指示列印是否
is enabled.
已啟用。


PRINTL FORTH
印刷 FORTH


PRIOR ( --- a1 ) KERNEL2
先驗 （ --- a1 ） KERNEL2
Points to the last vocabulary that was searched.
指向搜尋的最後一個詞彙。


PRIOR.CHECK FORTH
之前。查看


PRNHNDL ( --- a1 ) SEQREAD
PRNHNDL （ --- a1 ） 序列
The handle used by the system to talk to the printer. Normally
系統用來與印表機通訊的句柄。素
initialized to contain PRN. on handle 4, but may be opened on a
初始化以包含 PRN。在手柄 4 上，但可以在
real file to cause printing to a file. See also PFILE and
real 檔案，以導致列印至檔案。另請參閱 PFILE 和
PCLOSE.
關閉。


PRNTYPEL FORTH


PRTYPEL HIDDEN
PRTYPEL 隱藏


PUSH/POP-LEVEL FORTH
推送/彈出級向前


QTYPEL FORTH


QUERY ( --- ) KERNEL2
查詢 （ --- ） KERNEL2
Get more input from the user and place it at TIB.
從使用者取得更多輸入，並將其放在 TIB 中。


QUIT ( -- ) KERNEL4
退出 （ -- ） KERNEL4
The main loop in Forth. Gets more input from the terminal and
福斯的主要環路。從終端機獲取更多輸入，並
Interprets it. Responds with OK if healthy.
解釋它。如果健康，則以 OK 回應。


R# ( --- a1 ) KERNEL2
R# （ --- a1 ） KERNEL2
The cursor position during editing.
編輯期間的游標位置。


R.NAME HIDDEN
R.NAME 隱藏


R/W-DMODE FORTH
R/W-D 模式前進


R/W-MODE FORTH
R/W 模式向前


R> ( --- n1 ) KERNEL1
R> （ --- n1 ） KERNEL1
Pops a value off of the return stack and pushes it onto the
從傳回堆疊中彈出一個值，並將其推送到
parameter stack. It is dangerous to use this randomly!
參數堆疊。隨意使用這個很危險！


R>DROP ( --- ) KERNEL1
R>DROP （ --- ） KERNEL1
Pops a value off of the return stack and discards it. It is
從返回堆棧中彈出一個值並丟棄它。這是
dangerous to use this randomly!
隨意使用這個很危險！


R@ ( --- n1 ) KERNEL1
R@ （ --- n1 ） KERNEL1
Copies the value on the return stack to the parameter stack.
將傳回堆疊上的值複製到參數堆疊。


READ-ONLY FORTH
只讀 FORTH


READ-WRITE FORTH
讀寫


RECOVERLINE ( n1 --- ) SAVESCR
RECOVERLINE （ n1 --- ） SAVESCR
Recover a line n1 from the most recently saved screen with
從最近儲存的螢幕中恢復一行 n1
SAVESCR. The line is placed on the screen on line n1.
拯救。該行放置在屏幕上的第 n1 行。


RECOVERSCR ( --- ) SAVESCR
RECOVERSCR （ --- ） 保存
Recover a COPY of the most recently saved screen with SAVESCR.
使用 SAVESCR 恢復最近保存的屏幕的副本。
You can temporarily restore the screen with this word, in
您可以使用此單字暫時恢復螢幕，在
preperation for messing it up again before finally using
在最終使用之前，準備再次搞砸它
RESTSCR to restore the screen. This word does NOT pop the save
RESTSCR 來還原畫面。這個詞不會彈出保存
screen stack, it only makes a copy of the most recent save.
螢幕堆疊，它只會複製最近儲存的內容。


RECURSE ( -- ) KERNEL4
遞歸 （ -- ） KERNEL4
We prefer to use RECURSIVE rather than RECURSE. See RECURSIVE
我們更喜歡使用 RECURSIVE 而不是 RECURSE。參見遞迴


RECURSIVE ( -- ) immediate KERNEL3
遞迴 （ -- ） 立即 KERNEL3
Allow the current definition to be self referencing.
允許目前的定義是自我參照。


RED ( --- n1 ) COLOR
紅色 （ --- n1 ） 顏色
A CONSTANT that retuns the value of the color red on a color
重新調整顏色上紅色值的 CONSTANT
monitor.
班長。


REF ( | <name> --- ) REF
參考 （ |<name> --- ）參考文獻
Display all references found to <name> in the currently
顯示<name>在目前
compiled Forth system. Examines COLON definitions and DEFERed
編譯的 Forth 系統。檢查 COLON 定義和 DEFERRed
words.
言。


REFCFA HIDDEN
REFCFA 隱藏


REN ( <filespec> --- ) EXEC
REN （ <filespec> --- ） 執行委員會
Perform a RENAME with the filespec following the REN command.
在 REN 命令之後使用檔案規格執行 RENAME。


RENAME ( | <filespec> --- ) EXEC
重新命名 （ |<filespec> --- ）執行委員會
Perform a RENAME with the filespec following the RENAME
使用 RENAME 之後的 filespec 執行 RENAME
command.
令。


REPAIR ( | <name> --- ) TOPEDIT
維修 （ |<name> --- ）頂置
Perform a VIEW and EDit on the <name> following.
對以下項目執行 VIEW 和 EDit <name> 。


REPEAT ( -- ) KERNEL3
重複 （ -- ） KERNEL3
Unconditional backward branch to just after BEGIN in a BEGIN
無條件向後分支到 BEGIN 中 BEGIN 之後
<loop> flag WHILE <true> REPEAT loop.
<loop> flag WHILE <true> REPEAT 迴圈。


REPKEY HIDDEN
隱藏的 REPKEY


RES-IN FORTH
第四次補充


RESET-IN FORTH
重置後


RESTBASE FORTH
RESTBASE 第四


RESTCAPS FORTH
RESTCAPS 四出


RESTCURSOR FORTH


RESTLMRG FORTH
RESTLMRG 前進


RESTMENU FORTH
休息菜單


RESTNEXT FORTH
休息接下來


RESTORE> ( --- ) followed by a definition in a colon def.
RESTORE> （ --- ） 後面接著冒號定義中的定義。
SAVEREST
最節省
Restore the previous value of the body of the name following in
還原後面名稱內文的先前值
this colon definition. See also SAVE> and SAVE!>.
這個冒號定義。另請參閱 SAVE> 和 SAVE！>。


RESTORESTATE ( --- ) UTILS
RESTORESTATE （ --- ） 公用程式
Restore the system state as preserved by SAVESTATE.
還原 SAVESTATE 所保留的系統狀態。


RESTORE_VECTORS ( -- ) KERNEL4
RESTORE_VECTORS （ -- ） KERNEL4
Restores the CONTROL BREAK DOS vectors to their original value
將 CONTROL BREAK DOS 向量還原為原始值
as when Forth was entered. The CONTROL BREAK and DIVIDE by 0
就像福斯被輸入時一樣。控制 BREAK 和除以 0
vectors are saved by the assembly language cold start routines
向量由組合語言冷啟動常式儲存
before Forth is entered.
在輸入福斯之前。


RESTRMRG FORTH
RESTRMRG 前進


RESTSCR ( --- ) SAVESCR
RESTSCR （ --- ） 保存
Restore the screen from the external segment screen save area.
從外部區段螢幕儲存區域還原螢幕。
Un-nestable up to three times.
最多可嵌套三次。


RESTSTAT FORTH
RESTSTAT 前進


RESTTABS FORTH
RESTTABS 前進


REVEAL ( -- ) KERNEL3
揭示 （ -- ） KERNEL3
Activates (reveals) the Last definition in the Header
啟用 （顯示） 標頭中的最後一個定義
Dictionary.
字典。


REVERSEVAL FORTH
逆轉前進


REVVAL FORTH
轉動前進


RMARGIN ( -- a1 ) KERNEL4
RMARGIN （ -- a1 ） KERNEL4
Controls the right margin, used by ?LINE, ?CR. Specifys where
控制右邊距，由 ？LINE， ？CR. 指定位置
to wrap the line. Default value is 70.
以換行。預設值為 70。


ROLL ( n1 --- n2 ) KERNEL1
滾動 （ n1 --- n2 ） KERNEL1
Similar to SHAKE and RATTLE. Should be avoided. 1 ROLL is
類似於 SHAKE 和 RATTLE。應該避免。1 卷是
SWAP, 2 ROLL is ROT, etc. ROLL can be useful, but it is SLOW.
SWAP，2 ROLL 是 ROT，等等。ROLL 可能有用，但它很慢。


ROOT ( --- ) VOCABS
ROOT （ --- ） 詞彙
The root vocabulary that is always available in the vocabulary
詞彙表中始終可用的根詞彙表
list.
目錄。


ROOTDIR HIDDEN
ROOTDIR 隱藏


ROT ( n1 n2 n3 --- n2 n3 n1 ) KERNEL1
ROT （ n1 n2 n3 --- n2 n3 n1 ） KERNEL1
Rotate the top three element, bringing the third to the top.
旋轉前三個元素，將第三個元素帶到頂部。


ROWS ( --- n1 ) VIDEO
行 （ --- n1 ） 視頻
A VALUE that returns the number of ROWS available on the
傳回
current display as determined at boot time. You should use
在開機時確定的當前顯示。您應該使用
this VALUE to adjust your programs to work with displays having
此值來調整您的程式以使用具有
between 25 and 60 lines. See also COLS.
25 到 60 行之間。另見 COLS。


RP! ( a1 --- ) KERNEL1
RP！（ A1 --- ）KERNEL1
( Warning, this is different from FIG Forth )
（警告，這與圖四不同）
Sets the return stack pointer to the specified value.
將傳回堆疊指標設定為指定的值。


RP0 ( --- a1 ) KERNEL2
RP0 （ --- a1 ） KERNEL2
Empty return stack for this task.
此工作的空傳回堆疊。


RP@ ( --- a1 ) KERNEL1
Return the address of the next entry on the return stack.
傳回傳回堆疊上下一個專案的位址。


RPICK FORTH
選擇前進


RUN ( --- ) KERNEL3
運行 （ --- ） KERNEL3
Interpret or compile whatever is in the TERMINAL INPUT BUFFER.
解譯或編譯 TERMINAL INPUT BUFFER 中的任何內容。
Tests STATE, and does the appropriate thing.
測試 STATE，並執行適當的動作。


RUN-A; FORTH
跑動 A;第四


RWERR ( --- a1 ) HANDLES
RWERR （ --- a1 ） 手柄
A VARIABLE that holds the value of the most recent disk read or
保存最近磁碟讀取值的 VARIABLE 或
write error.
寫入錯誤。


RWMODE ( --- a1 ) HANDLES
RWMODE （ --- a1 ） 控制碼
the variable rwmode, which defaults to a value of 2, controls
變數 rwmode （預設值為 2） 會控制
the read write mode of the file being opened, the value 2 is
正在開啟的檔案的讀寫模式，值 2 為
read, or write, a value of 1 specifies write only, and a value
read 或 write，值 1 指定僅寫入，而值
of 0 specifies read only.
0 指定唯讀。


S>D ( n1 --- d1 ) KERNEL1
S>D （ n1 --- d1 ） KERNEL1
Take a single precision number and make it double precision by
取一個單精度數字，並使其雙精度為
extending the sign bit to the upper half.
將標誌位延伸至上半部。


SAVE!> ( n1 --- ) followed by the name of a definition SAVEREST
SAVE！> （ n1 --- ） 後面跟著定義 SAVEREST 的名稱
Saves the body contents of the definition following to the
將下列定義的內文內容儲存至
return stack, and sets the body to value n1. Used to save and
return stack，並將本文設定為值 n1。用於保存和
set VARIALBEs or VALUEs. Complimented by RESTORE>.
設定 VARIALBE 或 VALUE。由 RESTORE> 稱讚。


SAVE-EXE ( | <name> --- ) SAVEEXE
保存-EXE （ |<name> --- ）拯救
Save the current Forth memory image to the file <name> if
如果<name>出現以下情況，請將目前的 Forth 記憶體映像儲存到檔案中
present, or if not present, then prompt for a name to save to.
存在，如果不存在，則提示輸入要儲存的名稱。


SAVE-GET HIDDEN
儲存-隱藏


SAVE-GET1? HIDDEN
保存 GET1？潛


SAVE> ( --- ) followed by a name in definition SAVEREST
SAVE> （ --- ） 後面接著定義 SAVEREST 中的名稱
Saves the body contents of the definition following to the
將下列定義的內文內容儲存至
return stack. Used to save VARIABLEs or VALUEs that may be
返回堆疊。用於儲存可能為
changed by a following operation. Complimented with RESTORE>.
由以下操作更改。與 RESTORE> 相輔相成。
See also SAVE!>
另請參閱 SAVE！>


SAVECURSOR FORTH
拯救者前進


SAVEERR FORTH
拯救前進


SAVEFLG HIDDEN
保存隱藏


SAVEMACS HIDDEN
隱藏的 SAVEMACS


SAVEMENU FORTH
保存菜單


SAVEPOINTER ( --- ) SEQREAD
保存指標 （ --- ） SEQREAD
Save the file offset into the current file for later restoral.
將檔案偏移儲存到目前檔案中，以便稍後還原。


SAVESCR ( --- ) SAVESCR
SAVESCR （ --- ） SAVESCR
Save the current contents of the screen to an external segment
將畫面的目前內容儲存至外部區段
save area. Nestable up to three times.
節省區域。最多可嵌套三次。


SAVESTATE ( --- ) UTILS
SAVESTATE （ --- ） UTILS
Saves F-PC's state, including BASE, CAPS, LMARGIN, RMARGIN,
保存 F-PC 的狀態，包括 BASE、CAPS、LMARGIN、RMARGIN、
TABSIZE and STATV.
TABSIZE 和 STATV 的 STATV 中。


SCAN ( a1 n1 c1 --- ) KERNEL2
掃描 （ a1 n1 c1 --- ） KERNEL2
Given the address and length of a string, and a character to
給定字串的位址和長度，以及一個字元
look for, run through the string until we find the character.
尋找，遍歷字串，直到找到字元。
Leave the address of the match and the length of the remaining
留下匹配的地址和剩餘的長度
string.
繩子。


SCANW ( a1 w1 w2 --- a2 w3 ) SCAN
掃描 （ a1 w1 w2 --- a2 w3 ） 掃描
Scan array at a1 for length w1 words for word value w2. Returns
掃描 a1 處的陣列，尋找長度 w1 字，找出字值 w2。傳回
address a2 where w2 was found, and length remaining w3.
找到 W2 的地址 A2，剩餘長度 W3。


SCREENCHAR FORTH
SCREENCHAR 前進


SEARCH ( sadr slen badr blen -- n1 f1 ) SEARCH
搜尋 （ sadr slen badr blen -- n1 f1 ） 搜尋
Search for string sadr,slen contained in badr,blen. Returns f1
搜索 badr，blen 中包含的字符串 sadr，slen。傳回 f1
equal true if found, and n1 equal to the offset into the string
如果找到，則等於 true，並且 n1 等於字串的偏移量
where sadr,slen was found.
薩德爾，斯倫被發現的地方。


SEARCHEDIT HIDDEN
搜尋編輯隱藏


SEARCHFILE HIDDEN
搜尋檔案隱藏


SEARCHSETUP HIDDEN
搜尋設定隱藏


SEC-ELAPSED ( --- N1 ) TIMESTUF
SEC-ELAPSED （ --- N1 ） TIMESTUF
Return n1 the seconds that have elapsed since TIME-RESET.
傳回 n1 自 TIME-RESET 以來經過的秒數。


SECONDS ( N1 --- ) TIMESTUF
秒 （ N1 --- ） TIMESTUF
Wait n1 seconds.
等待 n1 秒。


SED ( | filename --- ) TOPEDIT
SED （ | 檔案名稱 --- ） TOPEDIT
Start the editor on the filename specified, or if no name is
在指定的檔案名稱上啟動編輯器，或者如果沒有名稱
specified, then prompt for a file. Will create a file if it
指定，然後提示輸入檔案。如果它，將創建一個文件
does not already exist. See also EDITOR
尚不存在。另請參閱編輯器


SEDCHAR FORTH
塞查爾·福斯


SEE ( <name> --- ) DECOM
參見 （ <name> --- ） DECOM
The user interface. To decompile something type SEE <name>.
使用者介面。若要反編譯某些內容，請鍵入 SEE <name>。


SEEK ( d1 --- ) SEQREAD
SEEK （ d1 --- ） 序列
Seek (move pointer) to position d1 in the current file.
搜尋 （移動指標） 至目前檔案中的 d1 位置。


SEGSET ( --- ) KERNEL4
SEGSET （ --- ） KERNEL4
A DEFERed word that contain the current function used to set up
包含用來設定的現行函式的 DEFERed 字組
the segment registers at cold start time. Typically contains
區段會在冷啟動時註冊。通常包含
SETYSEG.
塞蒂塞格。


SELECT ( n1 --- ) KERNEL4
選擇 （ n1 --- ） KERNEL4
Select drive n1 as the current disk drive to use as the DEFAULT
選取磁碟機 n1 作為現行磁碟機，以作為 DEFAULT
drive when no drive is specified. N1 ranges from 0 which is
驅動，如果未指定磁碟機。N1 的範圍從 0 開始，即
drive A:, to a legal value up to 255 in DOS.
驅動器 A：，在 DOS 中達到高達 255 的法定值。


SEQDOWN ( --- ) SEQREAD
序列 （ --- ） 序列
Step down one handle in the handle stack. closes the current
在手柄堆疊中放下一個手柄。關閉電流
file, and selects the next lower file.
檔案，然後選取下一個較低的檔案。


SEQHANDLE+ ( --- a1 ) SEQREAD
SEQHANDLE+ （ --- a1 ） SEQREAD
A VALUE that holds the address of the NEXT available sequential
一個 VALUE，它保存了 NEXT 可用循序的位址
file handle. Oftain used to hold temporary file information
檔案控點。用於保存臨時文件信息的 Oftain
during copy or rename operations.
在複製或重新命名作業期間。


SEQHANDLE ( --- a1 ) KERNEL2
SEQHANDLE （ --- a1 ） KERNEL2
A VALUE that holds the address of the current sequential file
保存現行循序檔案位址的 VALUE
handle. This handle holds the filename of the currently open
柄。此控制碼會保存目前開啟的檔案名稱
file if any, along with the DOS handle number if the file is
檔案（如果有）以及 DOS 句柄號碼（如果檔案是
open.
開。


SEQINIT ( --- ) SEQREAD
SEQINIT （ --- ） SEQREAD
Initialize the handle stack, in preparation for use.
初始化控制碼堆疊，以準備使用。


SEQUP ( --- ) SEQREAD
序列 （ --- ） 序列
Step up one handle in the handle stack.
在手柄堆棧中向上移動一個手柄。


SET-CURSOR ( N1 --- ) IBMCURSR
SET-CURSOR （ N1 --- ） IBMCURSR
Set the cursor shape to the mask value n1.
將游標形狀設定為遮罩值 n1。


SET-DTA ( a1 --- ) HANDLES
SET-DTA （ a1 --- ） 句柄
Set the Disk Transfer Area as a1.
將磁碟傳輸區域設定為 a1。


SETASSEM FORTH
塞塔西姆前進


SETBLOCK ( seg size --- f1 ) SETBLOCK
SETBLOCK （ seg 大小 --- f1 ） SETBLOCK
Adjust the segment seg to the new size in 16 byte segments.
將區段區段調整為 16 位元組區段中的新大小。
return error flag f1 non-zero if the adjustment did not
傳回錯誤旗標 f1 非零 （如果調整未完成）
succeed.
成功。


SETDATE ( NM Y --- ) TIMER
SETDATE （ NM Y --- ） 計時器
Set the DOS date given the double date.
設定給定雙重日期的 DOS 日期。


SETFL HIDDEN
隱藏的 SETFL


SETMAC HIDDEN
SETMAC 隱藏


SETTIB ( a1 --- ) SEQREAD
SETTIB （ a1 --- ） 序列
Sets the terminal input buffer to the counted string a1, in
將終端機輸入緩衝區設定為計數字串 a1，在
preperation for INTERPRETation, or WORD. Be sure to save the
為 INTERPRETation 或 WORD 做準備。請務必儲存
current TIB for later restoral.
當前 TIB 以供以後修復。


SETTIME ( HM Sh --- ) TIMER
SETTIME （ HM Sh --- ） 定時器
Set the DOS time given the double time.
設置給定雙倍時間的 DOS 時間。


SETVIEW ( | <path> --- ) VIEW
SETVIEW （ |<path> --- ）觀
Set the VIEWPATH handle to <path>. If <path> is omitted, it
將 VIEWPATH 控點設定為 <path>。如果<path>省略，則
will be prompted.
將被提示。


SETYSEG ( --- ) KERNEL2
SETYSEG （ --- ） KERNEL2
Set the segment variables as needed.
視需要設定區段變數。


SET_VECTORS ( -- ) KERNEL4
SET_VECTORS （ -- ） KERNEL4
Set the CONTROL BREAK and DIVIDE by 0 traps to point to the
將 CONTROL BREAK 和 DIVIDE by 0 設陷設定為指向
Forth provided functions, so we can handle them smoothly.
Forth 提供了函數，因此我們可以順利處理它們。


SEXE FORTH
塞克斯前進


SHOW.COLOR FORTH
示。色彩四射


SHOW.MOUSE FORTH
示。鼠標向前


SHOWDIR HIDDEN
隱藏的 SHOWDIR


SHOWKEYS HIDDEN
隱藏的顯示鍵


SHOWLINES ( --- ) SEQREAD
SHOWLINES （ --- ） 序列
Turn on listing of lines while loading.
載入時開啟線路清單。


SHOWMENUS FORTH
顯示菜單


SHOWPATH HIDDEN
隱藏的展示路徑


SHOWSRC FORTH
顯示來源


SIGN ( n1 --- ) KERNEL2
符號 （ n1 --- ） KERNEL2
If n1 is negative insert a minus sign into the string.
如果 n1 為負數，則在字串中插入減號。


SKIP ( a1 n1 c1 --- ) KERNEL2
跳過 （ a1 n1 c1 --- ） KERNEL2
Given the address and length of a string, and a character to
給定字串的位址和長度，以及一個字元
look for, run through the string while we continue to find the
尋找，在我們繼續尋找
character. Leave the address of the mismatch and the length of
字。留下不匹配的地址和長度
the remaining string.
剩餘的字串。


SKIP.BLANKS FORTH
遺漏。空白四出


SKIP_TO FORTH
SKIP_TO 向前


SLOW ( --- ) QVIDEO
慢速 （ --- ） QVIDEO
Select the BDOS screen output routines. Mose everything will
選取 BDOS 畫面輸出常式。摩西一切都會
still work but BOY WILL IT BE SLOW! NO COLOR SUPPORT in this
仍然有效，但天哪會很慢！此中不支援顏色
mode.
方式。


SMASK FORTH
斯馬斯普斯


SOURCE ( --- a1 n1 ) KERNEL2
來源 （ --- a1 n1 ） KERNEL2
Return a string from the current input stream.
從目前的輸入資料流程傳回字串。


SP! ( a1 --- ) KERNEL1
SP！（ A1 --- ）KERNEL1
( Warning, this is different from FIG Forth )
（警告，這與圖四不同）
Sets the parameter stack pointer to the specified value.
將參數堆疊指標設定為指定的值。


SP0 ( --- a1 ) KERNEL2
SP0 （ --- a1 ） KERNEL2
Empty parameter stack for this task.
此工作的空參數堆疊。


SP@ ( --- a1 ) KERNEL1
Return the address of the next entry on the parameter stack
傳回參數堆疊上下一個專案的位址


SPACE ( --- ) KERNEL2
空間 （ --- ） KERNEL2
Send a space to the terminal
將空間傳送至終端機


SPACES ( n1 --- ) KERNEL2
空格 （ n1 --- ） KERNEL2
Send a set of spaces to the terminal, uses the SPCS array to
將一組空格發送到終端機，使用 SPCS 陣列來
TYPE the spaces out very quickly
快速鍵入空格


SPAN ( --- a1 ) KERNEL2
跨度 （ --- a1 ） KERNEL2
Number of characters input by EXPECT.
EXPECT 輸入的字元數。


SPCHECK FORTH
檢查前進


SPCS ( --- a1 ) KERNEL2
SPCS （ --- a1 ） KERNEL2
An array of spaces used by SPACES to display spaces quickly.
SPACES 用來快速顯示空間的空間陣列。
This array holds 132 spaces, for displays up to 132 columns
此陣列可容納 132 個空格，最多可顯示 132 列
wide.
寬。


SPLIT ( n1 --- n2 n3 ) KERNEL1
斯普利特 （ n1 --- n2 n3 ） KERNEL1
SPLIT the 16 bit value n1 into two stack entries which are the
將 16 位值 n1 拆分為兩個堆疊條目，這些條目是
LOW and HIGH bytes of N1. The HIGH byte is on the top of the
N1 的 LOW 和 HIGH 位元組。HIGH 位元組位於
stack.
堆。


SPLIT-L# HIDDEN
SPLIT-L# 隱藏


SP_SAVE HIDDEN
SP_SAVE 隱藏


SRCCR FORTH
SRCCR 福斯


SRCEEOLCR HIDDEN
SRCEEOLCR 隱藏


SRCOFF ( --- ) DECOM
SRCOFF （ --- ） DECOM
A control to the debugger, to cause the source for a word being
偵錯工具的控制項，以導致單字的來源
debugged NOT to be displayed.
debugged 不顯示。


SRCON ( --- ) DECOM
SRCON （ --- ） DECOM
A control to the debugger, to cause the source for a word being
偵錯工具的控制項，以導致單字的來源
debugged to be displayed.
debugged 以顯示。


SSEG ( --- a1 ) KERNEL2
SSEG （ --- a1 ） KERNEL2
A VARIABLE that holds the absolure segment where SEARCHing is
一個 VARIABLE，它保存了絕對區段，其中 SEARCHing 是
done.
熟。


SS_SAVE HIDDEN
SS_SAVE 隱藏


STACKOVER FORTH
堆疊前


STACKUNDER FORTH
堆疊下 FORTH


START ( --- ) KERNEL4
START （ --- ） KERNEL4
A minimum initialization word, clears the input stream, and the
最小初始化字，清除輸入資料流程，以及
data stack, then performs DEFAULT, and INTERPRETs the input
資料堆疊，然後執行 DEFAULT，並 INTERPRET 輸入
stream.
河。


STATE ( --- a1 ) KERNEL2
狀態 （ --- a1 ） KERNEL2
A USER VARIABLE that holds the system STATE, used to determine
保存系統狀態的使用者變數，用來判斷
if Forth is COMPILING or INTERPRETING.
如果 Forth 正在編譯或解釋中。


STATOFF ( --- ) STATUS
STATOFF （ --- ） 狀態
Turn status displaying off.
關閉狀態顯示。


STATON ( --- ) STATUS
STATON （ --- ） 狀態
Turn status displaying on.
開啟狀態顯示。


STATUS ( -- ) KERNEL3
狀態 （ -- ） KERNEL3
Indicate the current status of the system.
指出系統的現行狀態。


STATV FORTH


STIME ( --- a1 ) TIMER
STIME （ --- a1 ） 定時器
A double variable that holds the BINARY start time for various
一個雙精度變量，用於保存各種
timing operations.
計時操作。


STRIPPING_BL'S HIDDEN
STRIPPING_BL 隱藏


STRIP_BL'S HIDDEN
STRIP_BL 隱藏


SUVEC FORTH
SUVEC 福斯


SV-CONTEXT HIDDEN
SV-上下文隱藏


SV-CURRENT HIDDEN
SV-電流隱藏


SVINIT ( --- ) SAVESCR
SVINIT （ --- ） SAVESCR
Cold start initialization word that allocates some space for
冷啟動初始化字，可為
the screen save segment.
螢幕儲存區段。


SVMAX FORTH
SVMAX 福斯


SVSEG ( --- seg1 ) SAVESCR
SVSEG （ --- seg1 ） SAVESCR
A constant that returns the segment of the screen save area.
傳回螢幕儲存區域區段的常數。
When not initialized, svseg return a zero.
未初始化時，svseg 會傳回零。


SVSIZE FORTH


SVTOTAL FORTH
SVTOTAL 福斯


SWAP ( n1 n2 --- n2 n1 ) KERNEL1
掉期 （ n1 n2 --- n2 n1 ） KERNEL1
Exchange the top two elements on the stack.
交換堆疊上的前兩個元素。


SYS ( | command --- ) EXEC
SYS （ | 命令 --- ） 執行
Accept the command line (up to line end) following SYS as a DOS
接受 SYS 後面的命令列 （直到行尾） 作為 DOS
command line.
命令列。


T>B ( d1 --- d2 ) TIMER
T>B （ d1 --- d2 ） 定時器
Convert the d1 DOS double time value to d2 the BINARY time.
將 d1 DOS 雙倍時間值轉換為 d2 BINARY 時間。


TAB ( -- ) KERNEL4
TAB （ -- ） KERNEL4
Print spaces to get to the next TAB increment as specified by
列印空格以取得下一個 TAB 增量，如
TABSIZE.
TABSIZE。


TABSIZE ( --- a1 ) KERNEL4
TABSIZE （ --- a1 ） KERNEL4
Controls the TAB increment for TAB. Default is 8.
控制 TAB 的 TAB 增量。預設值為 8。


TELETYPE ( --- ) PRTCTRL
電傳打字機 （ --- ） PRTCTRL
Select the dumbest printer, so NOT CONTROL CHARACTER aside from
選擇最愚蠢的打印機，因此除了 CONTROL CHARACTER
CR and LF will be sent to the printer. BOLD and UNDERLINE wil
CR 和 LF 將傳送到印表機。粗體和下劃線將
not function with this driver.
無法與此驅動程序一起使用。


TENTHS ( N1 --- ) TIMESTUF
十分之一 （ N1 --- ） TIMESTUF
Wait n1 tenths of a second.
等待 n1 十分之一秒。


THEN ( -- ) KERNEL3
然後 （ -- ） KERNEL3
Terminate a branch structure. Used in the form:
終止分支結構。以下列形式使用：
flag IF ... ELSE ... THEN
標記 IF ...其他的。。。當時


THESE ( --- ) WORDS
這些 （ --- ） 字
A option passed to WORDS, to control whether WORDS will look in
傳遞給 WORDS 的選項，用於控制 WORDS 是否會查閱
all vocabularys, or only the CONTEXT vocabulary. The following
所有詞彙，或僅 CONTEXT 詞彙。下列內容
command sequence will cause WORDS to display only those words
命令序列將導致 WORDS 僅顯示這些單字
containing XYZ in the HIDDEN vocabulary:
在 HIDDEN 詞彙表中包含 XYZ：
HIDDEN THESE WORDS XYZ <enter>
隱藏這些字詞 XYZ <enter>


TIB ( --- a1 ) KERNEL2
TIB （ --- a1 ） KERNEL2
Leaves address of text input buffer.
留下文字輸入緩衝區的位址。


TILLKEY ( n1 --- ) TIMESTUF
TILLKEY （ n1 --- ） TIMESTUF
Wait up to n1 seconds for the user to press a key, then
等待最多 n1 秒，讓使用者按下按鍵，然後
continue on whether they have pressed a key or not.
繼續他們是否按下了某個鍵。


TIME-ELAPSED ( --- d1 ) TIMER
時間流逝 （ --- d1 ） 計時器
Return d1 the binary time elapsed since the last TIME-RESET.
傳回 d1 自上次 TIME-RESET 以來經過的二進位時間。


TIME-RESET ( --- ) TIMER
時間重置 （ --- ） 計時器
Reset the start time to the current time.
將開始時間重設為目前時間。


TIMER ( | forth_commands --- )TIMER
計時器 （ | forth_commands --- ）計時器
Measure the time it takes to interpret the forth commands on
測量解釋第四個命令所需的時間
the following command line.
下列命令列。


TIMERCTRL FORTH


TIMERDATA FORTH
TIMERDATA 福斯


TIMES ( N1 -- ) UTILS
時間 （ N1 -- ） UTILS
Re-execute the input stream N1 number of times. Used in the
重新執行輸入資料流程 N1 次數。用於
form: CR HERE . 5 TIMES <enter>
表格：CR HERE 。5 次<enter>


TIMES ( n1 -- ) UTILS
TIMES （ n1 -- ） UTILS
Re-execute the input stream a specified number of times.
重新執行輸入串流指定的次數。


TLC HIDDEN
TLC 隱藏


TLN HIDDEN
TLN 隱藏


TONE FORTH
語氣


TONEGATE FORTH
音門前進


TOPCR HIDDEN
TOPCR 隱藏


TOPCRS HIDDEN
隱藏的頂部


TOPRINTER ( --- ) PRINT
打印機 （ --- ） 打印
An ALIAS for PCLOSE. Close the current print file, and restore
PCLOSE 的別名。關閉目前的列印檔案，然後還原
printing to the PRN device.
列印至 PRN 裝置。


TOS ( --- a1 ) KERNEL2
服務條款 （ --- a1 ） KERNEL2
Top OF Stack, Saved during Task switching.
堆疊頂部，在任務切換期間儲存。


TOTALLINES ( --- a1 ) SEQREAD
總線 （ --- a1 ） 順序
A VARIABLE that holds the total number of lines the system has
一個 VARIABLE，它保存了系統具有的行總數
read and compiled since it was last reset. Incremented by
自上次重設以來已讀取並編譯。遞增方式
LINEREAD.
線讀。


TOTALWORDS ( --- a1 ) WORDS
TOTALWORDS （ --- a1 ） 單詞
Accumulator for the total number of names.
名稱總數的累加器。


TRACK-MARKS HIDDEN
隱藏的痕跡


TRACK-MENU HIDDEN
軌道選單隱藏


TRACK-MOUSE FORTH
追蹤滑鼠向前


TRAVERSE ( a1 direction -- addr' ) KERNEL3
TRAVERSE （ a1 方向 -- addr' ） KERNEL3
Run through a name field in the specified direction. Terminate
沿指定方向穿過名稱欄位。絕
when a byte whose high order bit is on is detected.
當偵測到高位位元開啟的位元組時。


TRC HIDDEN
TRC 隱藏


TRIM ( faddr voc-addr -- ) KERNEL3
TRIM （ faddr voc-addr -- ） KERNEL3
Change the hash pointers in a vocabulary so that they are all
變更詞彙表中的雜湊指標，使其全部
less than a specified value, faddr.
小於指定值 faddr。


TRUE ( --- f1 ) KERNEL1
TRUE （ --- f1 ） KERNEL1
A CONSTANT that returns -1, a boolean true.
傳回 -1 的 CONSTANT，布林值 true。


TTIME ( --- a1 ) TIMER
TTIME （ --- a1 ） 計時器
A double variable that holds the DOS total time.
保存 DOS 總時間的雙重變數。


TUCK ( n1 n2 --- n2 n1 n2 ) KERNEL1
TUCK （ n1 n2 --- n2 n1 n2 ） KERNEL1
Tuck the first element under the second one.
將第一個元素塞到第二個元素下方。


TURNKEY ( | <name> --- ) SAVEEXE
交鑰匙 （ |<name> --- ）拯救
Save a copy of the current memory image to the file <name> as
將目前記憶體映像的副本儲存到檔案<name>中，作為
an .EXE file. The LIST segment id compressed as much as
一個.EXE 檔案。LIST 區段 ID 壓縮至
possible. The CODE segment is compressed as much as possible,
會。CODE 段盡可能壓縮，
and the HEAD segment is discarded completely. The created .EXE
並且 HEAD 段被完全丟棄。創建的.EXE
file is not Forth any more, and can only perform whatever
檔案不再是 Forth，只能執行任何
function was plugged into BOOT or DEFAULT before TURNKEY was
在 TURNKEY 之前，功能已插入 BOOT 或 DEFAULT
performed. The user is responsible for performing whatever
執行。使用者負責執行任何
initializaton is needed, and for handling ALL error conditions.
initializaton 是需要的，並且用於處理所有錯誤情況。
However wonderful this word may sound, it is NOT for the faint
無論這個詞聽起來多麼美妙，它都不適合膽小的人
of heart.
心。


TX HIDDEN
TX 隱藏


TY HIDDEN
泰隱藏


TYPE ( a1 n1 --- ) KERNEL2
類型 （ a1 n1 --- ） KERNEL2
A defered word used to Print a string to the current output
用於將字串列印到目前輸出的延遲字
device from the segment specified in the variable TYPESEG.
裝置，來自變數 TYPESEG 中指定的區段。


TYPEL FORTH
打字


U*D ( n1 n2 --- d1 ) KERNEL1
U*D （ n1 n2 --- d1 ） KERNEL1
U*D is a synonym for UM*
U*D 是 UM* 的同義詞


U. ( n1 --- ) KERNEL2
U. （ n1 --- ） KERNEL2
Output as an unsigned single number with trailing space.
輸出為帶有尾端空格的無符號單個數字。


U.R ( n1 n2 --- ) KERNEL2
U.R （ n1 n2 --- ） KERNEL2
Output as an unsigned single number right justified.
輸出為無符號單數右對齊。


U16/ ( n1 --- n2 ) KERNEL1
U16/ （ n1 --- n2 ） KERNEL1
Four 16 bit logical right shifts. Unsigned divide by 16
四個 16 位邏輯右移。無符號除以 16
decimal.
十進位的。


U2/ ( n1 --- n2 ) KERNEL1
U2/ （ n1 --- n2 ） KERNEL1
16 bit logical right shift.
16 位邏輯右移。


U8/ FORTH
U8/第四


U< ( n1 n2 --- f1 ) KERNEL1
U< （ n1 n2 --- f1 ） KERNEL1
Compare the top two elements on the stack as unsigned integers
將堆疊上的前兩個元素比較為無正負號整數
and return true if the second is less than the first. Be sure
如果第二個小於第一個，則傳回 true。確定
to use U< whenever comparing addresses, or else strange things
每當比較地址時使用 U<，否則會發生奇怪的事情
will happen beyond 32K.
將發生在 32K 之後。


U<= ( un1 un2 --- f1 ) UTILS
U<= （ un1 un2 --- f1 ） UTILS
Unsigned less than or equal.
無符號小於或等於。


U> ( n1 n2 --- f1 ) KERNEL1
U> （ n1 n2 --- f1 ） KERNEL1
Compare the top two elements on the stack as unsigned integers.
將堆疊上的前兩個元素比較為無符號整數。
True if n1 > n2 unsigned.
如果 n1 > n2 未負負號，則為 True。


U>= ( n1 n2 --- f1 ) UTILS
U>= （ n1 n2 --- f1 ） 效用
Unsigned greater than or equal.
無符號大於或等於。


UCSCAN FORTH
UCSCAN 福斯


UD. ( d1 --- ) KERNEL2
烏德。（ d1 --- ）KERNEL2
Output as an unsigned double number with a trailing space
輸出為帶有尾端空格的無符號雙精度數


UD.R ( d1 n1 --- ) KERNEL2
烏德。R （ d1 n1 --- ） KERNEL2
Output as an unsigned double number right justified.
輸出為無符號雙對齊。


UM* ( un1 un2 -- ud ) KERNEL1
UM* （ un1 un2 -- ud ） KERNEL1
Return a 32 bit unsigned product of two 16 bit unsigned
傳回兩個 16 位元未帶正負號的 32 位元未帶正負號乘積
numbers.
數字。


UM/MOD ( ud un --- uremainder uquotient ) KERNEL1
UM/MOD （ ud un --- uremainder uquotient ） KERNEL1
The unsigned double numerator ud is divided by an unsigned
無符號雙分子 ud 除以無符號
single denominator un to produce an unsigned quotient and
單分母 un 產生無符號商，並且
unsigned remainder. The quotient is at the top of the stack.
未簽名的餘數。商位於堆棧的頂部。


UMAX FORTH
UMAX 福斯


UMIN FORTH
烏明福斯


UNBUG ( -- ) DEBUG
取消錯誤 （ -- ） 偵錯
Remove the debug point currently in place.
移除目前就緒的偵錯點。


UNDEFER ( | <name> -- ) DEFERS
UNDEFER （ |<name> -- ）延期
This is sort of an undo for DEFERS. UNDEFER removes one level
這對 DEFERS 來說是一種撤消。UNDEFER 刪除了一級
from the chain of a defered word. Must be used with EXTREME
來自一個推遲的詞鏈。必須與 EXTREME 一起使用
caution, as there is no protection from trying to use it at the
請注意，因為沒有保護措施無法防止嘗試在
wrong time in the wrong place. YOU ARE ON YOUR OWN with this
錯誤的時間在錯誤的地方。你靠自己
one. See also DEFERS above.
一。另請參閱上面的 DEFERS。


UNDO ( --- ) KERNEL1
復原 （ --- ） KERNEL1
Cleans up the return stack so we can EXIT from the current loop
清理返回堆棧，以便我們可以退出當前循環
without crashing, as in DO and "UN"DO.
而不會崩潰，如 DO 和“UN”DO。


UNEDIT ( --- ) TOPEDIT
取消編輯 （ --- ） TOPEDIT
The word that gets plugged into CLEARMEM, which de-allocates
插入 CLEARMEM 的字，它取消配置
the memory used by the editor during an edit session. This is
編輯器在編輯工作階段期間使用的記憶體。這是
needed in the case where you want to spawn a DOS shell, as the
在您想要產生 DOS shell 的情況下需要，因為
SED editor consumes all of the available memory during an edit.
SED 編輯器會在編輯期間耗用所有可用記憶體。


UNINSTALL ( --- ) INSTALL
卸載 （ --- ） 安裝
Mark the F-PC currently in memory as un-installed. A subequent
將目前記憶體中的 F-PC 標示為已卸載。一個後續的
FSAVE will result in a system that comes up with the
FSAVE 將導致一個系統提出
UN-installed message in HELLO.
HELLO 中的 UN-installed 訊息。


UNINSTALLSTUFF ( --- ) UTILS
UNINSTALLSTUFF （ --- ） 公用程式
A DEFERed word that is executed by UNINSTALL. Typically
UNINSTALL 所執行的 DEFERed 字組。一般情況下
contains a chain of function to perform during the un-install
包含要在解除安裝期間執行的函式鏈
process.
過程。


UNNEST ( --- ) KERNEL1
UNNEST （ --- ） KERNEL1
Same as exit. Compiled by ; to help decompiling.
與退出相同。編譯者;以幫助反編譯。


UNTIL ( f1 -- ) KERNEL3
直到 （ f1 -- ） KERNEL3
Marks end of a BEGIN ... UNTIL loop; terminate if flag boolean
標記 BEGIN 的結束 ...UNTIL 迴圈;終止 if 旗標布林值
is true.
是真的。


UP ( --- a1 ) KERNEL1
UP （ --- a1 ） KERNEL1
Holds a pointer to the current USER area. ( multitasking )
保留指向當前 USER 區域的指標。（ 多工處理 ）


UPC ( char --- char' ) KERNEL2
UPC （ char --- char' ） KERNEL2
Convert a Char to upper Case
將 Char 轉換為大寫


UPPER ( a1 length --- ) KERNEL2
鞋面（a1 長度 --- ）KERNEL2
Take the string at the specified address and convert length
在指定位址取得字串並轉換長度
characters of it to upper case. It converts the string in
它的字符改為大寫。它將字串轉換為
place, so be sure to make a copy of the original if you need to
放置，因此如果需要，請務必複印原件
use it later.
稍後再用。


USED ( | <command_line> --- )UTILS
二手 （ |<command_line> --- ）公用事業
A word which calls USED! to save the current values of DP, XDP,
一個叫 USED 的詞！若要儲存 DP、XDP、
and YDP. USED then executes the command line following, and
和 YDP。然後，USED 執行以下命令列，並且
calculates the space used by the command line and displays the
計算指令行使用的空間，並顯示
results. USED is used as follows: USED FLOAD MYFILE <enter>
結果。USED 的用法如下：已使用 FLOAD MYFILE <enter>


USEDIN ( | <name> --- ) REF
使用於 （ |<name> --- ）參考文獻
An ALIAS for REF, this word looks through the dictionary and
REF 的別名，這個詞會翻閱字典，然後
finds words which use <name>, the names are then displayed.
尋找使用 的單字，<name> 然後顯示名稱。


USER ( --- ) KERNEL4
用戶 （ --- ） KERNEL4
VOCABULARY that holds multi tasking versions of defining
包含定義的多任務版本的詞彙
words.
言。


USER ( | <name> --- ) KERNEL4
用戶 （ |<name> --- ）KERNEL4
Vocabulary that holds task versions of defining words.
包含定義單字的任務版本的詞彙。


V FORTH
五福斯


VADDR FORTH
瓦德爾·福斯


VALUE ( n1 | <name> --- ) KERNEL3
值 （ n1 |<name> --- ）KERNEL3
Create <name> as a word which like a CONSTANT return its value,
創建<name>為一個單詞，它像 CONSTANT 一樣返回其值，
but which unlike a constant can be changed with the words: =:,
但與常數不同的是，可以用以下詞來更改：=：，
!>, INCR>, DECR>, OFF>, ON>, +!>. Values provide a more
！>、INCR>、DECR>、OFF>、ON>、+！>。值提供更多
readable source code than VARIABLES, and an improvement in
比 VARIABLES 更可讀的原始程式碼，並且改進了
performance as well.
性能也是如此。


VALUECOLOR HIDDEN
VALUECOLOR 隱藏


VARIABLE ( | <name> -- ) KERNEL3
可變 （ |<name> -- ）KERNEL3
A defining word to create variables. At runtime the address of
用於建立變數的定義詞。在執行階段，位址
the variable is placed on the stack.
變數會放置在堆疊上。


VARIABLECOLOR HIDDEN
可變顏色隱藏


VARIABLE FORTH
變量向前


VF FORTH
VF 福斯


VFIND FORTH


VIDEO-SEG ( --- a1 ) VIDEO
視訊 （ --- a1 ） 視訊
A variable that holds the segment value of the display screen.
保存顯示器區段值的變數。


VIDEO-TYPE ( a1 n1 --- ) VIDEO2
視訊類型 （ A1 N1 --- ） 視訊 2
The VERY FAST direct screen type routine, displays the string
VERY FAST 直接螢幕類型常式，顯示字串
starting at address a1 for length n1 at the current cursor
從位址 A1 開始，長度為 n1 在目前游標處
position specified by #LINE and #OUT. #OUT is incremented by
位置由 #LINE 和 #OUT 指定。#OUT 的遞增量為
n1. The variable NOSETCUR holds a flag that controls whether
註 1.變數 NOSETCUR 會保留一個旗標，可控制是否
VIDEO-TYPE should actually move the cursor during the type.
VIDEO-TYPE 實際上應該在類型期間移動游標。
VIDEO-TYPE is much faster if NOSETCUR is TRUE, but then the
如果 NOSETCUR 為 TRUE，則 VIDEO-TYPE 會快得多，但
cursor must be set later with an AT or TYPE with
游標必須稍後使用 AT 或 TYPE 設定，並
NOSETCUR=FALSE. This TRICK allows F-PC to re-display 10 full
NOSETCUR=FALSE 的 FALSE 。這個技巧允許 F-PC 重新顯示 10 個完整的
text screens per second on an XT (4.7mhz) class machine.
XT （4.7mhz） 類機器上每秒的文字螢幕數。


VIDEO-TYPEL FORTH
視訊類型


VIEW ( | <name> --- ) VIEW
查看 （ |<name> --- ）觀
A DEFERED word that contains either DOVIEW, or HELPVIEW. View
包含 DOVIEW 或 HELPVIEW 的 DEFERED 字組。觀
the source for <name>.
的來源 <name>。


VIEW> ( vfa -- cfa ) KERNEL3
觀點> （ vfa -- CFA ） KERNEL3
Go from view field address vfa to code field address cfa.
從檢視欄位位址 vfa 移至程式碼欄位位址 cfa。


VIEWFROM FORTH
從福斯開始


VIEWMACS HIDDEN
隱藏的 VIEWMACS


VMODE-VAR ( --- a1 ) VIDEO
VMODE-VAR （ --- A1 ） 視頻
A VARIABLE that holds the video mode that was obtained at
一個變數，用於保存在
system startup. See the IBM or Mictosoft documentation for
系統啟動。請參閱 IBM 或 Mictosoft 文件
further information on the various video modes.
有關各種視訊模式的更多資訊。


VMODE.SET ( --- ) VIDEO
VMODE。套裝 （ --- ） 視頻
Set the VIDEO-SEG variable after testing the current video
測試目前影片後設定 VIDEO-SEG 變數
mode, and perform any needed initialization required by
模式，並執行
executing the INITMONO, or INITCOLOR as needed.
視需要執行 INITMONO 或 INITCOLOR。


VOC-LINK ( --- a1 ) KERNEL2
Points to the most recently defined vocabulary.
指向最近定義的詞彙。


VOCABULARY ( | <name> -- ) KERNEL3
詞彙 （ |<name> -- ）KERNEL3
Defines a new Forth vocabulary <name>.
定義新的 Forth 詞彙 <name>。


VOCOFF FORTH
沃科夫·福斯


VOCON FORTH
沃肯福斯


VOCV FORTH
VOCV 福斯


VYET FORTH
前進


W$ FORTH
W$ 前進


W.ID FORTH
W.ID 向前


W.NAME ( NFA --- ) WORDS
W.NAME （ NFA --- ） 詞
Print name of word NFA. Test to see if conditions are correct,
列印單字 NFA 的名稱。測試條件是否正確，
like CODE, or ALL, or WITHIN, and print name.
例如 CODE、ALL 或 WITHIN，並列印名稱。


WARM ( -- ) KERNEL4
溫暖 （ -- ） KERNEL4
The WARM entry point for Forth, just calles the DEFERed word
Forth 的 WARM 入口點，只是呼叫 DEFERed 字
WARMFUNC, then calls BYE is WARMFUNC returns. A WARM start is
WARMFUNC，然後呼叫 BYE 是 WARMFUNC 傳回。熱啟動是
invoked whenever the CONTROL BREAK key is pressed.
每當按下 CONTROL BREAK 鍵時呼叫。


WARMFUNC ( --- ) KERNEL4
WARMFUNC （ --- ） KERNEL4
A DEFERed word that is invoked when a warm start occurs. This
發生暖啟動時呼叫的 DEFERed 字組。這
function is called whenever the CONTROL BREAK key is pressed.
每當按下 CONTROL BREAK 鍵時，都會呼叫函式。


WARMSTRT ( -- ) KERNEL4
WARMSTRT （ -- ） KERNEL4
The default function to be performed on a WARM start. This
要在 WARM 啟動時執行的預設功能。這
word is plugged into the DEFERed word WARMFUNC, to specify what
word 插入 DEFERed 字 WARMFUNC，以指定
is done when the CONTROL BREAK key is pressed. See also
當按下 CONTROL BREAK 鍵時完成。另請參閱
WARMFUNC and WARM.
WARMFUNC 和 WARM。


WARNING ( --- a1 ) KERNEL2
警告 （ --- a1 ） KERNEL2
A VARIABLE that holds a boolean flag that determines if you
一個 VARIABLE，它保存一個布林標誌，該標誌決定了您是否
should be warned in the event you re-define a definition name.
當您重新定義定義名稱時，應發出警告。


WARNOVER ( --- ) KERNEL3
華諾威 （ --- ） KERNEL3
A warning message that is issued by ?STACK in the event you are
所發出的警告訊息 ？STACK，前提是
close to running out of CODE memory.
快要耗盡 CODE 記憶體了。


WFLBUTTON HIDDEN
WFL 按鈕隱藏


WHILE ( f1 -- ) KERNEL3
而 （ f1 -- ） KERNEL3
Used in the form BEGIN <loop> flag WHILE <true> REPEAT. Repeat
以 BEGIN <loop> 旗標 WHILE REPEAT 的形式使用 <true>。重
<loop> and <true> clauses while the flag f1 is true (really,
<loop> 和<true>子句，而標誌 f1 為真（實際上，
non-zero).
非零）。


WHITE ( --- n1 ) COLOR
白色 （ --- n1 ） 顏色
A CONSTANT that return the value for the color white on a color
傳回顏色上白色值的 CONSTANT
display. White will blink if used in the background.
獻。如果在背景中使用白色會閃爍。


WHITE-ON-BLACK ( --- ) MONOCROM
黑底白字 （ --- ） 單色
Selects the normal display mode of light characters on a dark
選擇淺色字元在深色上的正常顯示模式
background. The opposite mode is BLACK-ON-WHITE.
背景。相反的模式是白底黑字。


WIDTH ( --- a1 ) KERNEL2
寬度 （ --- a1 ） KERNEL2
Number of characters to keep in name field.
要保留在名稱欄位中的字元數。


WITHHEADS FORTH
前行


WITHIN ( n1 n2 --- f1 ) KERNEL1
在 （ n1 n2 --- f1 ） KERNEL1 內
Return true if min <= n1 < max, otherwise false.
如果最小值 <= n1 < max，則傳回 true，否則傳回 false。


WITHNAME HIDDEN
隱藏名稱


WITHPATH ( --- f1 ) SEQREAD
WITHPATH （ --- f1 ） 後續讀取
A boolean VALUE that returns a true flag if the file path is to
布林值 VALUE，如果檔案路徑為
be included in the name of the variable that gets compiled by
包含在編譯的變數名稱中
LOADED, when adding a new file the loaded file list in the
LOADED，當新增檔案時，載入的檔案清單會
FILES vocabulary. WITHPATH is normally true, so user loaded
FILES 詞彙。WITHPATH 通常為 true，因此使用者載入
files can be located in whatever directory they are in.
檔案可以位於它們所在的任何目錄中。
WITHPATH is set to FALSE when compiling the system which allows
編譯系統時，WITHPATH 會設定為 FALSE，這允許
the VIEWPATH to be applied to system files and have their
要套用至系統檔案的 VIEWPATH ，並具有其
location specified at installation time.
安裝時指定的位置。


WORD ( C1 --- A1 ) KERNEL2
WORD（C1 --- A1 ）KERNEL2
Parse the input stream for char and return a count delimited
剖解析 char 的輸入資料流程，並傳回以分隔的計數
string at here. Note there is always a blank following it.
string 在這裡。請注意，它後面總是有一個空白。


WORDS ( | <text> <text> -- ) WORDS
文字 （ |<text> <text> -- ） 詞語
Display words that match text. <text> is optional, if ommited
顯示符合文字的字詞。<text> 是選用的，如果省略
then the CONTEXT vocabulary will be displayed. Two space
然後將顯示 CONTEXT 詞彙表。兩個空間
delimited <text> strings may follow, and only words containing
後<text>面可以有分隔字串，並且只有包含
both <text> strings will be printed:
<text> 將列印這兩個字串：


WORDSAVE FORTH
WORDSAVE 前方


WORDTYPE FORTH
字型第四


WRITE-EXE FORTH
寫入 EXE 前進


WRITE-ONLY FORTH
只寫 FORTH


X, ( n1 --- ) KERNEL2
X， （ n1 --- ） KERNEL2
Compile the value n1 into LIST space into the next available
將值 n1 編譯成 LIST 空間，進入下一個可用的
address as specified by XDPSEG and XDP. XDP is incremented by
XDPSEG 及 XDP 所指定的位址。XDP 的遞增量為
two.
二。


X," ( | <string>" --- ) KERNEL3
X“（ |<string>“ --- ）KERNEL3
A " delimited string from the input stream is compiled into
輸入流中的 “ 分隔字串會編譯成
LIST space. This word is used by ." and "" .
LIST 空間。這個詞由 .“ 和 ”“ 使用。


X>"BUF ( --- "BUF ) KERNEL3
X>“BUF （ --- ”BUF ） KERNEL3
This word is compiled by the "" word, it moves the string
這個字是由「」字編譯的，它移動字串
compiled into LIST space from LIST space to CODE space in the
編譯成 LIST 空間，從 LIST 空間到 CODE 空間，在
"BUF buffer. The address of "BUF is then returned on the stack.
“BUF 緩衝區。然後，「BUF」的位址會在堆疊上傳回。


XALIGN ( --- ) KERNEL3
XALIGN （ --- ） KERNEL3
Align XDP to the next higher even value. This word is not
將 XDP 對齊下一個較高的偶數值。這個詞不是
currently used in F-PC.
目前用於 F-PC。


XBINIT HIDDEN
XBINIT 隱藏


XBSEG HIDDEN
XBSEG 隱藏


XBUF# HIDDEN
XBUF# 隱藏


XBUF#+ HIDDEN
XBUF#+ 隱藏


XBUF#- HIDDEN
XBUF#- 隱藏


XBUF_INIT HIDDEN
XBUF_INIT 隱藏


XC, ( n1 --- ) KERNEL2
XC，（ n1 --- ） KERNEL2
Compile n1 into the next available byte in LIST space. XDP is
將 n1 編譯成 LIST 空間中的下一個可用位元組。XDP 是
incremented by one.
增加一。


XDOWN HIDDEN
XDOWN 隱藏


XDP ( --- a1 ) KERNEL2
XDP （ --- a1 ） KERNEL2
A VARIABLE that holds the offset into the XDPSEG where the next
一個 VARIABLE，它將偏移保留到 XDPSEG 中，其中下一個
word in a colon definition will be compiled. F-PC always
冒號定義中的單詞將被編譯。F-PC 始終
aligns colon definitions to the next higher segment boundry at
將冒號定義對齊下一個較高的區段邊界，位於
the start of a new definition, causing XDP to equal zero.
新定義的開頭，導致 XDP 等於零。


XDPSEG ( --- a1 ) KERNEL2
XDPSEG （ --- a1 ） KERNEL2
A VARIABLE that holds the current absolute segment where the
保存當前絕對段的 VARIABLE，其中
next colon definition will be compiled.
下一個冒號定義將被編譯。


XDPSEGLEN FORTH


XDUMP ( a1 n1 --- ) DUMP
XDUMP （ a1 n1 --- ） 傾出
DUMP an area of memory in the LIST segment. A1 is a relative
DUMP LIST 區段中的記憶體區域。A1 是親戚
segment offset from XSEG, and n1 is the length to dump in
segment 偏移至 XSEG 的，而 n1 是要傾出的長度
bytes. This is normally used as follows: ' HEX >BODY @ 10
位元組。這通常用法如下：' 十六進制 >BODY @ 10
XDUMP
XDUMP 的


XEVEN ( a1 --- a2 ) KERNEL3
XEVEN（ a1 --- a2 ） KERNEL3
LIST space is aligned on WORD boundries in F-PC, this word
LIST 空間在 F-PC 中的 WORD 邊界上對齊，這個單詞
aligns a1 to the next higher even address a2.
將 A1 與下一個較高的偶數位址 A2 對齊。


XEXPECT HIDDEN
XEXPECT 隱藏


XFDOS ( ?? --- ?? ) KERNEL2
XFDOS （ ?? --- ?? ）KERNEL2
call INT 21 with most any reg combination used. See the souce
使用大多數註冊組合呼叫 INT 21。查看來源
for this word in the KERNEL for more information on how to use
對於 KERNEL 中的這個詞，以獲取有關如何使用的更多信息
it.
它。


XHERE ( --- seg n1 ) KERNEL2
XHERE （ --- seg n1 ） KERNEL2
HERE for LIST space, returns the absolute segment SEG and the
HERE 對於 LIST 空間，傳回絕對區段 SEG 和
offset into that segment n1 of HERE in LIST space.
偏移到 LIST 空間中 HERE 的該段 n1。


XMAX HIDDEN
XMAX 隱藏


XMOVED FORTH
X 向前移動


XOR ( n1 n2 --- n3 ) KERNEL1
異或 （ n1 n2 --- n3 ） KERNEL1
Returns the bitwise Exclusive Or of n1 and n2 on the stack.
傳回堆疊上 n1 和 n2 的位元排他 Or。


XREF ( | <name> --- ) REF
外部參考 （ |<name> --- ）參考文獻
An ALIAS for REF, this word looks through the dictionary and
REF 的別名，這個詞會翻閱字典，然後
finds words which use <name>, the names are then displayed.
尋找使用 的單字，<name> 然後顯示名稱。


XSEG ( --- a1 ) KERNEL1
XSEG （ --- a1 ） KERNEL1
A system variable that holds the current absolute segment of
系統變數，可保存
the LIST area.
LIST 區域。


XSEGLEN FORTH
塞格倫福斯


XTMP HIDDEN
XTMP 隱藏


XUP HIDDEN
XUP 隱藏


Y! ( n1 a1 --- ) KERNEL2
Y!（ n1 a1 --- ）KERNEL2
Store the value n1 into the address a1 in HEAD space.
將值 n1 儲存到 HEAD 空間中的位址 a1 中。


Y, ( n1 --- ) KERNEL2
Y， （ n1 --- ） KERNEL2
Compile the value n1 into the next available location in HEAD
將值 n1 編譯到 HEAD 中的下一個可用位置
space. YDP is incremented by two.
間。YDP 會遞增 2。


Y-M-D ( --- ) TIMER
Y-M-D （ --- ） 計時器
Switch the system to using the date format Year-Month-Day.
將系統切換為使用日期格式 年-月-日。


Y@ ( a1 --- n1 ) KERNEL2
Fetch the 16 bit contents of a1 in HEAD space and return it as
在 HEAD 空間中獲取 a1 的 16 位內容並將其返回為
n1.
註1.


YC! ( n1 a1 --- ) KERNEL2
YC！（ n1 a1 --- ）KERNEL2
Store the byte value n1 into address a1 in HEAD space.
將位元組值 n1 儲存到 HEAD 空間中的位址 a1 中。


YC@ ( a1 --- n1 ) KERNEL2
Fetch the byte contents of a1 in HEAD space, and return it as
在 HEAD 空間中取得 a1 的位元組內容，並將其傳回為
n1.
註1.


YCOUNT ( a1 --- a2 n1 ) UTILS
YCOUNT （ a1 --- a2 n1 ） UTILS
The byte at a1 in HEAD space is returned as n1, and a2=a1+1.
HEAD 空間中 a1 處的位元組傳回為 n1，且 a2=a1+1。


YCSET ( byte a1 --- ) KERNEL2
YCSET （ 位元組 a1 --- ） KERNEL2
The byte located at a1 in HEAD space is ored with byte, and the
位於 HEAD 空間中 a1 的位元組會以位元組 OOR，而
result is saved back into addr.
結果儲存回 addr。


YDP ( --- a1 ) KERNEL2
YDP （ --- a1 ） KERNEL2
A variable that holds the address in HEAD space of the next
在下一個 HEAD 空間中保存地址的變量
available byte.
可用位元組。


YDP-HW HIDDEN
YDP-硬體隱藏


YDP-REG HIDDEN
YDP-REG 隱藏


YDP-SHIFT HIDDEN
YDP-SHIFT 隱藏


YDUMP ( A1 N1 --- ) DUMP
YDUMP （ A1 N1 --- ） 轉儲
Dump an area of the HEAD segment.
傾出 HEAD 區段的區域。


YELLOW ( --- n1 ) COLOR
黃色 （ --- n1 ） 顏色
The color value for YELLOW on a color monitor. Yellow blinks
彩色監視器上 YELLOW 的色彩值。黃色閃爍
when used in background.
在後台使用時。


YHASH ( yname vocaddr --- thre) KERNEL2
YHASH （ yname vocaddr --- thre） KERNEL2
Using the name address in HEAD space, and the vocabulary
在 HEAD 空間中使用名稱位址，以及詞彙
address, determine the address thread in the vocabulary that
address，則確定詞彙表中的地址執行緒
yname should go into. Used by HIDE and REVEAL.
yname 應該進入。由 HIDE 和 REVEAL 使用。


YHERE ( --- a1 ) KERNEL2
YHERE （ --- a1 ） KERNEL2
Push the contents of YDP the new HEAD pointer on the stack.
將 YDP 的內容推送到堆疊上的新 HEAD 指標。


YS: ( a1 --- yseg a1 ) KERNEL2
YS：（ a1 --- yseg a1 ） KERNEL2
Place a copy of the current HEAD segment under the address a1
將目前 HEAD 區段的副本放在位址 a1 下
on the stack.
在堆疊上。


YSEG ( -- a1 ) KERNEL1
YSEG （ -- a1 ） KERNEL1
A variable which holds the base of Head space.
一個變數，它保存了頭部空間的基礎。


YSTART ( --- a1 ) KERNEL2
YSTART（ --- a1 ）KERNEL2
System variable, If non-zero, ptr to start of headers after
系統變數，如果非零，則 ptr 為標頭的開頭
dictionary. Used to set DP in when SAVE-SYSTEM is used in
字典。用於在 SAVE-SYSTEM 使用時設定 DP in
making a .COM file.
製作一個.COM 文件。


[ ( -- ) KERNEL3
[ （ -- ） KERNEL3
Stop compiling and start interpreting.
停止編譯並開始解釋。


['] ( | <name> -- ) KERNEL3
[']( |<name> -- ）KERNEL3
Compile the CFA of <name> as a literal in a colon definition.
將 的 CFA 編譯<name>為冒號定義中的文字。
Like ' only used while compiling
像'只在編譯時使用


[COMPILE] ( | <name> -- ) KERNEL3
[編譯]( |<name> -- ）KERNEL3
Force <name> which is normally an immediate word to be compiled
力 <name>，通常是要編譯的直接詞
like any other word.
就像任何其他詞一樣。


\ ( -- ) KERNEL4
\ （ -- ） KERNEL4
This line is a comment till the end of this line, and any text
這一行是評論，直到這一行的末尾，任何文本
after the \ is ignored.
在忽略 \ 之後。


\%AT FORTH
\%在第四個


\%SPACES FORTH
\%空格向前


\%TENTHS FORTH
\%十分之一


\AT-REST FORTH
\靜止前進


\AT-SAVE FORTH
\AT-保存


\CHARS FORTH
\字符向前


\EMIT FORTH
\向前發射


\S ( n1 --- ) SEQREAD
\S （ n1 --- ） 序列
Stop loading the current file with the line that contains this
停止載入包含此行的目前檔案
word.
字。


\TYPE FORTH
\輸入 FORTH


\TYPEL FORTH


\U FORTH
\U 前進


\UNLESS ( | <name> --- ) UTILS
\除非 （ |<name> --- ）公用事業
An immediate word, dont load this line of source UNLESS <name>
立即說一句，除非加<name>載此源代碼行
is defined, that is treat this line as a comment if <name> is
定義了，即將此行視為註解，如果<name>是
not defined.
未定義。


\X FORTH
\X 向前


\Y FORTH
\Y 前進


\\ FORTH
\\ 向前


] ( -- ) KERNEL3
] （ -- ） KERNEL3
The Compiling Loop. First sets Compile State. Looks up the next
編譯迴圈。首先設定編譯狀態。查找下一個
word in the input stream and either executes it or compiles it
word 並執行它或編譯它
depending upon whether or not it is immediate. If the word is
取決於它是否是立即的。如果單字是
not in the dictionary, it converts it to a number, either
不在字典中，它也會將其轉換為數字
single or double precision depending on whether or not any
單精度或雙精度取決於是否有任何
punctuation was present. Continues until input stream is empty
有標點符號。持續到輸入資料流程為空為止
or state changes.
或狀態變化。


^CHAR FORTH
^查爾福斯


^NUM FORTH
^納姆·福斯


_BEHEAD HIDDEN
_BEHEAD 隱藏


_HEADERLESS HIDDEN
_HEADERLESS 隱藏


_HEADERS ( -- ) BEHEAD HIDDEN
_HEADERS （ -- ） 斬首隱藏
Internal beheader system word.
內部斬首系統詞。


` ( command --- ) EXEC
' （ 命令 --- ） 執行
A pseudonym for SYS. See also SYS.
SYS 的化名。另請參閱 SYS。

