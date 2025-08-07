# Project_SECOM-PatternMining

專案背景簡介，SECOM 是一組由 UCI Machine Learning Repository 提供的工業製程資料集，完整名稱是 SECOM Manufacturing Data Set。這份資料集來源於一家半導體製造公司（實際公司名稱未公開），主要應用場景用來進行製程品質監控與瑕疵預測（如早期故障偵測、品質異常檢測等）。而本專案目的是從這些大量感測器數據中找出與產品瑕疵（`y=1`）有關的潛在模式與異常。即感測器數據摘要與維度縮減、群組分析（如：以 y 為分群依據來比較感測器行為）

### 🎯 專案目標

1. **群組分析**
   - 以目標變數 `y`（0 = 正常產品，1 = 有缺陷）進行群組分群。
   - 分析各感測器在不同群組下的統計特徵（平均值、標準差、極值等）。

2. **視覺化分析**
   - 使用圖表工具（箱型圖、熱圖、PCA 等）呈現感測器在不同群組中的分布與變異。
   - 協助發現可能關鍵的異常感測器。

### 📊 資料集說明

本專案使用來自 UCI Machine Learning Repository 的 SECOM 製造資料集，其來源為一家半導體製造公司，用以監控製程品質並預測產品是否不良。該資料集為高維感測器資料，常用於資料探勘中的特徵選取、維度縮減、分類建模與異常偵測任務。

- 資料集概覽

| 項目    | 數量                                 |
| ----- | ---------------------------------- |
| 資料筆數  | 1567                               |
| 總欄位數  | 592                                |
| 感測器欄位 | 590 個（欄位名稱為 `0`～`589`）             |
| 時間欄位  | `Time`（1567筆時間戳）            |
| 目標變數  | `Pass/Fail`（`1` = 通過檢測，`-1` = 不合格） |

- 目標變數`y` - Pass/Fail
  - 類別型變數，用來表示每一筆樣本是否為瑕疵產品
  - 資料不平衡，合格產品數量明顯多於不合格

- 資料特性
  - 多數感測器變數存在不同程度的缺失值，部分欄位缺失超過 90%
  - 各感測器變數為連續型資料，但未提供具體單位或感測器名稱（為匿名特徵）
  - 存在大量共線性、零變異或極端值變數，適合進行資料清洗與降維處理

### 🛠️ 使用技術

- Python 3.x
- Pandas / NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

### 🚀 如何使用

```bash
git clone https://github.com/JackLaiplus/Project_MLforInfidelity.git
cd Project_SECOM_PatternMining
pip install -r requirements.txt
jupyter notebook Project_SECOM_PatternMining.ipynb
```
### 📚 參考資料

資料來源： UCI SECOM 資料集 https://archive.ics.uci.edu/dataset/179/secom



