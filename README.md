# 台灣景點介紹

用 Jekyll + GitHub Pages 建立的台灣景點介紹網站。

## 專案結構

```
台灣介紹/
├── _config.yml              # Jekyll 設定
├── index.html               # 首頁（自動列出所有景點）
├── _layouts/
│   ├── default.html         # 共用版型（header/footer）
│   └── attraction.html      # 景點頁版型
├── _attractions/            # 景點內容（每個景點一個 .md 檔）
│   ├── taipei-101.md
│   └── jiufen.md
├── assets/
│   ├── css/style.css        # 樣式
│   └── images/              # 圖片放這裡
└── README.md
```

## 新增景點的步驟

1. 在 `_attractions/` 建立新的 `.md` 檔（例如 `sun-moon-lake.md`）
2. 檔案開頭貼上以下 front matter，再寫景點內文：

```markdown
---
title: 日月潭
location: 南投縣魚池鄉
summary: 一句話介紹，會顯示在首頁卡片。
cover: /assets/images/sun-moon-lake.jpg
---

這裡開始寫詳細介紹，支援 Markdown 語法。

## 小標題

文字段落...

![圖片說明](/assets/images/sun-moon-lake-2.jpg)
```

3. 把對應的圖片放到 `assets/images/` 資料夾
4. push 到 GitHub，網站會自動更新

## 部署到 GitHub Pages

1. 在 GitHub 建立一個新的 repository（建議名稱如 `taiwan-attractions`）
2. 把這個資料夾推上去：

```bash
git init
git add .
git commit -m "init: 台灣景點網站"
git branch -M main
git remote add origin https://github.com/你的帳號/taiwan-attractions.git
git push -u origin main
```

3. 到 repo 的 **Settings → Pages**，將 Source 設為 `Deploy from a branch`，分支選 `main`、資料夾選 `/ (root)`，按 Save
4. 等 1-2 分鐘，網址會出現在同一頁面：`https://你的帳號.github.io/taiwan-attractions/`
5. 平板瀏覽器直接打開即可瀏覽

## 本機預覽（選用）

如果想推上 GitHub 前先在電腦上預覽，需要安裝 Ruby 與 Jekyll：

```bash
gem install bundler jekyll
jekyll serve
```

然後開啟 `http://localhost:4000`。

不裝也沒關係，直接 push 到 GitHub 就會看到結果。
