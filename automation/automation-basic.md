# Make 自動化基礎筆記

## 目標

本文件記錄我使用 Make 建立第一個自動化流程。

## 本次流程

Google Sheet 新增資料
↓
Make 偵測新資料
↓
Gmail 自動寄出通知

## 使用工具

- Google Sheet
- Make
- Gmail

## 測試用工作表

Google Sheet：cs-practice-database

工作表：automation_test

欄位：

- 建立時間
- 事件類型
- 內容
- 嚴重程度
- 通知狀態

## Trigger

Trigger 是自動化流程的起點。

本次使用：

Google Sheets - Watch New Rows

意思是：

當 Google Sheet 新增一列資料時，啟動流程。

## Action

Action 是 Trigger 發生後要執行的動作。

本次使用：

Gmail - Send an Email

意思是：

偵測到新資料後，自動寄出通知信。

## 本次測試資料

2026/06/26　測試通知　這是 Make 自動化測試　高　未通知

## 測試結果

成功收到 Gmail 通知信。

## 學到的事

Make 是自動化流程工具。

它可以把不同系統串起來。

基本邏輯是：

當某件事發生
↓
自動做某件事

也就是：

Trigger
↓
Action

## 和工作應用的關係

未來可以用在：

- 報修表單新增資料後，自動通知工務
- 巡檢發現異常後，自動寄信提醒
- 發票資料新增後，自動整理紀錄
- Google Sheet 新增資料後，自動傳 LINE 或 Email

## 下一步

進入工務應用任務，建立設備報修表單系統。
