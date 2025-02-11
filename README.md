# 📊 2024 電商銷售數據分析：探索夏季銷售額下降原因  

## 🎯 專案目標  
本專案旨在透過 **Python 資料分析工具**，深入探討不同時間段的產品銷售表現，分析影響銷售額的因素。  

## 🚀 專案功能與特色  

- **季節性銷售分析**：找出哪個季節的銷售表現最佳？哪個季節銷售額最低？  
- **夏季低銷售產品分析**：夏季銷售表現最差的品項，探討可能的影響因素。  
- **技術與工具**：  
  - 資料處理：`Pandas`、`NumPy`  
  - 視覺化：`Matplotlib`、`Seaborn`  
  - 統計檢定：`ttest_ind`、`chi2_contingency`  

## 📂 資料來源  

- **數據集**：[Kaggle - E-commerce Sales Data 2024](https://www.kaggle.com/datasets/datascientist97/e-commerece-sales-data-2024/data)  
- **主要檔案**：`customer_details.csv`  
- **數據欄位**：  
  - **消費者屬性**：性別、年齡  
  - **購買資訊**：購買商品、訂單季節、購買金額、消費頻率、顧客評分  

## 📊 分析結果與結論  

### 🏷 人口統計分析  
1. **主要客群**：  
   - **30 歲以下男性** 為 2024 年主要消費群體，特別偏好 **帽 T、毛衣、外套、襯衫**。  
   - **年輕女性** 在多種類別商品的銷售表現較差，尤其是 **帽 T、毛衣、外套**。  
   - **50-60 歲男性** 在 **毛衣、手套** 類別的消費額較高，而 **60 歲以上女性** 在這些品項的購買力相對較低。  

### ❄️ 夏季銷售低迷的商品  
1. **異常現象**：  
   - **短裙、短袖、襯衫** 這些典型的 **夏季商品**，反而在夏季銷售表現最差。  
   - **毛衣、帽 T** 這類冬季商品在夏季銷售不佳，並且經過 `ttest` 驗證後，確定 **夏季與冬季的銷售額存在顯著差異**。  

### 🎯 顧客分群分析  
根據每位顧客過去的購買次數，將其購買力分為三組（**低購買力、中購買力、高購買力**），並分別觀察四季的銷售額表現。  

- **低 & 高購買力客群**：購買行為受 **季節與外部因素影響較大**，特別是在折扣較多的 **秋冬季**，銷售額顯著提升。  
- **中購買力客群**：除了夏季銷售額較低，其他季節的購買行為變化較小。  

## ⚠️ 此份資料集的限制  

- **單一商品購買**：  
  - 每位顧客的數據僅記錄單次購買，無法分析購物籃組合（Basket Analysis）或顧客回購率，限制了交叉銷售（Cross-selling）與顧客忠誠度的研究。  

- **產品資訊缺乏**：  
  - 數據集中 **缺少產品詳細資訊**（如庫存數量、尺寸等），無法進行庫存管理、產品組合分析或需求預測（Demand Forecasting）。  

- **折扣與優惠券使用偏誤**：  
  - 數據顯示，只有 **男性顧客** 使用優惠券，這可能反映了數據收集過程中的偏誤，影響了對折扣影響銷售的評估。  
