# ⚡ 全台充電樁自動同步數據服務 (GitHub Actions 版)

本專案使用 GitHub Actions 免費排程服務，每日自動向交通部 TDX API 抓取全台最新充電站數據，並自動產生 `data/stations.json` 供 Wi玩世界 (wiyafunworld) Blogger 部落格地圖讀取。

---

## 🛠️ 簡單 3 步驟開啟 GitHub Actions 自動同步：

### 1. 在 GitHub 上建立儲存庫 (Repository)
1. 前往 GitHub 建立一個全新的 Public Repository。
2. 專案名稱命名為：`taiwan-ev-data`

### 2. 設定 TDX API 加密金鑰 (Secrets)
1. 進入您剛建立的 GitHub 儲存庫頁面。
2. 點選頂部的 **Settings** ➔ 左側欄 **Secrets and variables** ➔ 點選 **Actions**。
3. 點選 **New repository secret** 增加以下兩組加密密碼：
   * **`TDX_CLIENT_ID`** ➔ 填入您個人在 TDX 申請的 Client ID
   * **`TDX_CLIENT_SECRET`** ➔ 填入您個人在 TDX 申請的 Client Secret

### 3. 將本專案推送 (Push) 上去
在 Terminal 中執行：
```bash
git init
git add .
git commit -m "Initial commit for GitHub Actions EV data sync"
git branch -M main
git remote add origin https://github.com/WiFunworld/taiwan-ev-data.git
git push -u origin main
```

---

## 🌐 Blogger 前端介接 URL：
推送完成後，您的 Blogger 文章地圖即可直接載入以下網址：
`https://raw.githubusercontent.com/WiFunworld/taiwan-ev-data/main/data/stations.json`
