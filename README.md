# NLP_w_Disaster_Tweets_practice
# 應用大型語言模型辨別社群媒體上的災難資訊
#### 許耀文
## Introduction: 
有鑑於社群媒體在現今的日常生活中已經逐漸成為我們重要的消息來源之一，
且最即時的第一手資訊都是先於社群媒體上傳播，
故若能有效的程式化監控來挑選出真正的災難消息，
可以輔助救災組織與新聞媒體做更有效率的安排。
但現今主要碰到的問題是，許多情況下，
難以清楚的分辨是否為真正的在宣告一場災難，
例如: The sky last night it was ablaze. 這句中的ablaze是較為模糊隱喻的，
對人類來說可能是可以清楚理解的，但對於機器來說不一定總是如此。
故此次主題為嘗試建立一個機器學習模型預測哪些推特上的推文哪些是關於真正的災難。

## Proposed Methods: 
本次機器學習模型選用 KerasNLP 的 DistilBERT 預訓練模型。
BERT（Bidirectional Encoder Representations from Transformers）為基於Transformers模型的一種變體，
擅長學習和理解語言的內容。
BERT 和其他Transformer 編碼器架構在 NLP的各種任務上取得了巨大成功。
它們計算適合在深度學習模型中使用的自然語言的向量空間表示。
BERT 系列模型使用 Transformer 編碼器架構在前後所有標記的完整上下文中處理輸入文字的每個標記，因此得名。
BERT 模型通常在大型文字語料庫上進行預先訓練，然後針對特定任務進行微調。
DistilBERT 模型是 BERT 模型的蒸餾(distilled)形式。
透過預訓練階段的知識蒸餾，BERT 模型的大小減少了 40%，同時保留了 97% 的語言理解能力，速度提高了 60%。
預計步驟為: 載入災難推文 → 探索資料集 → 預處理數據 → 從 Keras NLP 載入 DistilBERT 模型 → 訓練自己的模型，微調 BERT → 產生提交文件

## Expected Result & Impact: 
會把訓練後的模型，拿去給預先設定好另外的測試資料來分析，
判斷出哪些是真正的災難，把認為是的預測標記為 1，否的預測標記為 0，分析準確率為何。
並使用F1 評估的計算方式判斷這個模型的表現優劣。

## 資料集來源: 
Kaggle-Natural Language Processing with Disaster Tweets

## 實作的程式碼連結: 
[程式碼連結](https://colab.research.google.com/drive/1mCWCBwt7RXITSOjRBAvhRQ3FwES1P5Cy?usp=sharing 
)
