煦衣 Closet v2.0｜Supabase 雲端同步版

本版功能：
- 沿用簡記既有 Supabase 專案及同一個登入帳號（與簡記相同的密碼）。
- 登入方式沿用簡記：畫面輸入密碼，程式使用簡記既有固定登入 Email 完成 Supabase Auth。
- 衣物資料同步至 public.closet_items。
- 主分類及子分類同步至 public.closet_categories。
- 衣物照片上傳至私有 Storage bucket closet-photos。
- 手機與電腦登入同一帳號後使用同一份雲端衣櫥。
- 拍照或選圖時自動縮圖及 JPEG 壓縮（最長邊 1600px，目標約 550KB 以下）。
- 點選衣物照片可全螢幕檢視。
- 保留 IndexedDB 作為本機快取；首次登入若雲端衣櫥為空，會將該裝置原有衣物及分類匯入雲端。雲端已有資料時，雲端資料為主並更新本機快取。

Supabase 設定：
Project URL: https://emwzognoixuvtzafxqlv.supabase.co
Publishable Key: 已寫入前端設定（此為可公開使用的 publishable key；不可將 service_role / Secret key 放入前端）。
登入 Email: peter830924@gmail.com（與簡記 v3.6 相同）
照片 bucket: closet-photos（private）
資料表: closet_items、closet_categories

重要注意：
1. 請使用原本簡記的密碼登入，不要建立新帳號。
2. 每一台裝置第一次登入時，如果雲端尚無衣櫥資料，會匯入該裝置 IndexedDB 的資料；請先在原本有完整衣物資料的裝置登入並完成匯入，再於其他裝置登入。
3. 若雲端已有資料，其他裝置會以雲端資料更新本機資料，不會把另一台裝置的本機未同步資料自動合併。請勿在不同裝置各自建立大量離線資料後才登入同步。
4. 請勿清除瀏覽器網站資料；更新 GitHub Pages 時保留相同網址及網域。
5. 本版使用 Supabase Storage 私有照片及短效簽名網址。資料表 RLS 必須已依照先前 SQL 設定完成。
6. 若首次登入後看到雲端連線或權限錯誤，請先截圖錯誤訊息，不要重複執行 SQL 或刪除資料。

部署：將 ZIP 解壓縮後，覆蓋 GitHub Repository 根目錄中的 index.html、manifest.json、sw.js、README.txt，再 Commit。等待 Pages 更新後，手機及電腦都使用同一個 Pages 網址。
