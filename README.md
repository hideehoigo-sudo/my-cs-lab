CS Practice

這是一個個人資工工具練習專案。

本專案的目標不是一開始就大量寫程式，而是先理解資工常用工具的用途與串接方式，例如 GitHub、GitHub Pages、LINE Bot、Webhook、Google Sheet、API、自動化工具等。

專案目標

我希望透過這個專案學會：

使用 GitHub 管理專案
使用 Issue 拆解任務
建立清楚的資料夾結構
部署一個簡單網頁
理解 LINE Bot 的基本架構
理解 Webhook 是什麼
使用 Google Sheet 作為簡易資料庫
設計報修、發票、巡檢等實用工具流程
專案資料夾
cs-practice/
  README.md
  docs/
  images/
  notes/
  line-bot/
  web-deploy/
  automation/
各資料夾用途
docs/

放正式筆記與整理文件，例如 GitHub、API、Webhook、部署流程等。

images/

放截圖、流程圖、架構圖。

notes/

放學習過程中的零散筆記。

line-bot/

放 LINE Bot 相關設計，例如 Webhook 流程、回覆訊息設計、發票兌獎 Bot 架構。

web-deploy/

放網頁部署相關內容，例如 GitHub Pages、Vercel、首頁設計。

automation/

放自動化工具相關筆記，例如 Make、n8n、Google Apps Script。

目前進度

建立 GitHub repository

建立 README.md

建立基本資料夾

練習 GitHub Issues

了解 GitHub Pages

部署第一個網頁

了解 LINE Bot Webhook

設計 Google Sheet 簡易資料庫

建立第一個自動化流程

學習原則

這個專案先不追求複雜功能。

目前重點是：

把想法整理成任務
把任務放進 GitHub Issue
把學到的東西寫成文件
每完成一件事就留下紀錄
最後把工具串成一個可以展示的專案
未來想完成的應用
發票兌獎 LINE Bot
設備報修表單
巡檢紀錄系統
報修統計 Dashboard
LINE 通知系統
工務資料管理工具
專案狀態

目前狀態：第一階段，建立專案架構與學習 GitHub 基本操作。

第一階段：GitHub 基礎任務
任務 1：建立你的第一個 GitHub 專案倉庫

工具：GitHub
任務：建立一個 repo，名字叫：

my-cs-lab

裡面放這些資料夾：

my-cs-lab/
  README.md
  docs/
  images/
  notes/
  line-bot/
  web-deploy/
  automation/

完成標準：

你打開 GitHub，可以看到一個專案頁面，裡面有 README 說明。

你會學到：

repo 是什麼、README 是什麼、資料夾如何分類、commit 是什麼。

任務 2：練習 Issue，不是寫程式，是寫需求

工具：GitHub Issues
任務：開 5 張 issue：

了解 GitHub Pages
部署一個個人網頁
研究 LINE Bot Webhook
研究 Google Sheet 當資料庫
做一個發票兌獎 bot 架構圖

完成標準：

每一張 issue 都有：

目標：
我想解決什麼問題？

完成條件：
做到什麼才算完成？

筆記：
我查到什麼？

你會學到：

資工不是一開始就寫程式，而是先把事情拆成任務。

第二階段：部署網頁任務
任務 3：用 GitHub Pages 部署一個超簡單網頁

工具：GitHub Pages
任務：做一個你的個人工具頁，例如：

Jerry 的工具實驗室

1. 發票兌獎 LINE Bot
2. 公司設備維修紀錄
3. 冷氣故障排查流程
4. 職安風險評估筆記

GitHub Pages 可以把 GitHub repository 變成公開網站，GitHub 官方 quickstart 也是用 username.github.io 這種 repo 名稱來建立網站。

完成標準：

你有一個網址可以打開，例如：

https://你的帳號.github.io

你會學到：

什麼是靜態網頁、什麼是部署、什麼是網址、什麼是公開資源。

任務 4：用 Vercel 部署一個模板網站

工具：Vercel + GitHub
任務：不要自己寫程式，直接用 Vercel 的 template 或匯入 GitHub 專案。

Vercel 官方文件說明，它可以從 GitHub、GitLab、Bitbucket、Azure DevOps 等 Git repository 建立專案，並且在分支 push 或合併到 production branch 時自動部署。

完成標準：

你改 GitHub 裡的文字，Vercel 網站會自動更新。

你會學到：

CI/CD 的感覺，也就是「我更新專案 → 系統自動部署」。

這個對你很重要，因為你以後會理解：

不是把檔案丟上去而已，
而是建立一條自動更新流程。
第三階段：LINE 機器人任務
任務 5：先不要寫 bot，先畫出 LINE Bot 流程圖

工具：LINE Developers、draw.io / Excalidraw
任務：畫出這張圖：

使用者傳照片
      ↓
LINE 官方帳號收到訊息
      ↓
LINE Platform 把事件送到 Webhook URL
      ↓
你的伺服器 / Google Apps Script / 自動化工具接收
      ↓
判斷內容
      ↓
回覆使用者

LINE Messaging API 的核心流程就是：使用者傳訊息給 LINE Official Account，LINE Platform 把 webhook event 送到你設定的 webhook URL，bot server 再檢查事件並回覆。LINE 官方也說這些請求是透過 HTTPS 和 JSON 傳送。

完成標準：

你能講出這四個詞：

LINE Official Account
LINE Developers
Webhook URL
Bot Server

你會學到：

LINE bot 不是「LINE 裡面有一個機器人」而已。

真正結構是：

LINE 只是入口
你的後端才是大腦
任務 6：建立 LINE Developers Channel

工具：LINE Developers
任務：

建立一個 Messaging API Channel。

先不用寫程式，只要找到這些地方：

Channel secret
Channel access token
Webhook URL
Use webhook
Auto-reply messages
Greeting messages

完成標準：

你知道哪一個是「身份」、哪一個是「鑰匙」、哪一個是「回呼網址」。

簡單理解：

Channel secret：證明這個 bot 是誰
Access token：讓你的程式可以代表 bot 發訊息
Webhook URL：LINE 要把訊息送去哪裡
第四階段：不用寫程式的資料庫任務
任務 7：用 Google Sheet 當假資料庫

工具：Google Sheets
任務：

建立一張表叫：

invoice-bot-db

欄位如下：

日期
發票號碼
店家
金額
是否中獎
備註

完成標準：

你可以手動輸入 10 筆發票資料。

你會學到：

資料庫不是一開始就 MySQL、PostgreSQL。

你先學會：

一筆資料是什麼？
欄位是什麼？
查詢是什麼？
更新是什麼？

這對你做發票 LINE bot 很有用。

任務 8：用 Google Apps Script 發布一個 Web App

工具：Google Apps Script
任務：

先不用寫完整程式，只要知道 Apps Script 可以部署成 Web App。

Google 官方文件說明，Apps Script 可以透過「Deploy」選單部署為 web app，並取得一個網址；web app 也可以設定成由 script owner 或存取者身分執行。

完成標準：

你知道 Google Apps Script 可以產生一個網址，這個網址未來可以接 LINE Webhook。

你會學到：

什麼叫：

雲端小後端

也就是不用自己架伺服器，也可以有一個可以接收請求的地方。

第五階段：API 與測試任務
任務 9：用 Postman 認識 API

工具：Postman
任務：

不用自己寫 API，先拿公開 API 測試，例如查天氣、匯率、假資料 API。

你只要練習看懂：

GET
POST
Headers
Body
JSON
Status Code

完成標準：

你能分辨：

GET：拿資料
POST：送資料
JSON：資料格式
Status 200：成功
Status 404：找不到
Status 500：伺服器錯

你會學到：

LINE bot、網頁、資料庫、自動化工具，最後都離不開 API。

第六階段：自動化任務
任務 10：用 Make / n8n / Zapier 做一個不用寫程式的流程

工具：Make、n8n、Zapier 任選一個
任務：

做一條流程：

收到 Google 表單
      ↓
寫入 Google Sheet
      ↓
傳一則通知到 LINE / Gmail / Telegram

完成標準：

你填表單後，系統會自動通知你。

你會學到：

這就是 no-code automation。

你會開始理解：

觸發器 Trigger
動作 Action
條件 Condition
資料 Mapping
第七階段：跟你工作結合的任務

這階段最重要，因為你不是純資工學生，你是機電工務。你可以做出比一般人更實用的東西。

任務 11：設備報修表單系統

工具：Google Form + Google Sheet
任務：

建立報修表單：

報修日期
報修人
樓層
設備類型
異常描述
照片
嚴重程度
是否影響營運
處理狀態

完成標準：

同事填表單後，資料會進 Sheet。

你會學到：

這就是最小型的 MIS 系統。

任務 12：設備巡檢儀表板

工具：Google Sheet + Looker Studio
任務：

把巡檢資料視覺化：

樓層故障次數
冷氣異常次數
照明異常次數
衛浴異常次數
平均處理天數

完成標準：

你能看到一張圖表，知道哪一層樓問題最多。

你會學到：

資料不是記錄而已，資料要能幫主管決策。

任務 13：LINE 報修 Bot 架構設計

工具：LINE、Google Sheet、流程圖
任務：

設計這個 bot：

使用者傳：
6F 男廁小便斗堵塞

Bot 回覆：
已收到報修
類型：衛浴
地點：6F 男廁
狀態：待處理

完成標準：

你不用真的做出來，但要畫出資料怎麼走。

你會學到：

這是需求分析。

資工最重要的不是寫出程式，而是知道：

誰輸入？
輸入什麼？
系統怎麼判斷？
資料存哪裡？
誰收到通知？
怎麼結案？
我建議你照這個順序做
1. GitHub 帳號與 repo
2. README 與 Issues
3. GitHub Pages
4. Vercel 部署
5. LINE Developers
6. LINE Bot 流程圖
7. Google Sheet 當資料庫
8. Apps Script Web App
9. Postman 測 API
10. Make / n8n 自動化
11. 報修表單
12. 巡檢儀表板
13. LINE 報修 Bot 設計
你真正要學的不是工具，是這張地圖
GitHub：專案放哪裡
README：專案說明
Issue：任務管理
Pages / Vercel：網頁部署
LINE Developers：使用者入口
Webhook：訊息送去哪裡
Apps Script / Server：後端大腦
Google Sheet：簡易資料庫
Postman：測試 API
Make / n8n：自動化流程
Looker Studio：資料視覺化

## 網站連結

GitHub Pages：

https://hideehoigo-sudo.github.io/my-cs-lab/


Vercel：
https://my-cs-lab-dnwi.vercel.app/
