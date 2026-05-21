# skill.md
## Skill Name
Medical Device Regulatory Review Report Generator (Word)

## Skill Purpose
本 Skill 用於自動產生「醫療器材詳細審查報告（Word）」，
依據預先定義之法規與測試項目樣板，
輸出可直接用於：
- FDA 510(k) Supporting Test Report Summary
- TFDA 技術文件
- CE MDR Technical Documentation
- 內部法規審查與測試彙總報告

## Target Output Format
- Microsoft Word (.docx)
- 正式法規文件語氣
- 可編輯表格
- 中文（繁體）為預設語言

---

## Input Schema
### Required Inputs
- 產品名稱（Product Name）
- 製造商（Manufacturer）
- 審查目的（例如：510(k)、TFDA、CE）
- 適用標準清單（可為空，AI 依樣板判定適用性）

### Optional Inputs
- 文件編號前綴規則（如 QA-REP-XXX）
- 出具單位（測試實驗室 / 製造商）
- 是否為軟體醫療器材（Yes / No）

---

## Core Logic（核心邏輯）

### Step 1：建立文件基本資訊
- 文件標題：產品規格審查報告
- 自動填入：
  - 產品名稱
  - 製造商
  - 審查目的
  - 文件編號（可自動生成）

### Step 2：依「法規/測試樣板清單」建立章節
對下列每一項目，**自動建立獨立章節 + 表格**：

#### 標準章節表格格式（固定）
| 欄位 | 內容 |
|---|---|
| 報告名稱 |  |
| 文件編號 |  |
| 出具單位 |  |
| 適用產品 |  |

---

## Review Item Template Library（審查項目樣板庫）

### 性能規格

### 電性安全
- IEC 60601-1

### 電磁相容性
- IEC 60601-1-2

### 生物相容性評估
- ISO 10993

### 警報系統
- IEC 60601-1-8
- （輸液幫浦、中央監護系統等可能適用）

### 雷射生髮帽
- 輸出功率密度
- 輸出功率準確度
- 波長輸出範圍
- 定時功能

### 雷射產品安全
- IEC 60825-1

### 光生物安全
- IEC 62471
- 光譜範圍 200 nm – 3000 nm
- 適用於 LED（不含雷射）
- 紅外線產品可能適用

### 雷射系統（肌肉與關節疼痛緩解）
- 膚色調整（Skin Tone Adjustment）
- 輸出功率與波長比
- 脈衝頻率
- 脈衝持續時間

### 眼科儀器
- ISO 15004-1（基本要求）
- ISO 15004-2（光風險評估）

### 直接眼底鏡
- ISO 10942

### 視網膜鏡（Retinoscope）
- ISO 12865

### 角膜地形測試儀
- ISO 19980

### 視覺功能分析儀
- 淚膜檢查（Tear Film Analysis）
- 乾眼分析

### 診斷用超音波安全
- IEC 60601-2-37
- 探頭表面溫度
- 熱指數（TI）
- 機械指數（MI）
- 超音波能量風險評估
- Freeze 功能
- 中心頻率
- 軸向與側向解析度

### 超音波物理治療設備
- IEC 60601-2-5
- IEC 61689（0.5–5 MHz）

### DICOM 標準影像傳輸

### X 光設備
- IEC 62220-1（影像品質）
- 平板偵測器相容性
- 劑量面積乘積（DAP）
- IEC 60601-2-28（X 光管）
- IEC 60601-1-3（輻射防護）
- IEC 60601-2-54
- IEC 60601-2-43（介入手術）

### CT 用 X 光設備
- IEC 60601-2-44

### 放射治療設備
- IEC 61217（坐標、運動、刻度）

### 電子加速器
- IEC 60601-2-1（1–50 MeV）

### 醫用磁振造影設備（MRI）
- IEC 60601-2-33

### 正子斷層掃描（PET）
- NEMA NU 2-2018

### 輸液幫浦
- IEC 60601-2-24

---

## Advanced AI Features（進階技能）

### Feature 1：適用性自動判定（Applicability Reasoning）
- 依產品類型（軟體 / 硬體 / 能量型）
- 自動標註：
  - Applicable
  - Not Applicable – with rationale

### Feature 2：法規用途對齊檢查
- 自動檢查是否出現：
  - 診斷宣稱
  - 治療宣稱
- 提供法規風險提示（FDA / CE）

### Feature 3：510(k) / CE 技術文件對應標籤
- 每章節自動附加：
  - 可對應之 Technical File / 510(k) Section

---

## Output Rules
- 所有章節皆須存在（即使 Not Applicable）
- 不假設測試結果
- 不自動填入數值
- 保留人工填寫空間
- 生成結果必須可直接儲存為 .docx

---

## Compliance Scope
- FDA 510(k)
- TFDA
- CE MDR
- IEC / ISO 國際標準

## End of Skill
