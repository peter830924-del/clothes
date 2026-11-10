煦衣 Closet v2.2｜雲端同步＋主／子分類篩選

本版修正：
1. 主畫面明確顯示「主分類篩選」及「子分類篩選」兩個下拉選單。
2. 手機版改為兩欄排列，兩個篩選選單不會被擠出畫面。
3. Service Worker 快取版本更新為 xuyi-closet-v5，啟用時清除舊版快取。
4. 保留既有 Supabase 雲端同步及原有衣物資料處理方式。

更新方式：
1. 解壓縮本 ZIP。
2. 將 index.html、manifest.json、sw.js、README.txt 覆蓋 GitHub Repository 根目錄同名檔案。
3. Commit changes，等待 GitHub Pages 部署完成。
4. 關閉煦衣頁面後重新開啟。若仍顯示舊畫面，請完全關閉瀏覽器分頁再開啟原網址。

注意：不要清除網站資料或 IndexedDB，以免刪除尚未同步的本機衣物資料。
