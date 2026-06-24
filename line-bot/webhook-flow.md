# Webhook Flow

## Webhook 是什麼？

Webhook 可以理解成：

當某件事發生時，系統主動通知另一個網址。

在 LINE Bot 裡，某件事可能是：

- 使用者加好友
- 使用者傳文字
- 使用者傳圖片
- 使用者傳貼圖
- 使用者取消追蹤

LINE 會把這些事件送到我設定的 Webhook URL。

## LINE Bot Webhook 流程

```text
1. 使用者傳訊息給 LINE Bot

2. LINE Platform 接收到訊息

3. LINE Platform 產生 webhook event

4. LINE Platform 將 event 用 POST 送到 Webhook URL

5. 後端接收 event

6. 後端判斷訊息內容

7. 後端決定要不要寫入資料庫

8. 後端透過 LINE Messaging API 回覆使用者
