# LINE Bot 架構筆記

## 目標

本文件用來記錄 LINE Bot 的基本架構。

目前階段先不寫程式，只理解 LINE 官方帳號、Messaging API、Webhook、後端與資料庫之間的關係。

## 基本角色

### 1. 使用者

使用者透過 LINE 傳送文字、圖片、發票號碼或報修內容。

### 2. LINE 官方帳號

LINE 官方帳號是使用者看到的 Bot 入口。

### 3. LINE Platform

LINE Platform 負責接收使用者訊息，並把事件送到 Webhook URL。

### 4. Webhook URL

Webhook URL 是後端接收 LINE 事件的網址。

### 5. Bot Server

Bot Server 負責接收事件、判斷內容、寫入資料、回覆使用者。

初期可能使用：

- Google Apps Script
- Make
- n8n
- Railway
- Render

### 6. Google Sheet

Google Sheet 可以作為初期的簡易資料庫，用來儲存發票、報修、巡檢資料。

## 資料流程

```text
使用者傳訊息
      ↓
LINE 官方帳號收到訊息
      ↓
LINE Platform 產生 webhook event
      ↓
LINE Platform 把 event 送到 Webhook URL
      ↓
Bot Server 接收資料
      ↓
Bot Server 判斷內容
      ↓
資料寫入 Google Sheet
      ↓
Bot Server 回覆 LINE 使用者
