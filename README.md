# RetailerLicence-fight

## 專案目的

本 repository 用於建立優選股份有限公司「再生能源售電業申照輔導暨申請服務」的標準文件。現階段已完成客戶用報價單、服務工作範圍書及正式服務契約之最終 Markdown 與 DOCX；三份文件採相同的服務範圍、價格、付款節點、責任分工及完成定義。

## Source hierarchy

歷史文件依下列角色使用：

1. 最新正式服務契約 precedent：提供法律及商務骨架。
2. 最新 SOW precedent：提供服務邊界、完成定義及變更管理結構。
3. 價格附件 precedent：提供未稅、第三方費用、差旅、追加服務及請款異議概念。
4. 過往售電業申照契約：提供實際申照流程及資料清單 precedent。
5. 過往營業規章及售電計畫書：提供真實申請成果的資訊顆粒度。

來源僅作分析與設計參考，不以替換客戶名稱方式重製，也不得將來源個案之客戶、案場、交易對象、價格或財務數字帶入新文件。

## Repository 結構

```text
RetailerLicence-fight/
├─ .gitignore
├─ README.md
├─ sources/                     # 本機機密來源，不得 commit
├─ drafts/                      # 客戶文件 Markdown 草稿
│  ├─ 01_再生能源售電業申照輔導暨申請服務_報價單.md
│  ├─ 02_再生能源售電業申照輔導暨申請服務_SOW.md
│  └─ 03_再生能源售電業申照輔導暨申請服務契約.md
├─ deliverables/                # 由最終 Markdown 生成之正式 DOCX
│  ├─ 01_再生能源售電業申照輔導暨申請服務_報價單.docx
│  ├─ 02_再生能源售電業申照輔導暨申請服務_SOW.docx
│  └─ 03_再生能源售電業申照輔導暨申請服務契約.docx
└─ internal/                    # 內部規格、來源對照及 QA
   ├─ BUSINESS_RULES.md
   ├─ SOURCE_MAP.md
   ├─ OPEN_ISSUES.md
   └─ QA_REPORT.md
```

## 客戶文件

- `drafts/01_再生能源售電業申照輔導暨申請服務_報價單.md`：供客戶內部評估及商務討論，呈現第 0 階段選配、標準完整申照專案、成果、費用與重要範圍說明；本身不作為正式簽約文件。
- `drafts/02_再生能源售電業申照輔導暨申請服務_SOW.md`：精確界定服務內容、交付成果、財務資料責任、客戶配合、完成標準、變更管理及排除事項。
- `drafts/03_再生能源售電業申照輔導暨申請服務契約.md`：完整處理角色分工、付款、確認、暫停、提前終止、責任限制、保密、智慧財產、通知及爭議處理。

## Internal 文件

- `internal/BUSINESS_RULES.md`：本案價格、付款、範圍、責任及法律起草原則，僅限內部使用。
- `internal/SOURCE_MAP.md`：記錄新版條文採用的來源思想、排除內容及本案新設計。
- `internal/OPEN_ISSUES.md`：記錄不宜自行推論、需由 Zac 決定的事項；目前無待決事項。
- `internal/QA_REPORT.md`：記錄跨文件一致性、修正事項、法律審閱建議及 Git 保護狀態。

## 來源文件保護

所有歷史來源均放在 `sources/`，僅允許在本機供本專案分析。`.gitignore` 已排除 `sources/`，該資料夾不得 staged、tracked 或 commit。如發現來源已被追蹤，應停止相關 Git 操作並記錄於 `internal/OPEN_ISSUES.md`，不得刪除來源或進行破壞性處理。

## 本輪狀態

- Final patch：已完成第 0 階段付款、完成、期間、暫緩、提前終止及第一筆 NT$100,000 請款分流之最終商業條件同步。
- Final Markdown：三份客戶文件均已完成，`internal/OPEN_ISSUES.md` 已關閉，無待決商業事項。
- Cross-document QA：已通過，標準 NT$450,000、正常付款 NT$100,000／200,000／150,000，以及 NT$275,000／375,000 終止結算均維持一致。
- DOCX：三份正式文件已生成至 `deliverables/`。
- Generated-DOCX verification：已完成程式化內容檢查及逐頁渲染檢查；關鍵金額、條文、表格、簽署欄與禁用字樣均驗證通過。
- 本輪未生成 PDF。

## 下一步

1. Zac 人工審閱最終 Markdown 與 DOCX。
2. 由法律專業人士確認提前終止服務費、確認機制、責任限制及其他重要法律條款。
3. 依實際客戶選擇勾選第 0 階段，並填入客戶、報價、聯絡及簽署資訊。
4. 完成必要之個案化法律、商務及版面確認後，再提供客戶。
