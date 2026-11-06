煦衣 Closet v1.2

檔案內容：
- index.html：衣櫥 App 主程式
- manifest.json：PWA 設定
- sw.js：離線快取

本版新增：
- 類別管理：新增、改名、刪除類別
- 上下移動調整類別順序
- 刪除已有衣物的類別時，可先將衣物移轉至其他類別
- 類別資料會保存在瀏覽器資料庫中

部署：
1. 在 GitHub 建立新的 Public Repository，例如 xuyi-closet。
2. 將 ZIP 解壓縮，將裡面的檔案直接上傳到 Repository 根目錄。
3. 到 Settings > Pages。
4. Source 選 Deploy from a branch；Branch 選 main，資料夾選 /(root)，按 Save。
5. 等待 GitHub Pages 部署完成，網址通常為 https://你的帳號.github.io/xuyi-closet/

資料儲存提醒：
本版本使用瀏覽器 IndexedDB 儲存衣物資料、照片及類別，資料留在目前這台裝置／瀏覽器，不會自動跨裝置同步。請勿清除網站資料；跨裝置同步可於後續版本加入 Supabase。
若你已使用 v1.0，請用本版檔案覆蓋原 Repository 的 index.html、manifest.json、sw.js；瀏覽器資料庫會升級，原有衣物資料會保留。


v1.2 修正與新增：
- 修正主程式中的語法錯誤，恢復新增／編輯衣物及類別管理功能。
- 類別支援自訂子分類，可新增、改名及刪除。
- 新增衣物時可選擇主分類與子分類；既有資料會保留。
- 更新離線快取版本，避免舊程式持續被快取。
