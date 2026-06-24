# Google Apps Script Web App 基礎

## 目標

本文件記錄 CS Practice 專案如何使用 Google Apps Script 建立 Web App。

這個 Web App 未來可以作為 LINE Bot 的 Webhook URL。

## 為什麼使用 Google Apps Script？

本專案目前選擇 Google Apps Script 作為簡易後端，原因是：

- 不需要自己架伺服器
- 不需要本機電腦一直開著
- 容易連接 Google Sheet
- 適合小型工具原型
- 適合練習 Webhook 和資料流

## 基本函式

### doGet(e)

用途：當使用者用瀏覽器打開 Web App URL，或外部系統用 GET 請求時執行。

目前測試回覆：

```text
CS Practice Web App is running.
