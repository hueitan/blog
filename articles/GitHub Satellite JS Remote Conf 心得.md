_原文刊登於：https://www.ptt.cc/bbs/Soft_Job/M.1589834001.A.2E1.html_

[心得] GitHub Satellite / JS Remote Conf 心得
===

**[COVID-19 a.k.a. 武漢病毒]**

資訊業紛紛都開始 WFH，期初很不習慣到後來完全已經變成日常，原本有機會到非洲歐洲泰國出差的機會因爲疫情全部取消了。陸續收到各種活動取消或改辦成線上的活動，有的乾脆直接免費開放，另有收費的都注明會把參加者的費用全數或者更多直接捐給 COVID-19 相關組織。

WFH 第一個月我感受到自己的墮落，時間變多好像不代表產能變多，反而是睡覺時間變多。第二個月的時候覺得不能再這樣下去，陸續看到了有興趣的線上活動，免費的就參加，要付費的就用公司個人發展經費參加。整理一下，分享參加 GitHub Satellite 2020 / JavaScript Remote Conf 2020 的心得，純屬個人立場，供大家參考

**[GitHub Satellite 2020]**

Microsoft + GitHub + npm 給整個 Open Source 社群來個重重的一擊，Microsoft 多年前決心要進入 Open Source 果然是要玩真的，投資不手軟。GitHub CEO 在開場的時候穿著 npm logo 的衣服，而不是自家的 logo，我認爲這是整個活動最精華的部分，其餘的可以加減看，畢竟很多段我覺得有點重叠，有些部分比較適合新手、非工程師或產品經理。

現場人數從 8k 慢慢降落到後來的 4k 3k， 深夜下半場我也離開去睡覺了。今年宣佈的内容主要著重在社群 (Communities)、程式編輯 (Code)、企業版本 (Enterprise) 和安全性 (Security)，想要瞭解細節的話可以去看 Discussions 順便嘗鮮這未來的新功能。也有一些像是標題殺的主題 ，換句話說就是，用我們的 Online Editor Tool 啦。整場沒有一字提到 Atom，心裡 OS：啊不過 VSCode 是從 Atom 衍生出來的，你們自己決定要用哪個啦，開源專案物競天擇很正常。

其中還有提到 GitHub Mobile App，個人期待了很久，但後來也習慣了 Mobile Web 的 UI，長期在 GitHub 網頁看 Code 後，突然要轉換成 App，説實在目前還不是很習慣這個流程。另外其中一段有提到 VSCode 的 Extension - GitHub Pull Request and Issues 實在不習慣，使用後因爲不放心還是要到網頁上確認自己到底有沒有執行成功。不然就是我這位老用戶不想接受改變，或者老人不想嘗試新技術。

至於安全性，有一位意大利的博後提到，產品隨著時間的更新就會有 Dependencies 安全性上的問題，決定是否更新還是維持現狀真的是一個大學問。 CodeQL Analysis、Code Scanning 等等的功能算是其中的賣點，當然 GitHub 也不可能自己搞完整一套，還是要靠社群 (partner) 來一起完整 Open Source 的安全。這裏我印象最深刻的是 GitHub 人提到 "GitHub can help" "GitHub code scanning can help" 。

GitHub 已經不像多年前只是用來上傳程式的 git 空間，現在已經是個巨人，上傳程式協作後續社群的功能，現在通通都能在平臺上完成。大家開發 Open Source 還是選擇 GitHub 為首選平台嗎？重播部分可以到 Youtube 看，不過我還是希望未來自己時間允許的情況下參加 live，參與感以及成就感上有大大的不同。

整場重點回顧可以到這裏看 https://github.blog/2020-05-06-new-from-satellite-2020-github-codespaces-github-discussions-securing-code-in-private-repositories-and-more/，讓人期待接下來 2021 GitHub 能繼續搬出什麽好東西！

**[JS Remote Conf 2020]**

我是在活動開始前兩個星期才認識此活動，還在深思這環繞 JS 各式主題的活動，沒想太多就先刷下去這連續三天的夜間場 75 美金。也因爲這個活動才第一次使用線上直播平臺 Crowdcast，大約 170 人參加。Crowdcast 其中一優點在於觀看重播時有記錄 Q&A 的時間點，缺點的話我認爲穩定度和使用者體驗。

果然逃離不開墨菲定律，第一位講者無法分享自己的簡報，這裏大概碰壁了五分鐘直到主持人分享畫面。講者是退役空軍飛行員的勵志開場，大家都在懷疑自己來錯場的時候主持人説明是要給大家一些有別於程式碼上的啓發，但我是沒抓到其中的精華啦。

由於主題太隨機了，所以我就把有印象的都記錄下來。來賓多數是經驗豐富的講者甚至講師，認真覺得口條都不錯不太會冷場。

其中有一場是關於 ECMAScript 和 TC39，這些大家都不太陌生，順路提到 ECMAScript 2020 新的及草稿中的標準，如 Decimal, Cancellation API, Slice Notation, Pattern Matching 等等，我個人是比較期待 Slice Notation，常常使用 slice / splice 都搞不清楚它那到底是 index 還是 count 的救星。當中還有人順便嘴一下 ?.，Ruby 用 &. 爲何不統一一下；ECMAScript 越來越像 TypeScript 了，或換個角度想 TypeScript 只不過是先研究了還在草稿中的標準；CoffeeScript：我呢？

再來是靜態網站結合線上現有的服務，講者來了個示範，丟了一個網頁讓我們輸入資料（使用Netlify），再來示範用 Trello 來搜集每個 Talk 大家給與的回饋。線上有各種服務，不需急著硬幹開發自己的系統，等公司到了一定的水平再考慮投資開發團隊也不遲。我還記得多年前參加 Hackathon 使用 Firebase，把前端 prototype 搞好接上 Firebase 的 API 就可以直接 Demo 了，省下了開發後端的時間。

其中有一個環節是講者分享把開源當作學習工具的心路歷程，講者的心態非常值得大家學習。講者本身沒有什麽大名的背景，透過好奇心以及學習能力在不同的開源社群中找到自己的出路。如果你想要貢獻開源專案，首先必須要親自跳下去成爲使用者、再來對專案中的 API 有好奇心，打開開發者工具使用節點一步一步深入程式碼學習。比如說你使用 React Hooks，如果對實作好奇的話就從這裏開始深入瞭解，沒有好奇心的話當個使用者即可。再來不要怕提問，開源專案就是一個開放的 Q&A 學習空間。

接下來是 TS 傳教士，剛開始的時候期待他分享從討厭到喜歡的心路歷程，結果只是接著介紹 TS 的功能，有點失望啊；Tensorflow.js 傳教士，比較適合像是我這種沒有 AI/ML 相關知識的人瞭解一下 JS 的潛能；當中也有關於 Web Assembly 的介紹，Web Assembly 在去年年底已經正式寫入 W3C 建議的標準，講者示範了如何用 Go 語言簡單寫 function，透過一些看不懂很懸的 API 來實作呼叫，再次强調這不是要用來取代 JS
的，請放心；關於開發者工具也有一些有趣的介紹，大家是否知道開發者工具也有夜間模式、開發者工具是由哪個語言開發、開發者工具中的開發者工具中的開發者工具功能、cmd+shift+p 來搜尋開發者工具的功能等等，説到這裏開發者工具還有待自行好好學習及運用；E2E 測試的部分有提到 Selenium / Cypress / Puppeteer / Playwright 的不同之處，但聽起來 WebDriver 標準要完善應用還有一大段路要走。

壓軸請到了 Douglas Crockford (JavaScript: The Good Parts 的作者) 做了個長達一小時的 Q&A，有點悲劇的是他的 audio 不清晰 video 又模糊，這真的很難讓人專心聽講所以整理不出什麽心得，這反而凸顯了主持人那清楚的聲音及那高級的設備。

因爲是夜晚場，每天的 Networking 因爲這美國時間又餓又想睡覺所以都沒參加，整天下來結束後直接累倒，躺下來沒多久就睡死到隔天，結果隔天比平時還要早起床！？看著自己的工作待辦事項跟著堆叠起來，沒時間幹嘛逼自己參加 Conference 根本就是找死。接下來主辦方還會舉辦 React (Native) Remote Conf / Angular Remote Conf / iOS Dev Remote Conf 等等，看起來活動内容風格會是一致的，有興趣的人我這裏有參與者共用的折價碼。

以上整理心得分享，接下來沒意外的話還會參加 Node Online Summit / ESNext Conf 2020！
