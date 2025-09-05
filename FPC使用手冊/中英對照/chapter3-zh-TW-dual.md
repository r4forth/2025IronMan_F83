# CHAPTER 3. HYPERTEXT BROWSER 第 3 章。超文本瀏覽器

On-line documentation was originally used by Forth, Inc. to allow its
線上文件最初由 Forth， Inc. 使用，以允許其
users a fast access to the source and documentation of all the compiled
用戶可以快速訪問所有編譯的源代碼和文檔
code. The command LOCATE and its abbreviation LL (VIEW in F83) looks up
法典。指令 LOCATE 及其縮寫 LL （F83 中的 VIEW） 會查閱
a word in the dictionary and find the block from which the word is
字典中的一個單詞，然後找到該單詞所在的塊
compiled and displays the text in this block. The command "A" alternates
編譯並顯示此區塊中的文字。命令「A」交替
between the source block and its corresponding shadow block, which
在來源區塊與其對應的影子區塊之間，而
contains comments and documentation on the compiled word. This technique
包含有關編譯字的註釋和文件。這種技術
was also used in F83 to provide access to multiple files of source and
也用於 F83 中，以提供對多個來源檔案的存取，以及
help texts.
幫助文本。

F-PC 2.25 inherited the VIEW mechanism from F83 to display the source
F-PC 2.25 繼承了 F83 的 VIEW 機制，以顯示源
code. Instead of combining the source code and shadow documentation in a
法典。而不是將原始程式碼和影子文件結合在
single file, F-PC put the documentation in separated .HLP files. Hence a
單個文件，F-PC 將文檔放在單獨的 .HLP 檔案。因此，一個
new word HELP was defined to access the help files.
定義了新詞 HELP 來存取說明檔案。

George Hawkins developed a browsing utility which allows a user to browse
喬治·霍金斯開發了一個瀏覽實用程序，允許用戶瀏覽
words freely in the editor. The user moves the editing cursor over a
在編輯器中自由表達。使用者將編輯游標移至
word, with a single key stroke the proper source file is opened and the
word，只需按一下按鍵即可開啟正確的原始檔，並且
source code of this word is displayed in the editor window. With this
此單字的原始碼會顯示在編輯器視窗中。有了這個
capability in the editor, the user can lookup any word in F-PC quickly
編輯器中的功能，用戶可以快速查找 F-PC 中的任何單詞
which greatly helps the programming process.
這極大地幫助了編程過程。

Tom Zimmer was duely impressed with the browser. He extended the
湯姆·齊默 （Tom Zimmer） 對這款瀏覽器印象深刻。他延長了
browsing mechanism to include not only the source code but also arbitrary
瀏覽機制不僅包含原始碼，還包含任意
documentation. He ended up with a powerful hypertext-like on-line
文檔。他最終得到了一個強大的類似超文本的在線
documentation system, which is the main attraction of F-PC 3.5. Tom also
文檔系統，這是 F-PC 3.5 的主要吸引力。湯姆也
spent much efforts in building a substantial amount of tutorial and
花費了大量精力來構建大量的教程和
documentational materials on the hypertext system to help a new user to
超文本系統上的文檔材料，以幫助新用戶
get acquainted with F-PC.
熟悉 F-PC。

## 3.1. LAUNCH THE HYPERTEXT BROWSE 3.1.啟動超文本瀏覽器

The best way to learn F-PC is to use it. If you have F-PC installed
學習 F-PC 的最佳方法是使用它。如果您安裝了 F-PC
according to the procedure outlined in Chapter 2, change your current
根據第 2 章中概述的程序，更改您當前的
directory to C:FPC and type "F" to execute the F.EXE your saved. A
目錄到 C：FPC 並鍵入“F”以執行您保存的 F.EXE。一個
sign-on screen appears on the screen and F-PC comes to life.
屏幕上出現登錄屏幕，F-PC 變得栩栩如生。

On the top of your screen is a status line. The two leftmost fields show
螢幕頂部是狀態行。最左邊的兩個欄位顯示
you the number of free bytes in the Code space, and that in the List
您是程式碼空間中的可用位元組數，以及清單中的可用位元組數
space. The third item tells you how many items are on the data stack.
間。第三項告訴您資料堆疊上有多少項。
Normally the data stack is empty, and it shows the "Stack Empty" message.
通常資料堆疊是空的，並顯示「堆疊為空」訊息。
The fourth item is the drive/directory/filename field. It shows your
第四項是磁碟機/目錄/檔案名稱欄位。它顯示您的
current directory. If a file is opened, the file name appears after the
目前目錄。如果開啟檔案，檔案名稱會出現在
directory path. The rightmost field show the current time, which is
目錄路徑。最右邊的欄位顯示目前時間，即
obtained from the DOS clock.
從 DOS 時鐘取得。

Under the current time is a picture of the vocabulary stack. The topmost
當前時間下方是詞彙堆疊的圖片。最頂層
item is the current vocabulary to which new definitions are linked. The
item 是新定義連結到的目前詞彙。這
next is the context vocabulary stack, which shows the vocabulary search
接下來是上下文詞彙堆疊，它展示了詞彙搜尋
order. Most often the current and the top context vocabulary are FORTH,
次。大多數情況下，當前和頂部上下文詞彙是 FORTH，
and the ROOT vocabulary is at the bottom of the vocabulary stack.
而 ROOT 詞彙表位於詞彙堆疊的底部。

The status line shows you the most vital information about F-PC. It is
狀態行向您顯示有關 F-PC 的最重要信息。這是
updated whenever you hit a key on the keyboard. Keep an eye on it
每當您按下鍵盤上的某個鍵時都會更新。密切關注它
occasionally as you work.
偶爾在你工作時。

The text in the sign-on screen suggests that you use F1 and ESC keys to
登入畫面中的文字建議您使用 F1 和 ESC 鍵來
get more information about F-PC. Pushing F1 launches the browser and
獲取有關 F-PC 的更多信息。按下 F1 會啟動瀏覽器，並
displays the root screen of the hypertext help system. A file
顯示超文本幫助系統的根畫面。一個檔案
FPCHELP.TXT is opened, the SED text editor is invoked, and you are put in
FPCHELP.TXT 開啟，呼叫 SED 文字編輯器，並將您放入
the browsing mode to examine the features of F-PC.
瀏覽模式來檢查 F-PC 的功能。

Pushing ESC key causes a menu bar to appear under the status line.
按下 ESC 鍵會導致狀態行下方出現功能表列。
Pushing <return> or <down- arrow> pulls down a menu. Use the up and down
按下<return>或<向下箭頭>可下拉選單。使用上下
keys to select a menu item, followed by <return> to execute the
鍵來選取功能表項目，然後<return>執行
selection. You can create a new file for editing, or open an old file,
選擇。您可以建立新檔案進行編輯，或開啟舊檔案，
spawn a DOS shell, quit F-PC, or launch the hypertext browser.
生成 DOS shell、退出 F-PC 或啟動超文本瀏覽器。

Use either method to launch the browser and start experimenting F-PC.
使用任一方法啟動瀏覽器並開始試驗 F-PC。
You are in the browsing mode of the SED editor, looking at the beginning
您處於 SED 編輯器的瀏覽模式，查看開頭
of the FPCHELP.TXT file. The text is enclosed in a double-line border,
FPCHELP.TXT 檔案。文字以雙行邊框括起來，
which indicates that you are in the browsing mode. If you are in the
這表示您處於瀏覽模式。如果您在
editing mode, the border is drawn using single-lines.
編輯模式時，邊框是使用單線繪製的。

A status line is at the top of the display. This line contains various
顯示畫面頂端會顯示狀態行。此行包含各種
pieces of information about the file being browsed or edited, including
有關正在瀏覽或編輯的檔案的資訊片段，包括
the word BROWSE at the left hand side. When you are in the editor, the
左側的「瀏覽」一詞。當您在編輯器中時，
word BROWSE will change to INSERT, or OVERWRITE indicating the
單詞 BROWSE 將更改為 INSERT 或 OVERWRITE，表示
appropriate edit mode.
適當的編輯模式。

The bottom line displays the name of the file being viewed, and a couple
底行顯示正在檢視的檔案名稱，以及幾個
of helpful hints. HELP=F1, and MENU=ESC. F1 will link you into another
有用的提示。HELP=F1，以及 MENU=ESC。F1 會將您連接到另一個
copy of the hypertext help system where you can get help on the various
超文本幫助系統的副本，您可以在其中獲得有關各種幫助
editor functions.
編輯器功能。

You can press F1 now if you want to, and press F10 to come back here.
如果你願意，現在可以按 F1，然後按 F10 回到這裡。

Pressing the ESC key will cause a menu bar to be displayed. Having
按 ESC 鍵將顯示一個菜單欄。擁有
pressed ESC, you can press the first letter of a menu name, or use the
按 ESC，您可以按選單名稱的第一個字母，或使用
keypad arrow keys to move around on the menubar. Pressing Enter while a
鍵盤方向鍵在菜單欄上移動。按下 Enter 鍵，同時
menu item is selected will cause the specified operation to be performed.
選單項目將導致執行指定的操作。
Pressing ESC again while the menubar is visible, will make it go away.
在菜單欄可見時再次按 ESC 將使其消失。

Use Down Arrow or the PgDn key on the keypad to advance through the
使用向下鍵或鍵盤上的 PgDn 鍵，在
FPCHELP.TXT file, and the Up Arrow or PgUp key to backup toward the
FPCHELP.TXT 檔案，然後向上鍵或 PgUp 鍵備份到
beginning of a file. Press F10 when you want to unlink to the previous
檔案的開頭。當您想要取消與上一個的連結時，請按 F10
browser.
瀏覽器。


## 3.2. NAVIGATE F-PC WITH THE BROWSER 3.2.使用瀏覽器導航 F-PC

To browse F-PC is very easy. You move the cursor around using the arrow
瀏覽 F-PC 非常簡單。您可以使用箭頭移動游標
keys and the PgUp/PgDn keys. After you position the cursor on a word
鍵和 PgUp/PgDn 鍵。將游標放在單字上之後
that you are interested, push <return> or F9 key, and the browser will
你有興趣，按下<return>或 F9 鍵，瀏覽器就會
try to find more information about that word. If the word is a Forth
嘗試找到有關該詞的更多信息。如果單詞是 Forth
command, the browser will open the corresponding source file and display
命令，瀏覽器會開啟對應的原始檔案並顯示
the source code of this command. If the word is displayed in reversed
此命令的原始程式碼。如果單字顯示為反轉
video, indicating that it contains a link, pressing <return> or F9 will
視頻，表示它包含鏈接，按<return>或 F9 將
lead you to the text linked to this word. You can also use the TAB key
引導您找到與該單詞相關的文本。您也可以使用 TAB 鍵
to jump from the current cursor location to the next hypertext link. The
從目前游標位置跳到下一個超文本連結。這
shift-TAB key moves the cursor to the link immediately above the cursor.
Shift-TAB 鍵將游標移動到游標正上方的鏈接。

<Return> and F9 keys allow you to search deeper and deeper into the
<Return> F9 鍵可讓您越來越深入地搜索
hypertext system. F10 allows you to back out to the last link you
超文本系統。F10 可讓您退回到最後一個連結
pointed to. Keep on pressing F10 will eventually lead you back to the
指向。繼續按 F10 最終將帶您回到
root help screen.
root 說明畫面。

F-PC hypertext help system present you with 8 major topics:
F-PC 超文本幫助系統為您呈現 8 大主題：

Hypertext How to use the hypertext system
超文本如何使用超文本系統
Hyper-System How to build your own hypertext system.
超系統：如何建立自己的超文本系統。
Get-Started Introduction to F-PC.
入門 F-PC 簡介。
SED-Help Editor help and documentation.
SED-Help 編輯器說明和文件。
Forth-Help Help on Forth words in F-PC.
F-PC 中 Forth 單詞的 Forth-Help 幫助。
F-PC-Utils Documentation on F-PC utilities.
F-PC 實用程式的 F-PC-Utils 文件。
Preferences Select options in F-PC.
偏好設定 在 F-PC 中選取選項。
Whats-new Update and bug-fixes.
新功能更新和錯誤修復。

Each of these topics starts a tree of tutorial or documentation. It is a
這些主題中的每一個都會啟動教學或文件樹狀結構。這是一個
very interesting system to explore interactively. Since F-PC is such a
非常有趣的系統，可以互動探索。由於 F-PC 是這樣的
huge system and no one can possible remember all the words and the
龐大的系統，沒有人能記住所有的單詞和
command key sequences, this hypertext system makes all these pertinent
命令鍵序列，這個超文本系統使所有這些都相關
information available at your fingertip.
信息觸手可及。


## 3.3. A SAMPLE SESSION 3.3. 範例會話

Once F-PC has been installed on your computer, you can start it up by
在您的計算機上安裝 F-PC 後，您可以通過以下方式啟動它
typing "F-PC <return>" or "F" from the keyboard. This will display a
從鍵盤上鍵入“F-PC<return>”或“F”。這將顯示
sign-on message about the version number, available memory, etc. Type
有關版本號、可用記憶體等的登入訊息。型
HELLO will display this sign-on screen any time.
HELLO 將隨時顯示此登錄屏幕。

To open a file, type the following:
若要開啟檔案，請輸入下列內容：

```
OPEN BANNER <return>
```

The file BANNER.SEQ will be opened. We can load it with:
檔案 BANNER.SEQ 將開放。我們可以加載它：

```
1 LOAD <return>
```

This prints a nice demo message. This demo came from the F83X system
這會列印一個不錯的演示訊息。此演示來自 F83X 系統
written by Wil Baden.
威爾·巴登編劇。

We can edit the source for BANNER by typing:
我們可以透過輸入以下內容來編輯 BANNER 的來源：

```
ED <return>
```

You will now be in the editor, viewing the first 23 lines of BANNER.SEQ.
您現在將在編輯器中查看 BANNER.SEQ 的前 23 行。
You can page down through the file with the PgDn key on the keypad, and
您可以使用鍵盤上的 PgDn 鍵向下翻閱文件，並且
back up with the PgUp key. For now, page down to the bottom of the file
使用 PgUp 鍵備份。現在，向下翻頁到檔案底部
with PgDn, and there you see the definition of the word DEMO, which
與 PgDn，然後您會看到 DEMO 一詞的定義，其中
prints out our demonstration banner.
列印出我們的示範橫幅。

Now let's create a new file and put a new DEMO definition with your own
現在讓我們建立一個新檔案，並使用您自己的 DEMO 定義來放置一個新的 DEMO 定義
banner message in it. Leave the editor by typing Alt-F10 ESC. You will
橫幅訊息。鍵入 Alt-F10 ESC 離開編輯器。你會
now be back in Forth without saving any changes you may have accidentally
現在返回 Forth，無需保存您可能意外進行的任何更改
made to BANNER.SEQ.
製作給 BANNER.SEQ。

To create the new file, type the following:
若要建立新檔案，請輸入下列內容：

```
NEWFILE MYBANNER <return>
```

F-PC will start the editor, and try to open the file MYBANNER. If it is
F-PC 將啟動編輯器，並嘗試開啟檔案 MYBANNER。如果是
present, F-PC will open it. If it is not, then F-PC will automatically
現在，F-PC 將打開它。如果不是，那麼 F-PC 將自動
create a new file called MYBANNER.SEQ and place you in the editor in that
建立名為 MYBANNER 的新檔案。SEQ 並將您放入編輯器中
file, prepared to accept text.
檔案，準備接受文字。

Type in the following definition, using the <return> key to add new lines
輸入下列定義，使用<return>鍵新增行
to the file as needed. The arrow keys can be used to move around, but you
視需要移至檔案。方向鍵可以用來四處移動，但你
will not be allowed to move below the mass of the reversed colored blank
不允許移動到反色坯料的質量以下
characters, as they represent the end of the current file.
字元，因為它們代表目前檔案的結尾。

```
: MYBANNER ( --- )
" HELLO" BANNER
" FROM" BANNER
" YOURNAME" BANNER ;
```

Note that YOURNAME must be no longer than 11 characters.
請注意，YOURNAME 不得超過 11 個字元。

Now that you have typed in or edited the above definition into the file
現在您已在檔案中輸入或編輯上述定義
MYBANNER.SEQ, leave the editor while saving the text you have entered, by
我的橫幅。SEQ，在保存您輸入的文本時離開編輯器，通過
pressing F10 ESC.
按下 F10 ESC。

Let's compile the program. Type:
讓我們編譯程式。型：

```
FLOAD MYBANNER <return>
```

The file MYBANNER.SEQ is opened, and loaded. If you entered the program
檔案 MYBANNER。SEQ 已開啟並載入。如果您進入了該計劃
as shown, then all should be well, and Forth should come back with the
如圖所示，那麼一切都應該會好起來的，符式語言應該會帶著
"ok" message. You could have also compiled the program by typing 1 LOAD
“確定”消息。您也可以透過鍵入 1 LOAD 來編譯程式
<return>, since the file was already open.
<return>，因為檔案已經開啟。

Now that MYBANNER is compiled, type its name to make it do its stuff:
現在 MYBANNER 已編譯完畢，請輸入其名稱以使其執行其操作：

```
MYBANNER <return>
```

You should have seen your name scroll up on the screen. If you didn't,
您應該已經看到您的名字在屏幕上向上滾動。如果你沒有，
try editing the source file and correcting your typing error.
嘗試編輯源文件並糾正輸入錯誤。

At this point, you can VIEW the source for MYBANNER by typing:
此時，您可以通過鍵入以下內容查看 MYBANNER 的源代碼：
VIEW MYBANNER <return>
查看我的橫幅<return>

F-PC will locate the source for your MYBANNER word, and display the
F-PC 將找到您的 MYBANNER 單字的來源，並顯示
source code starting at the line where MYBANNER was started. A shorter
原始碼從 MYBANNER 啟動的行開始。一個較短的
word for VIEW called V is provided to save typing.
提供了名為 V 的 VIEW 單詞以節省打字。

After all these work, you are ready to quit. Type:
完成所有這些工作後，您就可以辭職了。型：

```
BYE <return>
```

and you will return to DOS, which displays the familiar C> prompt.
您將返回 DOS，它顯示熟悉的 C> 提示符。


## 3.4. A SHORT TUTORIAL 3.4. 簡短教程

The browser is a great tool to explore F-PC. You can jump from place to
該瀏覽器是探索 F-PC 的絕佳工具。你可以從一個地方跳到
place, looking at documentation and code at will. However, to program in
地方，隨意查看文檔和代碼。但是，要在
F-PC, you need a set of basic tool words which allows you to compile
F-PC，你需要一組基本的工具字，讓你可以編譯
words in files, examine the dictionary, and test the code. As the editor
文件中的單詞，檢查字典並測試代碼。作為編輯
will be covered in detail later, we will give you a short tutorial on
後面會詳細介紹，我們會給大家一個簡短的教程
these tool words. You are assumed to know Forth from other Forth
這些工具詞。你被假定從其他人那裡認識 Forth
textbooks and manuals, and we will not try to teach you Forth. However,
教科書和手冊，我們不會試圖教你符式語言。但
Dr. Jack Brown runs an on-line tutorial on the North Coast Forth BBS,
傑克·布朗博士在北海岸符式語言 BBS 上運行在線教程，
(604) 434-5886. The tutorial materials are also available from GEnie,
(604) 434-5886.教學資料也可從 GEnie 獲得，
(800) 638-9636. Dr. Brown had agreed to upgrade the tutorial based on
(800) 638-9636.布朗博士同意根據以下內容升級教程
F-PC 2.25 to 3.5 and will shortly make it available in print.
F-PC 2.25 至 3.5，並將很快提供印刷版。

Following is a list of words that you have to know very well to be able to use F-PC effectively:
以下是您必須非常熟悉才能有效使用 F-PC 的單詞列表：

To open an existing file: OPEN <filename>
若要開啟現有檔案：開啟<filename>
To edit a file already open: ED
若要編輯已開啟的檔案：ED
To leave the browser: F10 or ESC F E
若要離開瀏覽器：F10 或 ESC F E
To leave the editor and save changes: F10 or ESC F E
若要離開編輯器並儲存變更：F10 或 ESC F E
To leave the editor and discard changes: Alt-F10 or ESC F Q
若要離開編輯器並捨棄變更：Alt-F10 或 ESC F Q
To create and edit a new file: NEWFILE <newfilename>
若要建立和編輯新檔案：NEWFILE <newfilename>
To load a file: FLOAD <filename>
若要載入檔案：FLOAD <filename>
To load a file already open: OK or 1 LOAD
若要載入已開啟的檔案：確定或 1 載入
To view/browse a words source: VIEW <word>
若要檢視/瀏覽單字來源：檢視<word>
BROWSE <word>
瀏覽 <word>
Some short cuts to view and browse: V <word> or B <word>
查看和瀏覽的一些快捷方式：V <word> 或 B <word>
To edit source of a word: ED <word> or E <word>
編輯單字來源：ED <word> 或 E <word>
To see all words containing a string: WORDS <substring>
若要查看包含字串的所有單字：WORDS <substring>
WORDS can be followed by two substrings:WORDS <substring> <substring>
WORDS 後面可以有兩個子字串：WORDS <substring> <substring>
To de-compile a dictionary word to the screen: SEE <word>
若要將字典單字反編譯到螢幕上：請參閱<word>
To find all occurrences of a string in a file: FLOOK <string> <filspec>
若要尋找檔案中所有出現的字串：FLOOK <string> <filspec>

Some specific examples are given in the following.
下面給出一些具體的例子。
WORDS H <return> \ Display all words in dictionary containing "H".
單詞 H <return> \ 顯示字典中包含“H”的所有單詞。

--[ FORTH ]-- \ F-PC displays these words
--[ FORTH ]-- \ F-PC 顯示這些字詞
OPEN $HOPEN HOPEN
打開 $HOPEN HOPEN

VIEW HOPEN <return> \ Enter the browser displaying the source code for
查看 HOPEN <return> \ 進入瀏覽器，顯示
\ HOPEN. Press F10 to leave the browser.
\ 霍彭。按 F10 離開瀏覽器。

```
ED <return>
```

After performing the above command sequence, ED will enter the editor on
執行上述命令序列後，ED 會在
the source for HOPEN. This is like the browser but you have to be careful
HOPEN 的來源。這就像瀏覽器，但你必須小心
not to make any changes. Press Alt- F10 to leave the editor and not
不做任何改變。按 Alt-F10 離開編輯器，而不是
saving changes.
儲存變更。

```
FLOAD SWINDOW <return>
```

If the file SWINDOW is present on your disk, it will be compiled. You
如果您的磁碟上存在 SWINDOW 檔案，則該檔案將被編譯。你
can now type "POPUP" to see a sample popup window. You may get an error
現在可以鍵入“POPUP”來查看示例彈出窗口。您可能會收到錯誤
message if the file SWINDOW.SEQ is not present on your disk.
如果檔案 SWINDOW.您的磁碟上不存在 SEQ。

```
OPEN SWINDOW.SEQ ED <return>
```

This command will open the file SWINDOW, and enter the editor. The
此指令將開啟檔案 SWINDOW，然後進入編輯器。這
extension .SEQ is used automatically if no extension is specified.
擴展名。如果未指定延伸模組，則會自動使用 SEQ。

```
OK <return>
```

Will compile the currently open file. This is the same as FLOAD but works
將編譯目前開啟的檔案。這與 FLOAD 相同，但有效
on the most recently edited or viewed file.
在最近編輯或檢視的檔案上。

```
SEE HEX <return>
```

```
F-PC displays:
```

```
: HEX 16 BASE ! ;
```

Allows you to see the source for a colon definition without having the
可讓您查看冒號定義的來源，而不需要
source file available on disk.
磁碟上可用的來源檔案。

Here are some additional words you can use to manipulate files.
以下是一些可用於操作文件的其他單詞。

```
<n1> LOAD \ Start loading file at <n1>.
LISTING \ Print out the current file.
NEWFILE <newfile> \ Create the file <newfile> if it
\ does not already exist, and edit it.
INDEX \ Display first line of all .SEQ
\ files in current directory.
```

The above examples should be enough to get you at least started in
上面的例子應該足以讓你至少開始
exploring F-PC. If you are the type of person who likes to read
探索 F-PC。如果你是那種喜歡讀書的人
everything before experimenting, then continue on and you will find out
在嘗試之前，然後繼續，你會發現的
how to print the documentation included with F-PC.
如何列印 F-PC 隨附的文檔。

There is a considerable amount of documentation provided on disk to
磁碟上提供了大量文件
assist you in discovering F- PC. Actually it is provided on disk because
幫助您發現 F-PC。實際上它是在磁盤上提供的，因為
many of you won't have this F-PC Users Manual available to help you get
你們中的許多人沒有這本 F-PC 用戶手冊來幫助您獲得
started. We of course recommend you get the F-PC Users Manual, it was
開始了。我們當然建議您獲取 F-PC 用戶手冊，它是
generated on a Macintosh, and laser printed. It is a good reference, with
在 Macintosh 上生成並激光打印。這是一個很好的參考，有
a good glossary, and is available from Offete Enterprises for $20.00
一個很好的詞彙表，可從 Offete Enterprises 購買，售價 20.00 美元
dollars plus postage.
美元加郵資。


If you insist on making printouts of all of documentation files, here is
如果您堅持要列印出所有文件文件，請按此
a command to print a text file in the current directory:
在目前目錄中列印文字檔案的指令：

```
FPRINT <filename.TXT> <return>
```

Be sure your printer is ready for printing. If you are going to print all
確保您的印表機已準備好列印。如果您要列印所有
the documentation, have at least several hundred sheets of paper
文件，至少有幾百張紙
available to complete the job. The F-PCGLOS.TXT file is too large to
可用於完成工作。F-PCGLOS.TXT 檔案太大，無法
print from F-PC, use the demo Z editor provided. Z is on the fourth F-PC
從 F-PC 打印，請使用提供的演示 Z 編輯器。Z 在第四個 F-PC 上
distribution diskette.
發行軟盤。

