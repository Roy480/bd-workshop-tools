# 📤 Vercel 部署教學

## 🚀 方法 1：直接拖曳上傳（最簡單）

### 步驟：

1. **登入 Vercel**
   - 前往 https://vercel.com
   - 用 GitHub 帳號登入

2. **上傳專案**
   - 點擊右上角「Add New...」→「Project」
   - 選擇「Deploy」標籤
   - 把整個 `bd-workshop-tools` 資料夾拖曳進去
   
   或者：
   - 解壓縮 `bd-workshop-tools.tar.gz`
   - 把裡面的所有檔案（index.html, vercel.json 等）拖曳上傳

3. **部署設定**
   - Project Name: `bd-workshop-tools`（或你想要的名字）
   - Framework Preset: 選擇「Other」
   - Root Directory: `./`（保持預設）
   - 點擊「Deploy」

4. **完成！**
   - 等待 1-2 分鐘
   - Vercel 會給你一個網址：`https://bd-workshop-tools.vercel.app`
   - 或者你自訂的網址

---

## 🔗 方法 2：透過 GitHub（進階）

### 步驟：

1. **上傳到 GitHub**
   ```bash
   # 在本地電腦
   cd bd-workshop-tools
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/你的帳號/bd-workshop-tools.git
   git push -u origin main
   ```

2. **在 Vercel 匯入**
   - 登入 Vercel
   - 點擊「Add New...」→「Project」
   - 選擇「Import Git Repository」
   - 選擇你的 GitHub Repository
   - 點擊「Deploy」

3. **優點**
   - 每次更新 GitHub，Vercel 會自動重新部署
   - 有版本控制

---

## 🎯 部署後的網址

### 預設網址格式：
```
https://你的專案名稱.vercel.app
```

例如：
```
https://bd-workshop-tools.vercel.app
```

### 自訂網域（可選）：
如果你有自己的網域，可以在 Vercel 設定：
- Settings → Domains
- 輸入你的網域（如：tools.yoursite.com）
- 按照指示設定 DNS

---

## 📱 分享給學員

部署完成後，你可以：

1. **直接給網址**
   ```
   https://bd-workshop-tools.vercel.app
   ```

2. **做 QR Code**
   - 用 https://qr-code-generator.com
   - 輸入你的 Vercel 網址
   - 下載 QR Code
   - 印在講義或投影

3. **短網址（可選）**
   - 用 bit.ly 或 tinyurl.com
   - 把長網址縮短成：`bit.ly/bd-tools`

---

## 🔧 更新網站內容

### 如果用方法 1（直接上傳）：
1. 在 Vercel 找到你的專案
2. Settings → Deployments
3. 上傳新的檔案
4. 或者刪除舊的 deployment 後重新上傳

### 如果用方法 2（GitHub）：
1. 修改本地檔案
2. Git commit + push
3. Vercel 自動重新部署（30秒內完成）

---

## ⚙️ 檔案說明

```
bd-workshop-tools/
├── index.html        # 主要網頁（必要）
├── vercel.json       # Vercel 設定（建議）
├── README.md         # 專案說明
└── .gitignore        # Git 忽略檔案
```

**最重要的是 `index.html`，其他檔案是輔助用的。**

---

## 🆘 常見問題

### Q1: 部署後顯示 404？
**A:** 確認 `index.html` 在根目錄，不是在子資料夾裡。

### Q2: 資料儲存會不會消失？
**A:** 不會。資料存在**學員自己的瀏覽器** LocalStorage，跟你的伺服器無關。

### Q3: 可以看到學員填寫的內容嗎？
**A:** 不行。這是純前端網頁，所有資料都在學員的瀏覽器，你看不到也拿不到。

### Q4: 需要付費嗎？
**A:** Vercel 免費版就夠用了。
- 免費額度：100 GB 流量/月
- 你的工作坊 100 人用完全夠

### Q5: 網址可以改嗎？
**A:** 可以！
- 方法 1：在 Vercel Settings → Domains 改 Project Name
- 方法 2：用自己的網域

---

## ✅ 檢查清單

部署前確認：
- [ ] index.html 在根目錄
- [ ] 本地測試過（用瀏覽器打開 index.html）
- [ ] 所有工具表（A/B/C/D）都能正常使用

部署後確認：
- [ ] 能正常開啟網址
- [ ] 手機/電腦都能用
- [ ] 填寫後資料會儲存
- [ ] 列印功能正常

---

## 🎓 給學員的使用說明

你可以這樣跟學員說：

> 「我們的工作坊工具表已經上線了！」
> 
> **網址：** https://你的網址.vercel.app
> 
> **使用方式：**
> 1. 用手機或電腦打開網址
> 2. 填寫工具表（會自動儲存）
> 3. 隨時可以回來查看或更新
> 
> **注意：** 資料存在你自己的瀏覽器，換裝置就看不到了。如果想備份，可以截圖或列印。

---

需要幫忙嗎？隨時問我！
