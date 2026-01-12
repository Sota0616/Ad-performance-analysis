# Ad Performance Analysis (Python)

## 概要
この分析では、広告配信データを用いて  
「どの広告を止めるか／直すか／伸ばすか」を判断するための分析**  
を行った。


## 使用データ
- Kaggle: Shopping Mall Paid Search Campaign Dataset
- 広告配信ログ（CSV）

主なカラム：
- Ad Group
- Impressions
- Clicks
- Conversions
- Cost
- Revenue
- P&L

---

## 分析の流れ

### Step 1：広告単位での集計
Ad Groupごとに広告成果を集計し、  
意思決定に必要な指標を算出。

算出指標：
- CTR = Clicks / Impressions  
- CVR = Conversions / Clicks  
- CPA = Cost / Conversions  

---

### Step 2：判断基準の設定
全広告の実績から  
「1件のコンバージョンで許容できるCPA　を算出し、  
これを赤字判断の基準とした

---

### Step 3：赤字広告の抽出
許容CPAを超過している広告を  
**赤字広告候補** として抽出

---

### Step 4：赤字原因の分解
CPA悪化の要因を  
**CTR（集客） / CVR（転換）** に分解し、  
問題の所在を整理した

分類：
- CTRのみ低い → クリエイティブ・訴求課題
- CVRのみ低い → LP・ターゲット課題
- 両方低い → 停止候補

---

### Step 5：アクション判断
改善余地のない広告を  
**停止候補** として明確にした

---

## この分析で意識したこと
- 指標を見るだけで終わらせない
- 判断基準をより明瞭に
- 次のアクションにつながる形で整理する

---



---

## 使用技術
- Python
- pandas
- Jupyter Notebook

---

## 目的
広告運用における  
**データに基づく意思決定力の習得**
