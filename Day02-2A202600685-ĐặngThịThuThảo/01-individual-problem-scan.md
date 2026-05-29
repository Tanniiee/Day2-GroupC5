# 01 — Individual Problem Scan

> Bối cảnh: Dev Intern tại startup 20-100 người, dùng GitHub hằng ngày.

---

## Scan rộng — 10 problems

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Mỗi khi tạo Pull Request, phải viết lại mô tả từ đầu: summary, change, test plan, link ticket — không có template chuẩn | Dev intern, junior dev | Mỗi PR mất 10-15 phút chỉ để viết description; các PR hay bị comment "thiếu context" |
| 2 | Lặp lại | Standup hằng ngày: mỗi sáng phải nhớ lại hôm qua làm gì, copy commit message hoặc tóm tắt tay | Dev intern, toàn team | 5-10 phút/người/ngày; hay bị "hôm qua làm gì vậy?" |
| 3 | Tốn thời gian | Onboarding codebase mới: đọc README cũ, hỏi senior về convention, tìm file config rải rác nhiều nơi | Dev mới, intern | Tốn 3-5 ngày đầu chỉ để hiểu project đủ dùng |
| 4 | Tốn thời gian | Review code: phải đọc toàn bộ diff để hiểu ý đồ, không có summary ngắn gọn "PR này làm gì" | Reviewer (senior dev, tech lead) | Reviewer hay bỏ qua review vì "không có thời gian đọc hết" |
| 5 | AI có thể tốt hơn | Viết commit message: hay viết kiểu "fix bug", "update code" — không đủ context cho người đọc sau | Dev intern | Team lead nhắc lại về commit convention ít nhất 2 lần/tuần |
| 6 | AI có thể tốt hơn | Giải thích bug cho senior: mỗi lần có lỗi phải viết lại toàn bộ context — đã thử gì, lỗi ở đâu, log là gì | Dev intern | Tốn 15-20 phút viết Slack message trước khi hỏi; vẫn bị hỏi lại |
| 7 | Pain từ người khác | Product Manager tạo ticket nhưng thiếu Acceptance Criteria rõ — dev phải hỏi lại nhiều lần mới làm được | Dev team, PM | Mỗi sprint có ít nhất 3-5 ticket bị block vì "chưa rõ yêu cầu" |
| 8 | Pain từ người khác | Tech lead review PR mất nhiều thời gian vì phải tự đoán intent của PR, không có context đi kèm | Tech lead | Tech lead hay comment "PR này làm gì?" trước khi review thật |
| 9 | Lặp lại | Tổng hợp sprint retrospective: scrum master hỏi "tuần này làm được gì, blocked gì" — mọi người phải nhớ lại | Scrum master, cả team | Retro hay im lặng 5-10 phút đầu vì không ai nhớ rõ |
| 10 | Tốn thời gian | Tìm quyết định kiến trúc cũ: "tại sao dùng thư viện X thay vì Y?" — không có log quyết định, phải hỏi người | Dev mới, intern | Mỗi lần hỏi mất 30-60 phút tìm người đúng và chờ trả lời |

---

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Viết PR description | Workflow rõ, lặp lại mỗi ngày, bottleneck cụ thể, metric thời gian dễ đo, reviewer cũng được lợi | "Đủ tốt" cho reviewer đo thế nào? |
| 2 | Giải thích bug cho senior | Pain thật với intern, AI có thể cấu trúc log/context tốt hơn, tiết kiệm thời gian cả hai phía | Quality cải thiện khó định lượng ngay |
| 3 | Tìm quyết định kiến trúc cũ | Nhiều người đau, ảnh hưởng tốc độ onboarding, nhưng scope có thể lớn (cần indexing codebase) | Data access phức tạp, có thể quá rộng cho lab |

---

## Problem Card #1 — Viết PR Description

```
┌──────────────────────────────────────────────────────────┐
│ PROBLEM CARD #1                                          │
│                                                          │
│ Problem 1 câu: Dev intern mất 10-15 phút viết PR         │
│ description từ đầu mỗi lần, không có template chuẩn,     │
│ PR vẫn bị comment "thiếu context".                       │
│                                                          │
│ Ai đang đau? Dev intern và junior dev; reviewer mất       │
│ thêm thời gian đọc PR thiếu thông tin.                   │
│                                                          │
│ Workflow hiện tại:                                       │
│ 1. Code xong → 2. git push → 3. Mở GitHub tạo PR →       │
│ 4. Tự nhớ và viết description tay → 5. Submit → 6. Chờ  │
│ reviewer → 7. Bị hỏi lại / bị comment thiếu context      │
│                                                          │
│ Bước nghẽn nhất: Bước 4 — viết description (10-15'/PR)   │
│                                                          │
│ Đo thành công bằng gì?                                   │
│ Giảm thời gian viết description từ 10-15' xuống < 3'/PR; │
│ giảm comment "thiếu context" từ ~3 PR/tuần xuống ≤ 1    │
│                                                          │
│ Quick gut: □ No AI  □ Rule  ■ Workflow  □ Agent          │
└──────────────────────────────────────────────────────────┘
```

**Problem 1 câu:**
Dev intern tại startup mất 10-15 phút viết PR description từ đầu mỗi lần push code, không có template và thiếu context, khiến reviewer phải hỏi lại hoặc bỏ qua review.

**Actor:**
Dev intern / junior dev là người viết PR. Tech lead / senior dev là reviewer bị ảnh hưởng gián tiếp.

**Thời điểm / bối cảnh:**
Mỗi lần tạo Pull Request — trung bình 2-3 lần/ngày với intern đang học.

**Current workflow (7 bước):**
1. Viết code xong, chạy test local
2. `git push` lên branch
3. Mở GitHub, tạo PR mới
4. Tự nhớ lại mình đã thay đổi gì, viết description tay từ đầu *(bottleneck)*
5. Submit PR
6. Chờ reviewer assign
7. Nhận comment "PR này làm gì?" hoặc "thiếu test plan" — phải sửa lại

**Bottleneck:**
Bước 4 — viết description thủ công, không có template, phải nhớ lại toàn bộ thay đổi mình vừa làm, mất 10-15 phút/PR.

**Impact:**
- Intern mất ~30-45 phút/ngày chỉ để viết PR description (2-3 PR/ngày × 10-15 phút).
- Reviewer mất thêm thời gian hỏi lại hoặc tự đoán intent.
- PR bị delay review → sprint bị kéo dài.
- Với team 5 dev, tổng có thể lên 2-3 giờ/ngày bị mất vào việc này.

**Success metric:**
- Giảm thời gian viết description từ 10-15 phút xuống dưới 3 phút/PR.
- Giảm số PR nhận comment "thiếu context" / "PR này làm gì?" từ ~3 PR/tuần xuống ≤ 1 PR/tuần.
- Đo bằng: bấm giờ trước/sau, đếm loại comment nhận được trong 2 tuần.

**Non-AI alternative:**
PR template trong GitHub (PULL_REQUEST_TEMPLATE.md) có thể giải quyết phần format. Nhưng dev vẫn phải tự điền nội dung, không giải quyết được phần tóm tắt diff và viết change summary.

**AI hypothesis:**
AI đọc git diff → tự generate draft description (summary, changes, test plan gợi ý) → dev chỉnh sửa trước khi submit.

**Quick gut:** Workflow

---

### Draft current workflow (ASCII)

```
CURRENT STATE — ~12 phút/PR (trung bình)

[1. Code + test local: không tính]
→ [2. git push: 1']
→ [3. Mở GitHub, tạo PR: 1']
→ [4. Viết description tay: 10-12']  ← BOTTLENECK
     - Nhớ lại mình đã làm gì
     - Nghĩ xem reviewer cần biết gì
     - Viết summary, changes, test plan
     - Không có cấu trúc cố định
→ [5. Submit: 1']
→ [6. Nhận comment "thiếu context": +5-10' để sửa]

Thực tế: ~15-22 phút nếu tính cả vòng sửa
```

### Draft future workflow (ASCII)

```
FUTURE STATE — ~3 phút/PR

[1. Code + test local: không tính]
→ [2. git push: 1']
→ [3. Chạy script/tool: 30 giây]
     - Tool đọc git diff tự động
     - AI generate draft description
       (summary, key changes, test checklist)
→ [4. Dev review + chỉnh sửa draft: 1-2']  ← HUMAN BOUNDARY
     - Kiểm tra accuracy
     - Thêm context riêng nếu cần
     - Xóa phần AI hiểu sai
→ [5. Submit PR: 30 giây]

Fallback: AI draft vô nghĩa hoặc sai hoàn toàn
→ Dev tự viết theo template cố định (Rule)

Bottleneck mới: Review + edit draft (chấp nhận được —
đây là điểm kiểm soát chất lượng, dev vẫn chịu trách nhiệm)
```

---

## Problem Card #2 — Giải thích bug cho senior

```
┌──────────────────────────────────────────────────────────┐
│ PROBLEM CARD #2                                          │
│                                                          │
│ Problem 1 câu: Intern mất 15-20 phút viết Slack message  │
│ giải thích bug trước khi hỏi senior, vẫn bị hỏi lại vì  │
│ thiếu cấu trúc rõ.                                       │
│                                                          │
│ Ai đang đau? Dev intern (viết), senior dev (đọc và       │
│ trả lời không đủ context).                               │
│                                                          │
│ Workflow hiện tại:                                       │
│ 1. Gặp bug → 2. Debug một mình → 3. Bí → 4. Viết Slack  │
│ message giải thích → 5. Ping senior → 6. Senior hỏi lại  │
│                                                          │
│ Bước nghẽn nhất: Bước 4 — viết bug report (15-20'/lần)  │
│                                                          │
│ Đo thành công bằng gì?                                   │
│ Giảm số lần bị hỏi lại từ ~3 lần/tuần xuống ≤ 1;        │
│ giảm thời gian viết từ 15-20' xuống < 5'                 │
│                                                          │
│ Quick gut: □ No AI  □ Rule  ■ Workflow  □ Agent          │
└──────────────────────────────────────────────────────────┘
```

**Actor:** Dev intern gặp bug, senior dev / tech lead là người được hỏi.

**Bottleneck:** Viết Slack message đủ context (error message, bước reproduce, đã thử gì, log liên quan) — không có template, tốn 15-20 phút, vẫn hay thiếu thông tin.

**Impact:** Intern mất 15-20 phút/lần × ~3 lần/tuần = ~45-60 phút/tuần. Senior bị ngắt tập trung nhiều lần, phải hỏi lại context.

**Metric:** Giảm thời gian viết bug report từ 15-20 phút xuống dưới 5 phút; giảm số lần hỏi lại từ ~3 lần xuống ≤ 1 lần/tuần.

**Quick gut:** Workflow — AI cấu trúc thông tin từ log/error message, dev review trước khi gửi.

**Vì sao chưa chọn làm #1:** Quality metric (senior có hiểu không, có giải được không) khó đo hơn time metric của PR. Workflow cũng phức tạp hơn một chút.

---

## Problem Card #3 — Tìm quyết định kiến trúc cũ

```
┌──────────────────────────────────────────────────────────┐
│ PROBLEM CARD #3                                          │
│                                                          │
│ Problem 1 câu: Dev mới và intern không tìm được lý do    │
│ tại sao team dùng thư viện/pattern X — không có log      │
│ quyết định, phải hỏi người và chờ 30-60 phút.           │
│                                                          │
│ Ai đang đau? Dev mới, intern, bất kỳ ai join sau         │
│                                                          │
│ Workflow hiện tại:                                       │
│ 1. Thắc mắc → 2. Search README/docs nội bộ → 3. Không   │
│ tìm thấy → 4. Hỏi Slack → 5. Chờ người đúng trả lời     │
│                                                          │
│ Bước nghẽn nhất: Bước 4-5 — chờ người biết (30-60'/lần) │
│                                                          │
│ Đo thành công bằng gì?                                   │
│ Giảm thời gian tìm quyết định cũ từ 30-60' xuống < 5'   │
│                                                          │
│ Quick gut: □ No AI  □ Rule  □ Workflow  ■ Agent          │
└──────────────────────────────────────────────────────────┘
```

**Actor:** Dev mới, intern cần hiểu "tại sao" của codebase.

**Bottleneck:** Không có nơi lưu quyết định kiến trúc (ADR — Architecture Decision Record). Phải hỏi người, chờ người đúng online, chờ trả lời.

**Impact:** Mỗi lần mất 30-60 phút, ~3-4 lần/tuần cho intern. Onboarding kéo dài hơn cần thiết.

**Metric:** Giảm thời gian tìm quyết định cũ xuống dưới 5 phút; giảm số lần phải hỏi Slack về "tại sao" kiến trúc từ 3-4 lần xuống ≤ 1 lần/tuần.

**Quick gut:** Agent (cần search nhiều nguồn: commits, Slack, docs, code comments) — nhưng scope rộng và data access phức tạp, nên chưa chọn làm candidate chính.

**Vì sao chưa chọn làm #1:** Data access khó (cần đọc Slack history, commits, docs rải rác), scope dễ bị quá rộng, khó validate trong lab.

---

## Card tôi muốn pitch nhất

**Card #1 — Viết PR Description**

Vì sao:
- Workflow rõ nhất, có thể vẽ before/after cụ thể từng bước.
- Metric thời gian dễ đo: bấm giờ trước/sau.
- Lặp lại hằng ngày (2-3 PR/ngày) → impact tích lũy lớn.
- Cả reviewer cũng được lợi → impact rộng hơn 1 người.
- Có non-AI alternative rõ (template) để so sánh Rule vs Workflow.

Câu hỏi tôi muốn nhóm challenge:
- "Template GitHub đã đủ chưa? Tại sao vẫn cần AI?"
- "Metric 'comment thiếu context' đo thế nào cho chính xác?"
- "AI đọc git diff có thể hiểu sai intent không? Rủi ro đó lớn không?"