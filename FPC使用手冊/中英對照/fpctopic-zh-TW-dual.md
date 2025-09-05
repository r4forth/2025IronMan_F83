F-PC Topics for discussion by: Tom Zimmer
F-PC 討論主題：湯姆·季默
Date: 03/29/93
日期：03/29/93


Possible F-PC discussion subject list
可能的 F-PC 討論主題列表


Subject Page
主題頁面


-------------------------------------------------------------


Dot (.) information display words 2
點 （.） 資訊顯示字 2


Color and blink control 4
顏色和閃爍控制 4


Boxes, windows and menus 6
盒子、窗口和菜單 6


Hypertext: how do I use it 7
超文本：如何使用它 7


Debugging: the watch command and others 11
偵錯：watch 指令等 11


Directives and aliases 13
指令和別名 13


Time measurment and control 15
時間測量與控制 15


Display and print redirection 16
顯示和列印重新導向 16


Pointers, what they are and how to use them 18
指針，它們是什麼以及如何使用它們 18


Memory usage and shelling to DOS 21
記憶體使用情況和 DOS 21 的 shelling


Number conversion and base specifying 23
數字轉換和基數指定 23


String processing words 24
字串處理字 24


Files: simple program file handling 26
檔案：簡單的程式檔案處理 26


LINEEDITOR: an example 28
LINEEDITOR：範例 28










Useful F-PC display words and what they display. Date: 03/29/93
有用的 F-PC 顯示單詞及其顯示的內容。日期：03/29/93


F-PC contains a number of words that display various kinds of
F-PC 包含許多顯示各種
information about things in F-PC.
有關 F-PC 中事物的信息。


.BASE Display the current base in decimal without
.BASE 以十進制顯示目前基數，不使用
changing the current base.
改變當前的基礎。


.COMPSTAT Display the compilers performance figure since
.COMPSTAT 顯示編譯器效能數據，因為
0COMPILER was executed.
0COMPILER 已執行。


.COMSPEC Display the DOS COMMAND.COM specification. The
.COMSPEC 顯示 DOS COMMAND.COM 規格。這
locaton where DOS will find COMMAND.COM.
DOS 將找到 COMMAND.COM 的位置。


.CURFILE Display the currently open file and its size.
.CURFILE 顯示目前開啟的檔案及其大小。
See also: .FILE
另請參閱： 。檔案


.DATE Display the date in the currenly selected display
.DATE 在目前選取的顯示畫面中顯示日期
format. See also: M/D/Y Y-M-D D.M.Y
格式。另請參閱：M/D/Y Y-M-D D.M.Y


.ELAPSED Display the elapsed time since TIME-RESET was
.ELAPSED 顯示自 TIME-RESET 以來經過的時間
last performed.
最後執行。


.ENV Display the contents of the DOS environment area.
.ENV 顯示 DOS 環境區域的內容。


.FILE Display the currently open file and its size.
.檔案 顯示目前開啟的檔案及其大小。
See also: .CURFILE
另請參閱： 。CURFILE


.FILES Displays a list of the contents of the file
.檔案 顯示檔案內容的清單
handle stack, showing any files that are open.
handle 堆疊，顯示任何開啟的檔案。


.FPATH Display F-PC's file search path. The directories
.FPATH 顯示 F-PC 的檔案搜尋路徑。目錄
where F-PC looks for a file when the user tries
其中 F-PC 在使用者嘗試時尋找檔案
to open a file without specifying its path.
以開啟檔案而不指定其路徑。


.FPCVER# Displays a limited F-PC version number. 3 digits.
.FPCVER# 顯示有限的 F-PC 版本號。3 位數。
See also .VERSION
另請參閱 。版本


.FREE Display the mount of available memory to F-PC.
.免費 顯示 F-PC 的可用記憶體安裝。


.LOADED Display a list of all file that have been loaded
.已載入 顯示已載入之所有檔案的清單
on this version of F-PC.
在這個版本的 F-PC 上。


.ME Display the name of the copy of F-PC currently
.ME 顯示目前 F-PC 副本的名稱
running. Can be used with ME@ and ME$ to find out
流動的。可搭配 ME@和 ME$一探究竟
which directory F-PC or an F-PC application is
F-PC 或 F-PC 應用程式是哪個目錄
running from.
逃離。


.MEM Display F-PC's current memory usage, including
.MEM 顯示 F-PC 目前的記憶體使用情況，包括
all defined pointers and their usage.
所有已定義的指標及其用法。


.PATH Display the DOS PATH as extracted from the DOS
.PATH 顯示從 DOS 擷取的 DOS PATH
environment.
環境。


.S Display the stack contents. Also try holding
.S 顯示堆疊內容。也嘗試按住
down both left and right shift keys, to see the
按下左右 Shift 鍵，即可查看
stack contents while in any program while waiting
在等待時在任何程序中堆疊內容
for a key to be pressed.
按下按鍵。


.SEQHANDLE Display the contents of the current SEQHANDLE in
.SEQHANDLE 顯示目前 SEQHANDLE 的內容
the file stack.
檔案堆疊。


.TIME Display the current time, in hours, minutes,
.TIME 顯示當前時間，以小時、分鐘、
seconds and hundreds.
幾秒鐘和幾百秒鐘。


.USED Display the amount of memory in the CODE, LIST
.USED 顯示 CODE、LIST 中的記憶體量
and HEAD segments used in F-PC since !USED was
和 HEAD 段用於 F-PC 自 ！USED 是
executed.
已執行。


.VALIDATE Display a validation message to inform the user
.VALIDATE 顯示驗證訊息以通知使用者
whether this copy of F-PC is as released from Tom
F-PC 的這個副本是否與湯姆發布的那樣
Zimmer, or one which another user has
Zimmer，或其他用戶擁有的
re-compiled since this version of F-PC was
重新編譯，因為這個版本的 F-PC 是
released.
發布。


.VERSION Display the full five digit compile version of
.VERSION 顯示完整的五位數編譯版本
F-PC. See also: .FPCVER#
F-PC。另請參閱： 。FPCVER#

















Color and Blink Control in F-PC Date: 03/29/93
F-PC 中的顏色和閃爍控制日期：03/29/93


Color Control
色彩控制


As you have no doubt seen, F-PC uses text of various colors to
毫無疑問，F-PC 使用各種顏色的文字來
highlight information in its various windows and menus. You applications
突出顯示其各種窗口和菜單中的信息。您的應用
programs can also use these or other color combinations to make your
程式也可以使用這些或其他顏色組合來製作
programs more attractive to the user.
對用戶更具吸引力的程序。


The most primitive color control words in F-PC are >FG and >BG. These
F-PC 中最原始的調色詞是>FG 和>BG。這些
words take a color number from the stack, and set the forground or
words 從堆疊中取得顏色編號，並將 forground 或
background color for any further TYPE operations.
任何進一步 TYPE 作業的背景顏色。


A set of words in F-PC named >ATTRIB1 through >ATTRIB8 are used to
F-PC 中的一組名為 >ATTRIB1 到 >ATTRIB8 的單詞用於
select one of eight predefined color combinations, making it easier
從八種預先定義的顏色組合中選擇一種，使其更輕鬆
to control the colors used in F-PC or an application. F-PC itself uses
控制 F-PC 或應用程式中使用的顏色。F-PC 本身使用
only the first four color sets, so word >ATTRIB5 through >ATTRIB8
只有前四種顏色集，所以單詞>ATTRIB5 到>ATTRIB8
duplicate color sets one through four.
重複顏色集 1 到 4。


The colors sets are define in the file COLOR.SEQ. An array called
顏色集在檔案 COLOR.SEQ 中定義。一個名為
COLORS holds eight pairs of forground and background color bytes. Other
COLORS 會保留八對前地和背景顏色位元組。他
primitives in F-PC extract the byte values from the COLORS array and set
F-PC 中的原語從 COLORS 陣列中提取位元組值並設定
the forground and background colors to the colors in the array.
forground 和 background 顏色轉換為陣列中的顏色。


To change the colors that >ATTRIB1 through >ATTRIB8 select, simply
若要變更>ATTRIB1>ATTRIB8 選取的顏色，只需
requires changing the values in the COLORS array. The words FG! and BG!
需要變更 COLORS 陣列中的值。The words FG!和 BG！
perform this function as follow:
執行此功能如下：


BLUE 5 BG! ORANGE 5 FG!
藍色 5 BG！橙色 5 FG！


Here color set five (5) is being set to display as orange on blue.
這裡顏色集五 （5） 被設置為顯示為藍色底上的橙色。
Subsequent use of >ATTRIB5 will select this color combination for any
後續使用>ATTRIB5 將為任何顏色選擇此顏色組合
following TYPE operations.
下列 TYPE 作業。


Blink Control
眨眼控制


When colors above seven are selected as the background color for any
當選取七以上的顏色作為任何
color set, the PC will normally subtract eight from the background color,
color set，電腦通常會從背景顏色中減去 8，
and cause text displayed in that color set to blink. F-PC includes two
並導致以該顏色集顯示的文字閃爍。F-PC 包括兩個
words to control whether the PC causes a color set containing a color
words 來控制電腦是否會導致包含色彩的色彩集
above seven in the background to blink, they are BLINKON and BLINKOFF.
後台七個以上要眨眼，分別是 BLINKON 和 BLINKOFF。
These are global blink control words, and F-PC normally defaults to
這些是全域閃爍控制字，F-PC 通常預設為
BLINKON. If you write an application that needs to use one of the bright
布林肯。如果您編寫的應用程式需要使用其中一個明亮的
color above seven in the background, then you will need to include the
顏色高於 7 的背景，那麼您需要包含
word BLINKOFF in your program initialization section.
word BLINKOFF 在您的程式初始化區段中。






Embeded COLOR Commands in Dot Quote Strings
在點引號字串中內嵌 COLOR 命令


F-PC also uses an interpreted dot quote (."), that allows embeded
F-PC 也使用解釋的點引號 （.“），允許嵌入
commands to be placed in dot quote statments. Colors can be selected
命令要放置在點引號語句中。可以選擇顏色
using "\x", where 'x' is '0' for >NORM, and '1' through '8' for color
使用 “\x”，其中 'x' 代表 >NORM，代表 '1' 到 '8' 代表顏色
sets >ATTRIB1 through >ATTRIB8.
>ATTRIB1 到 >ATTRIB8。


The file PERTYPE.SEQ contains the code to perform these functions, and
檔案 PERTYPE.SEQ 包含執行這些功能的程式碼，並且
details the embeded commands supported.
詳細說明支援的內嵌命令。
























Boxes, windows and menus Date: 03/30/93
盒子、窗口和菜單日期：03/30/93


Simple Windows in F-PC
F-PC 中的簡單視窗


With all the talk about Windows these days, you might wonder what kind
隨著這些天關於 Windows 的所有討論，您可能想知道什麼樣的
of window support is built into F-PC and whether you will be able to
F-PC 內建的視窗支援，以及您是否能夠
figure out how to use it. Let me assure you that window (NOT Windows)
弄清楚如何使用它。讓我向你保證那個窗口（不是 Windows）
support is built into F-PC, and it is easy to use though limited in
支援內建於 F-PC 中，儘管有限，但易於使用
scope.
範圍。


F-PC views a window as an area of the screen, usually surrounded by a
F-PC 將視窗視為螢幕的一個區域，通常被
border of one type or another. To put a window on the screen, you can
一種或另一種類型的邊框。若要在螢幕上顯示視窗，您可以
use the words: BOX and BOX&FILL. These words work in TEXT mode and take
使用以下詞語：BOX 和 BOX&FILL。這些單詞在文本模式下工作，並採取
a top left row/column position along with a bottom/right row/column
左上角的列/欄位置以及下角/右欄/欄
position. The box is then drawn and the text cursor is positioned at
位。然後繪製方塊，並將文字游標定位在
the top left inside the box, ready for you to use TYPE or ." (dot quote)
盒子內部的左上方，準備使用 TYPE 或 ”（點引號）
to put some text in the box. BOX&FILL simply prefills the box with
在方塊中放入一些文字。BOX&FILL 只是在盒子中預先填充
spaces, so the background information is covered up.
空格，因此背景信息被掩蓋了。


Example source:
範例來源：
ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ
³ : tst ³
³ ： TST ³
³ 20 10 60 15 BOX&FILL ³
³ 20 10 60 15 箱式及填料 ³
³ ." This is a test" ³
³ ."這是一個測試」³
³ BCR ." This is on the next line" ³
³ BCR “。這是在下一行」³
³ BCR ." This line is too long for the box I have drawn!" ³
³ BCR “。這條線對於我畫的盒子來說太長了！
³ BCR ." Press a key to continue" key drop cr cr ; ³
³ BCR “。按一個鍵繼續“key drop cr cr ;³
ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ


Example output:
輸出範例：
ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÜ
ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ
³ This is a test Û
³ 這是一個測試 Û
³ This is on the next line Û
³ 這是在下一行 Û
³ This line is too long for the box I have drawn!
³ 這條線對於我畫的盒子來說太長了！
³ Press a key to continue Û
³ 按鍵繼續 Û
ÀÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÛ
ÀÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜÜ


So, to put text in the box, you use TYPE or ." (dot quote). You DO
因此，要將文字放入方塊中，請使用 TYPE 或 。」（點引用）。你願意
have to be carful not to exceed the width of the box, or your text will
必須小心不要超過框的寬度，否則您的文字將
extend over the right border beyond the box. To move down and to the
延伸至方塊之外的右邊框。若要向下移動並移至
start of the next line in the box, use the word "BCR" (box CR), and your
在方框中下一行的開頭，使用單詞“BCR”（方框 CR），並且您的
cursor will be positioned down one line and at the left edge of the box.
游標將向下一行放置在框的左邊緣。


Thats just about all there is to it, though you may want to use SAVESCR
這就是它的全部內容，儘管您可能想使用 SAVESCR
and RESTSCR to save ane restore the screen when unnesting a window. Also
和 RESTSCR 在取消嵌套視窗時儲存並恢復螢幕。亦
to avoid completely redrawing a BOX, you way want to save BLINE (the BCR
為了避免完全重新繪製 BOX，您需要保存 BLINE （BCR
line counter), and redraw using BOX instead of BOX&FILL, to redraw the
線計數器），並使用 BOX 而不是 BOX&FILL 重新繪製，以重新繪製
border of the box.
框框。


As I say window support is limited. There is no automatic resizing, or
正如我所說，窗口支持是有限的。沒有自動調整大小，或
scroll bars or any of the other bells and whistles in Windows, but what
滾動條或 Windows 中的任何其他花里胡哨的功能，但什麼
is provided has worked well for me. I hope it will work for you also.
提供的對我來說效果很好。我希望它也對你有用。


Hypertext, how do I use it Date: 03/29/93
超文本，如何使用它日期：03/29/93


Hypertext and F-PC and NEWZ
超文本、F-PC 和 NEWZ


The tools for creating hypertext index files are built into NEWZ, so
用於建立超文本索引檔案的工具內建於 NEWZ 中，因此
NEWZ must be used to create the index files that can be accessed by
NEWZ 必須用來建立可由
either F-PC or NEWZ. For discussion purposes, the NEWZ editor will be
F-PC 或 NEWZ。出於討論目的，NEWZ 編輯器將是
used to illustrate how hypertext works in this illustration.
用於說明超文本在此圖中的工作原理。


If you have used the browse capability of F-PC, that is the ability to
如果您使用過 F-PC 的瀏覽功能，那就是能夠
place the cursor on a Forth word and press F9 to see the source for that
將光標放在 Forth 單詞上，然後按 F9 查看該單詞的來源
word, then you have used hypertext as F-PC and NEWZ view it.
word，那麼你已經使用了超文本作為 F-PC 和 NEWZ 查看它。


There are many different kinds of hypertext, and equally many different
超文本有許多不同種類，也同樣有很多不同的
ways of implementing it and of interconnecting the text that is being
實現它和相互連接正在發生的文本的方法
hypertext-ified. NEWZ uses one very simple technique to make
超文本化。NEWZ 使用一種非常簡單的技術來製作
interconnections between diverse locations within the same file or
同一檔案內不同位置之間的互連或
between different files. When a request is made by the user, to "hyper"
在不同檔案之間。當使用者提出請求時，「hyper」
to a new location as specified by the word under the cursor, NEWZ
至游標下單字指定的新位置 NEWZ
searches a file called HYPER.NDX attempting to locate the specified word.
搜尋名為 HYPER 的檔案。NDX 嘗試尋找指定的字詞。
If the word is located, then the location in the HYPER.NDX file tells
如果該單詞被定位，則在 HYPER.NDX 檔案告訴
NEWZ what file and to which line the hyper word is connected. NEWZ then
NEWZ 超字連接到什麼文件和哪行。紐茲那麼
save the current file, line and column, opens the destination file, and
儲存目前檔案、行和欄，開啟目標檔案，以及
positions the cursor on the destination line, displaying the new location
將游標定位在目標行上，顯示新位置
to the user. Having "hypered" to a new location, the user can "unhyper"
給用戶。「超」到新位置後，使用者可以「取消超」
or "unlink" to the previous location by pressing the F10 key.
或按 F10 鍵「取消連結」到先前的位置。


Thus NEWZ relies on a VERY FAST text search mechanism to locate the
因此，NEWZ 依靠非常快速的文本搜索機制來定位
desired target quickly. Now this technique is fast enough for hypertext
快速實現所需的目標。現在這種技術對於超文本來說已經足夠快了
databases upto a few thousand connections on a reasonably fast machine,
在相當快的機器上最多有幾千個連接的數據庫，
but will bog down quickly on very large databases of tens or hundreds of
但在數十或數百個非常大的資料庫上會很快陷入困境
thousands of link databases.
數以千計的鏈接數據庫。


The text search mechanism is built into both NEWZ and F-PC, so an F-PC
文本搜索機制內置於 NEWZ 和 F-PC 中，因此 F-PC
application can include a hypertext browser or online help function. In
應用程序可以包括超文本瀏覽器或在線幫助功能。在
F-PC, a dictinary search is performed before attemptint to perform a
F-PC，則在嘗試執行
hypertext search, so some caution must be used in naming hypertext links
超文本搜索，因此在命名超文本鏈接時必須謹慎
to avoid collisions with normal Forth words. Alternatively you can make
以避免與正常的 Forth 單詞發生衝突。或者，您可以製作
a headerless F-PC application, which obviously couldn't find any Forth
一個無標頭的 F-PC 應用程序，顯然找不到任何 Forth
words since no heads are present to interfere with the hypertext search.
單詞，因為沒有標題存在來干擾超文本搜索。


Creating a Hypertext Index File
建立超文本索引檔案


Hypertext as viewed by NEWZ consists of two parts, a source word (or
NEWZ 查看的超文本由兩部分組成，一個源詞（或
link) and a destination word (or link).
link） 和目標單字 （或連結）。


Source Words
源詞


The source words appear on the screen in the document being viewed,
來源單字會出現在正在檢視的文件的螢幕上，
intermixed with other document words. As such it is useful to have a way
與其他文件詞混合。因此，有一個方法很有用
of highlighting source words so they are obviously different from other
突出顯示源詞，使其與其他詞明顯不同
words the user is reading. To provide this functionality, NEWZ
使用者正在閱讀的字詞。為了提供此功能，NEWZ
recognizes a special IBM graphics character "ù" (decimal value 249) that
辨識特殊的 IBM 圖形字元 “ù” （十進位值 249）
can preceed a word that you want highlighted in the text when NEWZ is in
可以在 NEWZ 位於
browse mode. This character can be inserted by pressing Alt-F3 while on
瀏覽模式。此字元可以透過在開啟時按 Alt-F3 來插入
a word you want to highlight. The cursor will automatically move to the
一個你想強調的詞。游標會自動移至
left end of the word and insert the source word marker character.
單詞的左端，然後插入源單詞標記字符。


Other than providing a way for the editor to recognize which words to
除了為編輯提供一種識別哪些單詞的方法
highlight, the source marker character serves no other purpose. That is
醒目提示，來源標記字元沒有其他用途。那就是
NEWZ will actually perform a hypertext search for any word where the
NEWZ 實際上會對任何單字執行超文本搜尋，其中
cursor is located, whether it is preceeded by a source marker character
游標所在的位置，無論其前面是否有來源標記字元
or not. Most words of course won't appear in HYPER.NDX, and as such will
或不是。當然，大多數單詞不會出現在 HYPER 中。NDX，因此會
fail to be found.
找不到。


Here are some examples of hypertext-ified source words:
以下是超文本化源詞的一些示例：


ùThis ùis ùa ùtest
ù這個 ùis ùa ùtest


If you are viewing this in edit mode, then the above list of words
如果您在編輯模式下查看此內容，則上面的單詞列表
appears with a dot preceeding each word, and if you are viewing this in
每個單字前面都會顯示一個點，如果您在
browse mode, then the above list of words will be shown in reverse video.
瀏覽模式，則上面的單詞列表將以反向視頻形式顯示。


Destination Words
目的地詞


To allow the hypertext search capability to work, we need to create a
為了允許超文本搜尋功能發揮作用，我們需要建立一個
file called HYPER.NDX. HYPER.NDX contains references to hypertext
名為 HYPER 的檔案。NDX。超級。NDX 包含超文字的參考
destination words (or links). The hypertext compiler build into NEWZ is
目標詞（或鏈接）。NEWZ 中構建的超文本編譯器是
configured to search for words starting with the IBM graphics character
配置為搜尋以 IBM 圖形字元開頭的單字
"ø" (decimal value 248). When the hypertext compiler encounters this
“ø” （十進位值 248）。當超文本編譯器遇到這個
character, if extracts the word immediately following the character upto
字元，如果提取緊接字元後面的單字，直到
a space and insertes it into HYPER.NDX along with the line number where
一個空格並將其插入 HYPER.NDX 以及行號，其中
it was found. This allows the hypertext search to find a destination and
它被發現了。這可讓超文本搜尋找到目的地，並
link to it. Hypertext destination words should appear at the left edge
鏈接到它。超文本目標字詞應顯示在左邊緣
of the document, followed by at least one space.
文件，後面接著至少一個空格。


When NEWZ displays a file while in BROWSE mode, it recognizes words
當 NEWZ 在瀏覽模式下顯示文件時，它會識別單詞
starting in column one beginning with the destination character, and
從第一欄開始，以目的地字元開頭，以及
blanks them off of the screen as spaces. This makes hyper destination
將它們作為空格從屏幕上空白。這使得超級目的地
words invisible when reading the document.
閱讀文件時不可見的文字。


Here are some examples of hypertext destination words:
以下是超文本目標詞的一些範例：


øthis <- this
Ø這個<-這個
øis <- is
øis <- 是
øa <- a
øtest <- test
ø測試<-測試


Compiling HYPER.NDX
編譯 HYPER.NDX 的


Having created at one or more source words and one or more destination
在一或多個來源單字和一或多個目的地建立
words, you will need to run the hypertext compiler to build HYPER.NDX.
words，您將需要運行超文本編譯器來構建 HYPER。NDX。
BUT, before we do that, we need to do one more thing. We need to add a
但是，在我們這樣做之前，我們還需要做一件事。我們需要新增一個
file specification to the file NEWZ.CFG to let NEWZ know that we want it
檔案規格新增至檔案 NEWZ。CFG 讓 NEWZ 知道我們想要它
to include our file in HYPER.NDX. If we don't do this, then HYPER.NDX
將我們的檔案包含在 HYPER 中。NDX。如果我們不這樣做，那麼 HYPER。NDX 的
will not contain any of our hypertext destination words.
不會包含我們的任何超文本目標詞。


In the partial extract from NEWZ.CFG, notice particularly the line
在 NEWZ 的部分摘錄中。CFG，特別注意這行
starting with "SPECS". Here *.SEQ has been added to the normal SPECS
以“SPECS”開頭。這裏*。SEQ 已添加到正常 SPECS 中
pathlist, to make the hypertext compiler index all .SEQ files in the
pathlist，使超文本編譯器索引全部。SEQ 檔案中的
current directory. So if we are building a hypertext database that
目前目錄。因此，如果我們正在建立一個超文本資料庫，那麼
contains .SEQ files from the current directory, then they will get
包含 。SEQ 檔案，則它們將取得
included in HYPER.NDX. It is also important to note that the path to
包含在 HYPER 中。NDX。同樣重要的是要注意，通往
each file indexed is NOT saved in HYPER.NDX, so you must either be in the
每個索引的檔案都不會儲存在 HYPER 中。NDX，因此您必須位於
same directory when using the database as when it was compiled, or you
使用資料庫時與編譯資料庫時相同的目錄，或您
must include "\YOURDIR" in the PATH statment on the first line below.
必須在下面第一行的 PATH 語句中包含“\YOURDIR”。


ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ
³ PATH \YOURDIR;\;FPC\NEWZ ; file search path ³
³ 路徑 \YOURDIR;\;FPC\NEWZ ;檔案搜尋路徑 ³
³ DEFEXT SRC ; default file extension if none specified ³
³ DEFEXT SRC ;預設副檔名 （如果未指定） ³
³ DELIMS " " ; browse word delimiter max 32chars. ³
³ 德利姆斯“ ” ;瀏覽單詞分隔符最多 32 個字符。
³ SPECS *.SEQ;*.TXT;\FPC\NEWZ\ZHELP.TXT ; index compiler specs. ³
³ 規格 *。序列;*.TXT;\FPC\NEWZ\ZHELP.TXT ;索引編譯器規格。³
³ *GLOBAL . ; (disabled) do global index, starting with .(cur) dir ³
³ *全球。;（已停用） do global index，以 開頭。（cur） 方向 ³
³ .... ³
³ ....³
³ .... ³
³ ....³
³ TYPE 0 "ø" ; index compiler command ³
³ 0 型 “ø” ;索引編譯器指令 ³
³ .... ³
³ ....³
ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ


In the line "*GLOBAL . " following SPECS, you can remove the "*" from
在 SPECS 之後的 “*GLOBAL . ” 行中，您可以從
the line and cause the hypertext compile to perform a hypertext compile
該行，並導致超文本編譯執行超文本編譯
of the current directory (as specified by .), and any directories lower.
目前目錄的 （如 .） 所指定，以及任何較低的目錄。
You can slow put an explicit directory name after GLOBAL to cause a
您可以在 GLOBAL 之後緩慢放置明確的目錄名稱，以導致
hypertext compile of all directories from the specified directory and
超文本編譯指定目錄中所有目錄，以及
lower.
低。


The next section describes the TYPE command at the bottom of the
下一節說明
configuration file above, and shows how you can index various types of
設定檔，並顯示如何索引各種類型的
source files.
來源檔案。


ZHELP Index Compiler Extract
ZHELP 索引編譯器擷取


Three index compiler directives are currently supported, they each
目前支援三個索引編譯器指引，每個指令
start with the word "TYPE" followed by a type number and a "string"
以單字「TYPE」開頭，後面接著類型編號和「字串」
parameter:
參數：


0 "string" Pick up and index the word IMMEDIATELY following
0 “string” 立即選擇並索引緊接在後面的單詞
string. No space delimiter is required. If you
繩子。不需要空格定界字元。如果你
want to space delimit the string, include a space
要空格分隔字串，包含空格
within the quotes. Examples: ": " "CONSTANT "
在引號內。範例： “： ” “CONSTANT ”
"CODE " etc.
“代碼”等。


This type can pick up words following, as will be
這種類型可以拾取後面的單詞，就像
the case with the above examples, or you can pick
以上例子的情況，或者你可以挑
up words starting with a character by not
以字元開頭的單字
including a space at the end of the string. An
包括字串末尾的空格。一
example of this is the graphic symbol above "ø",
例如，“ø”上方的圖形符號，
which compiles any word starting with this
編譯以此開頭的任何單詞
symbol. That is any hypertext destination link.
標。這是任何超文本目標鏈接。


1 ":" Pick up and index the word preceeding this
1 “：” 拿起並索引前面的單詞
symbol. That is index all words that end in a ":"
標。也就是說，索引所有以“：”結尾的單詞
character. Normally used for assembler labels.
字。通常用於彙編器標籤。


2 "string " Pick up and index the word at the start of this
2 “string ” 拿起並索引開頭的單詞
line preceeding this string. Again this is
此字串之前的行。同樣，這是
typically used to include references to the
通常用來包含對
assembler word LABEL as it is used in some
彙編器單字 LABEL，因為它用於某些
assemblers. here is an example:
彙編商。這是一個例子：


symbol_name LABEL
symbol_name 標籤


Symbol_name will be included in the index file.
Symbol_name 將包含在索引檔案中。


Several of the above index commands can be included one per line
上述數個索引命令可以包含，每行一個
before the line starting with a ";" character. The index compiler
在以 “;” 字元開頭的行之前。索引編譯器
currently supports up to sixteen (16) index compiler commands in the
目前最多支援十六 （16） 個索引編譯器命令，以
above format.
以上格式。


What is INDEX.COM
什麼是 INDEX.COM


INDEX.COM is a standalone index compiler compiled with TCOM. It uses a
INDEX.COM 是使用 TCOM 編譯的獨立索引編譯器。它使用
similar configuration file called INDEX.CFG to specify parameters to the
類似的設定檔稱為 INDEX。CFG 來指定參數
compiler. It may be useful to look at INDEX.CFG to see an example of how
編譯器。查看 INDEX 可能會很有用。CFG 查看如何
to make the index compiler extract Forth words from source files.
使索引編譯器從源文件中提取 Forth 單詞。


Parting Notes on Hypertext
關於超文本的離別筆記


While the details of hypertext creation may at first seem overwhelming,
雖然超文本創建的細節乍一看似乎勢不可擋，
you may find it valuble to spend some time experimenting with the
您可能會發現花一些時間嘗試
possibilities presented here. I know of people using NEWZ to hyper index
這裡介紹的可能性。我知道有人使用 NEWZ 來超索引
client description files, and program source files, there are no doubt
客戶端描述文件，以及程序源文件，這是毫無疑問的
many other possible uses.
許多其他可能的用途。











Debugging: the watch command and others Date: 03/30/93
偵錯：watch 命令等日期：03/30/93


Debugging an Overview
偵錯概觀


In an ideal world, programs written in Forth will be so modular that
在理想的世界中，用 Forth 編寫的程式將是模組化的，以至於
each small piece of code can be debugged fully and interactively without
每個小段程式碼都可以完全互動地調試，無需
any need to resort to a debugger for assistance.
任何需要求助於調試器尋求幫助的。


In the real world however, I have found that as a program evolves and
然而，在現實世界中，我發現隨著一個程序的發展和
grows, it develops data and environmental dependancies that make it
它發展數據和環境依賴性，使其
increasingly difficult to setup all of the proper conditions needed to
設置所需的所有適當條件變得越來越困難
fully test each of the smaller pieces of the application.
全面測試應用程式的每個較小部分。


Debuggers therefore seem to be a neccesary part of a programmers tool
因此，偵錯器似乎是程式設計師工具的必要部分
kit, for use in dealing with those difficult problems that envariably
套件，用於處理那些總是遇到的難題
occur at the worst possible time (after release).
發生在最壞的時間（發布後）。


DEBUG: a watch function
DEBUG：一個監視功能


F-PC of course includes a debugger, which has evolved as a
F-PC 當然包括一個調試器，它已經發展成為
Super-Superset of the original Laxen & Perry F83 debugger. Recently
原始 Laxen & Perry F83 偵錯器的超級超集。最近
significant modifications have been to the debugger to provide simple
對偵錯工具進行了重大修改，以提供簡單的
watch capability. If you have worked with Non-Forth development systems,
手錶功能。如果您使用過非 Forth 開發系統，
you may be familiar with the "WATCH VARIABLE" concept. In other
您可能熟悉「WATCH VARIABLE」概念。在其他方面
languages it is often possible to open a window and tell the debuffer
語言通常可以打開一個窗口並告訴 debuffer
that you want ot watch a particular variable, to see when and how it
你想觀察一個特定的變量，看看它何時以及如何
changes. F-PC's watch function provides similar capability, but instead
變化。F-PC 的手錶功能提供了類似的功能，但相反
of watching only a single variable, it allows you to watch an area of
只觀看單一變數，它允許您觀看
memory. The 'W' command in the debugger accepts a word or address, and
記性。偵錯工具中的 'W' 命令會接受單字或位址，而
opens a three line window which is a dump of the address specified.
開啟三行視窗，這是指定位址的傾出。


Debugger Example Screen with Watch turned on:
開啟監看式的偵錯工具範例畫面：
ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ
³ : WORDS ³
³ ： 字數 ³
³ TOTALWORDS OFF SAVESTATE COLS 2- RMARGIN ! 15 TABSIZE ! ³
³ SAVESTATE COLS 2 的總字數 - RMARGIN ！15 標籤大小 ！³
³ LMARGIN OFF CR ³
³ ." ** Press SPACE to pause, or ESC to exit ** " PREWORDS ³
³ .“ ** 按 SPACE 暫停，或按 ESC 退出 ** ” 前言 ³
³ >IN @ #TIB @ <> ³
³ IF ['] ?INNAME IS ?W.NAME BL WORD W$ OVER C@ 1+ 32 MIN ³
³ 如果 ['] ？名義是？BL W.NAME 字 W$ 超過 C@ 1+ 32 分鐘 ³
³ CMOVE BL WORD W$ 32 + OVER C@ 1+ 32 MIN CMOVE ?*.* ³
³ CMOVE BL WORD W$ 32 + 超過 C@ 1+ 32 分鐘 CMOVE ？*.* ³
³ ?CODE.* ?:.* ?VARIABLE.* ?CONSTANT.* ?DEFERED.* ³
³ ?法典。*？：。*？不定的。*？恆。*？延期。
³ ?VALUE.* ?USER-VARIABLE.* ?USER-DEFERED.* ?TOTAL.* ³
³ ?價。*？USER-VARIABLE.* ？用戶延遲。總計。
³ CONTEXTONLY FALSE %!> CONTEXTONLY ³
³ CONTEXTONLY FALSE %！> CONTEXTONLY ³
³ Cont, Done, Nest, Quit, Rstk, Unnest, Watch, X-srctgl, Z-slow ³
³ 續、完成、巢狀、退出、rstk、取消巢狀、監看、X-srctgl、Z-慢速 ³
³ 0D1C:8294³05 57 4F 44 53 20 4E 2E 53 45 51 20 53³.WORDS ING.SEQ S ³
³ 0D1C：8294³05 57 4F 44 53 20 4E 2E 53 45 51 20 53³.字 ING.序列 S ³
³ 0D1C:82A4³52 43 3B 3A 5C 46 43 48 4C 50 3B 43 3A³RC;C:\FPC\HLP;C: ³
³ 0D1C：82A4³52 43 3B 3A 5C 46 43 48 4C 50 3B 43 3A³RC;C：\FPC\HLP;C：³
³ 0D1C:82B4³5C 46 50 5C 54 4F 4C 20 2D 4F 4E 4C D9³\FPC\TOOLS -ONLY ³
³ 0D1C：82B4³5C 46 50 5C 54 4F 4C 20 2D 4F 4E 4C D9³\FPC\TOOLS -ONLY ³
³ 45B5 WORDS nesting Debugger ready. Stack Empty. ³
³ 45B5 字嵌套偵錯器就緒。堆疊空。³
³ 2543 0 TOTALWORDS ?> ³
³ 2543 0 總字數 ？> ³
ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ


In this example screen, Watch has been opened at HERE. Since the word
在此範例畫面中，已在此處開啟觀看。自從這個詞
HERE returns an address, watch watches the address returned by HERE.
HERE 傳回一個地址，watch 會監視 HERE 傳回的地址。


You can also watch other things, for instance you can enter a word to
您還可以觀看其他內容，例如您可以輸入一個單詞
watch preceeded by a ' (tick) mark, and watch will display its dump
watch 前面有一個 ' （刻度） 標記，watch 將顯示其傾印
starting at the CFA of the word. This is useful for words that don't
從這個詞的 CFA 開始。這對於不這樣做的單字很有用
normally return an address when executed. You can also tell watch to
執行時通常會傳回一個位址。您也可以告訴手錶
watch an area of memory outside F-PC's CODE space by entering the address
通過輸入地址來觀看 F-PC 的 CODE 空間之外的內存區域
as "SEGMENT OFFSET", where segment and offset are separated by a space.
作為“SEGMENT OFFSET”，其中線段和偏移以空格分隔。
If you want to turn off the watch window, simply tell it to watch the
如果您想關閉手錶窗口，只需告訴它觀看
literal value -1 (minus one).
文字值 -1 （減一）。


The + (plus) and - (minus) keys can be used to expand or contract the
+ （加號） 和 - （減號） 鍵可用來展開或收縮
watch window lines, to allow monitoring a larger area of memory. The up
監視視窗線，以允許監控更大的記憶體區域。向上
and down arrows, and page up and page down can be used to scroll through
和向下箭頭，以及 Page Up 和 Page Down 可用於捲動瀏覽
memory, above or below the original area of memory being watched.
記憶體，高於或低於正在觀看的原始記憶體區域。


DEBUG: the display base and return stack
DEBUG：顯示基礎和傳回堆疊


Robert Smith recently added a toggle to the debugger, to switch the
Robert Smith 最近在偵錯工具中新增了切換，以切換
base for numbers displayed in the debugger from the default base to HEX,
base 用於偵錯工具中顯示的數字，從預設基數到 HEX，
with the 'H' key. The 'H' key toggles back and forth between the current
使用“H”鍵。“H”鍵在電流之間來回切換
base and HEX. Robert also added the ability to display the contents of
底座和十六進制。羅伯特還添加了顯示內容的功能
the return stack, using the 'R' command.
返回堆棧，使用“R”命令。


















Directives and aliases in F-PC Date: 03/29/93
F-PC 中的指令和別名日期：03/29/93


Directives and Compilation Control
指令和編譯控制


Within F-PC and in the applications you write, it is useful to control
在 F-PC 和您編寫的應用程式中，控制很有用
which portions of a program are loaded. When supporting multiple
載入程式的哪些部分。支援多個
versions, or when simply trying to increase the flexibility of the load
版本，或者當只是試圖增加負載的靈活性時
order of an application, you might want to have the compiler decide
應用程式的順序，您可能想要讓編譯器決定
whether to load a line or file that might either already be loaded, or
是否要載入可能已載入的行或檔案，或
might need to be loaded for this particular program configuration.
可能需要針對此特定程式配置載入。


F-PC provides several words to support this process as follows:
F-PC 提供了幾個詞來支持這個過程，如下所示：


NEEDS DIRECTIVE \- \+ #IF #ELSE #THEN
需要指令 \- \+ #IF #ELSE #THEN


The word NEEDS followed by a filename, checks to see if the file has
NEEDS 一詞後面跟著文件名，檢查文件是否有
already been loade, and if it has not, then it loads filename. This
已經加載，如果沒有，則加載文件名。這
prevents needlessly loading multiple copies of a file, but assures that
防止不必要地載入檔案的多個副本，但確保
needed functions within the file are available.
檔案中所需的函數可用。


The word DIRECTIVE allows the definition of compiler directives that
DIRECTIVE 一詞容許定義編譯器指引，以符合以下條件：
control whether the line following is compiled or not. Here is an
控制後面的行是否編譯。這是一個
example:
例：


TRUE DIRECTIVE \GRAPHICS
TRUE 指令 \圖形
FALSE DIRECTIVE \TEXT
錯誤指令 \TEXT


Directives can be treated like values, that is they can be stored into
指令可以像值一樣處理，也就是說，它們可以儲存在
with !>. Here \GRAPHICS is defined as TRUE, so when \GRAPHICS is used in
與 ！>。這裡 \GRAPHICS 定義為 TRUE，因此當 \GRAPHICS 在
a program, any words on the same line are compiled or interpreted. The
一個程序，同行上的任何單詞都會被編譯或解釋。這
directive \TEXT is defined as FALSE, so any words on the same line in the
指令 \TEXT 定義為 FALSE，因此
application source as \TEXT will be treated as comments and ignored.
應用程式來源為 \TEXT 會被視為註解並忽略。


A directive can be subsequently modified as follows:
後續可以修改指令，如下所示：


FALSE !> \GRAPHICS
錯誤 ！> \圖形
TRUE !> \TEXT
真 ！> \TEXT


The above lines invert the function of the \GRAPHICS and \TEXT
上面的行反轉了 \GRAPHICS 和 \TEXT 的功能
directives, so that words following \TEXT will be interpreted, and words
指令，以便 \TEXT 後面的單字將被解釋，而單字
following \GRAPHICS will be treated as comments.
後面的 \GRAPHICS 將被視為註解。


Sometimes is is useful to determine whether a line is to be interpreted
有時 is 有助於判斷是否要解譯一行
based simply on whether a word is already defined or not. When this need
僅僅基於一個詞是否已經定義。當需要
occurs you can use \+ and \- directives as follows:
發生時，您可以使用 \+ 和 \- 指令，如下所示：


\+ bill fload billstuf
\- george fload bobstuf
\- 喬治·弗洛德·鮑勃斯圖夫


Here is the word BILL is defined, then the sequence "FLOAD BILLSTUF" is
這裡定義了 BILL 一詞，那麼序列“FLOAD BILLSTUF”是
perform, and if GEORGE is NOT defined the "FLOAD BOBSTUF" is performed.
執行，如果未定義 GEORGE，則執行 “FLOAD BOBSTUF”。


The traditional #IF #ELSE and #THEN interpreted conditional are
傳統的 #IF #ELSE 和 #THEN 解釋條件是
also supported, allowing even more ways of controlling how your
也支援，允許更多方式來控制您的
application loads.
應用程式載入。


Aliases and Their Use
別名及其用途


An alias in F-PC is an additional header, created to point to an
F-PC 中的別名是一個額外的標頭，創建是為了指向
existing definition. Either name for the definition can then be used to
現有定義。然後，定義的任一名稱可用於
compile or execute the definition. Aliases are used in F-PC in two ways.
編譯或執行定義。別名在 F-PC 中以兩種方式使用。
First aliases are used as a way of allowing the user to spell a word more
首先，別名被用作允許用戶拼寫更多單詞的一種方式
than one way, as in VIEW, BROWSE, LL, V, B and L. Here VIEW is the
而不是單向，如 VIEW、BROWSE、LL、V、B 和 L。這裡的 VIEW 是
actual name of the word used to view the source for a dictionary word,
用於查看字典單詞源的單詞的實際名稱，
but the user can also type BROWSE, LL (Locate&List), V, B or L to get the
但使用者也可以鍵入 BROWSE、LL （Locate&List）、V、B 或 L 來取得
same effect. Each of the succeeding words is defined as an alias of
同樣的效果。後續的每個單字都定義為
VIEW. Aliases are also used as a way of controlling dictionary searches.
觀。別名也用作控制字典搜尋的一種方式。
Specifically in TCOM, many FORTH vocabulary words are aliased to the HOST
具體來說，在 TCOM 中，許多 FORTH 詞彙都別名為 HOST
directory, to make them available without requiring that all of the words
目錄，以使其可用，而不需要所有單字
in the FORTH vocabulary be available.
在 FORTH 詞彙表中可用。


ALIAS is used as follows:
ALIAS 的使用方式如下：


' NOOP ALIAS DO-NOTHING
' NOOP 別名 DO-NOTHING（無所事事）


Here DO-NOTHING is defined as an alias for NOOP. Only a header is
這裡 DO-NOTHING 被定義為 NOOP 的別名。只有標頭是
created for an alias, the headers code pointer field is filled with the
為別名建立，標頭程式碼指標欄位會填入
address of the CFA of the word it is being aliased to.
該詞的 CFA 地址。

















Time measurment and control Date: 03/29/93
時間測量和控制日期：03/29/93


Delaying tactics
拖延戰術


F-PC contains words that can provide several ways of pausing for a
F-PC 包含的單字可以提供多種暫停方式
period of time, words delaying include:
一段時間內，詞延遲包括：


MS TENTHS SECONDS MINUTES HOURS
MS 十分之一秒 分鐘 小時


MS is calibrated at F-PC startup time, to perform a proper delay on the
MS 在 F-PC 啟動時進行校準，以對
current machine. It is not extreamly acurate, but should be sufficient
當前機器。它不是非常準確，但應該足夠了
for most fine timing purposes. MS does call PAUSE, so if multi-tasking
用於大多數精細的計時目的。MS 確實會呼叫 PAUSE，因此如果多工處理
is running, it may slow the MS timing down somewhat when other tasks are
正在運行時，當其他任務
busy running.
忙著跑步。


The words TENTHS, SECONDS, MINUTES and HOURS all loop and perform a
TENTHS、SECONDS、MINUTES 和 HOURS 字樣都會循環並執行
delay based on the PC system clock GETTIME function. They will be fairly
延遲基於 PC 系統時鐘 GETTIME 函數。他們會公平的
precise regardless of the speed of the computer they are running on.
無論它們運行的計算機速度如何，都精確。
They each execute PAUSE, and a defered function PAUSE-FUNC, which can be
它們各自執行 PAUSE，以及一個延遲函數 PAUSE-FUNC，可以是
used to perform minor background operations while delays are being
用於在延遲時執行次要後台操作
performed.
執行。


Time Measurment
時間測量


F-PC also contains words that allow easy measurment of operations that
F-PC 還包含可以輕鬆測量操作的單詞
are performed in F-PC, or occur via DOS SHELL operations. These words
在 F-PC 中執行，或透過 DOS SHELL 操作發生。這些話
are as follows:
如下：


TIME-RESET TIME-ELAPSED .ELAPSED TIMER
時間重置時間經過。已耗盡計時器


TIME-RESET is used to mark the start of one or more operations that
TIME-RESET 用於標記一或多個操作的開始，這些操作
needs to be timed. TIME-ELAPSED returns a double number that is the
需要計時。TIME-ELAPSED 會傳回雙倍數，即
elapsed time since TIME-RESET in 100ths of a second resolution. .ELAPSED
自 TIME-RESET 以來經過的時間，分辨率為 100 分之一秒。.已淘汰
performs a TIME-ELAPSED and displays the result in Hours, minutes,
執行 TIME-ELAPSED 並以小時、分鐘、
seconds and hundreths. TIMER performs a TIME-RESET, then interprets the
秒和百倍。TIMER 執行 TIME-RESET，然後解譯
following commandline and displays the elapsed time for the commandline.
遵循命令列，並顯示命令列經過的時間。


It is useful to note that the precision of the timing function is
值得注意的是，計時函數的精度為
limited to units of 18th of a second by the PC system clock interrupt
受 PC 系統時鐘中斷限制為 18 秒的單位
rate, even though the resolution is returned and displayed in 100ths of a
rate，即使解析度會傳回並以 100 分之一顯示
second.
秒。


Performance Measurment
性能測量


Early in the development of F-PC, I added words to make it easy to
在 F-PC 開發的早期，我添加了文字以方便
measure the performance of the compiler. When I made changes to the
測量編譯器的效能。當我對
internal architexture of F-PC, I wanted to know how my changes effected
F-PC 的內部檔案紋理，我想知道我的更改如何影響
the compilers performance. The words 0COMPILER and .COMPSTAT make it
編譯器性能。0COMPILER 和 .COMPSTAT 讓它
easy to test the compiler, and evaluate it against other compiler venders
易於測試編譯器，並與其他編譯器供應商進行評估
claims. F-PC has always done well in these test, and has been hand tuned
聲稱。F-PC 在這些測試中一直表現出色，並且經過手工調整
to minimize disk transfers, linereads and word searches.
最大限度地減少磁盤傳輸、行讀和單詞搜索。


Display and print redirection Date: 04/14/93
顯示和列印重新導向日期：04/14/93


Display Redirection
顯示重新導向


F-PC includes words that can redirect all screen output to the printer,
F-PC 包含可以將所有螢幕輸出重新導向到印表機的字，
or any printed output directly into a file. To redirect the output of a
或直接將任何列印輸出直接放入檔案中。若要重新導向
commandline to the printer, use the word:
命令行到打印機，使用單詞：


PRINT <commandline> <enter>
印 <commandline> <enter>


Any display output from <commandline> above will be directed to the
任何來自上方的顯示輸出<commandline>都會導向至
printer instead of to the display.
印表機而不是顯示器。


Display to Browser Redirection
顯示至瀏覽器重新導向


If no printer is available, or if you just want to redirect the output
如果沒有可用的印表機，或您只想重新導向輸出
of a commandline to a file for detailed browsing, you can use:
的命令列到檔案進行詳細瀏覽，您可以使用：


>BROWSE <commandline> <enter>
>瀏覽 <commandline> <enter>


or the alias
或別名


>B <commandline> <enter>
>乙 <commandline> <enter>


Any display output from <commandline> will be directed into the file
任何顯示輸出<commandline>都將被導向到文件中
BROWSE.PRN instead of to the display or printer. When the command line
瀏覽。PRN 而不是顯示器或印表機。當命令列
finishes executing, the F-PC editor will automatically be invoked in
執行完畢時，會自動呼叫 F-PC 編輯器
"browse" mode, on BROWSE.PRN. The same filename BROWSE.PRN is always
“瀏覽”模式，在瀏覽上。PRN。相同的檔案名稱 BROWSE。PRN 始終是
used, so each successive use of >BROWSE, or >B will cause the previous
使用，因此每次連續使用 >BROWSE 或 >B 都會導致先前的
copy of BROWSE.PRN to be overwritten.
BROWSE 的副本。PRN 要被覆蓋。


Printer Redirection
印表機重新導向


It is sometimes useful to redirect printer output into a specific file
有時將印表機輸出重新導向到特定檔案會很有用
while in an application. Three words are provide to allow control of
在應用程式中。提供三個字來允許控制
printer redirection, as follows:
印表機重新導向，如下所示：


From the Forth commandline:
從 Forth 命令行：


PFILE MYFILE.PRN <enter>
PFILE 我的檔案。PRN <enter>


The above will redirect all printer output into MYFILE.PRN. Any use of
上述內容會將所有印表機輸出重新導向到 MYFILE。PRN。任何使用
the word PRINT will be directed to MYFILE.PRN. To finish printing to
PRINT 一詞將導向到 MYFILE。PRN。若要完成列印至
MYFILE.PRN, and return printing redirectin to the printer, use:
MYFILE 的檔案。PRN 並返回打印重定向到打印機，請使用：


PCLOSE or its alias TOPRINTER
PCLOSE 或其別名 TOPRINTER


Any printer output will be directed back to the real printer.
任何印表機輸出都將定向回真實印表機。


It is also useful to select the name of the printer file from within a
從
program, this is done in F-PC by using:
程序，這是在 F-PC 中使用以下方式完成的：


From within a Forth program:
在 Forth 程式中：


: MYPRINTFILE ( -- )
： 我的列印檔案 （ -- ）
" APRTFILE.PRN" ">$ $PFILE
“ APRT 檔案。PRN“ ”>$ $PFILE
ABORT" Failed to create print file" ;
ABORT“ 無法建立列印檔案” ;


Any printer output following the execution of the above definition will
執行上述定義後的任何印表機輸出都會
be directed into APRTFILE.PRN. Again PCLOSE is sued to restore printing
被導向到 APRTFILE 中。PRN。PCLOSE 再次被起訴以恢復打印
to the physical printer.
至實體印表機。


Printer Variable
印表機變數


The vaiable PRINTING when non-zero, causes typed output to go to the
非零時可用的 PRINTING 會導致鍵入的輸出轉到
printer instead of to the display. The variable PRINTING is turned OFF
印表機而不是顯示器。變數 PRINTING 已關閉
when an error occurs, so error messages will be displayed on the screen
發生錯誤時，螢幕上會顯示錯誤訊息
instead of onto the printer or into the print file.
而不是打印機或打印文件。




















Pointers, what they are and how to use them Date: 03/29/93
指針，它們是什麼以及如何使用它們日期：03/29/93


Pointers in F-PC a History
F-PC A 歷史中的指針


In early version of F-PC, memoru management was done using the standard
在 F-PC 的早期版本中，備忘錄管理是使用標準
DOS functions ALLOC and DEALLOC. These functions in F-PC allow an amount
DOS 函數 ALLOC 和 DEALLOC。F-PC 中的這些函數允許一定數量
of memory in paragraph outside of F-PC to be allocated for use as a
F-PC 之外段落中的記憶體分配用作
buffer for various kinds of things that the user might want to save for
緩衝區，用於使用者可能想要儲存的各種專案
later use within an applications program. Management worked kind of like
稍後在應用程式內使用。管理層的工作有點像
a stack, each successive use of ALLOC assigned a higher area of memory
堆疊，每次連續使用 ALLOC 都會指派較高的記憶體區域
outside of F-PC to the request. A call to DEALLOC would release the
在 F-PC 之外。呼叫 DEALLOC 會釋放
allocated space back to DOS, but unless DEALLOCs were performed in the
將空間配置回 DOS，但除非在
reverse order of the ALLOCs, then the DOS memory would become fragmented.
ALLOC 的倒序，則 DOS 記憶體將變得碎片化。
If fragmentation became excessive, then an ALLOC might fail even though
如果碎片變得過度，則 ALLOC 可能會失敗，即使
there was enough memory available, it was not contiguous, and as such
有足夠的可用內存，它不是連續的，因此
couldn't be passed back as a single block to the caller.
無法作為單一區塊傳回給呼叫端。


This fragmentation caused problems for F-PC, and applications programs
這種碎片化導致 F-PC 和應用程序出現問題
and could lead to premature program failure.
並可能導致程序過早失敗。


F-PC starting with Version 3.5500 on Feb 06th, 1991, switched to a new
F-PC 從 1991 年 2 月 6 日的 3.5500 版開始，切換到新的
memory management scheme, based on what I call the POINTER. A pointer is
記憶體管理方案，基於我所說的 POINTER。指標是
a word that automatically allocates a predefined area of memory above
自動分配上方預定義內存區域的單詞
F-PC's HEAD segment, but within F-PC when the word is first used by an
F-PC 的 HEAD 段，但在 F-PC 內，當該詞首次被
application. Since the allocation occurs automatically, the user doesn't
應用。由於配置會自動發生，因此使用者不會
need to include special initialization code in their application to
需要在其應用程式中包含特殊的初始化程式碼，以
allocate needed space, and space for unused pointers doesn't get
分配所需的空間，未使用的指標的空間不會
allocated at all even if defined in an application.
即使在應用程式中定義也一樣。


One of the new attributes of pointers in F-PC is that they are movable,
F-PC 中指標的新屬性之一是它們是可移動的，
that is the paragraph address returned by a pointer may change after the
也就是說，指標傳回的段落位址可能會在
space for a pointer is already allocated. The impact of this on your
已配置指標的空間。這對您的影響
program is that you MUST use the pointer name each time you need to
程式是每次需要時都必須使用指標名稱
paragraph address of the buffer, or you may stomp on the wrong memory
緩衝區的段落位址，否則可能會踩錯記憶體
area if the pointers buffer area got moved.
區域，如果指標緩衝區已移動。


You might ask why would a pointers buffer need to move, and the answer
您可能會問為什麼指標緩衝區需要移動，答案
goes back to the problem with ALLOC and fragmentation. To prevent memory
回到 ALLOC 和碎片的問題。為了防止記憶
from getting fragmented, any pointer buffer that is released with
從碎片化中釋放的任何指標緩衝區
UNPOINTER> causes any pointer buffer above it to be moved down to consume
UNPOINTER>會導致其上方的任何指標緩衝區向下移動以取用
the released space, and maintain a contiguous free memory above F-PC.
釋放的空間，並在 F-PC 之上保持連續的可用記憶體。


This did cause some problems early in the adaptation of F-PC to
這確實在 F-PC 適應的早期造成了一些問題
pointers. The editor had to be modified so it wouldn't care if the text
指標。編輯器必須修改，這樣它就不在乎文本
edit buffer moved during an edit session, which was a challenge to
編輯緩衝區在編輯會話期間移動，這對
accomplish, and other parts of F-PC had to be made pointer friendly, to
accomplish，並且 F-PC 的其他部分必須對指標友好，以
always use the pointer word when obtaining the paragraph address of the
在取得
pointers buffer.
指標緩衝區。


Programs you have written may need to be converted to use pointers,
你編寫的程式可能需要轉換成使用指標，
which will centainly cause you some headaches, but will be time well
這肯定會讓你有些頭痛，但時間很好
spent in reduced memory management problems later on.
後來花在減少的內存管理問題上。



Pointer Usage
指標用法


Here is an example of a pointer definition in F-PC:
以下是 F-PC 中指標定義的範例：


12345. POINTER MYSEG
12345. 指針邁塞格


Note that the number placed on the stack before POINTER is a DOUBLE
請注意，放置在 POINTER 之前的堆疊上的數字是 DOUBLE
number as indicated by the decimal pointe at the end of the number.
數字，如數字末尾的小數點所示。
POINTER aligns the double number to the next higher paragraph boundry
POINTER 會將雙倍數字對齊下一個較高的段落界限
before saving the amount of memory needed in the structure created for
在儲存為
MYSEG. It is useful to note that while a literal number is required at
邁塞格。值得注意的是，雖然
the time a pointer is defined, the actual size of the pointer can be
定義指標的時間，指標的實際大小可以是
changed prior to actually using the pointer an allocating the space.
在實際使用指標分配空間之前發生了變化。
Words to accomplish this will be discussed shortly.
實現這一目標的詞語將很快討論。


Using MYSEG in a definitions mioght occur as follows:
在定義中使用 MYSEG 的情況如下：


: ERASE-MYSEG ( -- )
： 擦除-MYSEG （ -- ）
MYSEG 0 \ segment and offset
MYSEG 0 \ 段和偏移量
SIZEOF@> MYSEG DROP \ size in bytes < 64k
SIZEOF@> MYSEG DROP \ 大小（以位元組為單位）< 64k
0 LFILL ; \ fill with nulls
0 LFILL ;\ 填入空值


Notice that SIZEOF@> was used to obtain the size of the pointer so it
請注意，SIZEOF@> 是用來取得指標的大小，因此
could be filled with nulls. SIZEOF@> returns the size of the pointer in
可以填入空值。SIZEOF@>傳回指標的大小
bytes with a double number, so in this case the high byte is assumed to
位元組，因此在此情況下，假設高位元組為
be zero, and only the lower word is used for the subsequent LFILL (long
為零，且只有較低的字用於後續 LFILL （長
fill).
填充）。


You might also want to define words to fetch from and store into the
您可能也想要定義要從中擷取並儲存到
the pointer, which could be accomplished as follows:
指標，可以按如下方式完成：


: MYSEG-C@ ( a1 -- c1 ) MYSEG SWAP C@L ;
： MYSEG-C@ （ a1 -- c1 ） MYSEG 交換 C@L ;
: MYSEG-C! ( c1 a1 -- ) MYSEG SWAP C!L ;
：米塞格-C！（ c1 a1 -- ）MYSEG 交換 C！L ;


Bytes are shown here, but operations for words, or strings could also
此處顯示位元組，但單字或字串的運算也可以
be easily defined using @L, !L, CMOVEL, or CMOVEL>.
使用 @L 輕鬆定義，！L、CMOVEL 或 CMOVEL>。


When the size of a pointer buffer needs to change at runtime before the
當指標緩衝區的大小需要在執行階段變更時，再
pointer is allocated, you can use the following technique to set the
指標，您可以使用以下技術將
pointer size:
指標大小：


: SIZE!-MYSEG ( -- )
： 尺寸！-MYSEG （ -- ）
UNPOINTER> MYSEG
RECORDS BYTE/RECORD UM* SIZEOF!> MYSEG ;
記錄位元組/記錄 UM* SIZEOF！> MYSEG ;


Notice that UNPOINTER is used to release any memory already in use by
請注意，UNPOINTER 是用來釋放任何已在使用的記憶體
MYSEG prior to adjusting its size. This is a prudent action that will
MYSEG 在調整其大小之前。這是一個謹慎的行動，將
assure MYSEG really gets adjusted. Note however that you CANNOT adjust
確保 MYSEG 確實得到調整。但請注意，您無法調整
the size of a pointer that has already been allocated. It MUST be
已配置指標的大小。它必須是
released and reallocated. Consequently any data in the pointer will be
釋放並重新分配。因此，指標中的任何資料都會
lost if it is resized.
如果調整大小，則遺失。



When a pointers buffer is not needed any longer it is prudent to
當不再需要指標緩衝區時，謹慎的做法是
release the unneeded memory as follows:
釋放不需要的記憶體，如下所示：


: NOMORE-MYSEG ( -- )
：不再-邁塞格 （ -- ）
UNPOINTER> MYSEG ;


This causes the memory allocated to MYSEG to be released back to the
這會導致配置給 MYSEG 的記憶體釋放回
available memory pool for use by other pointers.
可供其他指標使用的可用記憶體集區。

























F-PC Memory usage and shelling to DOS Date: 03/29/93
F-PC 記憶體使用情況和 DOS 的外殼日期：03/29/93


Memory an Overview
記憶體和概述


Of all the resources available in a personal computer, Random Access
在個人電腦中可用的所有資源中，隨機存取
Memory (RAM) is perhaps the most valuble. F-PC recognizes the value of
內存 （RAM） 可能是最有價值的。F-PC 認識到
RAM and uses it in many diverse ways. Please spend a few moments
RAM 並以多種不同的方式使用它。請花點時間
examining the following table, as it will be the basis for further
檢查下表，因為它將成為進一步的基礎
discussion.
討論。


Typical .MEM display for F-PC
典型的。適用於 F-PC 的 MEM 顯示器


line
線
ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ
1 ³ -------- DOS memory usage ³
1 ³ -------- DOS 記憶體使用量 ³
2 ³ 1024 bytes at seg 5D6F MACSEG 1744 bytes at seg 5D02 XBSEG ³
2 ³ 1024 位元組 （seg 5D6F） MACSEG 1744 位元組 （seg 5D02 XBSEG ³）
3 ³ 239616 bytes at seg 5DAF BASESEG 4272 bytes Unallocated DIRSEG ³
3 ³ 239616 位元組，在 seg 5DAF BASESEG 4272 位元組未配置 DIRSEG ³
4 ³ 20000 bytes at seg 5820 SVSEG 23008 bytes Unallocated LABSEG ³
4 ³ 20000 位元組，在 seg 5820 SVSEG 23008 位元組未配置 LABSEG ³
5 ³ 32000 bytes at seg 5050 INBSEG 275264 bytes at seg D1C F-PC ³
5 ³ 32000 位元組 （seg 5050） INBSEG 275264 位元組 （seg D1C F-PC ³）
6 ³ -------- ³
7 ³ 569648 bytes TOTAL used by F-PC, excluding Unallocated ³
7 ³ 569648 位元組 F-PC 使用的總計，不包括未分配的 ³
8 ³ -------- ³
8 立方米-------- ³
9 ³ 32000 bytes DOS memory Available ³
9 ³ 32000 位元組 DOS 記憶體 可用 ³
10 ³ 601648 bytes DOS memory Total ³
10 ³ 601648 位元組 DOS 記憶體總計 ³
11 ³ -------- Expanded Memory Version 4.0 at Paragraph E000 ³
11 ³ -------- 擴展記憶體 4.0 版，第 E000 ³ 段
12 ³ 2818048 bytes expanded memory Available ³
12 ³ 2818048 位元組擴充記憶體 可用 ³
13 ³ 7667712 bytes expanded memory Total ³
13 ³ 7667712 位元組擴充記憶體 總計 ³
ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ


F-PC is a very memory hungry development system. Line 7 shows F-PC
F-PC 是一個非常耗費記憶體的開發系統。第 7 行顯示 F-PC
using more than 569,000 bytes of DOS memory. How that 569k is used is
使用超過 569,000 位元組的 DOS 記憶體。569k 的使用方式是
detailed between lines 1 and 6, eight pointer names MACSEG through F-PC
詳細說明在第 1 行和第 6 行之間，八個指針名稱 MACSEG 到 F-PC
identify each of the areas of memory used by F-PC. You can use VIEW to
識別 F-PC 使用的每個記憶體區域。您可以使用 VIEW 來
examine each of these pointer, to see what they are used for. Notice the
檢查每個指標，看看它們的用途。請注意
the pointer "F-PC" shows that 275,264 bytes of memory is being used.
指標「F-PC」顯示正在使用 275,264 位元組的記憶體。
This memory is used for CODE, LIST and HEAD areas, and can be adjusted to
此記憶體用於 CODE、LIST 和 HEAD 區域，可調整為
some extend with the word LISTSET, or TURNKEY. It reflects the sum of
有些以 LISTSET 或 TURNKEY 一詞擴展。它反映了
the paragraph values as extracted from KERNEL2.SEQ below:
從 KERNEL2 中提取的段落值。如下圖：


$01000 VALUE #CODESEGS \ # of segments needed for CODE 64k
$01000 值 #CODESEGS \ # 代碼 64k 所需的區段
$01800 VALUE #LISTSEGS \ # of segments needed for : definitions 96k
$01800 值 #LISTSEGS \ # 所需區段數：定義 96k
$01000 VALUE #HEADSEGS \ # of segments needed for HEADS 64K
$01000 價值 #HEADSEGS \ 頭 64K 所需的區段數 #


These values are of course smaller than 275k, since they are
這些值當然小於 275k，因為它們是
representative of only F-PC's KERNEL.COM memory usage.
僅代表 F-PC 的 KERNEL.COM 內存使用情況。


Other pointers listed above are generally small, with the exception of
上面列出的其他指標通常很小，但
BASESEG, which reflects the memory usage of the EDITOR. If you subtract
BASESEG，它反映 EDITOR.如果您減去
239616 from 569648, you will see that F-PC needs about 330k of memory to
239616 從 569648，你會看到 F-PC 需要大約 330k 的內存才能
run, though you rill need at least 380k to use the editor on even small
運行，儘管您至少需要 380k 才能在很小的編輯器上使用
files.
檔案。


As you define your own pointers, they will be prepended to the list of
當您定義自己的指標時，它們會附加到
pointers shown by .MEM, so you can easily see how much memory your
指標由 所示。MEM，因此您可以輕鬆查看您的內存量
application is using. Note that UNEDIT can be used to release the amount
應用程序正在使用。請注意，UNEDIT 可用於釋放金額
of memory being used by the editor, to release memory for your
編輯器正在使用的記憶體，以釋放記憶體
applications use.
應用程序使用。


Line 9 shows the DOS memory that is currently available and not being
第 9 行顯示當前可用且未可用的 DOS 內存
used by F-PC. The F-PC editor always preserves 32k of DOS memory to
由 F-PC 使用。F-PC 編輯器始終保留 32k 的 DOS 內存，以
allow a SHELL to DOS from within the editor, even under the conditions
允許從編輯器內將 SHELL 傳送到 DOS，即使在以下條件下也是如此
that there is no Expanded memory or disk space available to save F-PC
沒有可用的擴展內存或磁盤空間來保存 F-PC
itself into.
本身進入。


Memory Usage when Shelling to DOS
shelling 到 DOS 時的記憶體使用量


Line 12 shows the amount of available Expanded Memory. This memory is
第 12 行顯示可用的擴充記憶體數量。這段記憶是
used by F-PC when shelling out to perform a DOS command. F-PC actually
F-PC 在執行 DOS 命令時使用。F-PC 實際上
moves all but 8k bytes of itself into expanded memory and releases the
將自身除 8k 位元組之外的所有位元組移動到擴展記憶體中，並釋放
remaining memory to DOS prior to performing a DOS command. This feature
在執行 DOS 命令之前，剩餘記憶體會儲存到 DOS。此功能
allows very large programs to be run from within F-PC, without running
允許從 F-PC 內部運行非常大的程序，而無需運行
out of program memory even though F-PC itself uses almost all of DOS's
即使 F-PC 本身使用幾乎所有 DOS 的
program memory when it is running.
程式記憶體。


Of course there may be conditions where there is either no Expanded
當然，在某些情況下，可能沒有擴展
Memory or not enough Expanded Memory available to allow F-PC to save
記憶體或不足 擴充記憶體可供 F-PC 儲存
itself. When this happens, you have two choices. Either your
它自己。發生這種情況時，您有兩個選擇。無論是您的
application can choose to shell to DOS and use only the very small amount
應用程式可以選擇 shell 到 DOS 並僅使用極少量
of memory available, or you can turn on the switch for disk storage of
可用記憶體的容量，也可以開啟磁碟儲存的開關
F-PC when shelling to DOS.
F-PC 在 DOS 上進行砲擊時。


The word SWAPFILE or "SWAPFILE both set the name of the disk swap file
SWAPFILE 或「SWAPFILE」一詞都設定磁碟交換檔案的名稱
to use when swapping F-PC to disk, and enable disk swapping with the
在將 F-PC 交換至磁碟時使用，並使用
primitive DISKON. When F-PC needs to perform a DOS command, it will
原始 DISKON。當 F-PC 需要執行 DOS 命令時，它會
first try to swap itself to Expanded Memory, and if that is not
首先嘗試將自身交換為擴展內存，如果不是
available, then it will swap to disk, freeing up program memory to
available，則會交換至磁碟，將程式記憶體釋放至
whatever DOS command you are performing. While it might seem like it
無論您正在執行什麼 DOS 命令。雖然看起來像是這樣
would be very slow, swapping about 500k bytes to disk, it is still a
會很慢，將大約 500k 位元組交換到磁盤，它仍然是一個
reasonable wah to provide a flexible facility that will run, but only
合理的 wah 提供一個靈活的設施，可以運行，但只能運行
slower on computers that don't have all of the modern resources. In fact
在沒有所有現代資源的計算機上速度較慢。事實上
swapping to a hard disk on a 286 machine only takes a few seconds, and is
在 286 機器上交換到硬碟只需要幾秒鐘，而且是
tolerable on these slower machines. You can of course set the swapfile
在這些較慢的機器上可以忍受。您當然可以將交換文件設置為
to reside on a large randisk, speeding up the process to almost that of
駐留在大型 Randisk 上，將該過程加快到幾乎
Expanded Memory.
擴展內存。


The converse words DISKOFF and EMMOFF disable F-PC's usage of these
相反的詞 DISKOFF 和 EMMOFF 禁用了 F-PC 對這些
areas when swapping for DOS shell commands.
交換 DOS shell 命令時的區域。






Number conversion and base specifying Date: 04/14/93
數字轉換和基數指定日期：04/14/93


F-PC defaults to DECIMAL at cold start. Any numbers entered in the
F-PC 在冷啟動時預設為 DECIMAL。在
decimal number base are converted from ascii into binary and placed on
十進制數基數從 ASCII 轉換為二進制並放置在
the data stack.
資料堆疊。


It is also useful at times to specify the base of a number being
有時指定數字的基數也很有用
entered either at the keyboard, or within a program source file. F-PC
在鍵盤上或程式原始檔案中輸入。F-PC
also supports the specification of the conversion base in several ways
也以多種方式支援轉換基數的規範
as long as the current base is DECIMAL!. Here are examples of valid ways
只要當前基數是十進制！以下是有效方法的範例
to specify the conversion base:
若要指定轉換基數：


DECIMAL \ MUST BE IN THE DECIMAL NUMBER BASE FOR THE
DECIMAL \ 必須在十進位數基數中，才能
\ FOLLOWING EXAMPLES TO WORK !!!!!!!!
\ 以下範例以!!!!!!!工作


ABCDh \ convert as HEX to the stack
ABCDDh \ 轉換為十六進制到堆棧
$1234 \ convert as HEX to the stack
$1234 \ 轉換為十六進制到堆疊
10001110b \ convert as BINARY to the stack
10001110b \ 轉換為 BINARY 到堆棧
'D' \ place the ASCII character D on stack
'D' \ 將 ASCII 字元 D 放在堆疊上
^G \ place the character Control-G on the stack
^G \ 將字符 Control-G 放在堆疊上


As you can see, F-PC is fairly flexible about allowing direct base
如您所見，F-PC 在允許直接基地方面相當靈活
specification.
規格。

















String processing words Date: 04/14/93
字串處理字 日期：04/14/93


F-PC includes a significant number of words to manipulate strings of
F-PC 包含大量單字來操作
characters. The operators are not as easy to use as those in BASIC, but
字符。運算子不像 BASIC 中的運算子那麼好用，但是
they are very powerful:
它們非常強大：



SCAN ( addr len char -- addr' len' )
SCAN （ addr len char -- addr' len' ）
Scan for char through addr for len, returning addr' and
通過 addr 掃描 char 以查找 len，返回 addr' 和
len' of char.
夏爾的 len'。


SKIP ( addr len char -- addr' len' )
SKIP （ addr len char -- addr' len' ）
Skip char through addr for len, returning addr' and len'
通過 addr 跳過 char for len，返回 addr' 和 len'
of char+1.
char+1 的。


-SCAN ( addr len char -- addr' len' )
-SCAN （ addr len char -- addr' len' ）
Scan for char BACKWARDS starting at addr+len, back
從 addr+len 開始掃描 char BACKWARDS，返回
through len bytes before addr, returning addr' and len'
通過 addr 之前的 len 位元組，傳回 addr' 和 len'
of char.
的 char。


-SKIP ( addr len char -- addr' len' )
-SKIP （ addr len char -- addr' len' ）
Skip occurances of char BACKWARDS starting at addr, back
跳過從 addr， back 開始的 char BACKWARDS 出現次數
through addr-len, returning addr' and len' of char.
通過 addr-len，返回 addr' 和 len' of char。


SCANW ( a1 w1 w2 --- a2 w3 ) \ Scan array a1 for word w2.
SCANW （ a1 w1 w2 --- a2 w3 ） \ 掃描陣列 a1 以取得字組 w2。
\ a1 = scan start address
\ a1 = 掃描開始位址
\ w1 = length to scan (words)
\ w1 = 掃描長度（字數）
\ w2 = word we are looking for
\ w2 = 我們正在尋找的單詞
\ a2 = address where w2 was found
\ a2 = 找到 w2 的位址
\ w3 = remaining search length (WORDS)
\ w3 = 剩餘搜尋長度 （字數）


/STRING ( addr len n -- addr' len' )
/STRING （ addr len n -- addr' len' ）
Index into the string by n. Returns addr+n and len-n.
將索引編入字串的 n 中。傳回 addr+n 和 len-n。


PARSE ( char -- addr len )
解析 （ char -- addr len ）
Scan the input stream until char is encountered.
掃描輸入流，直到遇到 char。


WORD ( c1 --- addr )
WORD （ c1 --- addr ）
Parse the input stream for char and return a count
剖析 char 的輸入資料流程並傳回計數
delimited string at here. Note there is always a blank
分隔字串。注意，總是有一個空白
following it.
跟隨它。


EXPECT ( adr len --- )
EXPECT （ adr len --- ）
Accept text into the buffer at "adr" for "len" bytes.
接受 “len” 位元組的 “adr” 緩衝區中的文字。


NEXPECT ( adr len start -- )
NEXPECT （ adr len start -- ）
Expect (append) to a buffer that may already contain some
預期 （附加） 至可能已包含某些
data.
資料。




A Simple String Example
一個簡單的字串範例


Following is an example of how the string operators can be used to
以下是如何使用字串運算子來的範例
parse a string. In this example, a counted string (a handle) is scanned
剖析字串。在此範例中，會掃描計數字串 （控點）
for repeated occurances of the '\' (backslash) character:
對於重複出現的 '\'（反斜線）字元：


: >PATHEND" ( a1 --- a2 n1 )
：>路徑」（ a1 --- a2 n1 ）
\ Return address=a2 and count=n1 of filename after path
\ 路徑後的檔案名稱的傳回位址=a2 和 count=n1
COUNT
算
BEGIN 2DUP '\' SCAN ?DUP
開始 2DUP '\' 掃描？DUP
WHILE 2SWAP 2DROP 1 /STRING
而 2SWAP 2DROP 1 /STRING
REPEAT DROP ;
重複下降;


Each occurance of '\' is found with " '\' SCAN " and then stripped off
每次出現的 '\' 都會用 “ '\' SCAN 」找到，然後剝離
with " 1 /STRING ", until no more occurances of '\' are found. Whatever
取代為“ 1 /STRING ”，直到找不到更多出現的 '\'。無論什麼
remains is assumed to be the filename with the path stripped off:
remains 被假定為路徑被剝離的檔案名稱：




















\\ Files: simple program file handling Date: 04/14/93
\\ 檔案：簡單的程式檔案處理日期：04/14/93


While working with files in F-PC is not very difficult, the details
雖然在 F-PC 中處理文件並不是很困難，但細節
have not been well documented. Here is an example program that processes
沒有很好的記錄。這是一個處理
all of the bytes of a file, and expands any tabs found before writing the
檔案的所有位元組，並在寫入
results to a second file:
結果新增至第二個檔案：


{


VARIABLE EXSIZE \ size of tab expansion in spaces
VARIABLE EXSIZE \ 空格中定位點展開的大小
8 EXSIZE ! \ set tab size to 8 spaces
8 EXSIZE ！\ 將定位點大小設定為 8 個空格


VARIABLE EXOUT \ counter of text on this line
VARIABLE EXOUT \ 此行上文字的計數器
HANDLE EXHNDL \ the expanded text file handle
HANDLE EXHNDL \ 展開的文字檔控點


CREATE CRLF$ $0D C, $0A C, \ A crlf character pair
建立 CRLF$ $0D C， $0A C， \ crlf 字元對


: EXPWRITE ( a1 n1 -- )
： EXPWRITE （ a1 n1 -- ）
dup>r exhndl hwrite r> - abort" Write error" ;
dup>r exhndl hwrite r> - 中止“ 寫入錯誤” ;


: EXTAB ( -- )
： EXTAB （ -- ）
spcs exsize @ exout @ over mod - expwrite ;


: EXPAND_A_LINE ( a1 -- ) \ expand tabs in counted string a1
： EXPAND_A_LINE （ a1 -- ） \ 展開計數字串 a1 中的製表符
crlf>bl's \ convert CRLF to blanks
crlf>bl 的 \ 將 CRLF 轉換為空白
count \ count the string
count \ 計算字串
begin 2dup 9 scan dup \ scan for a tab character
開始 2dup 9 掃描 dup \ 掃描定位字元
while 2dup 2>r nip - \ parse text before a tab
而 2dup 2>r nip - \ 解析選項卡前的文本
expwrite \ write it to file
expwrite \ 寫入檔案
2r> 1 /string \ strip off tab char
2r> 1 /string \ 剝離制表符字符
extab \ expand to next tab col
extab \ 展開至下一個索引標籤 col
repeat nip - -trailing \ strip trailing blanks
重複 nip - -trailing \ strip trailing blanks
expwrite \ write remainder of line
expwrite \ 寫入行的其餘部分
crlf$ 2 expwrite ; \ append CRLF to finish line
crlf$ 2 expwrite ;\ 將 CRLF 附加到終點線


: MAKE_EXFILE ( -- ) \ make the expanded output file
： MAKE_EXFILE （ -- ） \ 製作展開的輸出檔案
seqhandle exhndl $>handle \ move input name to output
seqhandle exhndl $>handle \ 將輸入名稱移至輸出
" EXP" ">$ exhndl $>ext \ change the file extention
“ EXP” “>$ exhndl $>ext \ 變更檔案擴充功能
exhndl hcreate \ try to make the output file
exhndl hcreate \ 嘗試製作輸出文件
\ and complain if we can't
\ 如果我們不能，就抱怨
abort" Failed to make the output file" ;
abort「無法製作輸出檔案」;






: EXPAND ( -<filename>- ) \ expand TABS in filename
： 展開 （ -<filename>- ） \ 展開檔案名稱中的 TABS
sequp \ step up to the next file handle
sequp \ 逐步執行至下一個檔案控點
bl word c@ 0= \ if no word following
bl 單詞 c@ 0= \ 如果後面沒有單詞
if cr ." File: " \ then ask for a filename
如果 cr 。檔案： “ \ 然後詢問檔案名稱
query \ and allow it to be entered
查詢 \ 並允許輸入
bl word c@ 0= \ MUST have a name!
bl 單詞 c@ 0= \ 必須有一個名字！
abort" No filename given" \ or error
abort“ 未給出檔案名稱” \ 或錯誤
then
當時
here $file ?open.error \ try to open the file, or error
這裡$file ？open.error \ 嘗試打開文件，或錯誤
make_exfile \ make the expanded file
make_exfile\ 製作展開的檔案
begin lineread \ -- a1, read a line from the file
begin lineread \ -- a1，從檔案中讀取一行
dup c@
重複的 c@
while \ while there is text to process
而\ while 有文字要處理
expand_a_line \ expand tabs in the line
expand_a_line \ 展開行中的標籤
repeat drop \ cleanup the stack
重複刪除 \ 清理堆疊
seqdown \ close the input file
seqdown \ 關閉輸入檔案
exhndl hclose drop ; \ close the output file
exhndl hclose drop ;\ 關閉輸出檔案




















\\ LINEEDITOR: an example Date: 04/14/93
\\ LINEEDITOR：範例日期：04/14/93


Built within F-PC is a very nice field (or line) editor. Everytime you
F-PC 內建了一個非常好的欄位（或線）編輯器。每次你
type a commandline into F-PC you are using the F-PC LINEEDITOR word.
在 F-PC 中鍵入命令行，您正在使用 F-PC LINEEDITOR 字。


The LINEEDITOR word is really a general purpose editor, that can be
LINEEDITOR 這個詞實際上是一個通用編輯器，可以是
used in any of your own applications in place of EXPECT or QUERY.
用於您自己的任何應用程式中，以取代 EXPECT 或 QUERY。
LINEEDITOR allows you to specify where on the screen the field or line
LINEEDITOR 允許您指定字段或行在屏幕上的位置
you are editing is to appear, its maximum length upto 80 characters.
您正在編輯的是出現，其最大長度為 80 個字符。


Full word and character operations using keypad or WordStar keys as
使用鍵盤或 WordStar 鍵作為的完整單詞和字符操作
follows:
如下：


Ctrl-A Left word
Ctrl-A 左單字
Ctrl-S Left character
Ctrl-S 左字元
Ctrl-D Right character
Ctrl-D 右字元
Ctrl-F Right word
Ctrl-F 正確的字
Ctrl-G Forward delete
Ctrl-G 向前刪除
Ctrl-T Word delete
Ctrl-T Word 刪除
Ctrl-Y Line delete or clear
Ctrl-Y 行刪除或清除
Left arrow Left character
向左箭頭 左字元
Ctrl-Left arrow Left word
Ctrl-向左鍵 向左單字
Right arrow Right character
右箭頭 右字元
Ctrl-Right arrow Right word
Ctrl-向右鍵 右字
Home Beginning of line
首頁 行首
End End of line
結束 行尾
ESC Discard changes and leave
ESC 丟棄變更並離開
Return/Enter Save changes and leave
返回/輸入 儲存變更並離開


The parameters needed by LINEEDIT are as follows:
LINEEDIT 所需的參數如下：


lineeditor ( x y a1 n1 --- f1 )
線編輯器 （ x y a1 n1 --- f1 ）


x = char pos on row, zero = left edge
x = 行上的字符位置，零 = 左邊緣
y = row number, zero = top line
y = 行號，零 = 頂行
a1 = counted string
a1 = 計數字串
n1 = edit limit length, maximum value = 80
n1 = 編輯限制長度，最大值 = 80
f1 = true for finished edit normally
f1 = true 表示正常完成的編輯
f1 = false for canceled edit
f1 = false 表示已取消的編輯


Here is an example of a command that would edit a line of text in
以下是編輯
SAMPLEBUFFER, with a maximum length of 12 characters, at location
SAMPLEBUFFER，長度上限為 12 個字元，位於位置
row 10 column 5 on the screen.
第 10 行第 5 欄。


5 10 samplebuffer 12 lineedit
5 10 樣本緩衝區 12 行編輯


Two auto resetting flags can be used to control the behavior of the
兩個自動重設旗標可用來控制
line editor in special ways.
行編輯器以特殊方式。


The STRIPING_BL'S boolean "VALUE" determines whether the line editor
STRIPING_BL 的布林值 “VALUE” 決定了行編輯器
will strip trailing blanks from an edited string at the completion of
將在完成時從編輯的字串中刪除尾端空白
the edit. this VALUE defaults to TRUE, do strip trailing blanks.
此 VALUE 預設為 TRUE，請刪除尾端空白。


OFF> STRIPPING_BL'S will prevent line edit from
OFF> STRIPPING_BL'S 將阻止行編輯
stripping spaces.
剝離空間。


The AUTOCLEAR boolean "VALUE" determines whether the line edit buffer
AUTOCLEAR 布林值 “VALUE” 決定行編輯緩衝區
will be automatically cleared if the first character you enter on
如果您輸入的第一個字符將自動清除
starting an edit is a normal text char. This is used to ease the users
開始編輯是普通的文字字元。這用於減輕用戶的負擔
life in the situation where you want to give them the option of re-using
生活在您希望給它們重複使用的選項的情況下
a string or easily entering a new one without having to delete the old
字串或輕鬆輸入新字串，而無需刪除舊字串
string first. This VALUE defaults to FALSE, no autoclear.
字串在前。此 VALUE 預設為 FALSE，沒有自動清除。


ON> AUTOCLEAR will cause line edit to
開啟>自動清除將導致行編輯
automatically clear the edit
自動清除編輯
string if a letter is the
string 如果字母是
first thing entered.
第一件事進入。


Here is a program example using LINEEDITOR, load this file and type:
這是一個使用 LINEEDITOR 的程式範例，載入此檔案並鍵入：


LETEST
萊斯特


{


CREATE LEBUF \ a buffer of text to edit with the LINEEDITOR
CREATE LEBUF \ 要使用 LINEEDITOR 編輯的文字緩衝區
HERE 61 +
這裡 61 +
," This is an example of a line to edit"
“這是要編輯的行的範例”
HERE SWAP - 0MAX ALLOT
這裡交換 - 0MAX 分配
\ allocate at least 60 characters plus a count byte
\ 配置至少 60 個字元加上一個計數位元組


: LETEST ( -- ) \ line editor test program
：LETEST （ -- ） \ 行編輯器測試程序
DARK \ clear the screen to start
DARK \ 清除螢幕開始
CR \ move down a couple of lines
CR \ 向下移動幾行
\ display current contents of buf
\ 顯示 buf 的當前內容
CR ." LEBUF contains: " LEBUF COUNT TYPE
CR 的 “。LEBUF 包含：“ LEBUF 計數類型
SAVECURSOR SAVESCR \ save cursor & screen
SAVECURSOR SAVESCR \ 儲存游標和螢幕
CYAN >BG YELLOW >FG \ select some colors for window
青色 >BG 黃色 >FG \ 為窗戶選擇一些顏色
[ HIDDEN ] \ the following vars are HIDDEN
[ 隱藏 ] \ 以下變數是隱藏的
OFF> STRIPPING_BL'S \ don't strip trail blanks
OFF> STRIPPING_BL'S \ 不要剝去軌跡空白
ON> AUTOCLEAR \ clear if direct typing
開啟>自動清除 \ 清除（如果直接輸入）
4 9 74 11 BOX&FILL \ box in editor line
4 9 74 11 編輯器行中的 BOX&FILL \ 框
." Line:" \ prompt text
."行：“ \ 提示文字
>ATTRIB1 \ colors for edit
>ATTRIB1 \ 顏色進行編輯
12 10 LEBUF 60 LINEEDITOR \ -- f1
12 10 勒布夫 60 行編輯器 \ -- f1
RESTSCR RESTCURSOR \ restore screen & cursor
RESTSCR RESTCURSOR \ 還原畫面和游標
IF CR ." Finished editing normally"
如果 CR 。正常完成編輯”
ELSE CR ." Edit canceled, no changes made to buffer"
否則 CR 。編輯已取消，未對緩衝區進行任何更改”
THEN \ show buffer to user again
THEN \ 再次向使用者顯示緩衝區
CR ." LEBUF contains: " LEBUF COUNT TYPE ;
CR 的 “。LEBUF 包含：“ LEBUF 計數類型;

