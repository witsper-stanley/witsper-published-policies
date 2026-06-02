# WitsPer 已公佈制度文件 Archive

WitsPer 內部正式公佈過之制度文件 archive。**Read-only 公告欄 + 永久不可修改 archive**。

> 對齊 [Draft repo `witsper-operating-cadence`](https://github.com/witsper-stanley/witsper-operating-cadence) Record paradigm:Draft repo 是設計 / 迭代場域,本 repo 是公佈版的不可變留底。

---

## 結構

```
witsper-published-policies/
├── README.md                                          ← 本檔(總索引)
└── <章資料夾>/
    ├── <文件名>_v<N>_<YYYY-MM-DD>.pdf                 ← 公佈版 PDF(讀者主要看的)
    └── source-snapshot/
        └── <文件名>_v<N>_<YYYY-MM-DD>.md              ← 當時 source markdown snapshot(audit 用 backup)
```

**讀者拿到 PDF 即可**;`.md` snapshot 是 audit / IPO 籌備期會計師或投資人要看「公佈當下 source 長什麼樣」時 dig 用,放 `source-snapshot/` 子資料夾不擋讀者視線。

**檔名慣例**:`<文件名>_v<N>_<YYYY-MM-DD>.<ext>`

範例:
- `04_我們怎麼保護自己/電腦設備管理原則_v1_2026-06-01.pdf`
- `04_我們怎麼保護自己/source-snapshot/電腦設備管理原則_v1_2026-06-01.md`

---

## 已公佈 entries

| 文件 | 公佈版本 | 公佈日期 | 對應 source draft | 狀態 |
|---|---|---|---|---|
| [電腦設備管理原則](./04_我們怎麼保護自己/電腦設備管理原則_v1_2026-06-01.pdf) | Version 1 | 2026-06-02 | v1.0 | Active(試行至 2026-07-01) |
| [天然災害停班出勤原則](./04_我們怎麼保護自己/天然災害停班出勤原則_v1_2026-06-01.pdf) | Version 1 | 2026-06-02 | v1.0 | Active(試行至 2026-07-01) |
| [資訊需求提出指引(試行版)](./04_我們怎麼保護自己/資訊需求提出指引_試行版_v1_2026-06-01.pdf) | Version 1 | 2026-06-02 | v1.0 | Active(試行至 2026-07-01) |

完整 publication metadata(對應 source draft / 公佈摘要 / 公佈管道 等)見 [Draft repo《公佈紀錄》Standard §3](https://github.com/witsper-stanley/witsper-operating-cadence/blob/main/04_%E6%88%91%E5%80%91%E6%80%8E%E9%BA%BC%E4%BF%9D%E8%AD%B7%E8%87%AA%E5%B7%B1/%E5%85%AC%E4%BD%88%E7%B4%80%E9%8C%84_Standard.md)。

---

## 操作原則

### 本 repo 不接受修改

公佈版**永久不可修改**(immutable archive)。如該制度有變動,要走「重新公佈」流程:

1. 在 Draft repo 改 source draft(v1.0 → v1.1 → ... → 達到 substantive change)
2. 走《核決權限表》核准重新公佈
3. Render 新公佈版 PDF
4. 在**本 repo** commit 新 PDF(放章資料夾)+ source snapshot(放 `source-snapshot/` 子資料夾),檔名用新 Version N+1
5. 在 Draft repo《公佈紀錄》§3 新增一筆 Version N+1 entry,前一筆 Version N 狀態改 Superseded

### 本 repo 不接受留言

留言 / feedback / 質疑請去 [Draft repo](https://github.com/witsper-stanley/witsper-operating-cadence) 對應 source 的討論 Issue(每份 source 都有自己的 Issue,連結見 source Sidecar)。

本 repo 為 archive,**Issues / Wiki / Discussions 都關了**。

### 維護者極少

預設只有 BEO 大隊主管(目前 = Stanley)維護。視實際需要再加 backup(如 CFO)。

---

## 為什麼跟 Draft repo 分開

| 維度 | Draft repo(`witsper-operating-cadence`)| 本 repo(`witsper-published-policies`)|
|---|---|---|
| 性質 | 設計探索、迭代、待解問題、實驗 | 不可變 archive、公告欄 |
| Maintainers | 多人(Stanley + leaders + collaborators) | 極少(BEO 主管) |
| 修改頻率 | 頻繁(每天) | 罕見(每次正式公佈才動) |
| Issues 互動 | 每份 source 有討論 Issue | 關閉(留言去 Draft repo) |
| 對 audit / IPO | 設計過程透明 | 公佈版永久留底 |
| Git history | 設計演化軌跡 | 公佈事件 immutable log |

兩個 repos **互補但分離**:設計討論不污染 archive,archive 不影響設計討論。

---

## 給 4 大會計師 / 投資人 / 主管機關

需要查「WitsPer 制度文件 公佈紀錄 / 公佈版內容」:

- **公佈紀錄總表**(metadata):[Draft repo《公佈紀錄》Standard](https://github.com/witsper-stanley/witsper-operating-cadence/blob/main/04_%E6%88%91%E5%80%91%E6%80%8E%E9%BA%BC%E4%BF%9D%E8%AD%B7%E8%87%AA%E5%B7%B1/%E5%85%AC%E4%BD%88%E7%B4%80%E9%8C%84_Standard.md)
- **公佈版實際內容**(PDF + source snapshot):本 repo 各檔案
- **Git history**(每次公佈是誰 / 何時 / hash):本 repo Git log
- **設計過程**(為何這樣設計、討論軌跡):[Draft repo](https://github.com/witsper-stanley/witsper-operating-cadence) 對應 source + Issue
