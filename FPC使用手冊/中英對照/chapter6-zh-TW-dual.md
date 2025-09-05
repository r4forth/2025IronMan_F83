CHAPTER 6. SEQUENTIAL FILES
第 6 章。循序檔案



6.1. SEQUENTIAL FILES IN F-PC
6.1. F-PC 中的順序檔案


More than 90% of what is in F-PC kernel came from F83. Much of what you
F-PC 內核中超過 90% 的內容來自 F83。你大部分的
are seeing should be somewhat familiar. Things that are different are
看到應該有些熟悉。不同的東西是
normally different because they need to be. There are a significant
通常不同，因為它們需要。有一個重要的
number of things about F83 that should have been changed, but were not
關於 F83 應該改變但沒有改變的許多事情
for compatibility reasons. However since BLOCK is not present (it is
出於兼容性原因。然而，由於 BLOCK 不存在 （它是
available as a load-on utility in the file BLOCK.SEQ in the ZIMMER
可作為檔案 BLOCK 中的載入公用程式使用。ZIMMER 中的 SEQ
archive) and is replaced by sequential files, you will have to adjust to
存檔）並被順序文件替換，您必須調整為
them. Nevertheless, many of the familiar file manipulation words from
他們。儘管如此，許多熟悉的文件操作詞
F83 are still present, and those that are will work in a very similar if
F83 仍然存在，而那些存在的將以非常相似的方式工作，如果
not identical way. Some of these are:
方式不一樣。其中一些是：


OPEN, CLOSE, VIEW, OK, ED, EDIT, LOAD, LIST
開啟、關閉、檢視、確定、編輯、載入、清單


Some words, like BLOCK and BUFFER, simply did not fit into the new scheme
有些詞，如 BLOCK 和 BUFFER，根本不適合新方案
of things in a logical manner, and so were omitted. To load an entire
以合乎邏輯的方式處理事物，因此被省略了。載入整個
file, use the sequence
檔案，請使用


FLOAD <filename>
載入<filename>


Scanning through a file is best done with VIEW, although of course the
掃描檔案最好使用 VIEW 來完成，當然
file must have already been loaded. To scan through a file which has not
檔案必須已載入。掃描未
been loaded, you can use LIST, which lists from a line number, rather
已加載，您可以使用 LIST，它從行號列出，而不是
than from a block, but the following sequence is easier:
而不是從區塊，但以下順序更容易：


OPEN <filename> Open a file
開啟 <filename> 開啟檔案
n LIST List 23 lines from n'th line in the SED
n LIST 列出 SED 中第 n 行的 23 行
window
窗


These words are very fast, using indices into the file to maintain their
這些字非常快，使用索引進入檔案來維護其
line pointer information. The text of the entire file is stored in a
線條指標資訊。整個檔案的文字儲存在
text segment, and the line number indices are stored in a line segment.
文字區段，行號索引會儲存在線段中。
Similar to LIST, LOAD and EDIT also take a line number as input to start
與 LIST 類似，LOAD 和 EDIT 也採用行號作為輸入來啟動
the loading or editing function in the middle of the current file. The
目前檔案中間的載入或編輯功能。這
line number before LIST, LOAD, or EDIT is optional. If the line number
LIST、LOAD 或 EDIT 之前的行號是選用的。如果行號
is omitted, the listing or loading starts from line 1.
省略，則清單或載入會從第 1 行開始。


The compiler in F-PC has been tailored to be as fast as it could be made.
F-PC 中的編譯器經過定制，速度盡可能快。
Since much of the functionality of WORD has been reworked into assembly
由於 WORD 的大部分功能都已重新設計成組合
code for performance and all text data are in RAM memory, F-PC compiles
效能程式碼，所有文字資料都在 RAM 記憶體中，F-PC 編譯
sequential text files much faster than standard F83 compiles BLOCKs. The
順序文字檔案比標準 F83 編譯 BLOCK 快得多。這
compilation speed averages 20,000 lines per minute on a 10 MHz AT.
編譯速度在 20,000 MHz AT 上平均每分鐘 10 行。


Utilities are provided to convert large BLOCK files into sequential files
提供實用程序將大型 BLOCK 文件轉換為順序文件
and vice versa. Converting a block file to a sequential file typically
反之亦然。將區塊檔案轉換為順序檔案通常
saves more than 60% in mass storage.
節省 60% 以上的大容量儲存。


6.2. HANDLES
6.2. 句柄


According to DOS manual, a handle is a 16 bit number used by the
根據 DOS 手冊，句柄是 16 位元的數字，由
operating system to identify a file or a device when it is opened or
作業系統在開啟檔案或裝置時識別檔案或裝置
created. I F-PC, a handle is a data structure which contains several
創建。I F-PC，句柄是一個包含多個
fields,. Words have been defined to traverse to the various fields.
田野。單詞已被定義為跨越各個領域。
Here is a picture of the data structure of a handle as shown in Figure
下面是句柄的資料結構圖，如圖所示
6.1.


Figure 6.1. The file handle array
圖 6.1.檔案句柄陣列















Each of the words shown in Figure 6.1 after 'handle array', steps from
圖 6.1 中顯示的「handle 陣列」之後的每個單字，從
the address returned by the handle name, to the field indicated. The word
句柄名稱傳回的位址，以至指定的欄位。這個詞
HANDLE followed by <name> creates and initializes the above structure.
HANDLE 後面接著<name>建立並初始化上述結構。
When <name> is later used, it returns the address labeled +0 above.
<name> 稍後使用時，它會傳回上面標示為 +0 的位址。


A file handle stack is used in F-PC to allow a file to load other files.
F-PC 中使用檔案句柄堆疊來允許檔案載入其他檔案。
SEQHANDLE is a value which contains the pointer to the currently opened
SEQHANDLE 是一個值，其中包含指向目前開啟的
file in the handle stack. A sequential line read word LINEREAD is
檔案。循序行讀取字 LINEREAD 是
provided, which reads one line at a time from the file whose handle is in
提供，一次從句柄位於
SEQHANDLE, returning an address of a counted string which also includes
SEQHANDLE，傳回計數字串的位址，其中也包含
the CRLF characters at the end of the line. You will have to strip them
行尾的 CRLF 字元。你將不得不剝離它們
off if you don't want them. The LINEREAD word is used as follows:
如果你不想要它們，就關掉。LINEREAD 單字的用法如下：


: sample ( -- ) \ followed by <filename>
： 範例 （ -- ） \ 後面接著<filename>
open \ open a file
開啟 \ 開啟檔案
0.0 seek \ reset file pointer buffer
0.0 搜尋 \ 重設檔案指標緩衝區
begin
開始
lineread \ read a line, returns an address of counted $
lineread \ 讀取一行，傳回計數 $ 的位址
dup c@ \ check for length,
dup c@ \ 檢查長度，
0 <> while \ while buffer contains something
0 <> while \ while 緩衝區包含某些內容
cr count 2- type\ type line just read without the CRLF chars.
cr count 2- 類型\類型行僅讀取，沒有 CRLF 字元。
repeat drop \ repeat till file empty.
重複刪除 \ 重複直到文件清空。
close ; \ close the file.
近;\ 關閉檔案。


This simple example may seem complicated, but it really is easy to read
這個簡單的例子可能看起來很複雜，但它確實很容易閱讀
the lines of a sequential file, and writing is just as easy. The word
連續文件的行，書寫也同樣簡單。這個詞
LINEREAD automatically buffers the reads from disk in a 4K buffer to
LINEREAD 會自動將磁碟的讀取緩衝到 4K 緩衝區中
minimize the number of DOS calls performed. Lines up to 250 characters
將執行的 DOS 呼叫次數降到最低。行數最多 250 個字元
can be read with LINEREAD. Longer lines or lines not terminated by a
可以使用 LINEREAD 讀取。較長的行或未以
CRLF will be split at 250 characters.
CRLF 將以 250 個字元分割。


For more detailed and comprehensive examples, please consult the files
如需更詳細、更全面的範例，請查閱文件
SEQTOBLK.SEQ and BLKTOSEQ.SEQ. These two files contain code which
塞克托布爾克。SEQ 和 BLKTOSEQ.SEQ。這兩個檔案包含的程式碼
converts sequential files to block files and vice versa. You will find
將順序檔案轉換為區塊檔案，反之亦然。你會發現
useful word sequences which open and close files, read data from a file,
打開和關閉文件、從文件中讀取數據的有用詞序列，
write data to a file, move the file pointer around, pushing and pooping
將資料寫入檔案，移動檔案指標，推送和拉
the file stack, etc.
檔案堆疊等。


6.3. SEQUENTIAL FILE WORD SET
6.3. 順序檔案字集


The file system interface in F-PC uses handles to talk to DOS, and
F-PC 中的檔案系統介面使用句柄與 DOS 通訊，並且
only the number representing the File ID is passed to DOS from Forth. To
只有代表檔案 ID 的數字會從 Forth 傳遞至 DOS。到
make the interface as simple and clean as possible, you the Forth
讓界面盡可能簡單乾淨，你是第四
programmer need never deal with the details of how this works. You only
程序員永遠不需要處理其工作原理的細節。您僅
need to know that handles are created with the word HANDLE. Handles are
需要知道句柄是用單詞 HANDLE 創建的。句柄是
arrays within which special file information is stored, and when a
儲存特殊檔案資訊的陣列，以及當
handle's name is executed, it returns an address which is the address
handle's name 時，它會傳回一個位址，即位址
that is passed to the handle file control words. Word definitions and
傳遞至句柄檔案控制字組。單字定義和
usage in this set of file handling words are as follows:
這組檔案處理詞中的用法如下：


.FILES ( -- )
.檔案 （ -- ）


Print to the screen a list of the files currently open.
將目前開啟的檔案清單列印到螢幕上。


.LOADED ( -- )
.已加載 （ -- ）


Print a list of the files that have been loaded. This list is used to
列印已載入檔案的清單。此清單用於
locate the source file for a particular word that has been compiled.
找到已編譯的特定字的原始檔案。


">$ ( char-addr count -- counted-string )
“>$ （ char-addr count -- counted-string ）


Convert a string compiled as a 'quoted string' to a counted string, by
將編譯為「引號字串」的字串轉換為計數字串，方法是
dropping the count and decrementing the char-addr by one.
捨棄計數並將 char-addr 遞減 1。


$>HANDLE ( a1 handle-addr -- )
$>HANDLE （ a1 handle-addr -- ）


Move the counted string at a1 into the filename field in a handle.
將 a1 處的計數字串移至控點中的檔案名稱欄位。


$>EXT ( a1 handle-addr -- )
$>EXT （ a1 handle-addr -- ）


Move the counted string at a1 into the extension field of handle. The
將 a1 處的計數字串移至句柄的延伸欄位。這
extension string should not contain a decimal point, and should be
延伸字串不應包含小數點，而且應該是
exactly (3) three characters long.
正好 （3） 三個字元長。


$HOPEN ( a1 -- return-code )
$HOPEN （ a1 -- 回碼 ）


Close the current file if one is open. Move the counted string from
如果目前檔案已開啟，請關閉該檔案。將計數字串從
address a1 to the current handle on the handle stack. Return the result
位址 A1 至控制碼堆疊上的目前控制碼。傳回結果
code from DOS as return-code.
代碼作為 DOS 中的返回代碼。


!HCB <filename> ( handle-addr -- )
!HCB <filename> （ handle-addr -- ）


Pick up text from the input stream with WORD, and place the name into the
使用 WORD 從輸入資料流程中挑選文字，並將名稱放入
handle array.
handle 陣列。


?DEF.EXT ( -- )
?防禦。分機 （ -- ）


Conditionally apply the extension specified in the array DEFEXT to the
有條件地將陣列 DEFEXT 中指定的延伸模組套用至
filename in handle. DEFEXT is a counted string, three characters long
檔案名稱。DEFEXT 是計數字串，長度為三個字元
plus a count.
加上一個計數。


CHARREAD ( -- c1 )
查里德 （ -- c1 ）


Read a character from the currently open file specified by SEQHANDLE.
從 SEQHANDLE 指定的目前開啟檔案中讀取字元。
Before using this word, you will need to initialize the sequential input
在使用此單字之前，您需要初始化順序輸入
buffer to empty ( to force a refill from the currently selected file) by
buffer 變空 （ 強制從目前選取的檔案重新填入）
saying IBRESET. This will force a disk read on the next call to
說 IBRESET。這會強制在下次呼叫時讀取磁碟
CHARREAD, insuring that you get data from the file you selected.
CHARREAD，確保您從所選檔案取得資料。


CLOSE ( -- )
關閉 （ -- ）


Close the currently open file on SEQHANDLE. Move down one level on the
關閉 SEQHANDLE 上目前開啟的檔案。在
handle stack, so another file may be open after performing this
handle 堆疊，因此執行此操作後可能會開啟另一個檔案
operation. Normally you will be able to operate on the handle in SHNDL
手術。通常，您可以在 SHNDL 中對手柄進行操作
as an empty handle after performing CLOSE.
在執行 CLOSE 之後做為空句柄。


CLR-HCB ( handle-addr -- )
CLR-HCB （ handle-addr -- ）


Clear the handle to nulls, and reset the handle identifier field to -1 to
清除控制碼為 Null，並將控制碼識別碼欄位重設為 -1 以
indicate no file is open.
表示沒有開啟任何檔案。


CURPOINTER ( handle-addr -- double-current-ptr )
CURPOINTER （ handle-addr -- double-current-ptr ）


Return the current 32-bit double pointer into the file specified by
將目前的 32 位元雙指標傳回
handle.
柄。


DEFEXT ( -- a1 )
DEFEXT （ -- a1 ）


Return the address of the default file extension that will be applied to
傳回將套用至的預設副檔名位址
any file to be opened, if no extension is specified in the filename when
任何要開啟的檔案，如果檔案名稱中未指定副檔名，則
the HOPEN occurs. The address a1 is the address of a 4 byte array
HOPEN 發生。位址 a1 是 4 位元組陣列的位址
containing a count byte, and three extension bytes following. In no case
包含一個計數位元組，以及後面的三個擴充位元組。在任何情況下
should a string longer than 3 characters plus count be placed in DEFEXT.
是否應該將長度超過 3 個字元加上計數的字串放在 DEFEXT 中。


ENDFILE ( handle-addr -- double-end-ptr )
ENDFILE （ handle-addr -- double-end-ptr ）


Return the double-end number which represents the length of the file
傳回代表檔案長度的雙端編號
specified by handle. The file must already be open.
由句柄指定。檔案必須已開啟。


EXHREAD ( a1 n1 handle-addr segment -- n2 )
EXHREAD （ a1 n1 handle-addr segment -- n2 ）


Read from file handle into the buffer specified by segment and address a1
從檔案控點讀取至區段和位址 a1 所指定的緩衝區
for a length of bytes n1, and return n2 the length of bytes actually
對於位元組長度 n1，並傳回 n2 實際位元組長度
read. The file must already be open. Useful for reading from a file
讀。檔案必須已開啟。從檔案讀取很有用
into memory other than Forth's Code Segment. A read from a file is
進入 Forth 代碼段以外的內存中。從檔案讀取是
limited to 65535 bytes.
限制為 65535 位元組。


EXHWRITE ( a1 n1 handle-addr segment -- n2 )
EXHWRITE （ a1 n1 handle-addr 區段 -- n2 ）


Write from segment and address a1 for a length of n1 bytes to file
從區段和位址 a1 寫入檔案，長度為 n1 位元組
handle, and return n2, the length of bytes actually written. The file
handle，並傳回 n2，實際寫入的位元組長度。檔案
must already be open. Useful for writing from memory other than Forth
必須已經打開。對於從 Forth 以外的內存寫入很有用
code segment to a file. A write to a file is limited to 65535 bytes.
code 區段新增至檔案。寫入檔案限制為 65535 個位元組。


FILE>TIB ( a1 -- )
檔案>TIB （ a1 -- ）


Move the counted string filename from address a1 to the Terminal Input
將計數字串檔案名稱從位址 a1 移至終端機輸入
Buffer (TIB), available for use by !HCB.
緩衝區 （TIB），可供 ！HCB。


FLOAD <filename> ( -- )
載入 <filename> （ -- ）


Open and load the file specified by filename.
開啟並載入檔案名稱指定的檔案。


HANDLE <handlename> ( -- )
手柄 <handlename> （ -- ）


Create a handle with name <handlename>. When <handlename> is later
建立名稱 的控點 <handlename>。什麼時候<handlename>是晚
executed, it returns the address of the handle array created.
執行時，它會傳回所建立的句柄陣列的位址。


HANDLE>EXT ( handle-addr -- a1 )
HANDLE>EXT （ handle-addr -- a1 ）


Step from the handle address to the address of the file extension in the
從句柄位址到副檔名位址的步驟
handle, if an extension exists; else it steps to the null following the
handle，如果存在擴充功能;否則，它會逐步執行
filename. The address a1 will be the address of a decimal point
檔案名稱。位址 a1 將是小數點的位址
character if the file contains an extension, or the address of a null if
如果檔案包含副檔名，則為字元，如果檔案包含副檔名，則為空值位址
no extension was contained in the handle.
手柄中沒有包含擴展名。


HCLOSE ( handle-addr -- return-code )
HCLOSE （ handle-addr -- 傳回碼 ）


Close the file currently open on handle, and return the result code from
關閉目前在句柄上開啟的檔案，並從
DOS as return-code.
DOS 作為傳回碼。


HCREATE ( handle-addr -- return-code )
HCREATE （ handle-addr -- 傳回碼 ）


Create a file with the filename specified by the handle array, and return
使用句柄陣列指定的檔案名稱建立檔案，然後傳回
the DOS result code as return-code.
DOS 結果碼做為傳回碼。


HDELETE ( handle-addr -- return-code )
HDELETE （ handle-addr -- 傳回碼 ）


Delete the filename as specified by handle name, and return the result
刪除句柄名稱指定的檔案名稱，並傳回結果
code from DOS as return- code.
代碼作為 DOS 中的返回代碼。


HIDELINES ( -- )
隱藏線 （ -- ）


Specify that lines loaded with FLOAD NOT be displayed to the display
指定不將載入 FLOAD 的線顯示在顯示畫面上
screen.
幔。


HOPEN ( handle-addr -- return-code )
HOPEN （ handle-addr -- 傳回碼 ）


Given the handle address, open the filename in it, and return the result
給定句柄地址，打開其中的文件名，並返回結果
code from DOS as return- code.
代碼作為 DOS 中的返回代碼。


HREAD ( a1 n1 handle-addr -- n2 )
HREAD （ a1 n1 handle-addr -- n2 ）


Read from file handle into the buffer address a1 for length of bytes n1,
從檔案句柄讀取到緩衝區位址 a1 中，長度為位元組 n1，
and return n2 the length of bytes actually read. The file must already
並傳回 n2 實際讀取的位元組長度。檔案必須已經
be open. A read from a file is limited to 65535 bytes.
保持開放。從檔案讀取限制為 65535 個位元組。


HRENAME ( handle1 handle2 -- return-code )
HRENAME （ handle1 handle2 -- 回覆碼 ）


Rename the filename specified by handle1 to be the name specified in
將 handle1 指定的檔案名稱重新命名為
handle2, and return the DOS result code as return-code.
handle2，並將 DOS 結果代碼傳回為 return-code。


HWRITE ( a1 n1 handle-addr -- n2 )
HWRITE （ a1 n1 handle-addr -- n2 ）


Write from address a1 for length n1 bytes to file handle, and return n2
從位址 a1 寫入長度 n1 位元組到檔案句柄，並傳回 n2
the length of bytes actually written. The file must already be open. A
實際寫入的位元組長度。檔案必須已開啟。一個
write to a file is limited to 65535 bytes.
寫入檔案限制為 65535 個位元組。


IBRESET ( -- )
IBRESET （ -- ）


Clear the input read buffer in preparation for reading a new file. This
清除輸入讀取緩衝區，準備讀取新檔案。這
is done by OPEN.
由 OPEN 完成。


LINEREAD ( -- a1 )
線讀 （ -- a1 ）


Read one line from the current file, buffered by INBUF, which holds 4k
從目前檔案中讀取一行，由 INBUF 緩衝，該檔案可儲存 4k
bytes. Return a1 the address of OUTBUF, a 256 byte buffer used to hold
位元組。傳回 a1 OUTBUF 的位址，這是一個 256 位元組的緩衝區，用於保存
lines read. When switching to a new file, use MOVEPOINTER to reset the
行讀。切換至新檔案時，請使用 MOVEPOINTER 重設
file pointer to the beginning of the file, and execute IBRESET so the
檔案指標指向檔案開頭，並執行 IBRESET，以便
next LINEREAD will cause a read from the disk file. The read line length
next LINEREAD 將導致從磁碟檔案讀取。讀取行長度
is limited to 250 bytes. Lines read with LINEREAD are terminated with
限制為 250 個位元組。使用 LINEREAD 讀取的行會以
LF=$0A.
LF=$0A 的 LF。


LIST ( line-number -- )
LIST （ 行號 -- ）


List 18 lines starting at line-number from the currently open file.
列出從目前開啟的檔案的行號開始的 18 行。
Default to line 1 if line-number is omitted.
如果省略行號，則預設為第 1 行。


LOAD ( line-number -- )
LOAD （ 行號 -- ）


Start loading the currently open file, at line-number. Used alone
開始載入目前開啟的檔案，位於行號處。單獨使用
without a line number, it defaults to load from line 1. Load through the
如果沒有行號，則預設會從行 1 載入。載入
end of the file or until \S if no errors are encountered.
檔案結尾或直到 \S （如果未遇到錯誤）。


MOVEPOINTER ( double-offset handle-addr -- )
MOVEPOINTER （ 雙偏移 handle-addr -- ）


Move the filepointer into the file handle to the offset location
將檔案指標移至檔案控點至位移位置
specified by double-offset. The file must already be open.
由雙重偏移指定。檔案必須已開啟。


PATHSET ( handle -- f1 )
PATHSET （ 控點 -- f1 ）


Check the file contained in handle. If it does not contain a path, then
檢查句柄中包含的檔案。如果它不包含路徑，則
apply the current drive and path to the handle. Return f1 FALSE if it
將目前的磁碟機和路徑套用至控點。如果
succeeded; else TRUE if it failed to read the path from DOS.
成功了;否則，如果無法從 DOS 讀取路徑，則為 TRUE。


RWMODE ( -- a1 )
RWMODE （ -- a1 ）


A variable which holds the read/write attributes for any file to be
一個變數，它保存任何檔案的讀取/寫入屬性
opened by HOPEN, normally contains a two (2) for read/write. It may be
由 HOPEN 打開，通常包含兩 （2） 個用於讀取/寫入。可能是
set to one (1) for write only, or to zero (0) for read only.
設定為一 （1） 表示僅寫入，或設定為零 （0） 表示唯讀。


SEEK ( d1 -- )
搜尋 （ d1 -- ）


Position the file pointer for the file currently open on SEQHANDLE, to
將目前在 SEQHANDLE 上開啟之檔案的檔案指標定位為
d1, that is SEEK to position d1 relative to the beginning.
d1，即 SEEK 將 d1 相對於開頭定位。


SEQDOWN ( -- )
順序 （ -- ）


Close the current file on the current level of the handle stack, and step
關閉控點堆疊目前層級上的目前檔案，然後逐步執行
down one level to the previous handle. The handle stack is five levels
向下一級到上一個手柄。手柄堆疊為五級
deep allowing files to load files.
深度允許檔案載入檔案。


SEQHANDLE ( -- a1 )
序列控點 （ -- a1 ）


A VALUE that returns the address of the current file handle in the handle
傳回控制碼中目前檔案控制碼位址的 VALUE
stack.
堆。


SEQHANDLE+ ( -- a1 )
序列手柄+ （ -- a1 ）


A VALUE that returns the address of the next available handle in the
VALUE，傳回下一個可用句柄的位址
handle stack. This handle is used by the SED editor for temporary file
處理堆疊。此控點由 SED 編輯器用於暫存檔
operations like renaming, or deleting. You can use SEQHANDLE+ as well,
重新命名或刪除等作業。您也可以使用 SEQHANDLE+，
but its usage duration should be kept very short to avoid problems with
但其使用持續時間應保持非常短，以避免出現問題
other sections of the program using it.
使用它的程序的其他部分。


SEQUP ( -- )
序列 （ -- ）


Step up one Handle on the handle stack, if there is a file open on that
在句柄堆疊上向上移動一個句柄，如果該句柄上有一個檔案開啟
stack level, close it. The handle stack is five levels deep. FLOAD can
堆疊級別，關閉它。手柄堆疊有五層深。FLOAD 可以
thus be nested for four levels.
因此嵌套了四個級別。


SHOWLINES ( -- )
展線 （ -- ）


Specify that lines loaded with FLOAD will be displayed to the display
指定將以 FLOAD 載入的行顯示在顯示畫面中
screen.
幔。


6.4. CONVERSION BETWEEN SEQUENTIAL AND BLOCK FILES
6.4. 順序檔案和區塊檔案之間的轉換


To ease your transition from F83 to F-PC, utilities are provided to
為了簡化您從 F83 到 F-PC 的過渡，我們提供了實用程序
convert block files used by F83 to the sequential files required by F-PC.
將 F83 使用的區塊檔案轉換為 F-PC 所需的順序檔案。


The command sequence is :
命令順序為：


FLOAD BLKTOSEQ <enter> \ load converter
FLOAD BLKTOSEQ <enter> \ 負載轉換器


CONV <filespec> <enter>
轉換 <filespec> <enter>


The file specified after CONV will be converted to a sequential file of
CONV 之後指定的檔案將轉換為
the same name with .SEQ extension. If a file specification is not given
與 同名。SEQ 擴展名。如果未提供檔案規格
after CONV, CONV will request a valid file name to be converted. CONV
在 CONV 之後，CONV 將要求轉換有效的檔案名稱。轉換
also assumes that the block file has shadow blocks in its second half if
也假設區塊檔案的後半部分有影子區塊，如果
the source file has an extension of .BLK. It then brackets the text in
來源檔案的副檔名為 .BLK。然後，它會在
the shadow blocks between COMMENT: and COMMENT; , and inserts them after
COMMENT： 和 COMMENT 之間的影子區塊;，並在
the corresponding source block. However, if the source file has an
對應的來源區塊。不過，如果來源檔案具有
extension of .SCR, the entire file will be converted as source blocks and
的擴展。SCR，則整個檔案將轉換為來源區塊，並且
the second half of the file is not treated as shadow blocks.
檔案的後半部分不會被視為陰影區塊。


The utility package SEQTOBLK.SEQ will do the opposite: converting a
公用程式套件 SEQTOBLK.SEQ 將做相反的事情：將
sequential file back to a block file. The commands are:
循序檔案回區塊檔案。命令包括：


FLOAD SEQTOBLK <enter>


CONV <enter>
轉換<enter>


CONV will request the names of the sequential and block files. The
CONV 將要求順序和塊文件的名稱。這
extensions must not be given, as the sequential file defaults to .SEQ and
不得提供副檔名，因為循序檔案預設為 。SEQ 和
the block file to .SCR. CONV does a line to line conversions and does
塊文件轉換為 .SCR。CONV 會執行行對行轉換，並執行
not try to detect boundaries between definitions. It tends to break long
不要嘗試檢測定義之間的界限。它往往會長期突破
definitions and puts them in consecutive blocks. However, as all
定義並將它們放在連續的區塊中。然而，正如所有
experienced Forth programmers tend to write single line short
有經驗的 Forth 程式設計師傾向於寫單行短
definitions, the block file thus produced should be compilable under F83
定義，由此產生的區塊檔案應可在 F83 下編譯
without trouble, we hope.
我們希望沒有麻煩。


These two conversion utility files contain the best examples on how to
這兩個轉換公用程式檔案包含有關如何
open/create files and how to read/write them. If you have to use files
開啟/建立檔案以及如何讀取/寫入檔案。如果您必須使用文件
in your application, pay special attention to these two files for advice
在您的申請中，請特別注意這兩個文件以獲取建議
and guidance. The meanings of the words in the glossary become clear as
和指導。詞彙表中單詞的含義變得清晰，因為
you see them in action.
你看到他們的行動。


6.5. PROGRAMMING STYLE AND SEQUENTIAL FILES
6.5. 程式設計風格和順序檔案


The use of sequential files for source code instead of blocks has its
使用順序檔案作為原始程式碼而不是區塊具有其
most significant influence on the style of Forth programming. Using
對 Forth 編程風格影響最顯著。使用
blocks, the favored style of Forth code is the 'Horizontal code style' by
區塊中，Forth 程式碼最喜歡的樣式是
which code is arranged in horizontal lines with many Forth words spread
哪些代碼以水平線排列，並展開許多 Forth 單詞
in the same line. This style emphasizes the structure of words, whose
在同一行中。這種風格強調單詞的結構，其
definitions appear to be small, modular units. These units are then used
定義似乎是小型模組化單位。然後使用這些單位
to form other words which are again small units to build other words.
形成其他單詞，這些單詞又是構建其他單詞的小單元。
Word definitions expressed in the horizontal style are concise and
以水平樣式表達的單詞定義是簡潔的和
powerful. The problem is that it tends to leave little space for
強。問題是它往往給
comments and documentation. The lack of comments and in-line
評論和文檔。缺乏評論和內聯
documentation make Forth code difficult to understand and hard to
文檔使 Forth 代碼難以理解且難以理解
maintain.
維。


There are only 16 lines in a block, while each line has 64 characters.
一個區塊中只有 16 行，而每行有 64 個字元。
The aspect ratio of a block is 4:1, an much elongated rectangle. The
塊的縱橫比為 4：1，是一個細長得多的矩形。這
block seems to exert a great pressure on the source code in the vertical
區塊似乎對垂直的源代碼施加了很大的壓力
directions and presses the code into flat, horizontal lines. In a text
指示，並將代碼壓成平坦的水平線。在文字中
file, the vertical pressure is completely released because the file does
文件，垂直壓力完全釋放，因為文件確實
not have practical limitation on the number of lines it can contain. The
對它可以包含的行數沒有實際限制。這
residual pressure is from the limited number of characters that one can
殘餘壓力來自於一個人可以發揮的有限數量的字符
put in a line. This pressure in the horizontal direction tends to press
排成一排。水平方向的這種壓力往往會受到壓力
the code into the 'Vertical code style' favored by traditional
將程式碼轉換為傳統
programming languages. In the vertical code style, each line is limited
程式語言。在垂直程式碼樣式中，每一行都是有限的
to have one statement, leaving plenty of white space for comments and
有一個聲明，為評論留出足夠的空白，並且
documentation.
文檔。


It is thus natural that you will find most of the source files in F-PC
因此，您很自然會在 F-PC 中找到大部分源文件
follows the vertical code style. It is especially evident in the low
遵循垂直程式碼樣式。這在低處尤為明顯
level code definitions. Each line contains only a small number of Forth
等級代碼定義。每行僅包含少量的 Forth
words, allowing much space for documentation, which may or may not be
單詞，為文檔留出大量空間，這些空間可能是也可能不是
filled in by the author. Nevertheless, this mechanism is apparently
由作者填寫。然而，這種機制顯然是
favoring less code in a line. Indentation can also be used with much
偏愛一行中更少的代碼。縮排也可以與許多一起使用
more freedom than under the pressure between block boundaries.
比在街區邊界之間的壓力下更自由。


By removing blocks from the system, F-PC also eliminates the last excuse
通過從系統中刪除塊，F-PC 還消除了最後一個藉口
for Forth programmers not to write clear and well-documented code.
讓 Forth 程式設計師不要編寫清晰且有據可查的程式碼。
Henceforth, if we see bad, undocumented code in F- PC, we will shoot the
從今以後，如果我們在 F- PC 中看到不良的、未記錄的程式碼，我們將射擊
programmer and leave Forth in peace.
程序員並平靜地離開 Forth。

