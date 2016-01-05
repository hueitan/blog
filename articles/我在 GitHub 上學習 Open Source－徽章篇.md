_原文刊登於：PTT_

我在 GitHub 上學習 Open Source－徽章篇
===

哈囉大家好，新年新希望，系列文短篇第一炮《徽章篇》

在 Open Source 世界裡你常常會看到一個詞「Badge」，好吧，我承認我不知道應該用什麼詞代表，容許我先在這裏翻譯成「徽章」。但我想不是大家都懂這徽章指的是什麼。已經在開發 Open Source 的人應該對這徽章不陌生了，歡迎糾正以及補充資料！至於專案什麼時候使用徽章？他如何幫助你的 Open Source 專案開發呢？讓我來為各位做個簡單的介紹。廢話少說，先來看看什麼是徽章

![badge](http://i.imgur.com/PEZpnpb.png)

**[徽章介紹]**

為何我會推薦大家使用徽章呢？使用徽章有幾種紅綠燈通用顏色－紅色、黃色、綠色。如果專案內有紅色的徽章，馬上反應就會覺得這專案是不是有什麼問題，反之徽章全都是綠色的時候，是不是就有安心的感覺呢。通常徽章用來回報專案目前的狀態如：測試順不順利、Issue 狀態、Code 品質、文件是否齊全、專案下載量、專案版本等等。設定上不會很困難，一旦第一次設定好後（依據服務要求），基本上往後就是自動化你也不需要再操心，任何一個動作都會直接影響到專案徽章狀態。不要小看這小小的狀態列，它能即時把專案的詳情告知使用者，他們不必多做猜測，你也不用多花心思檢查，因為徽章都會幫你處理好一切。

以我自身使用的例子，我常使用 [Travis CI] [CodeClimate] [Coverage] [David] [Gitter Chat] [Awesome Badge] [MORE]

以下簡單介紹 ▼

**[Travis CI]**

如果你的專案是 Open Source 開放的，Travis 提供一個免費的 CI 環境，讓你每 Commit 一次執行你設定好的 Bash，不過大家一般都還是拿來跑測試結果。Travis CI 支援各種程式語言，你只要在專案中產生一個文件 .travis.yml，設定好即可。以 A-V 的範例，跑完測試後，會執行 Coverage 再推上 Coveralls。

網站：https://travis-ci.org/
<br/>文件：https://docs.travis-ci.com/
<br/>範例：https://travis-ci.org/huei90/angular-validation
<br/>推薦：必學！必用！簡單上手。

**[CodeClimate]**

就如網站上說的，CodeClimate 會自動化幫你的專案 Code Review，經過自動化 Review，他會為你的專案打 GPA 分數。使用上非常簡單，登入後只要把專案名稱輸入進去即可。分數最高4分，其實除了自我感覺良好外，也給其他人馬上知道你的專案的分數。

有些檔案不需要被打分，這時候就要用到 .codeclimate.yml 檔案了，詳情請看文件。

網站：https://codeclimate.com
<br/>文件：https://docs.codeclimate.com/
<br/>範例：https://codeclimate.com/github/huei90/angular-validation
<br/>推薦：改到分數高在放上去比較可口。

**[Coverage]**

其實我之前不懂這是什麼，只聽說 Test Coverage 可以自動幫你檢查測試涵蓋率，其實聽起來超威的。它擁有特殊的演算法（istanbul），會自動檢查專案和測試的程式碼做複雜的比對，最後給上測試涵蓋率 Coverage 成績。

就如我之前常常提到的測試，一旦你程式寫完後，測試的部分也完成了，但其實自己也不知道漏了哪些部份沒有寫上測試，這時候 Test Coverage 就能幫上你忙了！

網站：https://coveralls.io
<br/>文件：https://coveralls.zendesk.com/hc/en-us
<br/>範例：https://coveralls.io/github/huei90/angular-validation
<br/>推薦：我搞了一陣子才理解 Coverage 的運作，不過一旦學會，未來就沒什麼問題了。

**[David]**

如果你有使用 npm 的話，這個徽章工具非常推薦，它會自動幫你檢查 package.json 中的 Dependencies 和 devDependencies 的版本號，並亮紅燈提醒你是時候更新了。使用越多的套件，你不可能一個一個去檢查版本號，這時候大衛先生絕對幫得上忙！

網站：https://david-dm.org
<br/>文件：無
<br/>範例：https://david-dm.org/huei90/angular-validation#info=devDependencies
<br/>推薦：一目了然，沒什麼難的

**[Gitter Chat]**

之前文章我有簡單介紹到 Gitter 這個 Repo 聊天室，這個徽章其實只是提供一個快速連結到聊天室，僅此。（有時候會覺得提供徽章比提供一長串 URL 連接乾淨許多）

網站：https://gitter.im
<br/>文件：無
<br/>範例：無
<br/>推薦：根據專案需求

**[Awesome Badge]**

Awesome 系列在 GitHub 上潮了一整子，你今天 Awesome 了嗎？後來 Awesome 的作者提供了 Awesome 徽章，算是對 Awesome-XX 專案的一個認可。其實 Awesome 的作者很嚴格，並不是取名為 Awesome-XX 都能被列在 Awesome list 中－專案介紹、內容、成熟度等等的條件加總起來才有機會實質獲得 Awesome 的徽章。

網站：https://github.com/sindresorhus/awesome
<br/>推薦：有寫 Awesome 文的才需要

**[MORE]**

這說也說不完，以下幾個推薦的連結，你可以找到各種類型的徽章，不過有些徽章使用的服務是要付費的喔。
1. https://github.com/boennemann/badges
2. http://shields.io/

每個專案都有屬於自己的徽章，
<br/>去吧 去找尋茫茫之中屬於你專案的徽章 吧～

**[END]**

希望這篇介紹對於想要進入 Open Source 世界的朋友們有所幫助，一旦你的專案逐漸壯大起來，放上徽章也算是對它的一個肯定喔！（自己的專案自己救）

這次要來工商一下，一直 po 在 PTT 實在不好意思，我在自己的 GitHub 上開了個 blog 的空間，對於我分享的文章有興趣的朋友，我來討星星和眼睛^^咯，眼睛了才能持續追蹤新的文章喔，嘿嘿呵哈嘿呵呵哈哈哈哈 < https://github.com/huei90/blog 。

另外，開了一個 Issue，歡迎大家提供意見。https://github.com/huei90/blog/issues/1

結束，句點。
