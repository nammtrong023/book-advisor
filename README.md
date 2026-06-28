# Personal Knowledge Base

Kho tri thức cá nhân — cố vấn ra quyết định backed by sách đã distill. Claude đọc repo theo thứ tự `overview → hot → index → sources`, cite nguồn, và surface mâu thuẫn giữa các sách.

## Cấu trúc

```
kb/
├── wiki/
│   ├── overview.md          # Big picture — đọc trước index
│   ├── hot.md               # Session cache (~500 từ)
│   ├── index.md             # Problem → Source → Section routing
│   ├── sources/             # Sách đã distill
│   └── questions/           # Q&A đã lưu
├── tools/distill_prompt.md  # Schema distill sách mới
├── skills/                  # kb-query, kb-save, think
├── CLAUDE.md                # Instructions cho Claude khi đọc repo
└── SYSTEM_PROMPT.md         # Copy vào Claude Project Instructions
```

`about-me.md` **không** nằm trong repo — upload riêng vào Claude Project.

---

## Setup

1. Clone hoặc fork repo này
2. Kết nối repo với Claude Project (Project Knowledge → GitHub → chọn repo)
3. Upload `about-me.md` riêng vào Claude Project (không commit vào repo)
4. Copy nội dung `SYSTEM_PROMPT.md` vào Claude Project Instructions

---

## Adding a new book

1. Distill sách bằng `tools/distill_prompt.md`
2. Lưu output thành `wiki/sources/<book-name>.md`
3. Paste block `## Index Entries` vào `wiki/index.md`
4. Cập nhật `wiki/overview.md` nếu thêm domain hoặc mâu thuẫn mới
5. Git push

---

## Updating hot.md

1. Cuối session có ý nghĩa, hỏi Claude: *"output hot.md update"*
2. Paste output vào `wiki/hot.md` (ghi đè hoàn toàn)
3. Git push

---

## Saving a Q&A

1. Sau session tốt, hỏi Claude: *"save this conversation as a question file"* hoặc `/kb-save`
2. Claude output file markdown có cấu trúc
3. Lưu thành `wiki/questions/<topic-YYYY-MM>.md`
4. Thêm một dòng vào `wiki/questions/_index.md`
5. Git push
