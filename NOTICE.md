# 注意事項

## 不可刪除的
html文件中會有<script type="module" src="../main.js"></script>，這是指有用到 main.js 初始啟動程式用


## 忘記 EJS 語法請看這裡
<%- include('./layout/header'); -%>

## 資料結構
  ### HTML
  index.html
  story.html
  topic-1.html
  topic-2.html
  topic-3.html
  mag.html
  mag-202307.html
  mag-202308.html
  coop.html
  about-us.html
  sub.html

  ### SCSS
  #### 共用區檔案
    _variable.scss 
    _navbar.scss
    _header.scss
    _footer.scss

  #### 非共用區塊的檔案命名
    _index.scss
    _story.scss
    _topic-1.scss
    _topic-2.scss
    _topic-3.scss
    _mag.scss
    _mag-202307.scss
    _mag-202308.scss
    _coop.scss
    _about-us.scss
    _sub.scss







## Node.js 版本
  - 專案的 Node.js 版本需為 v16 以上
  - 查看自己版本指令：`node -v`


## 指令列表
- `npm install` - 初次下載該範例專案後，需要使用 npm install 來安裝套件
- `npm run dev` - 執行開發模式
  - 若沒有自動開啟瀏覽器，可嘗試手動在瀏覽器上輸入
    `http://localhost:5173/<專案名稱>/pages/index.html`
- `npm run build` - 執行編譯模式（不會開啟瀏覽器）
- `npm ru deploy` - 自動化部署

## 資料夾結構
  - assets # 靜態資源放置處
    - images # 圖片放置處
    - scss # SCSS 的樣式放置處

  - layout # ejs 模板放置處
  - pages # 頁面放置處

- JavaScript 程式碼可寫在 main.js 檔案

### 注意事項
- 已將 pages 資料夾內的 index.html 預設為首頁，建議不要任意修改 index.html 的檔案名稱
- .gitignore 檔案是用來忽略掉不該上傳到 GitHub 的檔案（例如 node_modules），請不要移除 .gitignore

## 開發模式的監聽
vite 專案執行開發模式 `npm run dev` 後即會自動監聽，不需要使用 `Live Sass Compiler` 的 `Watch SCSS` 功能


## 部署 gh-pages 流程說明
### Windows 版本
1. 在 GitHub 建立一個新的 Repository

2. 部署前請務必先將原始碼上傳到 GitHub Repository 也就是初始化 GitHub，因此通常第一步驟會在專案終端機輸入以下指令
```cmd
git init # 若已經初始化過就可以不用輸入
git add .
git commit -m 'first commit'
git branch -M main
git remote add origin [GitHub Repositories Url]
git push -u origin main // 僅限第一次輸入，往後只需要輸入 git push
```

3. 初始化完畢後，執行 `npm run deploy` 指令進行自動化部署
