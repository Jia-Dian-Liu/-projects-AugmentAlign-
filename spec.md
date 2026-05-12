# Spec.md: AugmentAlign (智協科技顧問) 專案規格說明書

---

## A 區：公司精神（Manifesto 精簡版）

### 我們的信仰：不為取代，只為互補 (Not to replace, but to complement)

在 AI 代理人（Agent）技術鋪天蓋地的變革浪潮中，**AugmentAlign (智協科技顧問)** 堅信：技術的終極價值絕非消滅人類的崗位，而是重塑人機協作的邊界，釋放人類的創造力。

根據 Morgan Stanley 報告的歷史科技規律，蒸汽、電力與網際網路等創新浪潮，初期皆會對「常規、可自動化任務」造成局部衝擊（特別是 22–27 歲的年輕初階白領）。然而，當產業與教育調適完成後，新技術將透過**「互補效應（Complementarity）」**，將人類的生產力年成長率推向歷史頂峰。

我們拒絕盲目的裁員與冷酷的自動化。我們的使命是協助面臨轉型陣痛的中小企業與年輕專業者，將枯燥的「常規文書與代碼處理」完全託付給客製化的 AI Agent，引導人類升級為**「決策者、監督者與最終把關者」**。

我們用技術為人類搭起階梯，而非用技術搶走人類的飯碗。這是資工系畢業生應有的技術擔當，也是 AugmentAlign 的立業之本。

---

## B 區：服務目錄（服務套餐 & 招牌服務）

### 1. 服務套餐
為了降低中小企業與部門主管導入 AI 的門檻，我們將顧問與開發服務歸納為以下三大套裝方案：

#### 套餐 A：【AI 轉型與業務常規診斷套裝】(AI Readiness Evaluation)
* **適用對象**：想引入 AI 但不知道從何做起、不清楚哪些職位可以被增強的中小企業。
* **服務內容**：
    * 企業組織架構與工作流程掃描（Flow Diagnostics）。
    * 鑑定高暴露、高度常規（Routine）之工作流程。
    * 提供一份精準的《AI 轉型與 Agent 導入可行性評估報告》。
* **交付時間**：1 - 2 週。

#### 套餐 B：【企業知識無形資產庫 RAG 套裝】(Enterprise Knowledge RAG)
* **適用對象**：內部擁有大量 PDF、專利、合約或財報，需要精準內部檢索、防範 AI 幻覺的事務所（法律、會計、代書等）。
* **服務內容**：
    * 架設企業專屬向量資料庫（Milvus / Pinecone / ChromaDB）。
    * 建立自動化數據清洗與導入管線（Data Pipeline）。
    * 部署專屬 RAG 知識檢索 Agent，消除 AI 幻覺。
* **交付時間**：3 - 4 週。

#### 套餐 C：【客製化多代理人協作套裝】(Custom Multi-Agent Workflow)
* **適用對象**：行銷、行政、初階開發部門主管，需要自動化跨平台、複雜且具備多角色的協同工作流。
* **服務內容**：
    * 基於 CrewAI 或 AutoGen 框架客製化開發多代理人矩陣（如：行銷小編 Agent、程式碼優化 Agent）。
    * 部署網頁端「人類把關控制台」（React/Vue Dashboard）。
    * 串接企業現有通訊工具（Slack / Line / Email / Notion）。
* **交付時間**：5 - 8 週。

---

### 2. 招牌服務：【Human-in-the-Loop 流程重新設計】
* **核心特色**：此為 AugmentAlign 的靈魂服務。我們不提供「全自動化且無人看管」的黑盒子方案。
* **運作機制**：所有部署的 Agent 矩陣不論如何高效，其產出的最終結果（文案、代碼、報告）皆會強制暫停於控制台的「任務審核區（Oversight Panel）」。必須經由客戶公司的「人類員工（特別是年輕初階白領）」進行審查、潤飾，點擊確認後方可發佈。
* **商業價值**：將員工從「繁瑣的執行者」升級為「高價值的監督者與把關人（Reviewer）」，在保證企業輸出品質零出錯的前提下，將部門整體生產力大幅拉升。

---

## C 區：3 位 Specialists 的角色與定位

在 AugmentAlign 中，我們的專案由三位各司其職的 AI 專家負責開發與設計。以下是他們的完整規格：

### 1. 知識儲存與數據架構師 (Data & RAG Architect)
* **我是誰**：負責企業大腦「數據根基與無形資產整合」的技術專家。
* **會做什麼**：
    * 設計高可用性、高併發的向量資料庫架構與索引策略。
    * 開發無形資產自動清洗、分塊（Chunking）、向量化與寫入的 ETL Data Pipeline。
    * 優化檢索演算法（如混合檢索 Hybrid Search、重排重分 Reranking），杜絕 AI 模型幻覺。
* **不做什麼**：
    * 不做前端網頁 UI 刻板與 CSS 美化。
    * 不負責編寫高層的 Agent 人格特質（Prompt）與對話邏輯。
* **Quality Gate (品質關卡)**：
    * **資料管線延遲性**：新增文檔在 5 分鐘內必須完成向量化並可被檢索。
    * **檢索準確度 (Recall/Precision)**：在測試數據集上，檢索相關文檔的 Top-5 準確度（Recall@5）必須大於 90%。

### 2. 多智能體工作流工程師 (Multi-Agent Workflow Engineer)
* **我是誰**：負責將多個單一 AI 串聯成「協作團隊與工作鏈」的系統架構師。
* **會做什麼**：
    * 使用 CrewAI, AutoGen 或 LangGraph 框架，設計 Agent 之間的溝通協議、決策邏輯與回退機制（Fallback）。
    * 優化 Agent 的 System Prompt、Few-shot 範例與 Tool Calling 的穩定度。
    * 配置 Agent 的記憶體機制（Short-term & Long-term memory）。
* **不做什麼**：
    * 不負責底層向量資料庫效能優化與硬體部署。
    * 不負責網頁控制台的使用者體驗與版面佈局。
* **Quality Gate (品質關卡)**：
    * **工具調用成功率 (Tool Calling Rate)**：在 100 次連續測試中，Agent 成功調用外部工具與 API 的機率必須達 95% 以上。
    * **死鎖避免 (Deadlock Prevention)**：Agent 協同對話中，單次任務流程的對話迭代上限（Max Iterations）強制限制在 15 次以內，避免發生死鎖或無限循環，保障運行成本。

### 3. 人機協作介面設計師 (Oversight Interface Designer)
* **我是誰**：負責「人機協作中樞」及「人類最終把關 Dashboard」的使用者體驗與系統開發工程師。
* **會做什麼**：
    * 使用 React / Vue 開發「Oversight Panel（任務審核區）」與「系統監控面板（Analytics）」。
    * 利用 FastAPI/Node.js 建立高響應速度的後端 API，將 Agent 異步處理的狀態透過 WebSocket 即時推送至前端。
    * 設計友善的人類干預（Human-in-the-Loop）修改機制與一鍵審批流程。
* **不做什麼**：
    * 不撰寫 Prompt，也不調研 LLM 的參數量與演算法效能。
    * 不碰數據清洗與向量化管線。
* **Quality Gate (品質關卡)**：
    * **前端響應時間**：Dashboard 任務載入與頁面切換時間必須在 1 秒以內。
    * **操作流失率**：人類審批一項 Agent 產出，操作步驟不得超過 2 個點擊行為。

---

## D 區：COO 的工作流程 (Chief Operating Officer Workflow)

COO 負責串聯三位 Specialist 的產出，控管專案從零到交付客戶的生命週期。工作流標準作業程序（SOP）如下：

```
 [ 步驟 1：客戶業務診斷與流程掃描 ] (COO 主導)
                 │
                 ▼
 [ 步驟 2：技術規格拆解與任務派發 ] (COO 拆解，派發至 Specialist)
                 │
                 ├─► 知識架構師 (資料庫與管線)
                 ├─► 工作流工程師 (Agent 矩陣設計)
                 └─► 介面設計師 (把關 Dashboard)
                 │
                 ▼
 [ 步驟 3：三方技術模組整合與測試 ] (COO 監督 Quality Gate)
                 │
                 ▼
 [ 步驟 4：人機協調沙盒演練 (Sandboxing) ] (COO 與客戶員工實測)
                 │
                 ▼
 [ 步驟 5：上線交付與技能重塑手冊培訓 ] (COO 完成最後交付)
```

### COO 的四大核心職責與檢核標準

1.  **客戶流程拆解與評估 (Step 1 - 2)**：
    * COO 進入客戶現場進行「常規與非常規任務」拆解，轉譯為技術規格。例如：將律師助理的「找過去案例、整理摘要、撰寫比對報告」拆解為「向量庫、Data-Agent、Draft-Agent、審核 UI」四大部分，派發給對應的 Specialist。
2.  **跨 Specialist 品質看守與整合 (Step 3)**：
    * COO 在整合期必須扮演專案總指揮。他必須檢視**資料庫、Agent 矩陣、Dashboard 系統**三者之串聯。
    * 嚴格把關三位 Specialist 的 **Quality Gate** 是否全數通過。
3.  **沙盒演練與安全回饋 (Step 4)**：
    * 在正式部署前，COO 負責在沙盒環境（Sandbox）進行壓力測試，模擬 Agent 出現幻覺、API 斷線、使用者誤按批准等異常情況，建立系統的回滾機制（Rollback）。
4.  **轉型引導（Reskilling）與驗收 (Step 5)**：
    * COO 負責撰寫《員工技能重塑手冊》，並親自為客戶的 22-27 歲年輕初階員工進行「如何從執行者轉型為 AI 監督者」的教育訓練。唯有當客戶員工能流暢操作控制台、完成審批，專案才算正式驗收。

---

## E 區：Deliverable 結構 (交付物結構清單)

當專案完成，我們交付給客戶的實體與虛擬產品，其代碼庫與文檔結構規範如下：

```
augmentalign-project-delivery/
├── README.md                           # 專案總覽、快速啟動指引與架構說明
├── config.env                          # 環境變數與 API 密鑰配置文件
│
├── 📁 01_core-dashboard/                # 產品一：核心協同控制台 (Web 系統原始碼)
│   ├── frontend/                       # React / Vue 網頁前端原始碼
│   │   ├── src/components/Oversight/   # 核心「任務審核區」UI 元件
│   │   └── src/components/Analytics/   # 生產力與工時節省統計圖表
│   └── backend/                        # FastAPI / Node.js 後端服務原始碼
│       ├── api/v1/endpoints/           # 任務審批、Agent 狀態即時推送 API
│       └── websockets/                 # 即時任務更新推送機制
│
├── 📁 02_agent-matrix/                 # 產品二：客製化多代理人矩陣 (AI 核心引擎)
│   ├── agents/                         # CrewAI / AutoGen 代理人角色 Prompt 與配置
│   │   ├── crawler_agent.py            # Data-Agent: 數據爬取與監控
│   │   ├── draft_agent.py              # Draft-Agent: 內容/報告草稿生成
│   │   └── rag_agent.py                # RAG-Agent: 內部知識庫精準檢索與比對
│   ├── tools/                          # Agent 可調用的自定義工具集 (Python Scripts)
│   └── Dockerfile                      # 容器化包裝，支援 AWS / GCP 或本地一鍵部署
│
├── 📁 03_data-pipeline/                # 產品三：企業無形資產向量資料庫架構
│   ├── schemas/                        # 向量資料庫（Schema）定義檔
│   ├── pipeline/                       # PDF, Word 數據清洗、切分（Chunking）與上傳管線
│   └── assets/                         # 客戶初始化無形資產資料夾 (機密加密)
│
└── 📁 04_documentation/                # 產品四：企業轉型與操作培訓文檔
    ├── 01_AI_Readiness_Report.pdf      # 業務診斷、常規掃描與生產力評估報告
    ├── 02_Reskilling_Manual.pdf        # 員工技能重塑與人機協同操作指南
    └── 03_System_Architecture.pdf      # 系統架構圖與資安合規白皮書
```

### 交付標準規範
* **程式碼品質**：所有 Python/JavaScript 程式碼必須通過 Linter（如 Flake8, ESLint），且附帶單元測試覆蓋率（Unit Test Coverage）不低於 80%。
* **部署環境**：系統必須能在單一台 Ubuntu 22.04 LTS 或 Docker 容器環境中，透過 `docker-compose up --build` 指令在 10 分鐘內一鍵部署完成。
* **資安防護**：向量資料庫與 API 傳輸必須採用 TLS 1.3 加密，所有客戶機密數據不得在外部公共 LLM 伺服器留存紀錄。
