# CHAPTER 2. INSTALL F-PC 第 2 章。安裝 F-PC

## 2.1. THE ZIP FILES 2.1. ZIP 檔案

F-PC is distributed on four 360K 5.25" MS-DOS DSDD diskettes or one 1.2M
F-PC 分佈在四張 360K 5.25 英寸 MS-DOS DSDD 軟盤或一塊 1.2M 上
quad density diskette. The first diskette of the DSDD disk set contains
四密度軟碟。DSDD 磁碟集的第一張磁片包含
the installation instructions and the main body of F-PC execution files.
安裝說明和 F-PC 執行文件的主體。
The second disk contains mostly the source code of F-PC. The third disk
第二個磁盤主要包含 F-PC 的源代碼。第三個磁碟
contains documentation and help files, with some utilities. The last
包含文件和說明文件，以及一些實用程式。最後
disk contains the zip utility from PKware. The file names and statistics
磁碟包含 PKware 的 zip 公用程式。檔案名稱和統計資料
are summarized in Appendix C1.
總結在附錄 C1 中。


We will be using the PKUNZIP program to restore all the .ZIP files back
我們將使用 PKUNZIP 程序恢復所有.ZIP 文件
to their original form. The PKZIP.EXE is the zip utility which you can
恢復到它們的原始形式。PKZIP.EXE 是 zip 實用程序，您可以
use to compress your files. The PKZ101.EXE file, when executed will
用於壓縮檔案。PKZ101.EXE 檔案執行時將
produce PKZIP.EXE, PKUNZIP.EXE and the complete documentation on the zip
在 zip 上生成 PKZIP.EXE、PKUNZIP.EXE 和完整的文檔
utilities. The zip utility is provided by PKWARE, Inc. as a shareware
公用事業。zip 實用程序由 PKWARE， Inc. 作為共享軟件提供
product. PKWARE, Inc. requires that the entire package be distributed
品。PKWARE， Inc. 要求分發整個套件
with applications. This is the reason why PKZ101.EXE is included in
與應用程序。這就是 PKZ101.EXE 被收錄在
F-PC.
F-PC。


F-PC 2.25 was distributed in .ARC form. The arc utility was also
F-PC 2.25 在 中分發。ARC 形式。電弧實用程序也是
produced by PKWARE. However, the zip utility is adopted here because it
由 PKWARE 製作。但是，這裡採用 zip 實用程序，因為它
has better compression efficiency than the arc utility. You should be
具有比 Arc 實用程式更好的壓縮效率。你應該是
aware that the zip utility is not public domain program. If you find it
請注意 ZIP 實用程序不是公共領域程序。如果你找到它
is useful, please register with PKWARE, Inc. Send $47 to PKWARE and you
有用，請向 PKWARE， Inc. 註冊。向 PKWARE 發送 47 美元和您
will receive, when available, the next version of the PKZIP, PKUNZIP, and
如果可用，將收到下一個版本的 PKZIP、PKUNZIP 和
PKSFX programs. Please state the version of the software that you
PKSFX 計劃。請說明您所擁有的軟件版本
currently have. Send check or money order to: PKWARE, Inc. 7545 N.
目前有。將支票或匯票發送至：PKWARE， Inc. 7545 N。
Port Washington Rd, Glendale, WI 53217.
華盛頓港路，格倫代爾，威斯康星州 53217。


The command syntax to unzip a zip file is:
解壓縮 zip 檔案的命令語法為：


PKUNZIP [options] zipfile [d:outpath\] [file...]
PKUNZIP [選項] zipfile [d：outpath\] [檔案...]


Options are:
選項包括：
-c[m] extract to screen [with more]
-c[m] 提取到屏幕 [更多]
-d create directories stored in ZIP
-d 建立儲存在 ZIP 中的目錄
-h display this help message
-h 顯示此說明訊息
-j<H,S,R> mask off Hidden/System/Readonly attributes
-j<H，S，R> 遮罩關閉隱藏/系統/唯讀屬性
upon extraction
提取後
-J<H,S,R> don't mask off Hidden/System/Readonly attributes
-J<H，S，R> 不會遮罩隱藏/系統/唯讀屬性
-l display software license
-l 顯示軟體授權
-n extract only newer files
-n 僅提取較新的文件
-o overwrite existing files
-o 覆寫現有檔案
-p[a,b,c][1,2,3] extract to printer [Asc mode,Bin mode,Com port]
-p[a，b，c][1,2,3] 解壓縮到印表機 [Asc 模式，Bin 模式，Com 連接埠]
[port #]
[連接埠 #]
-q enable ANSI in comments
-q 在評論中啟用 ANSI
-s<pwd> unScramble with password
-s<pwd> 使用密碼進行解密
-t test zipfile integrity
-t 測試 zip 檔案完整性
-v[b,c,d,e,n,p,s,r] view ZIP(s) [Brief listing/sort by Crc/Date/Ext
-v[b，c，d，e，n，p，s，r] 查看 ZIP（s） [按 Crc/Date/Ext 簡要列出/排序
/Name/Percentage/Size/sort Reverse (descending)
/名稱/百分比/大小/排序 反向 （遞減）
order]
訂購]


zipfile ZIP file name, wildcards *,? ok. Default
zipfile ZIP 檔案名稱，萬用字元 *，？好。預設
extension is .ZIP file
副檔名是.ZIP 檔案
Name(s) of files to extract. Wildcards *,? ok. Default is ALL files.
要擷取的檔案名稱。萬用字元 *，？好。預設值為所有檔案。
Unzip all .ZIP files on Drive A: to directory C:\FPC\SRC is:
將磁碟機 A 上的所有.ZIP 檔案解壓縮到目錄 C：\FPC\SRC 是：


PKUNZIP A:*.ZIP C:\FPC\SRC
PKUNZIP A：*.ZIP C：\FPC\SRC


If you forget the options you want to use, type the following to get the
如果您忘記要使用的選項，請輸入下列內容以取得
above option list:
以上選項清單：


PKUNZIP -h


An interesting unzip command is:
一個有趣的解壓縮命令是：


PKUNZIP -v A:*.ZIP
PKUNZIP -v A：*.ZIP


which lists all the zipped files on the monitor, with file statistics and
它列出了監視器上的所有壓縮文件，以及文件統計信息和
checksums. Appendix C2-C5 shows the lists of all zipped files in F-PC.
總和檢查碼。附錄 C2-C5 顯示了 F-PC 中所有壓縮檔案的清單。
You can compare your file lists against them to verify the integrity of
您可以將檔案清單與檔案清單進行比較，以驗證檔案清單的完整性
your F-PC system.
您的 F-PC 系統。


## 2.2. INSTALL F-PC USING INSTALL.EXE 2.2. 使用 INSTALL.EXE 安裝 F-PC

F-PC includes an installation program INSTALL.EXE. It creates
F-PC 包括一個安裝程序 INSTALL.EXE。它創造了
directories and expands .ZIP files onto your hard disk. This process
目錄並將.ZIP 檔案擴充到硬碟上。這個過程
takes only a few minutes, and will consume about 2 megabytes if all
只需幾分鐘，如果全部
portions of F-PC are installed. After installation completes, the program
安裝了 F-PC 的一部分。安裝完成後，程式
proceeds into the configuration section. You are asked questions about
進入組態區段。系統會問您有關
your hardware. After which an installed copy of F-PC is created.
你的硬件。之後，將建立已安裝的 F-PC 副本。

If the above process make you uncomfortable, or you just want to do the
如果上述過程讓你感到不舒服，或者你只是想做
installation yourself, proceed to the next section. Otherwise just type:
自行安裝，請繼續下一節。否則只需輸入：

A:INSTALL
A：安裝

The first thing INSTALL.EXE does is ask you whether you are installing
INSTALL.EXE 做的第一件事就是詢問您是否正在安裝
F-PC on your hard disk, or configuring a copy of F-PC already present on
F-PC 在硬碟上，或設定 F-PC 的複本，或設定 F-PC 的複本
your hard disk. To this question, you would answer "I" for Install, or
你的硬碟。對於這個問題，您會回答「我」表示安裝，或
"C" for configure. The default is "I". You can simply push the <return>
“C”代表配置。預設值為「I」。您只需將<return>
key to select the default choice.
按鍵來選取預設選項。

Question two is where you want F-PC placed on your hard disk and its
問題二是您希望 F-PC 放置在硬盤上的位置及其
directory. The default is "C:\FPC".
目錄。預設值為「C：\FPC」。

Question three is where are you installing F-PC from, usually drive "A:".
問題三是從哪裡安裝 F-PC，通常是驅動器“A：”。

At this point you are asked six (6) yes or no questions about what
此時，您會被問到六 （6） 個是或否的問題，關於什麼
portions of F-PC to install. You will need all the files if you are new
要安裝的 F-PC 部分。如果您是新手，您將需要所有文件
to F-PC. Push <return> to make the default selections. However, after
到 F-PC。按以<return>進行預設選取。然而，在
you gain experience and confidence in using F-PC, you will not need the
您獲得了使用 F-PC 的經驗和信心，您將不需要
help and text files, and you may eliminate these files by pushing "N" to
help 和文字檔案，您可以透過將「N」推送到
some of the questions.
一些問題。

Lastly you are prompted to insert F-PC disk number one, and press <enter>
最後，系統會提示您插入 F-PC 磁盤一號，然後按<enter>
to start the installation. After the files on disk one is unzipped, you
以開始安裝。解壓縮磁碟一上的檔案後，您可以
will be asked to remove disk one and insert disk 2, etc. Follow the
將被要求移除磁碟一並插入磁碟二等。遵循
instructions and all the files needed will be unzipped and moved into the
說明，所有需要的檔案都會解壓縮，並移至
appropriate directories on your hard disk.
硬碟上的適當目錄。

After the files are copied, you will be asked several questions to
複製文件後，系統會問您幾個問題
configure or customize F-PC to your computer environment, such as your
根據您的電腦環境配置或自訂 F-PC，例如
monitor, whether backup files are created automatically for editing, etc.
監控，是否自動建立備份檔案進行編輯等。
Detailed explanation to each question is displayed to guide your
顯示每個問題的詳細解釋以指導您的
selection. At the end of the configuration session, a file "F.EXE" will
選擇。在配置會話結束時，檔案「F.EXE」將
be created, which is the F-PC execution file you will use. You can give
建立，這是您將使用的 F-PC 執行檔案。你可以給
it a different name if you do care.
如果你真的在乎的話，那就換個名字了。

## 2.3. INSTALL F-PC WITHOUT USING INSTALL.EXE 2.3. 安裝 F-PC 而不使用 INSTALL.EXE

In this section you are assumed to be an experienced DOS user. If you are
在本節中，假設您是經驗豐富的 DOS 使用者。如果你是
not, then please go ahead and use INSTALL.EXE. The process is pretty
不是，那麼請繼續使用 INSTALL.EXE。過程很漂亮
painless as INSTALL.EXE was designed to eliminate much of the problems in
無痛 INSTALL.EXE 旨在消除
adapting F-PC to a wide variety of PC's and their clones. There are
使 F-PC 適應各種 PC 及其克隆。有
occasions when INSTALL would fail to complete the installation process.
INSTALL 無法完成安裝程序的情況。
This section will help you to get a working F-PC system in this
本節將幫助您在此獲得一個有效的 F-PC 系統
unfortunate situation.
不幸的情況。

Unlike F-PC 2.25 and earlier versions, F-PC 3.5 has its own Forth PATH
與 F-PC 2.25 及更早版本不同，F-PC 3.5 有自己的 Forth PATH
command and several directories to hold its files. This keeps the clutter
命令和幾個目錄來保存其文件。這樣可以保持混亂
down in the main FPC directory while keeping all the supporting files
向下，同時保留所有支援檔案
available when needed. F-PC's directory structure looks like this:
需要時可用。F-PC 的目錄結構如下所示：

```
C:\FPC --------- \SRC
           |---- \HLP
           |---- \TOOLS
           |---- \NEWZ
```

You can of course put F-PC on a drive other than C:, and in directories
當然，您可以將 F-PC 放在 C： 以外的磁碟機上，並放在目錄中
other than \FPC etc. but for this discussion we will assume you will be
除了 \FPC 等，但對於本次討論，我們將假設您將是
using the above directory structure.
使用上述目錄結構。

Create the above directory structure on your hard disk using the DOS
使用 DOS 在硬碟上建立上述目錄結構
"MKDIR" (make directory) command. Use PKUNZIP.EXE to "unzip" the .ZIP
“MKDIR”（製作目錄）命令。使用 PKUNZIP.EXE 「解壓縮」.ZIP
files from floppy into the directories as shown below:
檔案從軟碟放入目錄中，如下所示：


Directory .ZIP File
\FPC FPC.ZIP
\FPC\SRC FPCSRC.ZIP
\FPC\HLP FPCDOC.ZIP
FPCHLP.ZIP
\FPC\TOOLS SAMPLES.ZIP
\FPC\工具 SAMPLES.ZIP
SMITH.ZIP
CURLEY.ZIP
ZIMMER.ZIP
\FPC\NEWZ NEWZ.ZIP


A typical PKUNZIP command line looks like this:
典型的 PKUNZIP 命令列如下所示：

C:> PKUNZIP A:FPC C:\FPC <Enter>
C：> PKUNZIP A：FPC C：\FPC <Enter>

When you have finished the above, copy the following files from floppy to
完成上述操作後，將以下文件從軟盤複製到
the "\FPC" directory:
“\FPC” 目錄：
README FLOPPY.TXT INSTALL.TXT INSTALL.EXE
自述文件 FLOPPY.TXT INSTALL.TXT INSTALL.EXE

This completes installation, and leads us into configuration.
這樣就完成了安裝，並引導我們進行配置。


## 2.4. CONFIGURE F-PC 2.4. 設定 F-PC

F-PC uses a configuration file to execute several default configuration
F-PC 使用設定檔來執行幾個預設配置
commands. The F-PC.CFG file is automatically loaded each time you start
命令。F-PC。每次啟動時，都會自動載入 CFG 檔案
F-PC from the DOS command line. Part of the installation process is
F-PC 來自 DOS 命令列。安裝過程的一部分是
creating a configuration file for your hardware environment. Since we are
為您的硬體環境建立組態檔。既然我們是
doing the installation manually, we need to create this configuration
手動進行安裝，我們需要建立此配置
file.
檔案。


At the end of the installation process, you are asked questions above
在安裝過程結束時，系統會問您上述問題
your hardware configuration and some software preferences. The
您的硬體配置和一些軟體偏好設定。這
INSTALL.EXE then generates a F-PC.CFG file, which is loaded by F.EXE when
然後 INSTALL.EXE 生成一個 F-PC。CFG 檔案，該檔案由 F.EXE 載入
you invoke F-PC. If you install the F-PC system yourself, you will still
您調用 F-PC。如果您自己安裝 F-PC 系統，您仍然會
have to create the F-PC.CFG file to let F-PC know the precise
必須創建 F-PC。CFG 檔案讓 F-PC 知道精確的
configuration you have. The easier way is to execute INSTALL.EXE again.
您擁有的組態。更簡單的方法是再次執行 INSTALL.EXE。
After the first question is displayed:
顯示第一個問題後：

Do you want to install F-PC on your hard disk, or
您想在硬碟上安裝 F-PC，還是
Configure a copy of F-PC already on your hard disk [I/C]? I
配置硬碟上已有的 F-PC 副本 [I/C]？我

Type C instead of I followed by a <return>. INSTALL.EXE will then bypass
輸入 C 而不是 I，後面跟著 <return>。然後 INSTALL.EXE 將繞過
the installation procedure and go directly to the configuration
安裝程序，直接進入配置
procedure. Answer the questions and the configuration file F-PC.CFG will
手續。回答問題和配置文件 F-PC。CFG 將
be created for you.
為你創造。

The following procedure will allow you to configure F-PC for your
以下過程將允許您為您的 F-PC
hardware without using INSTALL.EXE. It is however much easier to
硬體，無需使用 INSTALL.EXE。然而，這要容易得多
configure F-PC using the install program, so please use it if possible.
使用安裝程式配置 F-PC，因此請盡可能使用它。

Using your favorite text editor, place the following lines in a file
使用您最喜歡的文字編輯器，將下列行放入檔案中
named "F-PC.CFG". If you have F-PC.EXE on the hard disk, you can use the
名為“F-PC.CFG“。如果硬碟上有 F-PC.EXE，您可以使用
F-PC editor to create and edit this file.
F-PC 編輯器來建立和編輯此檔案。

```
FPATH C:\FPC;C:\FPC\SRC;C:\FPC\HLP;C:\FPC\TOOLS
FAST
COLORIZEON
BLANKOFF
' >COLOR IS INITCOLOR
BACKUPON
```

When creating F-PC.CFG, if you installed F-PC on a hard drive other than
創建 F-PC 時。CFG，如果您在硬碟上安裝了 F-PC
"C:", change each occurrence of "C:" following the FPATH command above to
“C：”，將上述 FPATH 命令後面出現的每次“C：”更改為
the drive letter you are using.
您正在使用的磁碟機代號。

The above words setup F-PC for a normal configuration. It will work even
上述文字將 F-PC 設置為正常配置。它甚至會起作用
if you have a monochrome system. The commands have the following meaning:
如果你有一個單色系統。這些命令具有下列意義：

FPATH C:\FPC;C:\FPC\SRC;C:\FPC\HLP;C:\FPC\TOOLS

The Forth PATH tells F-PC which directories to search
第四個 PATH 告訴 F-PC 要搜尋哪些目錄
when you open or load a file. You can include other
當您開啟或載入檔案時。您可以包含其他
directories as well up to a maximum of 132 characters.
目錄以及最多 132 個字符。

FAST Select direct video writes. The opposite option is "SLOW"
快速選擇直接視頻寫入。相反的選項是“慢”
DOS i/o.
DOS i/o。

COLORIZEON Use colors when displaying various Forth word
COLORIZEON 顯示各種 Forth 單字時使用顏色
classes. This is automatically disabled on Monochrome
類別。這在單色上會自動停用
systems. The opposite option is "COLORIZEOFF".
系統。相反的選項是“COLORIZEOFF”。

BLANKOFF Don't blank the screen when writing to the
BLANKOFF 寫入
display. If you have a CGA display you may want to use
獻。如果您有 CGA 顯示器，您可能需要使用
"BLANKON", all other displays use BLANKOFF.
“BLANKON”，所有其他顯示器都使用 BLANKOFF。

' >COLOR IS INITCOLOR Allows F-PC to support a color
' >COLOR IS INITCOLOR 允許 F-PC 支援一種顏色
monitor if one is available. Will support monochrome even
監控是否有可用。甚至會支持單色
with this command included.
包含此命令。

BACKUPON Keep a single backup file for each file edited. If you
BACKUPON 為每個編輯的檔案保留一個備份檔案。如果你
are very short on disk space, or are using F-PC on a
磁碟空間非常不足，或在
floppy system, you may want to use "BACKUPOFF".
軟盤系統，您可能需要使用“BACKUPOFF”。

For all the options or preferences that you might choose, consult Section
如需您可能選擇的所有選項或偏好設定，請參閱 區段
9.4. In the hypertext root screen, there is a 'Preference' link. You
9.4. 在超文本根畫面中，有一個「偏好設定」連結。你
can browse from there to look at all the options.
可以從那裡瀏覽以查看所有選項。

After the configuration file is saved to disk, issue the following
將設定檔儲存至磁碟之後，請發出下列
command from the DOS prompt while in the "\FPC" directory:
命令，同時在「\FPC」目錄中：

```
C:> F-PC - FSAVE F BYE <Enter>
```

This command will start F-PC, which automatically reads in the
此命令將啟動 F-PC，它會自動讀取
configuration file we just created. The "-" above signifies no other file
我們剛剛創建的配置文件。上面的「-」表示沒有其他檔案
is to be opened. The next two words "FSAVE F", save F-PC to disk with the
即將打開。接下來的兩個字「FSAVE F」，將 F-PC 儲存到磁碟，並使用
new name "F.EXE". You can of course use a name other than "F". "BYE"
新名稱“F.EXE”。當然，您可以使用“F”以外的名稱。“再見”
leaves F-PC and returns to DOS. This process creates a fully configured
離開 F-PC 並返回 DOS。此程式會建立完全設定的
copy of F-PC called F.EXE that contains all of the default configuration
名為 F.EXE 的 F-PC 副本，其中包含所有預設配置
parameters you specified.
您指定的參數。

Be sure to include the "C:\FPC" directory in your system PATH command in
請務必在系統 PATH 命令中包含「C：\FPC」目錄
AUTOEXEC.BAT.
AUTOEXEC.BAT。

After rebooting your computer, you can run F-PC from any drive and
重新啟動計算機後，您可以從任何驅動器運行 F-PC，並且
directory by typing "F <filename> <enter>", and Forth will be able to
目錄中<filename><enter>輸入“F”，Forth 將能夠
find its source files, help files, and tools from wherever you are.
無論您身在何處，都可以找到其源文件、幫助文件和工具。


## 2.5. INSTALL F-PC ON A DUAL FLOPPY SYSTEM 2.5.在雙軟盤系統上安裝 F-PC

If you are trying to install F-PC on a dual floppy system, then you will
如果您嘗試在雙軟盤系統上安裝 F-PC，那麼您將
encounter some problems. When you are asked what to install while in the
遇到一些問題。當系統詢問您在
installation program, you will only be able to install the program, not
安裝程序，您將只能安裝該程序，而不能
the sources, help, or other things onto a 360k floppy. Therefore respond
將來源、幫助或其他內容放到 360k 軟盤上。因此，請回應
"Y" to only the first question (program), and "N" to the following
“Y”僅表示第一個問題（程序），“N”表示後面的問題
questions. After installation of the program section completes, enter "
問題。程式部分安裝完成後，輸入”
A:;B: " for the Forth path question. Answer the rest of the configuration
一個：;B： “ 對於第四條路徑問題。回答其餘的設定
questions about your hardware as you see fit. The final question for the
有關您認為合適的硬件的問題。最後一個問題
name of Forth, must be set to "F-PC.EXE" which will overwrite the copy of
name of Forth，必須設定為「F-PC.EXE」，這會覆寫
F-PC.EXE that was just installed on the floppy, as there is no room for
F-PC.EXE 只是安裝在軟盤上，因為沒有空間
an additional copy called "F.EXE".
一個名為“F.EXE”的附加副本。

When you have finished running the installation program, delete the
當您執行完安裝程式時，請刪除
following files from the installed disk to free up some space for your
從已安裝的磁盤中關注文件，為您的
program files:
程式檔案：

```
INSTALL.EXE
EXTEND.BAT
EXTENDH.BAT
FMETA.BAT
PFMETA.BAT
KERNEL.COM
KERNEL.CFG
```

These files are not useful on a system that has no room to re-build F-PC
這些檔案在沒有空間重建 F-PC 的系統上沒有用處
anyway, so you might as well get rid of them as this will recover about
無論如何，你不妨擺脫它們，因為這會恢復大約
60k or so for you files.
60k 左右的文件。

You can run INSTALL.EXE again, and install the help files on a second
您可以再次執行 INSTALL.EXE，然後安裝說明檔案
floppy, but you will have to set your FPATH to include the other floppy
軟盤，但您必須將 FPATH 設置為包含另一張軟盤
drive, and the directory into which the install program placed the help
磁碟機，以及安裝程式放置說明的目錄
files. After this is done, they should be available by typing
檔案。完成此操作後，它們應該可以通過鍵入

BROWSE <wordname> <enter>

You will probably find F-PC fairly difficult to learn in this limited
您可能會發現 F-PC 在這個有限的遊戲中相當難以學習
hardware environment, but its the best we can do. Once you are familiar
硬體環境，但這是我們能做的最好的事情。一旦你熟悉了
with F-PC and do not need all the handholding, you will only need the
使用 F-PC 並且不需要所有的手持，您只需要
F-PC.EXE file on a floppy with your application files. As F.EXE occupies
F-PC.EXE 軟碟上的檔案與您的應用程式檔案一起。正如 F.EXE 佔據的那樣
150K bytes of disk space, there are plenty of rooms for you to write
150K 字節的磁盤空間，有充足的空間供你寫入
programs and try them on a single floppy disk.
程式並在單一軟碟上嘗試它們。

