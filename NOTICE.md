# 注意事項

## 不可刪除、更動的

* html文件中會有 `<script type="module" src="../main.js"></script>`，這是指有用到 main.js 初始啟動程式用

- 已將 pages 資料夾內的 index.html 預設為首頁，建議不要任意修改 index.html 的檔案名稱
- .gitignore 檔案是用來忽略掉不該上傳到 GitHub 的檔案（例如 node_modules），請不要移除 .gitignore

## Commit Message 規範組成：

* feat: 新增/修改功能 (feature)。
* fix: 修補 bug (bug fix)。
* docs: 文件 (documentation)。
* style: 格式 (不影響程式碼運行的變動 white-space, formatting, missing semi colons, etc)。
* refactor: 重構 (既不是新增功能，也不是修補 bug 的程式碼變動)。
* perf: 改善效能 (A code change that improves performance)。
* test: 增加測試 (when adding missing tests)。
* chore: 建構程序或輔助工具的變動 (maintain)。
* revert: 撤銷回覆先前的 commit 例如：revert: type(scope): subject (回覆版本：xxxx)。

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

### 設計稿連結

[設計稿連結](https://www.figma.com/file/boEkPWQE2TJ4CODOoV8DV6/%E5%85%AD%E8%A7%92_%E8%BE%A6%E5%85%AC%E5%AE%A4%E9%9B%B6%E9%A3%9F?node-id=0%3A1&mode=dev)

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

### 間距 Spacer

```scss
$spacer: 
  0: 0,
  1: $spacer * .25,  //4px
  2: $spacer * .5,   //8px
  3: $spacer,        //16px
  4: $spacer * 1.5,  //24px
  5: $spacer * 2,    //32px
  6: $spacer * 3,    //48px
  7: $spacer * 4,    //64px
  8: $spacer * 5,    //80px
  9: $spacer * 12.5,    //120px

```

#### Spacer 寫法

```html
<h2 class="mb-4">成為零食嶼島民</h2>
```

### Display 大小

尺寸

```scss
display-headings
$display-font-sizes: (
  1: 3rem,    //48px
  2: 2.5rem,  //40px
  3: 2rem,    //32px
  4: 1.75rem,  //28px
  5: 1.5rem,    //24px
  6: 1.25rem   //20px
) !default;
```

加粗體

```html
<h2 class="font-weight-bold">成為零食嶼島民</h2>
```

字重(字粗細 scss 設定)

```scss
$font-weight-bold:            900 !default;
```

### Display 寫法

```html
<h2 class="display-1">成為零食嶼島民</h2>
```

### max-width 設定

```scss
// scss-docs-start container-max-widths
$container-max-widths: (
  sm: 576px,
  md: 720px,
  lg: 960px,
  xl: 1140px,
  xxl: 1296px
) !default;
// scss-docs-end container-max-widths
```

## break-point 設定

```scss
$grid-breakpoints: (
  xs: 0,
  sm: 375px,
  md: 768px,
  lg: 992px,
  xl: 1200px,
  xxl: 1400px
) !default;
```

## 其他設定

### Node.js 版本

- 專案的 Node.js 版本需為 v16 以上
- 查看自己版本指令：`node -v`

### 開發模式的監聽

vite 專案執行開發模式 `npm run dev` 後即會自動監聽，不需要使用 `Live Sass Compiler` 的 `Watch SCSS` 功能

### 想測試 Bootstrap 有沒有成功的話

[嘗試互動視窗 (Modal)](https://bootstrap5.hexschool.com/docs/5.0/components/modal/#live-demo)

測試
