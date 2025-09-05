# F-PC USER'S MANUAL  F-PC 用戶手冊

F-PC Version 3.5, November 1989     
F-PC 3.5 版，1989 年 11 月



F-PC is a public domain Forth system optimized for IBM-PC/XT/AT type of
F-PC 是針對 IBM-PC/XT/AT 類型最佳化的公有領域 Forth 系統
computers under MS-DOS operating system. It is supplied on a set of four
MS-DOS 作業系統下的電腦。它以四件套的形式提供
diskettes with all the source code and documentation. Files are all
包含所有原始程式碼和文件的軟碟。檔案都是
compressed in the .ARC format. The diskettes are not copy-protected and
壓縮在 .ARC 格式。軟碟不受版權保護，且
the users are free to make backup copies and give copies to others. The
用戶可以自由製作備份副本並將副本提供給其他人。這
only exception is that Dr. Robert L. Smith reserved the copyright on his
唯一的例外是 Robert L. Smith 博士保留其版權
software floating point package contained in the files SFLOAT.SEQ,
軟體浮點套件包含在檔案 SFLOAT 中。序列，
SFLOAT1.SEQ, SFLOAT2.SEQ, and SFLOAT3.SEQ. This package is made
SFLOAT1。SEQ，SFLOAT2。SEQ 和 SFLOAT3.SEQ。這個包裝是
available for unlimited personal, non-commercial use. If you want to
可用於無限制的個人、非商業用途。如果你想
include the whole or part of this package in your product for sell at a
將此套件的全部或部分包含在您的產品中，以便在
profit, you should obtain a license from Robert Smith.
利潤，您應該從羅伯特·史密斯那裡獲得許可證。


This Manual is also in the public domain and the copyright is forfeited.
本手冊也屬於公共領域，版權被沒收。
You are free to copy it and distribute it with the F-PC diskettes.
您可以自由複製它並與 F-PC 軟碟一起分發。
However, the companying F-PC Technical Reference Manual is copyrighted by
但是，該公司的 F-PC 技術參考手冊的版權歸
Dr. C. H. Ting.
丁陳漢蓀博士。


As F-PC is produced on volunteer efforts and donated to the public
由於 F-PC 是在志願者的努力下生產並捐贈給公眾的
domain, the authors and the F- PC Working Group declined to bear
域名，作者和 F-PC 工作組拒絕承擔
responsibility for any special, consequential or other damages on using
對使用過程中的任何特殊、後果性或其他損害的責任
F-PC system for any application, although every possible effort was made
F-PC 系統適用於任何應用程序，儘管已盡一切可能
to ensure its integrity for correct operation.
以確保其正確操作的完整性。


Authentic copies of F-PC diskettes, F-PC Technical Reference Manual and
F-PC 軟碟的正品副本、F-PC 技術參考手冊和
this F-PC User's Manual can be obtained from Offete Enterprises, Inc.
本 F-PC 用戶手冊可從 Offete Enterprises， Inc. 獲得。
The diskette set is $25.00, the Technical Reference Manual is $30.00, and
軟碟組售價 25.00 美元，《技術參考手冊》售價 30.00 美元，以及
this Manual is $20.00 plus handling and sales tax.
本手冊售價 20.00 美元，另加手續稅和銷售稅。


There are two versions of F-PC in circulation. Version 2.25 was released
F-PC 有兩個版本在流通。2.25 版本發布
in November 1988. All files were in the .ARC format. Version 3.5 is
1988 年 11 月。所有檔案都位於 .ARC 格式。3.5 版是
released in November 1989 and files are in the .ZIP format.
於 1989 年 11 月發布，文件為.ZIP 格式。





Offete Enterprises, Inc.
奧菲特企業公司
1306 South B Street
南 B 街 1306 號
San Mateo, CA 94402
加利福尼亞州聖馬刁 94402
Tel. (415) 574-8250
電話：（415） 574-8250


# PREFACE TO THE THIRD EDITION 第三版序言

F-PC has been circulated in the Forth community for more than a year now.
F-PC 已經在 Forth 社區流傳一年多了。
The user response is very positive as people need good tools to do
用戶反應非常積極，因為人們需要好的工具來做
productive work in the MS-DOS and IBM- PC/XT/AT environments. Text files
在 MS-DOS 和 IBM-PC/XT/AT 環境中進行生產性工作。文字檔
are used almost universally. F-PC fills these needs very nicely, with
幾乎被普遍使用。F-PC 很好地滿足了這些需求，包括
its rather powerful SED text editor, the capability to access all 640K
其相當強大的 SED 文本編輯器，能夠訪問所有 640K
bytes of memory, and the smooth interface to MS-DOS and the hardware
位元組內存，以及與 MS-DOS 和硬件的流暢接口
underneath. We have also seem very large applications built upon F-PC,
底。我們似乎也有基於 F-PC 構建的非常大的應用程序，
free from the 64K byte limitation.
不受 64K 位元組限制。


Although many people had made substantial contributions to F-PC, it is
儘管許多人對 F-PC 做出了重大貢獻，但它確實如此
still a product of a single person, Tom Zimmer. Tom is very prolific in
仍然是一個人的產物，湯姆·齊默。湯姆在
producing code. The most interesting thing about him is that he has a
產生程式碼。他最有趣的是，他有一個
very fluid and open mind about programming, and very receptive to other
對編程非常流暢和開放，並且非常樂於接受其他人
peoples ideas and techniques. People ask him questions on the phone,
人們的想法和技術。人們在電話裡問他問題，
complaining about some inadequacies in F-PC, and sending him programs and
抱怨 F-PC 的一些不足之處，並向他發送程序和
applications. He would say: "Hmmm. That's very interesting. Let me
應用。他會說：「嗯。這很有趣。讓我
think about it." The next day he would have some new features added to
想想看。第二天，他將添加一些新功能
F-PC, and the version number was automatically incremented.
F-PC，版本號會自動遞增。


This is the mindset which allows F-PC to grow and to include many
正是這種心態讓 F-PC 能夠成長並包容許多人
utilities useful for Forth programmer in their daily programming
對 Forth 程序員在日常編程中有用的實用程序
activity. An old Chinese proverb says:
活動。中國有句古老的諺語說：


The ocean is big because it does not refuse water from small streams;
海洋很大，因為它不拒絕來自小溪流的水;
Mount Tai is tall because it does not reject dirt and small pebbles.
泰山之所以高大，是因為它不排斥泥土和小鵝卵石。


F-PC thus becomes a great reservoir of tools and utilities that each of
因此，F-PC 成為工具和實用程序的重要寶庫，每個工具和實用程序
us can use to build applications and to further our understanding of
我們可以使用來構建應用程序並進一步了解
Forth.
第四。


On the other had, it is very difficult to document a changing system and
另一方面，很難記錄不斷變化的系統和
make the system useful for people near and far. It was a Herculean
使該系統對遠近的人有用。這是一個巨大的
struggle to hold down F-PC's version auto-incrementer. After I finished
努力按住 F-PC 的版本自動增量器。我吃完之後
the User's Manual and the Technical Reference Manual for Version 2.21, I
2.21 版的使用者手冊和技術參考手冊，i
was confronted by Version 2.25. Under great pressure, I agreed to update
面對的是 2.25 版本。在巨大的壓力下，我同意更新
the documents to 2.25, but under one condition: I would keep the 2.21
文件到 2.25，但有一個條件：我會保留 2.21
documents in ready reserve. In case 2.25 got changed again, I would go
文件已準備好。如果 2.25 再次被更改，我會去
back and supply 2.21 documentation only. For this reason, I had used
返回並提供 2.21 文檔。因此，我使用
F-PC 2.21 on all my computers, even after I started distribution F-PC
F-PC 2.21 在我所有的電腦上，即使在我開始分發 F-PC 之後也是如此
2.25 and its documentation to other people.
2.25 及其向其他人提供的文件。


In the late spring, 1989, Tom was ready to revise F-PC again, although
1989 年春末，湯姆準備再次修改 F-PC，儘管
our understanding was that no update would be considered before the
我們的理解是，在
August. However, there were a few serious bugs which needed to be fixed,
八月。但是，有一些嚴重的錯誤需要修復，
and many new features Tom just could not wait to install. In the end, we
以及許多新功能，湯姆迫不及待地想安裝。最後，我們
reached the compromise that F-PC was upgraded to Version 2.2501, with 01
達成妥協，F-PC 升級到 2.2501 版，01
in lower case, with only the bug-fixes. As for the new features, Tom
小寫，僅包含錯誤修復。至於新功能，湯姆
could do whatever he saw fit and distributed to whoever wanted it, but
可以做任何他認為合適的事情，並分發給任何想要的人，但是
not under the name F-PC. With that, Tom marched right off, changed the
不是以 F-PC 的名義。說完，湯姆立即走了，改變了
name to F-TZ, and turned on the version auto-incrementer.
name 設為 F-TZ，並開啟版本自動遞增器。


There were many significant improvements in F-TZ, like the browser which
F-TZ 有許多重大改進，例如瀏覽器
allows the user to browse source and help files inside the editor, the
允許使用者在編輯器內瀏覽來源和說明檔案，則
hypetext on-line documentation system, the new system installation
hypetext 在線文檔系統，新系統安裝
procedure, better help files on the kernel, improved mouse support, and
程序、更好的內核幫助文件、改進的鼠標支持，以及
other minor enhancements. In September, 1989, the F-PC Working Group was
其他小增強功能。1989 年 9 月，F-PC 工作組成立
reconvened in the Silicon Valley FIG Chapter to consider upgrading F-PC.
在矽谷 FIG 分會重新召開會議，考慮升級 F-PC。
The Group accepted F-TZ as the new version of F-PC, and I got the job to
集團接受 F-TZ 作為 F-PC 的新版本，我得到了這份工作
upgrade the documentation.
升級文件。


October 1989 C. H. Ting
1989 年 10 月 丁陳漢蓀


# PREFACE TO THE FIRST EDITION 第一版序言


A TRADITION OF PUBLIC DOMAIN FORTH
公共領域的傳統

Forth was invented by Charles Moore in the 1960's as he developed
Forth 是由 Charles Moore 在 1960 年代開發時發明的
specialized tools for various applications. It was formalized into a
適用於各種應用的專用工具。它被正式化為
programming language for telescope automation while Mr. Moore was with
摩爾先生在望遠鏡自動化期間的編程語言
the National Radio Astronomy Observatory. As this work was supported by
國家射電天文台。由於這項工作得到了
public funds, Forth was born as a public domain software package which
公共資金，Forth 誕生於一個公共領域軟件包，它
followed telescopes to many different countries. In 1972 Mr. Moore left
跟隨望遠鏡前往許多不同的國家。1972 年，摩爾先生離開
NRAO to form FORTH, Inc. in order to market Forth systems and services.
NRAO 將成立 FORTH， Inc.，以銷售 Forth 系統和服務。
Implementations developed in FORTH, Inc. were proprietary and their usage
在 FORTH， Inc. 中開發的實作是專有的，其使用方式是專有的
required license from FORTH, Inc. However, a copy of Forth for PDP-11
需要 FORTH， Inc. 的許可證。然而，PDP-11 的 Forth 副本
was released to DECUS, the DEC Users Group, which became the only readily
被發布給 DECUS，即 DEC 用戶組，該組成為唯一容易
available public domain Forth for many years.
多年來可用的公共領域 Forth。


Forth Interest Group was organized in 1978 to encourage the use of Forth
Forth Interest Group 成立於 1978 年，旨在鼓勵使用 Forth
on small personal computers, which gradually became available for
在小型個人電腦上，逐漸可用於
individual users. One major effort by Forth Interest Group was the
個人使用者。福斯興趣小組的一項主要努力是
formation of Forth Implementation Team lead by Bill Ragsdale to build
成立由 Bill Ragsdale 領導的 Forth 實施團隊，以建立
figForth and put it in the public domain for general distribution.
figForth 並將其置於公共領域以供一般分發。
Because figForth was implemented on many microprocessors based on a
因為 figForth 是在許多微處理器上實現的，基於
single model and released with complete source listings, it became the de
單一模型並發布完整的源列表，它成為 DE
facto standard of Forth on personal computers, eclipsing polyForth which
Forth 在個人電腦上的事實標準，使 polyForth 黯然失色，後者
was by then the main product from FORTH, Inc.
當時是 FORTH， Inc. 的主要產品。


The other major objective of Forth Interest Group was to establish a
福斯興趣小組的另一個主要目標是建立一個
standard definition of Forth as a programming language. Forth Standards
Forth 作為程式語言的標準定義。第四個標準
Team was organized in 1978. It took the Forth-77 Standard developed by
團隊成立於 1978 年。它採用了由
Forth users in Europe and produced Forth-78 Standard. It was very
歐洲用戶眾多，生產了 Forth-78 標準。這非常
unsatisfactory and was almost immediately reworked into the Forth-79
不令人滿意，幾乎立即被重新設計成 Forth-79
Standard which was accepted by Forth Interest Group for promotion.
標準，該標準被 Forth Interest Group 接受進行推廣。
However, Forth Interest Group also decided that it would not publish
不過，福斯興趣集團也決定不出版
implementations and only encouraged Forth vendors to provided
實施，僅鼓勵 Forth 供應商提供
implementations and support. The only major public domain Forth
實施和支援。唯一的主要公共領域 Forth
supporting Forth-79 Standard was MVP-Forth written by Glen Haydon and
支持 Forth-79 Standard 的是 MVP-Forth 由 Glen Haydon 編寫和
distributed by Mountain View Press.
由山景出版社發行。


Forth Standard Team continued the refinement of Forth language and
福斯標準團隊繼續對福斯語言進行細化，並
published the Forth-83 Standard in 1983. Again, Forth Interest Group
1983 年發布了 Forth-83 標準。再次，第四個興趣小組
supported and promoted it, but did not provided any implementation.
支持並推廣它，但沒有提供任何實施。
Henry Laxen and Mike Perry felt that the Standard could not spread
亨利·拉克森和邁克·佩里覺得《標準》無法傳播
without a faithful and useful implementation. They implemented a
沒有忠實和有用的實施。他們實施了
comprehensive model on 8080, 8086, and 68000 processors with fairly
8080、8086 和 68000 處理器上的綜合模型，具有相當
uniform and transparent interfaces to the CP/M and MS-DOS operating
與 CP/M 和 MS-DOS 操作的統一透明接口
systems. This public domain F83 model found wide acceptance, especially
系統。這種公共領域的 F83 模型得到了廣泛接受，尤其是
among IBM PC users after it was listed in the PC-SIG catalog.
在 IBM PC 用戶中，在它被列入 PC-SIG 目錄後。


From 1983 to 1988, personal computers have made significant progress in
從1983年到1988年，個人電腦在以下方面取得了顯著的進步
memory size and in disk space. The traditional minimalist's approach in
記憶體大小和磁碟空間。傳統極簡主義者的方法
the Forth operating system seems to be inadequate to stay abreast with
Forth 操作系統似乎不足以跟上步伐
the tools and facilities embedded in the current personal computers. It
當前個人電腦中嵌入的工具和設施。它
is necessary that Forth must communicate with the operating system in
是必要的，Forth 必須與
standard file formats, and it has to address memory outside of the 64K
標準文件格式，並且它必須在 64K 之外尋址內存
byte addressing space. These capabilities were included in many 68000
位元組定址空間。這些功能包含在許多 68000 中
Forth implementations, but not in the PC world due to the segmented
第四次實現，但由於分段
architecture and the handicapped operating system. F-PC is a collective
架構和殘障作業系統。F-PC 是一個集體
effort to provide PC users a highly optimized version of public domain
努力為 PC 用戶提供高度優化的公共領域版本
Forth addressing these problems. It allows the user a well integrated
第四解決這些問題。它允許用戶很好地集成
environment to develop and maintain large applications utilizing the
環境來開發和維護大型應用程式，以利用
memory and storage space generally available in a mid-range IBM PC/XT/AT
記憶體和儲存空間通常適用於中階 IBM PC/XT/AT
and its clones. It is released to public domain with complete source,
及其克隆。它以完整的來源發佈到公共領域，
following the spirit of figForth and F83, so that users will have the
遵循 figForth 和 F83 的精神，讓用戶擁有
freedom to tailor it to their specific applications and to build
自由地根據其特定應用進行定制並構建
commercial products from it.
商業產品。


F-PC is a greatly enhanced version of Forth derived from the F83 model
F-PC 是 Forth 從 F83 型號衍生而來的大幅增強版本
for the IBM-PC, XT, or AT developed by Tom Zimmer at Maxtor Corp. A
適用於 IBM-PC、XT 或 AT，由 Tom Zimmer 在 Maxtor Corp. 開發。一個
major stepping stone between F-PC and F83 was the F83Y system produced by
F-PC 和 F83 之間的主要墊腳石是由 F83Y 系統生產的
Wil Baden, who adopted J. D. Hooper's separated heads and many other
威爾·巴登 （Wil Baden），他收養了 JD Hooper 的分離頭像和許多其他頭顱
features like interpreted conditionals, full featured decompiler, etc.
解釋條件、全功能反編譯器等功能。
Many other people also contributed to it, including Robert L. Smith,
許多其他人也為此做出了貢獻，包括羅伯特·史密斯，
Charles Curley, and Jerry Modrow, but the major work was done by Tom
查爾斯·柯利和傑里·莫德羅，但主要工作是由湯姆完成的
Zimmer.
齊默。


In order to release this system for public usage, it is necessary to
為了發布該系統供公眾使用，有必要
provide better and more complete documentation on the system so that a
在系統上提供更好、更完整的文檔，以便
Forth programmer can pick it up and use the system productively on his
第四個程序員可以拿起它並在他的
own, without having to have access to Tom Zimmer for support and
擁有，無需向 Tom Zimmer 尋求支持和
consultation. A F-PC Working Group was organized to serve two very
會診。組織了一個 F-PC 工作組，為兩個非常
specific purposes: to do beta testing on the system to flush out as many
具體用途：在系統上進行 Beta 測試以清除盡可能多的
bugs as possible, and to provide user and system documentation so that
錯誤，並提供使用者和系統文件，以便
both application and system Forth programmers can use the system in
應用程式和系統 Forth 程式設計師都可以在
isolated (in the Forth sense) geographic locations.
孤立的（第四意義上的）地理位置。


The F-PC Working Group was very loosely organized in the Silicon Valley
F-PC 工作組在矽谷組織得非常鬆散
FIG (SVFIG) Chapter, during the chapter meeting at April 23, 1988. Many
圖 （SVFIG） 分會，在 1988 年 4 月 23 日的分會會議上。多
Chapter members participated and contributed to this effort. The Chapter
分會成員參與了這項工作並為這項工作做出了貢獻。章節
also permitted the Working Group to use the morning FORML sessions in May
還允許工作組在 5 月使用上午的 FORML 會議
and June to discuss and work on F-PC. Dr. C. H. Ting served as the focus
六月討論和研究 F-PC。丁志強博士擔任焦點
of this Group to coordinate the efforts in documentation. Bug reports,
協調文件編制工作。錯誤報告、
suggestions, and recommendation were collected and forwarded to Tom
建議和建議被收集並轉發給湯姆
Zimmer for consideration.
齊默考慮。


This Manual is part of the documentation to be made available with the
本手冊是隨
F-PC system. It provides information on how to install F-PC, and the
F-PC 系統。它提供有關如何安裝 F-PC 的信息，以及
most useful utilities for normal programming activity. It also assumes
對正常程式設計活動最有用的實用程式。它還假設
that the user is familiar with Forth and DOS, and does not try to include
用戶熟悉 Forth 和 DOS，並且不嘗試包含
introduction materials. As F-PC retains the look-and-feel of F83, prior
介紹材料。由於 F-PC 保留了 F83 的外觀和感覺，因此之前
knowledge on F83 will be extremely helpful. The background information
有關 F83 的知識將非常有幫助。背景資訊
can be obtained from the following sources:
可從以下來源取得：


Starting Forth, Leo Brodie, Prentice Hall.
從 Leo Brodie 開始，Prentice Hall。
Programmer's Guide to the IBM-PC, Peter Norton, MicroSoft Press.
IBM-PC 程序員指南，Peter Norton，MicroSoft Press。
Inside F83, C. H. Ting, Offete Enterprises.
F83 內部，CH Ting，Offete Enterprises。


We hope that you will find F-PC valuable as you try to make the best use
我們希望您在嘗試充分利用 F-PC 時會發現 F-PC 很有價值
of the resources in your PC or compatible computer. We would also like
您的 PC 或相容電腦中的資源。我們也想要
to know if you succeeded in using it to develop real and interesting
要知道你是否成功地利用它來開發真實有趣的內容
applications. The User Contributions section of F-PC will always be open
應用。F-PC 的用戶貢獻部分將始終打開
to new submissions. We hope that F-PC will provide a common format for
到新的提交。我們希望 F-PC 能夠提供一種通用的格式
users to exchange code, ideas, and applications, the same way F83 has
用戶交換代碼、想法和應用程序，就像 F83 一樣
been over the last five years.
在過去的五年裡。


F-PC has evolved over the last six months. Tom Zimmer made substantial
F-PC 在過去六個月中不斷發展。湯姆·齊默 （Tom Zimmer） 製作了大量
modifications and enhancements to it. However, due to the pressure
對其進行修改和增強。然而，由於壓力
exerted on him by many users and members in this Working Group, Tom
這個工作組的許多用戶和成員對他施加了壓力，湯姆
reluctantly agreed to freeze F-PC at the current Version 2.25. It will
不情願地同意將 F-PC 凍結在當前的 2.25 版本。它會
not be modified until late next year so that users can start using it to
要到明年年底才能修改，以便用戶可以開始使用它
do applications. Both the User's Manual and the Technical Reference
做應用程序。用戶手冊和技術參考
Manual were updated to this version. Having accomplished its mission,
手冊已更新至此版本。完成使命後，
the F-PC Working Group ceases its existence. However, technical
F-PC 工作組不復存在。然而，技術
discussions on F- PC and a very extensive tutorial lead by Jack Brown
關於 F- PC 的討論和由 Jack Brown 領導的非常廣泛的教程
have appeared on the Forth Roundtable in the GEnie Network. F-PC users
出現在 GEnie Network 的第四次圓桌會議上。F-PC 用戶
are encouraged to join the Forth Roundtable for information, assistance,
鼓勵加入第四圓桌會議以獲取資訊、協助、
and possibly bug fixes.
以及可能的錯誤修復。


Dr. C. H. Ting
丁陳漢蓀博士
Documentation Coordinator
文件協調員
F-PC Working Group
F-PC 工作小組
December, 1988
1988 年 12 月
San Mateo, California
加利福尼亞州聖馬刁

```
CONTENTS

F-PC User's Manual                                                  i
Preface to the Third Edition                                        ii
Preface to the First Edition: A Tradition of Public Domain Forth    iii
1.   Introduction to F-PC                                           1
        1.   How did we get here?                                   1
        2.   F-PC, what is it all about                             3
        3.   Features in F-PC 2.25                                  4
        4.   New features in F-PC 3.5                               5
2.   Install F-PC                                                   6
        1.   The ZIP files                                          6
        2.   Install F-PC using INSTALL.EXE                         7
        3.   Install F-PC without using INSTALL.EXE                 8
        4.   Configure F-PC                                         9
        5.   Install F-PC on a dual floppy system                   10
3.   Hypertext Browser                                              12
        1.   Launch the hypertext browser                           12
        2.   Navigate F-PC with the browser                         13
        3.   A sample session                                       14
        4.   A short tutorial                                       15
4.   Programming Tools                                              18
        1.   DUMP                                                   18
        2.   The debugger                                           18
        3.   VALUES: Constants as variables                         20
        4.   Help words                                             20
        5.   Date and time                                          22
        6.   Comments                                               23
        7.   Screen control words in F-PC                           23
        8.   Compilation control words                              25
        9.   Printing source files in F-PC                          26
        10. Global search                                           26
        11. ALIAS                                                   27
        12. Browsing a large file                                   27
        13. The NEWZ editor                                         27
        14. The SZ editor                                           28
5.   SED, the Editor                                                30
        1.   Invoking SED editor                                    31
        2.   Using SED                                              32
        3.   Menu and mouse control                                 33
        4.   Function keys                                          34
        5.   Selecting another file to edit                         36
        6.   Search and replace                                     37
        7.   Cut, copy and paste                                    37
        8.   Line and word commands                                 38
        9.   Margin control                                         39
        10. Case conversion                                         39
        11. Line drawing                                            40
        12. Paragraph sorting                                       40
        13. Keystroke macros                                        40
        14. Print a file                                            41
        15. Other help                                              42
6.   Sequential Files                                               43
        1.   Sequential files in F-PC                               43
        2.   Handles                                                43
        3.   Sequential file word set                               45
        4.   Conversion between sequential file and block files     49
        5.   Programming style and sequential files                 50
7.   DOS Interface                                                  51
        1.   System interrupts and BIOS calls                       51
        2.   DOS service calls                                      52
        3.   The DOS shell                                          53
        4.   BATCH commands                                         54
        5.   DOS memory map of F-PC                                 54
        6.   Long memory word set                                   58
        7.   Memory allocation                                      59
8.   PASM, the F-PC Assembler                                       60
        1.   Prefix or postfix?                                     60
        2.   PASM glossary                                          61
        3.   Syntax comparison                                      63
        4.   Usage of 8086 machine registers in F-PC                63
        5.   Addressing modes                                       64
        6.   Assembly macros in PASM                                66
        7.   Local label                                            66
        8.   Inline code                                            67
        9.   Assembler style                                        69
        10. Debugging code words                                    70
IX.   Advanced Utilities                                            71
        1.   Rebuilding the system                                  71
        2.   Turnkey systems                                        72
        3.   Macros in F-PC and SED                                 72
        4.   F-PC preferences                                       72
        5.   Task chaining                                          74
        6.   Control structure enhancements                         75
        7.   Headless words                                         77
        8.   Save and restore                                       78
        9.   Line editor                                            79
10.   User Contributions                                            80
        1.   From Tom Zimmer                                        80
        2.   From Charles Curley                                    84
        3.   From Bob Smith                                         85
                HFLOAT/SFLOAT glossary                              87
Epilogue                                                            91
        How to Hang F-PC without a Long Rope                        91
        The kitchen sink                                            92
        An invitation                                               92
        Forth Interest Group local chapters                         93
        Forth on-line resources                                     96
Appendix A.     Glossary of the Forth Vocabulary                    A-1
        A1.   Introduction                                          A-1
        A2.   F-PC word glossary by category                        A-2
        A3.   F-PC alphabetic glossary                              A-12
Appendix B.     Samples and Tutorial Files                          B-1
        B1.   Memory allocation                                     B-1
        B2.   User boot process                                     B-2
        B3.   F-PC keystroke macros                                 B-3
        B4.   A sample menu file                                    B-6
        B5.   My startup message                                    B-7
        B6.   Subscreen scroll                                      B-8
        B7.   Usage of values                                       B-8
        B8.   Popup window                                          B-9
Appendix C.   Files in F-PC                                         C-1
        C1.   Files on the distribution disks                       C-1
        C2.   Zipped files on Disk 1                                C-2
        C3.   Zipped files on Disk 2                                C-3
        C4.   Zipped files on Disk 3                                C-5
Appendix D.     Index                                               D-1
Figures
        Figure  6.1.    The file handle                             44
        Figure  7.1.    The memory segments in F-PC                 56
        Figure  7.2.    Data structure in a colon definition        57
        Figure  8.1.    Comparison of assembly syntax               62
        Figure  8.2.    Examples of local labels                    68
```

F-PC USER'S MANUAL
THIRD EDITION FOR VERSION 3.5

NOVEMBER 1989

Offete Enterprises, Inc.

1306 South B Street
San Mateo, CA 94402
Tel. (415) 574-8250

