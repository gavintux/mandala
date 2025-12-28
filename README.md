# 🌸 Mandala Garden (曼陀羅思考花園)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/部署-GitHub%20Pages-brightgreen)](https://pages.github.com/)
[![React](https://img.shields.io/badge/Frontend-React-blue)](https://reactjs.org/)
[![Firebase](https://img.shields.io/badge/Backend-Firebase-orange)](https://firebase.google.com/)

> **您的思維花園，讓靈感像植物一樣生長。**

Mandala Garden 是一款基於網頁的曼陀羅思考法（Mandala Chart）工具。它結合了現代化的響應式介面與雲端同步功能，幫助使用者透過九宮格結構化地拆解目標、規劃專案或進行創意思考。無論是簡單的 3x3 筆記，還是深度的 9x9 核心目標規劃，都能在此輕鬆實現。

---

## ✨ 功能特色

* **多維度思考模式**：支援基礎的 **3x3 九宮格** 與進階的 **9x9 全景曼陀羅**，並具備直覺的縮放導航功能（點擊中心擴展至周邊）。
* **雲端同步與管理**：
    * 整合 **Firebase Authentication** 進行使用者註冊與登入。
    * 使用 **Firestore** 即時儲存與同步您的思考筆記。
    * 完整的檔案管理系統：包含分類標籤（Tags）、垃圾筒回收機制與全域關鍵字搜尋。
* **豐富的編輯體驗**：
    * 支援 **Markdown** 語法與行內預覽。
    * 內建 **Emoji 選擇器**，將圖示分類以便快速插入。
    * 支援儲存 **圖片** 與自訂 **單元格顏色**，讓思考更視覺化。
* **強大的匯出分享**：
    * **影像化**：一鍵匯出為高解析度 `JPG` 或 `PDF`。
    * **數據化**：支援匯出為 `Excel` 表格或 `Markdown` 文件。
    * **代碼分享**：可生成 JSON 代碼與他人分享您的曼陀羅架構。
* **響應式設計**：基於 Tailwind CSS 構建，完美支援桌面端與行動裝置操作。

## 🚀 線上展示 (Demo)

您可以直接透過以下連結體驗 Mandala Garden 的完整功能：

👉 **[點擊前往 Live Demo](https://gavintux.github.io/yi/demomandala.html)**

---

## 🛠 技術架構

本專案採用 **單一文件 (Single File)** 的開發模式，方便部署與輕量化運行，主要技術棧包括：

* **核心框架**：React 18 (UMD)
* **樣式處理**：Tailwind CSS (CDN)
* **後端服務**：Firebase (Auth, Firestore, Storage)
* **編譯工具**：Babel (Standalone)
* **工具函式庫**：
    * `html2canvas` & `jspdf` (圖片與 PDF 生成)
    * `marked` (Markdown 解析)

---

## 💻 安裝與使用說明

由於本專案設計為單一 HTML 架構，您可以非常容易地在本地端運行或部署。

### 1. 取得專案
```bash
git clone [https://github.com/gavintux/您的專案名稱.git](https://github.com/gavintux/您的專案名稱.git)
cd 您的專案名稱
```
### 2. 配置 Firebase (重要)
打開 demomandala.html，找到頂部的 USER_CONFIG 區域。為了確保數據安全與獨立性，建議您建立自己的 Firebase 專案並替換以下參數：
``` html
const USER_CONFIG = {
    seo: { /* ... */ },
    firebase: { 
        apiKey: "YOUR_API_KEY",
        authDomain: "YOUR_PROJECT.firebaseapp.com",
        projectId: "YOUR_PROJECT_ID",
        storageBucket: "YOUR_PROJECT.appspot.com",
        messagingSenderId: "YOUR_SENDER_ID",
        appId: "YOUR_APP_ID",
        measurementId: "YOUR_MEASUREMENT_ID"
    },
    system: { collectionName: 'mandala_charts', defaultGridSize: 3, defaultViewStyle: 'standard' }
};
```
### 3. 本地運行
直接使用瀏覽器打開 demomandala.html 即可開始使用。
## 📸 介面預覽
- [Demo Mandala Garden](https://gavintux.github.io/yi/demomandala.html)

## 📂 專案結構
雖然是單一 HTML 文件，但程式碼內部邏輯結構清晰：
- HTML Head: 引入 React, Tailwind, Firebase SDK 等 CDN 資源。
- App Component: 主應用入口。
  -State Management: 處理使用者登入狀態、檔案列表、當前編輯內容。
  -Components:
    - SidebarContent: 側邊選單、標籤過濾。
    - renderGrid/renderCell: 核心九宮格渲染邏輯。
    - Modals: 包含編輯、匯出、搜尋、分享等對話框。
- Utils: 包含顏色處理、Markdown 解析、匯出邏輯 (PDF/Img)。

## 🗺 未來規劃 (Roadmap)
- 離線模式：利用 PWA 技術支援離線編輯。
- 協作功能：允許多人同時編輯同一個曼陀羅。
- 深色模式：優化夜間編輯體驗。
- 模板庫：內建常見的曼陀羅思考模板（如：SWOT、OKR）。
## 🤝 貢獻指南
歡迎任何形式的貢獻！如果您有好的想法：

### Fork 本專案。
- 建立您的 Feature Branch (git checkout -b feature/AmazingFeature)。
- 提交您的變更 (git commit -m 'Add some AmazingFeature')。
- 推送到 Branch (git push origin feature/AmazingFeature)。
- 開啟 Pull Request。

## 📜 授權聲明
本專案採用 MIT License 授權。
### 📞 聯絡與贊助
如果您喜歡這個專案，或是有任何合作需求，歡迎透過以下方式聯繫作者。
- 作者：Linkc
- 個人網站：https://gavintux.github.io/yi/
###  ☕ 請作者喝杯咖啡
如果您覺得這個工具對您有幫助，歡迎贊助支持開發！
<a href="https://www.buymeacoffee.com/gavintux" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>
