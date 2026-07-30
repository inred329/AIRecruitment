# AI 招募對話與面試預約系統需求目錄種子版

> 文件編號：AIR-REQ-001  
> 版本：v0.1 Draft  
> 狀態：Draft  
> 最後更新：2026-07-30

---

# 1. 文件目的

本文件依目前流程圖與初步討論建立第一版需求候選清單，供後續 Discovery 訪談、SRS、SAD、WBS、測試與報價追蹤使用。

目前所有需求均未完成正式確認，因此不得直接視為最終驗收範圍。

---

# 2. 需求管理規則

## 2.1 需求狀態

| 狀態 | 定義 |
|---|---|
| Confirmed | 已由具決策權之利害關係人確認 |
| Proposed | 由現有資料或規劃推導，尚待確認 |
| T.B.D. | 已知需要定義，但內容仍不明確 |
| Deferred | 延後至後續階段 |
| Rejected | 已決議不採用 |

## 2.2 優先度

| 優先度 | 定義 |
|---|---|
| Must | 缺少即無法完成該階段核心目標 |
| Should | 對使用價值或品質有顯著影響 |
| Could | 可增加便利性，但可延後 |
| Won't | 明確不納入目前階段 |

## 2.3 階段

| 階段 | 定義 |
|---|---|
| Discovery | 需求尚在訪談與驗證中 |
| PoC | 驗證核心流程與技術可行性 |
| MVP | 支援單一公司小規模正式營運 |
| Future | 後續擴充 |

---

# 3. 需求領域

| 代碼 | 領域 |
|---|---|
| CAM | 廣告與招募入口 |
| MSG | 對話通路整合 |
| JOB | 職缺管理 |
| CONV | 求職者對話流程 |
| CAND | 候選人與人才資料 |
| SCREEN | 初步篩選與適配判斷 |
| REVIEW | 人工覆核與人工接手 |
| SCHED | 面試時段與預約 |
| NOTICE | 通知與提醒 |
| CONSENT | 個資告知與同意 |
| ADMIN | 管理後台 |
| AUDIT | 操作、對話與決策紀錄 |
| INT | 外部系統介接 |
| OPS | 維運與異常處理 |
| NFR | 非功能需求 |

需求 ID 建立後不得重複使用。取消需求應保留編號並標示狀態。

---

# 4. 初始需求候選

| ID | 需求名稱 | 階段候選 | 優先度候選 | 狀態 |
|---|---|---|---|---|
| CAM-001 | 提供由招募廣告進入對話的入口 | PoC | Must | Proposed |
| MSG-001 | 接收求職者由 Messenger 傳入的訊息 | PoC | Must | Proposed |
| MSG-002 | 將系統回覆傳回 Messenger | PoC | Must | Proposed |
| MSG-003 | 保存對話識別資訊與處理狀態 | PoC | Must | Proposed |
| MSG-004 | 支援對話中斷後續接 | MVP | Should | Proposed |
| JOB-001 | 建立與維護職缺基本資料 | PoC | Must | Proposed |
| JOB-002 | 定義職缺必要條件與初步篩選條件 | PoC | Must | T.B.D. |
| JOB-003 | 支援多職缺管理 | MVP | Must | Proposed |
| CONV-001 | 依招募流程與求職者進行初步對話 | PoC | Must | Proposed |
| CONV-002 | 蒐集求職者基本資料與應徵資訊 | PoC | Must | Proposed |
| CONV-003 | 處理求職者答非所問或資料不足 | MVP | Should | T.B.D. |
| CONV-004 | 求職者可要求人工協助 | MVP | Should | T.B.D. |
| CAND-001 | 建立或更新求職者人才資料 | PoC | Must | Proposed |
| CAND-002 | 保存對話紀錄與候選人關聯 | PoC | Must | Proposed |
| CAND-003 | 查詢求職者是否已有既存人才紀錄 | PoC | Should | Proposed |
| CAND-004 | 處理重複候選人資料 | MVP | Should | T.B.D. |
| CAND-005 | 管理候選人處理狀態 | MVP | Must | Proposed |
| SCREEN-001 | 依職缺條件產生初步適配結果 | PoC | Must | Proposed |
| SCREEN-002 | 保存適配結果及其依據 | PoC | Must | Proposed |
| SCREEN-003 | 對資料不足或低信心結果標示人工處理 | MVP | Must | Proposed |
| SCREEN-004 | AI 不直接做最終錄取或淘汰決策 | PoC | Must | Proposed |
| REVIEW-001 | 專員可查看 AI 初篩結果 | PoC | Should | Proposed |
| REVIEW-002 | 專員可覆核或調整候選人狀態 | MVP | Must | Proposed |
| REVIEW-003 | 保存人工修改前後結果與理由 | MVP | Should | Proposed |
| SCHED-001 | 查詢面試相關人員可用時段 | PoC | Must | Proposed |
| SCHED-002 | 提供求職者選擇可預約時段 | PoC | Must | Proposed |
| SCHED-003 | 建立面試預約 | PoC | Must | Proposed |
| SCHED-004 | 建立預約前再次檢查時段衝突 | PoC | Must | Proposed |
| SCHED-005 | 支援面試改期與取消 | MVP | Should | Proposed |
| SCHED-006 | 支援面試提醒 | MVP | Should | Proposed |
| NOTICE-001 | 面試建立後通知求職者 | PoC | Must | Proposed |
| NOTICE-002 | 面試建立後通知專員或面試官 | PoC | Must | Proposed |
| NOTICE-003 | 通知失敗時保存錯誤狀態 | MVP | Must | Proposed |
| CONSENT-001 | 蒐集個人資料前提供告知內容 | PoC | Must | T.B.D. |
| CONSENT-002 | 保存求職者同意紀錄 | MVP | Must | T.B.D. |
| CONSENT-003 | 支援個資更正或刪除處理 | Future | Should | T.B.D. |
| ADMIN-001 | 管理者可查看候選人清單 | PoC | Must | Proposed |
| ADMIN-002 | 管理者可查看候選人詳細資料與對話 | PoC | Must | Proposed |
| ADMIN-003 | 管理者可維護職缺與篩選條件 | MVP | Must | Proposed |
| ADMIN-004 | 提供基本角色與權限管理 | MVP | Must | Proposed |
| ADMIN-005 | 提供基本統計與狀態查詢 | MVP | Should | Proposed |
| AUDIT-001 | 保存訊息、判斷、資料異動與預約結果 | PoC | Must | Proposed |
| AUDIT-002 | 保存管理者操作與人工覆核歷程 | MVP | Must | Proposed |
| INT-001 | 串接單一 Meta Messenger 粉絲專頁 | PoC | Must | Proposed |
| INT-002 | 串接單一行事曆來源 | PoC | Must | Proposed |
| INT-003 | 串接 Email 通知服務 | PoC | Must | Proposed |
| INT-004 | 串接 LINE 通知或其他通知通路 | Future | Could | T.B.D. |
| OPS-001 | 外部服務失敗時保存錯誤 | PoC | Must | Proposed |
| OPS-002 | 支援失敗工作重新執行 | MVP | Must | Proposed |
| OPS-003 | 建立基本備份與監控 | MVP | Must | Proposed |
| NFR-001 | 定義個人資料存取與保存規則 | Discovery | Must | T.B.D. |
| NFR-002 | 定義預估使用量與效能目標 | Discovery | Must | T.B.D. |
| NFR-003 | 管理介面以桌面瀏覽器操作為主 | PoC | Should | Proposed |
| NFR-004 | 第一階段以繁體中文為主 | PoC | Must | Proposed |
| NFR-005 | 系統應保留可追蹤之處理與錯誤紀錄 | PoC | Must | Proposed |

---

# 5. 目前不得直接確認的項目

下列內容仍屬技術或流程候選，需透過 Discovery 決策：

- 使用 Make、n8n 或自行開發流程引擎。
- 使用 Claude、OpenAI 或其他 AI 模型。
- 採 Google Calendar 或 Microsoft 365。
- 透過 LINE、Email 或其他管道通知。
- AI 初篩後直接預約或先由人工核准。
- 黑名單的存在、來源與使用規則。
- 人才庫為新建或介接既有 ATS、CRM。

---

# 6. 後續治理要求

每項需求完成訪談後，至少應補充：

- 業務目的。
- 觸發條件。
- 主要角色。
- 正常流程。
- 例外流程。
- 輸入與輸出資料。
- 權限與個資要求。
- 驗收條件。
- 階段、優先度與狀態。
- 對應流程、設計、WBS 與測試案例。
