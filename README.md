[資安新手入門手冊] Web Security 領航之路
==============================



這是一篇以 Web 網站安全為主，給資安新手學習的路徑指南，也可以作為資安社團的資訊安全入門的課程安排。也希望提供給零基礎學習資訊安全的夥伴們一點的系統化的教學。

其他系列文章
------

*   **第 10 屆 iT 邦幫忙鐵人賽：**[資訊安全大補帖](https://ithelp.ithome.com.tw/users/20108446/ironman/1980)
*   **第 12 屆 iT 邦幫忙鐵人賽：**[資安這條路─以自建漏洞環境學習資訊安全](https://ithelp.ithome.com.tw/users/20108446/ironman/3463)

前言
==

這幾年針對社團儲備幹部想了很多**_鬼點子_**，不過總覺得沒有太大的成效，這次公開分享給大家今年我想做的方法。這篇文章想要解決的事情，就是網路上的資源這麼多，該從哪裡下手，然後透過檢核點來看自己究竟有沒有扎實的學習到該學的事情，歡迎各位補充。

Note：2021.09.04 更新 [2021 SITCON 學生計算機年會](https://sitcon.org/2021/agenda/f9d32ce5-2f26-4df0-bd39-351bae36cdb1)

Web Security 領航之路

本身作為資安工程師與經營過資安社團，透過 Web Security 比較好上手的特性，希望可以藉由該議程讓許多資安社團作為新手入門資安的課程安排與參考，也歡迎對資安有興趣想入門的與會者了解有哪些資源可以利用，透過議程介紹的學習路徑與教學方法可以讓上手的速度更快減少狀況期，後段也會介紹進階課程（Windows AD、提權）的安排。



資安概論
====

了解駭客為什麼要攻擊企業或其他人的電腦，駭客是為了何者目的而進行攻擊，以下列舉關鍵字提供大家進行搜尋。

*   攻擊、檢測：資安檢測、弱點掃描、滲透測試、紅隊演練
*   防禦、偵測：資安鑑識、資安防禦、資安健診、資安規劃

推薦實戰：
-----

*   熟悉 Google 查詢的技巧，找到問題的關鍵字再進行搜尋

Linux 指令操作
==========

會在實戰當中運用很多 Command Line 指令，所以一些常見的指令要會。  
推薦：[鳥哥的Linux 私房菜](http://linux.vbird.org/)，當作工具書使用，也就是有需要用到再查即可。  
之前修過 Unix 課程，課堂中老師推薦的 [dywang 呆王老師](https://dywang.csie.cyut.edu.tw/)教材，這份教材我覺得是有架構性的教材，各位可參考使用：[Linux 系統](https://dywang.csie.cyut.edu.tw/dywang/rhcsaNote/) 、 [Linux 伺服器](https://dywang.csie.cyut.edu.tw/dywang/linuxserver/)。

舉凡，ls, cd , mv , cp, cat ,vim 的熟練度、如何使用 ssh 進行連線也該知道 nc 如何使用。

推薦實戰：
-----

*   熟悉虛擬機器軟體（ [VirtualBox](https://zh.wikipedia.org/wiki/VirtualBox)、[VMware](https://zh.wikipedia.org/wiki/VMware)）或 Docker
*   練習用虛擬機安裝作業系統 Ubuntu , Kali Linux 來練習指令
*   可以使用 Bash on Ubuntu on Windows 練習指令
*   使用 GCP 免費方案安裝 Ubuntu , Kali Linux 練習
*   了解實體主機與虛擬空間與虛擬主機的差別

線上資源：
-----

*   Linux 線上練習 jsLinux：[https://bellard.org/jslinux/](https://bellard.org/jslinux/)
*   Linux 線上練習 copy.sh：[https://copy.sh/v86/?profile=linux26](https://copy.sh/v86/?profile=linux26)
*   Linux 線上練習 webminal：[https://www.webminal.org/register/](https://www.webminal.org/register/)
*   Linux 線上練習 linuxcontainers：[https://linuxcontainers.org/lxd/try-it/](https://linuxcontainers.org/lxd/try-it/)
*   Linux WarGame：[https://overthewire.org/wargames/bandit/](https://overthewire.org/wargames/bandit/)

教學方法：
-----

設計 Linux 闖關活動，讓學員可以透過 Linux 指令去解題。

Git 指令操作
========

學習 Git 不僅可以在自己開發專案的時候做到版本控制，了解 add , commit , push , pull 基本 Git 指令，以及透過跟他人協作知道 branch 的使用，更可以自行撰寫一個小工具上傳在 github 或 gitlab 開源給他人使用。

推薦閱讀：[連猴子都能懂得 Git 入門指南](https://backlog.com/git-tutorial/tw/)、[為你自己學 Git](https://gitbook.tw/)。

推薦實戰：
-----

*   安裝 git 在自己的主機
*   使用 github-pages 架設自己個人網頁
*   在 github 跟他人合作專案

線上資源：
-----

*   git 練習場：[https://gitbook.tw/playground](https://gitbook.tw/playground)

教學方法：
-----

設計 git 使用情境，引導學員學習 git 。

網路概論
====

了解網路的運作方法對資安入門有一定的幫助，在 TCP\\IP 中常見的協定有哪些，而這些協定做了什麼事情，可以從了解我們在訪問網站究竟背後的運作原理有哪些，從封包跟 Request 與 Response 到 DNS 、Domain 是什麼，HTTP 的 Header 、Method、 Status code 到 HTTPS 摸清楚這些原理。

常見名詞： IP, PORT, TCP, UDP

推薦實戰：
-----

*   使用開發者工具查看封包內容
*   使用 curl 指令了解如何該指令的各參數
*   能簡單說明網路七大層

線上資源：
-----

*   HTTP 概論：[https://www.tutorialspoint.com/http/](https://www.tutorialspoint.com/http/)
*   HTTP 規範：[https://httpwg.org/specs/](https://httpwg.org/specs/)
*   HTTP 請求與回應練習：[https://httpbin.org/](https://httpbin.org/)
*   Lidemy HTTP Challenge：[https://lidemy-http-challenge.herokuapp.com/](https://lidemy-http-challenge.herokuapp.com/start)

教學方法：
-----

設計 HTTP 闖關遊戲，可針對 HTTP 、 封包、DNS 進行設計，初學者可先練習使用**開發者工具**，推薦 FireFox 瀏覽器，可「編輯並重新傳送封包」。再練習 curl 的使用方式。

WEB 網站基礎
========

以 Web 網站安全為基礎，就要了解網站的架構有哪些，所以可以從前端、後端、API 去深入了解他們之間的差別。

*   前端（HTML , CSS , Javascript ）：BOM vs DOM
*   後端程式語言（範疇太多這裡不列舉）
*   資料庫（MySQL ,PostgreSQL…)：資料庫查詢語言必學、雜湊 vs 加密
*   伺服器軟體（Apache HTTP Server 、Microsoft IIS 、 Nginx）
*   常見名詞：Session, Cookie, [同源政策(Same-origin policy)](https://developer.mozilla.org/zh-TW/docs/Web/Security/Same-origin_policy), [跨來源資源共用（CORS）](https://developer.mozilla.org/zh-TW/docs/Web/HTTP/CORS), Cache , 框架 , 函式庫, DOM, URL 編碼

推薦實戰：
-----

*   學習寫一個網站（不管後端用什麼程式語言）
*   學習操作資料庫（Select、Insert、Delete 、 Update）
*   了解開發網站的流程

線上資源：
-----

*   練習操作資料庫：[https://sqlbolt.com/](https://sqlbolt.com/)
*   Web 入門：[https://developer.mozilla.org/zh-TW/docs/Learn/Getting\_started\_with\_the\_web](https://developer.mozilla.org/zh-TW/docs/Learn/Getting_started_with_the_web)

教學方法：
-----

可帶領學員熟悉任一後端程式語言，並由程式語言製作網站，可使用網站框架建立網架的架構，也可透過原生 PHP 了解後端程式語言的特性。

Web 網站安全漏洞/弱點
=============

常見的網站安全漏洞，以 OWASP TOP 10 為例，可先認識 OWASP TOP 10 的內容，了解弱點的漏洞原理、駭客利用手法、修補方式。

*   OWASP TOP 10
*   常見注入型弱點： XSS、 SQL injection 、Command injection、Code injection (Local File Inclusion）
*   Session 相關弱點：Session 劫持、Session 固定
*   前端相關弱點：CSRF、點擊劫持、DOM base、
*   進階弱點：SSRF、XXE、Insecure Deserialization、WebSockets

線上資源：
-----

*   WarGame 始祖：[https://www.hackthissite.org/](https://www.hackthissite.org/)
*   高手過招：[https://www.csie.ntu.edu.tw/~b94102/game/game.htm](https://www.csie.ntu.edu.tw/~b94102/game/game.htm)
*   Web WarGame：[https://overthewire.org/wargames/natas/](https://overthewire.org/wargames/natas/)
*   Web Security Academy：[https://portswigger.net/web-security](https://portswigger.net/web-security)
*   PentesterLab Bootcamp：[https://www.pentesterlab.com/bootcamp](https://www.pentesterlab.com/bootcamp)
*   漏洞動畫：[https://www.hacksplaining.com/owasp](https://www.hacksplaining.com/owasp)

教學方法：
-----

每一個漏洞深入探討原理與漏洞應用，並透過演練讓學員更了解原理。

常見的漏洞例子
=======

我們可以透過 HITCON ZeroDay 看台灣網站常見的漏洞有哪些，也可以透過自己的能力試著回報漏洞。或是透過 Bug Bounty Programs 去檢測上面可以合法檢測的目標，並獲得雄厚的獎金。

*   [HITCON ZeroDay](https://zeroday.hitcon.org/)
*   [Hackerone Bug Bounty Programs](https://hackerone.com/bug-bounty-programs)

寫在以下的進階技術之前的線上練習平台：
===================

*   Hack the Box：[https://www.hackthebox.eu/](https://www.hackthebox.eu/)
*   Vulnhub：[https://www.vulnhub.com/](https://www.vulnhub.com/)

Linux 提權
========

*   SUID/SGID 原理
*   常見的提權手法：sudo、cron job、history

線上資源：
-----

*   PayloadsAllTheThing：[Linux — Privilege Escalation](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Linux%20-%20Privilege%20Escalation.md)
*   Hacktricks：[Linux Privilege Escalation](https://book.hacktricks.xyz/linux-unix/privilege-escalation)

Windows 基礎
==========

學習 Windows AD 之前，要先了解 Windows 的基礎知識。

*   了解 Windows 作業系統
*   Windows 歷史
*   Windows 介面
*   Windows File System，如：New Technology File System(NTFS)
*   Windows 資料夾(`%windir%`)與 System32 資料夾
*   使用者帳號、設定與權限 `lusrmgr.msc`

Windows AD
==========

*   為什麼企業要使用 AD
*   Domain Controllers
*   Forests：AD 的架構
*   Trees：AD 使用的層次結構
*   Domains：針對使用者、群組進行管理
*   Object：Users、Groups
*   Trusts：允許使用者在 domain 底下有權限瀏覽資源
*   Domain Services：DNS 伺服器、LLMNR、IPv6

滲透測試實踐
======

了解滲透測試跟弱點掃描的差別，深度了解滲透測試的流程與報告寫法。

推薦實戰：
-----

*   收集 Recon
*   弱點利用
*   提升權限
*   後滲透
*   整理與報告
*   後期追蹤

線上資源：
-----

*   Web Security Testing Guide：[https://github.com/OWASP/wstg](https://github.com/OWASP/wstg)

SITCON Q&A TIME
===============

Q&A：假如要學 pwn 題目相關的知識，有推薦學習的網站或是 wargame

*   [https://github.com/HexRabbit/pwnable101](https://github.com/HexRabbit/pwnable101)
*   [https://pwn.college/](https://pwn.college/)
*   [https://malwareunicorn.org/workshops/re101.html#0](https://malwareunicorn.org/workshops/re101.html#0)
*   [https://github.com/vavkamil/awesome-vulnerable-apps](https://github.com/vavkamil/awesome-vulnerable-apps)

Q&A：社團社課靶機應該要設計成題目的方式，還是全弱點的網站

*   初學者：題目式，透過題目設計讓新手有成就感。
*   有基礎：設計全弱點網站，課程中帶滲透測試思維。
*   進階者：限定時間內完成指定靶機，並撰寫滲透測試流程。

