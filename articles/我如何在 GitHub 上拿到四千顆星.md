
_（作者同意轉載）_

_原文刊登於：https://www.ptt.cc/bbs/Soft_Job/M.1467888742.A.259.html_

我如何在 GitHub 上拿到四千顆星
===

兩個月前我在 GitHub 發表了一個開源專案，發表後一夕爆紅，在一開始的 24 小時內就
得到 1200+ 顆星，目前已累積 4000+ 顆星。這個專案名叫 HTTP Prompt，網址是：

https://github.com/eliangcs/http-prompt

我想在這裡分享一下它的開發故事。

這一切要先從 Vertica 講起。沒多久前我的工作幾乎每天都會使用 Vertica，Vertica
是一個強大的資料庫，但它官方的客戶端程式（vsql）一點都不強大。另一個 GUI 的選擇
DbVisualizer 也是難用到爆。

我就想起 PostgreSQL 那邊有一個叫 pgcli 的好物，我想如果 fork 它，應該不需要太大
功夫就能把它改成 Vertica 版本。最後也如我所想，沒花幾天就寫出了 vcli：

https://github.com/dbcli/vcli

我還聯絡了 pgcli 的原作者，告訴他「我用你的東西寫了另一個專案」，他很高興的幫我
在他網站上宣傳。但 Vertica 實在是小眾，所以 vcli 並沒有得到很多注意。但至少有了
 vcli，我終於能每天快快樂樂的使用 Vertica 了。

vcli、pgcli、mycli（for MySQL）其實都是建於一個叫 prompt-toolkit 的 Python 套件
之上。有了 prompt-toolkit 的加持，任何命令列程式因為有了自動完成和語法高亮，都
會變得超酷炫，去它的首頁看看有多少專案使用它就知道了：

https://github.com/jonathanslenders/python-prompt-toolkit

當時有一陣子工作常會需要連接 HTTP/REST API，這應該也是很多人工作的一部分，我相
信大部分人應該都是用 Postman 這類 GUI 工具，但身為一個什麼都要盡量用命令列介面
的 hacker，用 GUI 實在有點 low，而且跟 terminal 切換起來也不方便。所以我就選擇
使用類似 curl 的 HTTPie。使用 HTTPie 的缺點是常需要打很多重複的字，不像 Postman
會幫你記住之前的狀態，我想如果 HTTPie 或 curl 有互動模式就好了。我調查了一下，
原來早在一年前就有人這麼想了：

https://github.com/jkbrzt/httpie/issues/343

甚至在五年前就有人寫出我心目中理想的工具了：

https://github.com/chrislongo/HttpShell

但 HTTPie 實在設計得太完美讓我不想放棄它，而且 HttpShell 似乎也沒在更新，所以我
也就不考慮使用 HttpShell。

「任何命令列程式受了 prompt-toolkit 加持，都會變得超酷炫」，那我何不站在巨人肩
膀上，結合 HTTPie 和 prompt-toolkit，寫出一個有自動完成和語法高亮的 HTTP client
，不要求使用者放棄完美的 HTTPie，肯定有賣點。

於是我開始著手開發 HTTP Prompt，我還告訴我老婆，我這寫完至少會在 GitHub 拿一千
顆星星。我當時不是隨便推算的。因為 pgcli 都有四千多顆星了，用 HTTP 的人一定多過
PostgreSQL，所以如果我執行得好，吸引一千顆星星應該不是問題。

一開始卡最久是我想找出一個完美的寫法，使得自動完成、語法高亮、指令解析三大模組
能用一個統一的 context-free grammar（CFG）解決，但 prompt-toolkit 的作者告訴我
這個想法不切實際：

https://github.com/jonathanslenders/python-prompt-toolkit/issues/276

所以最終只有指令解析是以 CFG 實做，另兩個模組則分別土法煉鋼。CFG parser 一開始
也讓我有點頭痛，幸虧有人寫了一個現成的 parser：

https://github.com/erikrose/parsimonious

讀過 parsimonious 的程式碼，我只能說這套件的作者功力深厚，沒有編譯器或正規語言
的基礎還真寫不出這樣的東西。

prompt-toolkit 已解決大部分的難題，所以除了 CFG 之外就沒什麼特別困難的地方了。
我前後大概花了三個禮拜完成基本功能，即發佈到 Reddit/programming，沒多久就登上熱
門第一名：

https://www.reddit.com/r/programming/comments/4k1l2o

Reddit 廣告效益真的很強，HTTP Prompt 初期的流量都是靠 Reddit 吸引進來的。之後星
星數愈增愈快，幾乎是每一分鐘都就多一顆星，也成功登上 GitHub Trending 第一名，老
婆還幫我拍了一張照片做紀念：

![4zkkv98 - imgur](https://user-images.githubusercontent.com/2560096/28724802-9a2f87b4-73bb-11e7-8475-dad5ba1c4db6.jpg)

Issue 和 pull request 也跟著星星一起來，其中有不少不錯的功能建議，我也陸續加入
，在後面幾個版本釋出。

開發開源專案是很好玩的，當你知道很多人正在使用你寫的軟體、給你回饋，你會覺得你
在做一件有意義的事。希望這篇文章能鼓勵更多人使用 HTTP Prompt，也能幫助到一些想
參與開源專案的人，當然最好是可以貢獻到 HTTP Prompt :P。
