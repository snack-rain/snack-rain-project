# 注意事項

## 不可刪除、更動的

* html文件中會有 `<script type="module" src="../main.js"></script>`，這是指有用到 main.js 初始啟動程式用

- 已將 pages 資料夾內的 index.html 預設為首頁，建議不要任意修改 index.html 的檔案名稱
- .gitignore 檔案是用來忽略掉不該上傳到 GitHub 的檔案（例如 node_modules），請不要移除 .gitignore

## 忘記 EJS 語法請看這裡

<%- include('./layout/header'); -%>

## 資料夾結構

### 資料夾

- assets # 靜態資源放置處
  - images # 圖片放置處
  - scss # SCSS 的樣式放置處
- layout # ejs 模板放置處
- pages # 頁面放置處
- JavaScript 程式碼可寫在 main.js 檔案

### HTML

| 頁面            | 說明                  |
| --------------- | --------------------- |
| index.html      | 零食嶼首頁            |
| story.html      | 零食的故事            |
| topic-1.html    | 零食主題一-健身好朋友 |
| topic-2.html    | 零食主題二-低卡無負擔 |
| topic-3.html    | 零食主題三-懷舊零食   |
| mag.html        | 零食誌首頁            |
| mag-202307.html | 零食誌七月刊          |
| mag-202308.html | 零食誌八月刊          |
| coop.html       | 合作夥伴              |
| about-us.html   | 關於我們              |
| sub.html        | 訂閱零食嶼            |

### SCSS

#### 共用區檔案

| scss檔              | 說明             |
| ------------------- | ---------------- |
| _customize-all.scss | 修改不需要的樣式 |
| _navbar.scss        | 導覽列元件       |
| _header.scss        | 頁首元件         |
| _footer.scss        | 頁底元件         |

#### 非共用區塊的檔案命名

| 頁面            | 說明                  |
| --------------- | --------------------- |
| index.scss      | 零食嶼首頁            |
| story.scss      | 零食的故事            |
| topic-1.scss    | 零食主題一-健身好朋友 |
| topic-2.scss    | 零食主題二-低卡無負擔 |
| topic-3.scss    | 零食主題三-懷舊零食   |
| mag.scss        | 零食誌首頁            |
| mag-202307.scss | 零食誌七月刊          |
| mag-202308.scss | 零食誌八月刊          |
| coop.scss       | 合作夥伴              |
| about-us.scss   | 關於我們              |
| sub.scss        | 訂閱零食嶼            |

## Node.js 版本

- 專案的 Node.js 版本需為 v16 以上
- 查看自己版本指令：`node -v`

## 開發模式的監聽

vite 專案執行開發模式 `npm run dev` 後即會自動監聽，不需要使用 `Live Sass Compiler` 的 `Watch SCSS` 功能

## 想測試 Bootstrap 有沒有成功的話

[嘗試互動視窗 (Modal)](https://bootstrap5.hexschool.com/docs/5.0/components/modal/#live-demo)
