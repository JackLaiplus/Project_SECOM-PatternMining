# Project_SECOM_PatternMining

本專案以SECOM-UCI機器學習庫中來自半導體製造過程的數據為基礎進行資料探勘分析，著重於透過群組分析與視覺化探索感測器數據中的潛在模式與異常。
<br>

### 📌 專案簡介

SECOM 是一組由 UCI Machine Learning Repository 提供的工業製程資料集，完整名稱是 SECOM Manufacturing Data Set。這份資料集來源於一家半導體製造公司（實際公司名稱未公開），主要目的是用來進行製程品質監控與瑕疵預測（如早期故障偵測、品質異常檢測等）。而本專案目的是從大量感測器變數中找出與產品瑕疵（`y=1`）有關的統計差異與潛在模式。
<br>

### 📊 資料集簡介：

資料來源： UCI SECOM 資料集 https://archive.ics.uci.edu/dataset/179/secom
- 觀測數量（instances）：1567 筆
- 特徵數量（features）：590 個（大部分是感測器數值）
- 變數類型：
-- 主要是連續型感測器數值資料。
-- 有一些欄位代表時間戳或製程條件。
-- y 欄位為二元類別變數（0 或 1），通常代表產品是否達標或製程是否失敗。

### 📊 應用場景：

- 製程監控（Process Monitoring）
- 故障預測（Fault Prediction）
- 感測器數據摘要與維度縮減
- 群組分析（如：以 y 為分群依據來比較感測器行為）

### 📊 主要變數說明（SECOM 製造資料集）

| 變數名稱        | 類型     | 說明                                                    |
| ----------- | ------ | ----------------------------------------------------- |
| `Pass/Fail` | 二元類別變數 | **目標變數**。產品是否通過品質檢測：`-1` 代表 Fail（不良品），`1` 代表 Pass（良品） |
| `0`～`589`   | 連續型變數  | 共 590 個**感測器變數**，記錄製程中不同感測器的數值。名稱為數字代號。               |
| `Time`  | 時間型變數  | 資料收集時間戳記                         |

### 🧾 欄位摘要

- 總欄位數：592 欄位
- 總筆數：1567 筆觀測值
- 感測器欄位：0～589，資料型態為浮點數（含大量缺失值）
- 目標欄位：Pass/Fail，值為 1（合格）或 -1（不合格）

### 🎯 分析目標

1. **群組分析**
   - 以變數 `y`（0 = 正常產品，1 = 有缺陷）進行群組分群。
   - 分析各感測器在不同群組下的統計特徵（平均值、標準差、極值等）。

2. **視覺化分析**
   - 使用圖表工具（箱型圖、熱圖、PCA 等）呈現感測器在不同群組中的分布與變異。
   - 協助發現可能關鍵的異常感測器。

### 🛠️ 使用技術

- Python 3.x
- Pandas / NumPy
- Scikit-learn
- Jupyter Notebook

### 🚀 如何使用

```bash
git clone https://github.com/JackLaiplus/Project_MLforInfidelity.git
cd Project_SECOM_PatternMining
pip install -r requirements.txt
jupyter notebook Project_SECOM_PatternMining.ipynb
```

