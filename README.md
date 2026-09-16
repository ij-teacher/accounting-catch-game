# 會計接接樂：GitHub 共用題庫版

遊戲網址：https://ij-teacher.github.io/accounting-catch-game/

學生免登入。每次開啟網頁、開始新回合，從 GitHub 讀取 bank.json；進行中的回合使用開始時的題目。載入失敗會提示重試，不會偷偷改用本機舊題庫。發布後 GitHub Pages 需重新部署，通常約 1–2 分鐘。畫面先顯示已送出，確認公開學生版版本後才顯示學生版已更新。

## 老師編輯

1. 在 GitHub 建立 Fine-grained personal access token。
2. Resource owner 選 ij-teacher，Repository access 選 Only select repositories，只選 accounting-catch-game。
3. Repository permissions 的 Contents 設為 Read and write，選擇合適到期日。
4. 打開遊戲的「老師登入／編輯共用題庫」，貼上權杖登入。
5. 編輯後按「發布共用題庫」。學生開啟原網址或開始新回合即可載入。
6. 完成後登出。權杖只保留在頁面記憶體，不寫入 localStorage、sessionStorage 或儲存庫；重新整理後需再次輸入。權杖到期可在 GitHub 重新建立，遺失可撤銷。

不是 GitHub 帳號密碼，也不是所有學生共用的密碼。GitHub 會在寫入 API 驗證儲存庫權限。存取權杖具有選取儲存庫的內容寫入權限，不只 bank.json，請勿提供給學生。網站及題庫公開，請勿放入私人資料。

舊版在同一瀏覽器儲存的題庫，可在老師登入後按「匯入此瀏覽器舊題庫」，檢查後發布。載入預設題庫只修改草稿，按發布才會影響全班。編輯衝突或發布失敗時保留草稿，並提供 JSON 備份下載。

本版本僅使用 GitHub Pages 及 GitHub REST API，無 Cloudflare 依賴。不儲存學生作答紀錄。

