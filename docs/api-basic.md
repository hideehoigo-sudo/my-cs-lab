# API 基礎筆記

## 目標

本文件記錄我使用 Postman 練習 API 的基本概念。

---

## GET 測試

GET 用來取得資料。

本次測試網址：

```text
GET https://jsonplaceholder.typicode.com/posts/1
```

測試結果：

```text
Status：200 OK
```

回傳資料範例：

```json
{
  "userId": 1,
  "id": 1,
  "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
  "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
}
```

---

## POST 測試

POST 用來送出資料。

本次測試網址：

```text
POST https://jsonplaceholder.typicode.com/posts
```

送出的 JSON：

```json
{
  "title": "CS Practice 測試",
  "body": "這是我第一次用 Postman 測試 POST",
  "userId": 1
}
```

測試結果：

```text
Status：201 Created
```

---

## Header

Header 是請求的附加資訊。

常見例子：

```text
Content-Type: application/json
Authorization: Bearer token
```

---

## Body

Body 是 POST 時送出的資料內容。

---

## JSON

JSON 是常見的資料格式。

範例：

```json
{
  "name": "Jerry",
  "type": "test"
}
```

---

## Status Code

| 狀態碼 | 意思    |
| --- | ----- |
| 200 | 成功    |
| 201 | 建立成功  |
| 400 | 請求錯誤  |
| 401 | 未授權   |
| 404 | 找不到   |
| 500 | 伺服器錯誤 |

---

## 和 LINE Bot 的關係

LINE Bot 也是 API 應用。

目前專案中已經用到：

* LINE Webhook POST 到 Apps Script
* Apps Script 解析 JSON
* Apps Script 呼叫 LINE Reply API
* LINE Bot 回覆使用者
