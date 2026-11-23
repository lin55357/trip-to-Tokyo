# trip-to-Tokyo：Jekyll 網站檔案

## 本包內容
- `_config.yml`：Jekyll 與 GitHub Pages 網站設定
- `index.html`：新部落格首頁
- `about.md`：關於頁
- `_layouts/default.html`、`_includes/`：共用版型與導覽
- `_posts/2026-11-29-tokyo-travel.md`：第一篇東京遊記範本
- `assets/css/style.css`：網站樣式

## 放進 GitHub 專案的方式
1. 先在 GitHub 專案下載 ZIP 備份目前版本。
2. 解壓縮本包，把裡面的檔案與資料夾上傳到 `trip-to-Tokyo` 專案根目錄。
3. 以本包的 `index.html` 取代舊 `index.html`；原本的 `guide.html` 請保留，不要刪除或改名。
4. 確認 `_config.yml` 的 `url` 是 `https://lin55357.github.io`，`baseurl` 是 `/trip-to-Tokyo`。
5. GitHub 專案進入 Settings → Pages，Source 選擇 Deploy from a branch，Branch 選 `main`、資料夾選 `/ (root)`，儲存。
6. 等待 GitHub Pages 建置完成，網站網址應為 `https://lin55357.github.io/trip-to-Tokyo/`。

## 圖片放置
建議新增 `assets/images/tokyo/`，把照片放進去。文章內可用：

```liquid
![東京街景]({{ '/assets/images/tokyo/photo-01.jpg' | relative_url }})
```

## 注意
- `guide.html` 是既有的獨立旅遊手冊，Jekyll 會將它保留為 `/guide.html`，首頁導覽已連結它。
- `_config.yml` 使用 `jekyll-feed` 與 `jekyll-seo-tag` 外掛；GitHub Pages 可支援這些外掛。
- 若 GitHub Pages 尚未啟用，請先依上方步驟設定 Pages。
