煦衣 Closet v1.0

檔案內容：
- index.html：衣櫥 App 主程式
- manifest.json：PWA 設定
- sw.js：離線快取

部署：
1. 在 GitHub 建立新的 Public Repository，例如 xuyi-closet。
2. 將 ZIP 解壓縮，將裡面的三個檔案直接上傳到 Repository 根目錄。
3. 到 Settings > Pages。
4. Source 選 Deploy from a branch；Branch 選 main，資料夾選 /(root)，按 Save。
5. 等待 GitHub Pages 部署完成，網址通常為 https://你的帳號.github.io/xuyi-closet/

注意：
本版本使用瀏覽器 IndexedDB 儲存衣物資料及照片，資料留在目前這台裝置／瀏覽器，不會自動跨裝置同步。請勿清除網站資料；跨裝置同步可在下一版加入 Supabase。
