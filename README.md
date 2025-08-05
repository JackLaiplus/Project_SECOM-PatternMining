# Project_SECOM_PatternMining

一個以 SECOM 來自半導體製造過程的數據為基礎的資料探勘專案，著重於透過群組分析與視覺化探索感測器數據中的潛在模式與異常。

## 📌 專案簡介

本專案針對SECOM - UCI機器學習庫來自半導體製程的資料集進行分析，目的是從大量感測器變數中找出與產品瑕疵（`y=1`）有關的統計差異與潛在模式。
<br><br><br>

## 📊 資料集說明

資料來源： UCI SECOM 資料集 https://archive.ics.uci.edu/dataset/179/secom
樣本數：1567 筆
變數數量：590 個感測器數據（多為連續型）
目標變數：y（0 = OK，1 = Faulty）

## 📊 主要變數說明（SECOM 製造資料集）

| 變數名稱        | 類型     | 說明                                                    |
| ----------- | ------ | ----------------------------------------------------- |
| `Pass/Fail` | 二元類別變數 | **目標變數**。產品是否通過品質檢測：`-1` 代表 Fail（不良品），`1` 代表 Pass（良品） |
| `0`～`589`   | 連續型變數  | 共 590 個**感測器變數**，記錄製程中不同感測器的數值。名稱為數字代號。               |
| `Time`  | 時間型變數  | 資料收集時間戳記                         |

## 🧾 欄位摘要

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

