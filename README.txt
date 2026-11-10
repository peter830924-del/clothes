煦衣 Closet v2.3｜雲端同步＋主／子分類篩選＋新增日期時間

本版更新：
1. 新增／編輯衣物表單在「尺寸」旁增加「日期時間」，新增時預設為目前裝置的當地日期與時間，並可自行修改。舊衣物若沒有日期時間，會以原有建立時間帶入；既有 created 欄位保留，不影響原有資料。
2. 移除主畫面的品牌／顏色／尺寸文字搜尋欄位及其篩選邏輯。
3. 移除「最近新增」排序選項，保留「類別排序」及「品牌排序」。
4. 保留主分類、子分類篩選及既有 Supabase 雲端同步。
5. Service Worker 快取更新為 xuyi-closet-v6。

更新方式：
1. 解壓縮本 ZIP。
2. 將 index.html、manifest.json、sw.js、README.txt 覆蓋 GitHub Repository 根目錄同名檔案。
3. Commit changes，等待 GitHub Pages 部署完成。
4. 關閉煦衣頁面後重新開啟原網址。

注意：不要清除網站資料或 IndexedDB，以免刪除尚未同步的本機衣物資料。

【v2.5 自動更新】
本版加入 Service Worker 主動更新檢查。GitHub Pages 發布新檔後，已安裝的 PWA 在下次連線開啟時會檢查新版，安裝完成後自動重新載入。離線時會使用快取版本。此更新不會清除 IndexedDB 或 Supabase 衣物資料。

發布時請將 ZIP 內全部檔案覆蓋 GitHub 專案根目錄同名檔案並 Commit。若更新剛發布但手機尚未連線，待網路恢復後重新開啟 App 即會再檢查。
