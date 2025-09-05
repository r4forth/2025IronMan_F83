EPILOGUE
跋




HOW TO HANG F-PC WITHOUT A LONG ROPE
如何在沒有長繩的情況下懸掛 F-PC


Instead of the usual ending of a book, telling you how wonderful F-PC is
而不是一本書通常的結局，告訴你 F-PC 有多精彩
(it is) and that with it you will live happily ever after (you will), let
（確實如此），有了它，你就會從此幸福地生活（你會的），讓
us do something unusual. Let us talk about things that you can do to
我們做了一些不尋常的事情。讓我們談談您可以做的事情
crash this system. This has the advantage that we can use a positive
使這個系統崩潰。這樣做的好處是我們可以使用正數
tone, saying what you can do instead of warning you about things you
語氣，說你能做什麼，而不是警告你的事情
should not do. It will give you much more insight into F-PC and let you
不應該做。它將使您更深入地了解 F-PC，並讓您
taste the power you gain over the computer and the operating system.
品嚐您通過計算機和操作系統獲得的強大功能。


The question is: "How to hang your F-PC without a long rope?" Here is a
問題是：“如何在沒有長繩的情況下懸掛你的 F-PC？這是一個
short list to begin with. You will certainly find other ways to do it.
首先是簡短清單。你肯定會找到其他方法來做到這一點。
We welcome your input and suggestions to make this list complete.
我們歡迎您提出意見和建議，以完善此清單。


1. Use a short rope.
1. 使用短繩。


2. Type " -1 @ ". It will crash the AT system. However, AT can
2. 輸入“ -1 @ ”。它會使 AT 系統崩潰。然而，AT 可以
still be rebooted by Ctrl- Alt-Del. It does not affect PC or XT.
仍需由 Ctrl-Alt-Del 重新啟動。它不會影響 PC 或 XT。


3. Type " -1 ! ". It will crash the AT system for good. You will
3. 輸入“ -1 ！ ”。它將使 AT 系統永遠崩潰。你會
have to recycle power, if you don't have that hardware reset button on
如果您沒有打開硬件重置按鈕，則必須回收電源
your computer.
你的電腦。


4. Type " >R ". It works every time.
4. 輸入“ >R ”。它每次都有效。


5. Store anything into your dictionary in the Code Segment. You can
5. 將任何內容儲存到字典的程式碼區段中。你可以
use !, but that's not bold enough. Use ERASE, FILL, BLANK, or CMOVE.
使用！，但這還不夠大膽。使用 ERASE、FILL、BLANK 或 CMOVE。


6. Store anything into the DOS area below the Code Segment. It will
6. 將任何內容儲存到程式碼區段下方的 DOS 區域中。它會
probably not affect F- PC. However, wait until you say 'BYE'. Ms. DOS
可能不會影響 F-PC。但是，請等到您說“再見”。多斯女士
will lay the computer down flat.
將電腦平放。


7. Store anything into the dictionary in the Head Segment. F-PC
7. 將任何內容儲存到字典的「頭部」區段中。F-PC
will still say 'ok', but it will not recognized words you type in. You
仍會說“確定”，但它不會識別您輸入的單詞。你
will get the 'What?' message.
將收到“什麼？


8. Store anything into the dictionary in the List Segment.
8. 將任何內容儲存到「清單區段」的字典中。


9. Do a " 0 0 DO ... LOOP ". If you have anything useful in this
9. 做一個“0 0 DO ...循環“。如果你對此有什麼有用的東西
loop, F-PC will spend a long, long time doing it for you. You might just
循環，F-PC 會花很長很長的時間為你做這件事。你可能只是
as well assume the system crashed and do a reset. (You can do a warm
也假設系統崩潰並進行重置。（可以做一個暖
restart by pressing the Control-Break key.)
按 Control-Break 鍵重新啟動。


10. In a code definition, use any of the SI, DS, ES, SS and CS
10. 在代碼定義中，使用 SI、DS、ES、SS 和 CS 中的任何一個
registers and not restore it before NEXT.
註冊，而不是在 NEXT 之前還原它。


11. Do a " JMP " in assembler.
11. 在彙編器中做一個「JMP」。


12. Implement your own hardware interrupt.
12、實現自己的硬體中斷。


13. Do multi-tasking.
13. 同時處理多項任務。


14. Build a large loop without balancing the stacks inside the loop.
14. 建立一個大循環，而不平衡循環內部的堆疊。


15. Print a binary file on your printer. You may not totally crash
15. 在印表機上列印二進位檔案。你可能不會完全崩潰
the computer, but a bucketful of paper shooting through the printer at 10
電腦，但一桶紙在 10 點時穿過印表機
miles per hour is an impressive sight.
每小時英里是一個令人印象深刻的景象。


16. Do a " TYPE " without parameters. See 15.
16. 做一個沒有參數的「TYPE」。參見 15。


17. FORGET a part of the dictionary that contains a definition that
17. 忘記字典中包含定義的部分
has been DEFERred to. When you next execute the deferred word, the system
已被推遲到。當您下次執行延遲字時，系統會
will hang.
會掛起來。


18. FORGET a task in the round robin task chain. The system will
18. 忘記循環任務鏈中的任務。系統將
work for a while until new definitions creep into the place where the
工作一段時間，直到新的定義悄悄進入
forgotten task was defined.
已定義忘記的任務。


Now that you know how to crash F-PC, you may want to use it to do
現在您已經知道如何使 F-PC 崩潰，您可能想用它來做
something useful.
有用的東西。


THE KITCHEN SINK
廚房水槽


The last time we counted, F-PC contains 1800 regular words and 700
上次我們統計時，F-PC 包含 1800 個常規單詞和 700 個
headless words. It contains everything except the kitchen sink. Well,
無頭詞。它包含除了廚房水槽之外的所有東西。井
such omission is certainly not to be tolerated. So, let us throw in the
這種遺漏當然是不能容忍的。那麼，讓我們把
kitchen sink as well to make it complete:
廚房水槽也使其完整：


: SINK ." A conduit to BBB, the great Big Bit Bucket." ;
：沉沒。通往 BBB（偉大的 Big Bit Bucket）的管道。
: KITCHEN ." See SINK" ;
：廚房。參見 SINK“;
' KITCHEN ALIAS KITCHEN-SINK
' 廚房別名 KITCHEN-SINK


These words only cost us 100 bytes in memory with absolutely no run-time
這些詞只消耗了我們 100 位元組的記憶體，而且絕對沒有運行時間
penalty. That is a very small price to pay for the potential claim of
刑罰。對於潛在的索賠來說，這是一個非常小的代價
system closure. A petition will be sent forward to the ANS Forth
系統關閉。請願書將被轉發給 ANS Forth
Standards Committee to include them in the coming Forth standard.
標準委員會將它們納入即將到來的 Forth 標準中。


This joke was attributed to Allen Furman, the resident philosopher at the
這個笑話出自艾倫·弗曼 （Allen Furman） 之手，他是
Silicon Valley FIG Chapter.
矽谷圖章節。


AN INVITATION
邀請函


Before parting, let us remind you that F-PC is an open system and
臨別前，讓我們提醒您，F-PC 是一個開放的系統，
contributions from users like you are always welcome. We think F-PC will
我們隨時歡迎像您這樣的用戶做出貢獻。我們認為 F-PC 會
be a very useful vehicle for the MS-DOS segment of the Forth community to
成為 Forth 社區的 MS-DOS 部分非常有用的工具，以
exchange ideas and code, for as long as there are still PC/XT/AT
交流想法和程式碼，只要還有 PC/XT/AT
computers and their clones. Join the Forth Interest Group local chapter
計算機及其克隆。加入 Forth Interest Group 當地分會
nearest you because there you will most likely find some people
離你最近，因為在那裡你很可能會找到一些人
knowledgeable about F-PC. You can ask for the address and phone number
了解 F-PC。您可以詢問地址和電話號碼
of the local chapters from the FIG central office, (408) 277-0668. FIG
FIG 中央辦公室的地方分會，（408） 277-0668。無花果
also sponsors a Forth Roundtable on the GEnie Network. There are very
還贊助了 GEnie Network 上的第四次圓桌會議。有非常
active discussions on F-PC on-line. Dr. Jack Brown is running an on-line
在線對 F-PC 的積極討論。傑克·布朗博士正在經營一個在線
F-PC tutorial. Sysops of the Forth Roundtable are very helpful on
F-PC 教學。第四次圓桌會議的管理員非常有幫助
technical problems. Here we include a list of local FIG chapters and a
技術問題。在這裡，我們包括本地 FIG 章節列表和
list of the on-line resources, in case you want to find help in a chapter
在線資源列表，以防您想在某一章中找到幫助
near you or through on-line services.
就近或透過線上服務。



FORTH INTEREST GROUP
第四興趣小組
LOCAL CHAPTERS
地方分會


U.S.A.
美國


ALABAMA
阿拉巴馬州
Huntsville Chapter
亨茨維爾分會
Tom Konantz
湯姆·科南茨
(205) 881-6483


ALASKA
阿拉斯加
Kodiak Area Chapter
科迪亞克地區分會
Ric Shepard
里克·謝潑德
Box 1344
盒子 1344
Kodiak, Alaska 99615
阿拉斯加科迪亞克 99615


ARIZONA
亞利桑那州
Phoenix Chapter
鳳凰章
4th Thurs., 7:30 p.m.
第四個星期四，晚上 7：30
AZ State University
亞利桑那州立大學
Memorial Union, 2nd floor
紀念聯盟，二樓
Dennis L. Wilson
丹尼斯·威爾遜
(602) 956-7578


ARKANSAS
阿肯色州
Central Arkansas Chapter
阿肯色州中部分會
Little Rock
小石城
2nd Sat., 2 p.m. &
第二個星期六，下午 2 點 &
4th Wed., 7 p.m.
第四週三，晚上 7 點
Jungkind Photo, 12th & Main
榮金德照片，12 號和主
Gary Smith (501) 227-7817
加里·史密斯 （501） 227-7817


CALIFORNIA
加利福尼亞
Los Angeles Chapter
洛杉磯分會
4th Sat., 10 a.m.
第四個星期六，上午 10 點
Hawthome Public Library
霍托姆公共圖書館
12700 S. Grevillea Ave.
南格雷維利亞大道 12700 號
Phillip Wasson
菲利普·沃森
(213) 649-1428


North Bay Chapter
北灣分會
2nd Sat., 10 a.m. Forth, AI
第二個星期六，上午 10 點第四，人工智慧
12 Noon Tutorial, 1 p.m. Forth
中午 12 點教程，下午 1 點第四
South Berkeley Public Library
南伯克利公共圖書館
George Shaw (415) 276-5953
喬治·肖 （415） 276-5953


Orange County Chapter
橙縣分會
4th Wed., 7 p.m.
第四週三，晚上 7 點
Fullerton Savings
富麗敦儲蓄
Huntington Beach
亨廷頓海灘
Noshir Jesung (714) 842-3032
諾希爾·傑松 （714） 842-3032


Sacramento Chapter
薩克拉門托分會
4th Wed., 7 p.m.
第四週三，晚上 7 點
1708-59th St., Room A
1708-59th St.，A 室
Tom Ghormley
湯姆·戈姆利
(916) 444-7775


San Diego Chapter
聖地牙哥分會
Thursdays, 12 Noon
週四，中午 12 點
Guy Kelly (619) 454-1307
蓋伊·凱利 （619） 454-1307


Silicon Valley Chapter
矽谷分會
4th Sat., 10 a.m.
第四個星期六，上午 10 點
H-P Cupertino
H-P 庫比蒂諾
Bob Barr (408) 435-1616
鮑勃·巴爾 （408） 435-1616


Stockton Chapter
斯托克頓分會
Doug Dillon (209) 931-2448
道格·狄龍 （209） 931-2448


COLORADO
科羅拉多州
Denver Chapter
丹佛分會
1st Mon., 7 p.m.
第一個星期一，晚上 7 點
Clifford King (303) 693-3413
克利福德·金 （303） 693-3413


CONNECTICUT
康涅狄格州
Central Connecticut Chapter
康涅狄格州中部分會
Charles Krajewski
查爾斯·克拉耶夫斯基
(203) 344-9996


FLORIDA
佛羅里達州
Orlando Chapter
奧蘭多分會
Every other Wed., 8 p.m.
每隔週三晚上 8 點
Herman B. Gibson
赫爾曼·吉布森
(305) 855-4790


Southeast Florida Chapter
佛羅里達州東南部分會
Coconut Grove Area
椰林區
John Forsberg (305) 252-0108
約翰·福斯伯格 （305） 252-0108


Tampa Bay Chapter
坦帕灣分會
1st Wed., 7:30 p.m.
第一個星期三，晚上 7：30
Terry McNay (813) 725-1245
特里·麥克奈 （813） 725-1245


GEORGIA
喬治亞
Atlanta Chapter
亞特蘭大分會
3rd Tues., 6:30 p.m.
第三個星期二，下午 6：30
Western Sizzlen, Doraville
西西茲倫，多拉維爾
Nick Hennenfent
尼克·亨南芬特
(4o4) 393-3010
（4o4） 393-3010


ILLINOIS
伊利諾伊州
Cache Forth Chapter
快取第四章
Oak Park
橡樹公園
Clyde W. Phillips, Jr.
小克萊德·菲利普斯
(312) 386-3147


Central Illinois Chapter
伊利諾伊州中部分會
Champaign
香檳
Robert Illyes (217) 359-6039
羅伯特·伊利斯 （217） 359-6039


INDIANA
印第安納州
Fort Wayne Chapter
韋恩堡分會
2nd Tues., 7 p.m.
第二個星期二，晚上 7 點
I/P Univ. Campus, B71 Neff
I/P 大學校園，B71 Neff
Hall
殿
Blair MacDermid
布萊爾·麥克德米德
(219) 749-2042


IOWA
愛荷華州
Central lowa FIG Chapter
中央 lowa fig 章節
1st Tues., 7:30 p.m.
第一個星期二，晚上 7：30
Iowa State Univ., 214 Comp.
愛荷華州立大學，214 Comp。
Sci.
科學。
Rodrick Eldridge
羅德里克·埃爾德里奇
(S15) 294-5659
（S15） 294-5659


Fairfleld FIG Chapter
費爾弗萊德無花果章節
4th Day, 8:15 p.m.
第四天，晚上 8：15
Gurdy Leete (515) 472-7077
古迪·利特 （515） 472-7077


MARYLAND
馬里蘭州
MDFIG
中無花果
Michael Nemeth
邁克爾·內梅斯
(301) 262-8140


MASSACHUSETTS
麻薩諸塞州
Boston Chapter
波士頓分會
3rd Wed., 7 p.m.
第三個星期三，晚上 7 點
Honeywell
霍尼韋爾
300 Concord, Billerica
300 康科德，比勒里卡
Gary Chanson (617) 527-7206
加里·香頌 （617） 527-7206


MICHIGAN
密西根州
Detroit/Ann Arbor Area
底特律/安娜堡地區
4th Thurs.
第四個星期四。
Tom Chrapkiewicz
湯姆·克拉普凱維奇
(3]3) 322-7862
Fred Olsen (612) 588-9532
弗雷德·奧爾森 （612） 588-9532


MINNESOTA
明尼蘇達州
MNFIG Chapter
MNFIG 章節
Minneapolis
明尼阿波利斯


MISSOURI
密蘇里州
Kansas City Chapter
堪薩斯城分會
4th Tues., 7 p.m.
第四個星期二，晚上 7 點
Midwest Research Institute
中西部研究所
MAG Conference Center
MAG 會議中心
Linus Orth (913) 236-9189
萊納斯·奧斯 （913） 236-9189


St. Louis Chapter
聖路易斯分會
1st Tues., 7 p.m.
第一個星期二，晚上 7 點
Thornhill Branch Library
桑希爾分館
Robert Washam
羅伯特·瓦沙姆
91 Weis Drive
韋斯大道 91 號
Ellisville, MO 63011
密蘇里州埃利斯維爾 63011


NEW JERSEY
新澤西州
New Jersey Chapter
新澤西州分會
Rutgcrs Univ., Piscataway
Rutgcrs Univ.，皮斯卡塔韋
Nicholas Lordi
尼古拉斯·洛迪
(201) 338-9363


NEW MEXICO
新墨西哥州
Albuquerque Chapter
阿爾伯克基分會
1st Thurs., 7:30 p.m.
第一個星期四，晚上 7：30
Physics & Astronomy Bldg.
物理與天文學大樓
Univ. Of New Mexico
大學新墨西哥州
Jon Bryan (505) 298-3292
喬恩·布萊恩 （505） 298-3292


NEW YORK
紐約
FlG, New York
FlG，紐約
2nd Wed., 7:45 p.m.
第二個星期三，晚上 7：45
Manhattan
曼哈頓
Ron Martinez. (212) 866-1157
羅恩·馬丁內斯。(212) 866-1157


Rochester Chapter
羅徹斯特分會
Odd month, 4th Sat., 1 p.m.
奇數月，第 4 個星期六，下午 1 點
Monroe Comm. College
門羅通訊學院
Bldg. 7, Rm.102
7號樓，102室
Frank Lanzafame
弗蘭克·蘭扎法姆
(716) 482-3398


OHIO
俄亥俄州
Cleveland Chapter
克利夫蘭分會
4th Tues., 7 p.m.
第四個星期二，晚上 7 點
Chagrin Falls Library
懊惱瀑布圖書館
Gary Bergstrom
加里·伯格斯特羅姆
(216) 247-2492


Columbus F1G Chapter
哥倫布 F1G 章節
4th Tues.
第四個星期二。
Kal-Kan Foods, Inc.
卡爾坎食品公司
5115 Fisher Road
費雪道5115號
Terry Webb
特里·韋伯
(614) 878-7241


Dayton Chapter
代頓分會
2nd Tues. & 4th Wed., 6:30 p.m.
第 2 個星期二和第 4 個星期三，下午 6：30
CFC. 11 W. Monument Ave.
氟氯化碳。西紀念碑大道 11 號
#612
Gary Ganger (513) 849-1483
加里·甘格 （513） 849-1483


OREGON
俄勒岡州
Wiliamette Valley Chapter
威廉梅特谷分會
4th Tues., 7 p.m.
第四個星期二，晚上 7 點
Linn Benton Comm. College
林恩·本頓通訊學院
Pann McCuaig (503) 752-5113
潘·麥奎格 （503） 752-5113


PENNSYLVANIA
賓夕法尼亞州
Villanova Univ. FIG. Chapter
維拉諾瓦大學 圖。章
Bryan Slueben
布萊恩·斯魯本
321-C Willowbrook Drive
321-C 柳溪大道
Jerfersonville, PA 19403
賓夕法尼亞州傑弗森維爾 19403
(215) 265-3832


TENNESSEE
田納西州
East Tennessee Chapter
東田納西州分會
Oak Ridge
橡樹嶺
2nd Tues., 7:30 p.m.
第二個星期二，晚上 7：30
Sci. Appl. Int'l. Corp., 8th Fl
國際應用科學應用。公司，第 8 樓
800 Oak Ridge Turnpike
800 橡樹嶺收費公路
Richard Secrist
理查德·塞克里斯特
(615) 483-7242


TEXAS
德克薩斯州
Austin Chapter
奧斯汀分會
Matt Lawrence
馬特·勞倫斯
PO Box 180409
郵政信箱180409
Austin, TX 78718
德克薩斯州奧斯汀 78718


Dallas Chapter
達拉斯分會
4th Thurs., 7:30 p.m.
第四個星期四，晚上 7：30
Texas Instruments
德州儀器 （TI）
13500 N. Central Expwy.
13500 北中央高速公路。
Semiconductor Cafeteria
半導體自助餐廳
Conference Room A
會議室 A
Clif Penn (214) 995-2361
克利夫·佩恩 （214） 995-2361


Houston Chapter
休斯頓分會
3rd Mon., 7:45 p.m.
第三個星期一，晚上 7：45
Intro Class 6:30 p.m.
介紹課下午 6：30
Univ. at St. Thomas
聖托馬斯大學
Russell Harris (713) 461-1618
拉塞爾·哈里斯 （713） 461-1618


VERMONT
佛蒙特州
Vermont Chapter
佛蒙特州分會
Vergennes
韋爾根
3rd Mon., 7:30 p.m.
第三個星期一，晚上 7：30
Vergennes Union High School
Vergennes 聯合高中
RM 210, Monkton Rd.
RM 210，蒙克頓路
Hal Clark (802) 453-4442
哈爾·克拉克 （802） 453-4442


VIRGINIA
維吉尼亞州
First Forth of Hampton
漢普頓第一福斯
Roads
道路
William Edmonds
威廉·埃德蒙茲
(804) 898-4099


Potomac FlG
波托馬克 FlG
D.C. & Northem Virginia
華盛頓特區和弗吉尼亞州諾瑟姆
1st Tues.
第一個星期二。
Lee Recreation Center
李康樂中心
5722 Lee Hwy., Arlington
5722 Lee Hwy.， 阿靈頓
Joseph Brown
約瑟夫·布朗
(703) 471-4409
E. Coast Forth Board
E. Coast Forth 董事會
(703) 442-8695


Richmond Forth Group
列治文福斯集團
2nd Wed., 7 p.m.
第二個星期三，晚上 7 點
154 Business School
154商學院
Univ. Of Richmond
大學里士滿
Donald A. Full
唐納德·富爾
(804) 739-3623


WISCONSIN
威斯康辛州
Lake Superior Chapter
蘇必利爾湖分會
2nd Fri., 7:30 p.m.
第二個星期五，晚上 7：30
1219 N. 21st St., Superior
1219 N. 21st St.， 蘇必利爾
Allen Anway (715) 394-4061
艾倫·安威 （715） 394-4061


INTERNATIONAL
國際


AUSTRALIA
澳洲
Melbourne Chapter
墨爾本分會
1st Fri., 8 p.m.
第一個星期五，晚上 8 點
Lance Collins
蘭斯·柯林斯
65 Martin Road
馬丁道65號
Glen Iris, Victoria 3146
格倫艾里斯，維多利亞 3146
03/29-2600
BBS: 61 3 299 1787
論壇：61 3 299 1787


Sydney Chapter
悉尼分會
2nd Fri., 7 p.m.
第二個星期五，晚上 7 點
John Goodsell Bldg., RM
約翰·古德塞爾大廈，RM
LG19
Univ. Of New South Wales
大學新南威爾士州
Peter Tregeagle
彼得·特雷格爾
10 Binda Rd., Yowie Bay
10 Binda Rd.， 約伊灣
2228
02/524-7490


BELGIUM
比利時
Belgium Chapter
比利時分會
4th Wed., 8 p.m.
第四週三，晚上 8 點
Luk Van Loock
陸文祿克
Lariksdreff 20
拉里克斯德雷夫 20
2120 Schoten
2120 斯霍滕
03/658-6343


Southern Belgium Chapter
比利時南部分會
Jean-Marc Bertinchamps
讓-馬克·貝爾廷尚
Rue N. Monnom, 2
N. Monnom 街，2
B-6290 Nalinnes
B-6290 納林內斯
071/213858


CANADA
加拿大
BC FIG
BC 圖
Ist Thurs., 7:30 p.m.
週四晚上 7：30
BCIT, 3700 Willingdon Ave.
BCIT，威靈登大道 3700 號。
BBY, Rm. IA-324
BBY，IA-324 號
Jack W. Brown (604) 596-9764
傑克·布朗 （604） 596-9764
BBS (604) 434-5886
論壇 （604） 434-5886


Northern Alberta Chapter
北艾伯塔省分會
4th Sat., lOa.m.-noon
第四個星期六，上午至中午
N. Alta. Inst. ol Tech.
北阿爾塔。學院。
Tony Van Muyden
托尼·範·穆登
(403) 486-6666 (days)
（403） 486-6666（天）
(403) 962-2203 (eves.)
（403） 962-2203（前夕）


Southern Ontario Chapter
安大略省南部分會
Quarterly, I st Sat., Mar., Jun.,
季刊，我星期六，三月，六月，
Sep., Dec., 2 p.m.
9 月、12 月，下午 2 點
Genl. Sci. Bldg., RM 212
Genl. Sci. 大樓，RM 212
McMaster University
麥克馬斯特大學
Dr. N. SoIntseff
N. SoIntseff 博士
(416) 525-9140 x3443
（416） 525-9140 轉 3443


Toronto Chapter
多倫多分會
John Clark Smith
約翰·克拉克·史密斯
PO Box 230, Station H
郵政信箱 230，H 站
Toronto, ON M4C 5J2
安大略省多倫多 M4C 5J2


ENGLAND
英格蘭
Forth Interest Group-UK
第四興趣小組-英國
London
倫敦
1st Thurs., 7 p.m.
第一個星期四，晚上 7 點
Polytechnic Of South Bank
南岸理工學院
RM 408
馬幣 408
Borough Rd.
博羅路
D.J. Neale
DJ 尼爾
58 Woodland Way
林地道 58 號
Morden, Surry SM4 4DS
莫登，薩里 SM4 4DS


FINLAND
芬蘭
FinFlG
金融金融
Janne Kotiranta
珍妮·科蒂蘭塔
Arkkitehdinkatu 38 c 39
33720 Tampere
33720 坦佩雷
+358-31-184246


HOLLAND
荷蘭
Holland Chapter
荷蘭分會
Vic Van de Zande
維克·範·德·贊德
Finmark 7
芬馬克 7
3831 JE Leusden
3831 傑·盧斯登


ITALY
意大利
FIG Italia
圖意大利
Marco Tausel
馬可·陶塞爾
Via Gerolamo Forni 48
通過 Gerolamo Forni 48
20161 Milano
20161 米蘭
02/435249


JAPAN
日本
Japan Chapter
日本分會
Toshi Inoue
井上俊
Dept. Or Mineral Dev. Eng.
系或礦物開發工程。
University of Tokyo
東京大學
7-3-1 Hongo, Bunkyo 113
7-3-1 本鄉、文京 113
812-2111 x7073


NORWAY
挪威
Bergen Chapter
卑爾根分會
Kjell Birger Faeraas,
凱爾·比爾格·法拉斯，
47-518-7784


REPUBLIC OF CHlNA
中國共和國
R.O.C. Chapter
中華民國分會
Chin-Fu Liu
劉展富
5F, #10, Alley 5, Lane 107
5 巷 #10,107 巷 5 樓
Fu-Hsin S. Rd., Sec. 1
福新南路第1段
Taipei, Taiwan, 10639
Taipei、台灣、10639


SWEDEN
瑞典
SweFIG
斯威圖
Per Alm
每額施捨
46/8-929631


SWITZERLAND
瑞士
Swiss Chapter
瑞士分會
Max Hugelshofer
馬克斯·休格爾斯霍弗
Industrieberatung
工業
Ziberstrasse 6
齊伯大街 6 號
8152 Opfikon
8152 奧菲康
01 810 9289


SPECIAL GROUPS
特殊團體
Forth Engine Users Group
第四個引擎使用者群組
John Carpenter
約翰·卡彭特
1698 Villa St.
1698 別墅街
Mountain View, CA 94041
加利福尼亞州山景城 94041
(415) 960-1256 (eves.)
（415） 960-1256 （前夕）



FORTH ON-LINE RESOURCES
第四個在線資源



To communicate with these systems, set your modem and communication
若要與這些系統通訊，請設定數據機和通訊
software to 300/1200/2400 baud with eight bits, no parity, and one stop
軟體達到 300/1200/2400 波特率，具有 8 位元、無奇偶校驗和一級
bit, unless noted otherwise. GEnie requires local echo.
位，除非另有說明。GEnie 需要本地回聲。


GEnie (For information, call 800-638-9636)
GEnie（如需信息，請致電 800-638-9636）


Forth RoundTable (ForthNet link*)
第四次圓桌會議（ForthNet 連結*）
Call GEnie local node, then type M710 or FORTH
呼叫 GEnie 本機節點，然後鍵入 M710 或 FORTH
SysOps: Dennis Ruffer (D.RUFFER), Scott Squires (S.W.SQUIRES),
系統運營人員：丹尼斯·魯弗 （D.RUFFER）、斯科特·斯奎爾斯 （SW 先生）、
Leonard Morgenstern (NMORGENSTERN), Gary Smith (GARY-S)
倫納德·摩根斯坦 （NMORGENSTERN）、加里·史密斯 （GARY-S）


MACH2 RoundTable
MACH2 圓桌會議
Type M450 or MACH2
M450 或 MACH2 型
Palo Alto Shipping Company
帕洛阿爾托航運公司
SysOp: Waymen Askey (D.MILEY)
管理員：Waymen Askey （D.MILEY）


BIX (ByteNet)
BIX（字節網）


For information, call 800-227-2983
如需信息，請致電 800-227-2983


Forth Conference Access BIX via TymeNet, then type j forth Type FORTH at
通過 TymeNet 訪問 BIX 的 Forth 會議，然後鍵入 j 第四個 Type FORTH at
the: prompt SysOp: Phil Wasson (PWASSON)
the： 提示系統運營：Phil Wasson （PWASSON）


LMI Conference
LMI 會議
Type LMI at the: prompt
在以下位置鍵入 LMI：提示符
Laboratory Microsystems products
實驗室微系統產品
Host: Ray Duncan (RDUNCAN)
主持人：雷·鄧肯 （RDUNCAN）


CompuServe
CompuServe（康普服務）


For information, call 800-848-8990
如需信息，請致電 800-848-8990


Creative Solutions Conference
創意解決方案會議
Type !Go FORTH SysOps: Don Colburn, Zach Zachariah, Ward McFarland, Jon
型！Go FORTH 系統運營：Don Colburn、Zach Zachariah、Ward McFarland、Jon
Bryan, Greg Guerin, John Baxter, John Jeppson
布萊恩、格雷格·蓋林、約翰·巴克斯特、約翰·傑普森


Computer Language Magazine Conference
電腦語言雜誌大會
Type !Go CLM SysOps: Jim Kyle, Jeff Brenton, Chip Rabinowitz, Regina
型！Go CLM 系統運營：Jim Kyle、Jeff Brenton、Chip Rabinowitz、Regina
Starr Ridley
斯塔爾·雷德利


Unix BBS's with Forth conferences (ForthNet links*)
Unix BBS 與 Forth 會議（ForthNet 鏈接*）


WELL Forth conference
WELL Forth 會議
Access WELL via CompuserveNet or 415-332-6106
通過 CompuserveNet 或 415-332-6106 訪問 WELL
Fairwitness: Jack Woehr (jax)
公平證人：傑克·沃爾（賈克斯）


Wetware Forth conference
Wetware Forth 會議
415-753-5265
Fairwitness: Gary Smith (gars)
公平證人：加里·史密斯（gars）


PC Board BBS's devoted to Forth (ForthNet links*)
PC Board BBS 致力於 Forth （ForthNet 連結*）


East Coast Forth Board
東海岸福斯委員會
703-442-8695
SysOp: Jerry Schifrin
管理員管理員： Jerry Schifrin


British Columbia Forth Board
不列顛哥倫比亞省第四委員會
604-434-5886
SysOp: Jack Brown
管理員：Jack Brown


Real-Time Control Forth Board
即時控制前板
303-278-0364
SysOp: Jack Woehr
管理員 Op： Jack Woehr


Other Forth-specific BBS's
其他 Forth 特定的 BBS


Laboratory Microsystems, Inc.
實驗室微系統公司
213-306-3530
SysOp: Ron Braithwaite
管理員： Ron Braithwaite


This list was accurate as of March 1989. If you know another on-line
截至 1989 年 3 月，該列表是準確的。如果您認識另一個在線
Forth resource, please let me know so it can be included in this list. I
第四個資源，請告訴我，以便將其包含在此列表中。我
can be reached in the following ways:
可以通過以下方式到達：


Gary Smith
加里·史密斯
P. 0. Drawer 7680
第 0 頁。抽屜 7680
Little Rock, Arkansas 72217
阿肯色州小石城 72217
Telcphonc: 501-227-7817
電話：501-227-7817
Fax: 501-228-0271
傳真：501-228-0271
Telcx: 6501165247 (storc and forward)
Telcx：6501165247（storc 和轉發）
GEnie (co-SysOp, Forth RoundTable): GARY-S
GEnie（第四次圓桌會議聯合管理員）：GARY-S
BIX (Bytenct): GARYS
BIX（Bytenct）：加里斯
Delphi: GARY S
德爾福：加里·S
MCIMAIL: 116-5247
麥基郵箱：116-5247
CompuServe: 71066,707
佣金：71066,707
Wetware Diver, (Fairwitness, Forth Conference): gars
濕紙潛水員，（Fairwitness，第四次會議）：gars
Usenet domain.: gars@well.WCP or gars@ wct.WCP
Usenet 網域：gars@well。WCP 或 gars@ wct。WCP 的
Internet: welkgars@lll-winken.arpa
網址：welkgars@lll-winken.arpa
WELL: gars
嗯：雀鱝


*ForthNet is a virtual Forth network that links designated rnessage bases
*ForthNet 是一個連接指定 rnessage 基地的虛擬 Forth 網絡
in an attempt to provide greater inforrnation distribution to the users
試圖為用戶提供更大的信息分發
served. It is provided courtesy of the SysOps of its various Iinks.
服務。它是由其各種 Iinks 的 SysOps 提供的。

