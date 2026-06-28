---
name: kb-save
trigger: "/kb-save", "save this", "lưu lại", "lưu conversation này"
---

# KB Save — Lưu Q&A vào wiki/questions/

Khi được trigger, output toàn bộ conversation hiện tại thành một file markdown
có cấu trúc, sẵn sàng để user paste vào `wiki/questions/`.

---

## Output format

Xuất ra **đúng block markdown sau**, không thêm bất kỳ thứ gì ngoài nó:

```markdown
---
title: <tóm tắt câu hỏi/quyết định trong 5-8 từ tiếng Việt>
date: <ngày hôm nay: YYYY-MM-DD>
tags: [<2-3 tags liên quan>]
sources: [<tên các sách được cite trong conversation>]
---

# <Câu hỏi hoặc quyết định chính>

## Bối cảnh
<1-2 câu: tình huống nào khiến user hỏi điều này>

## Insights từ KB
<bullet points — mỗi point kèm citation: *(Tên sách — Section)*>

## Tensions / Mâu thuẫn giữa các nguồn
<nếu có — nêu rõ từng phía và lý do tension tồn tại>
<nếu không có — ghi "Không có mâu thuẫn đáng kể">

## Kết luận / Góc nhìn của tao
*(để trống — user tự điền sau)*
```

---

## Sau khi output

Hướng dẫn user 3 bước:
1. Copy block trên
2. Lưu thành `wiki/questions/<topic-YYYY-MM>.md`
   (ví dụ: `wiki/questions/job-vs-freelance-2026-06.md`)
3. Thêm một dòng vào `wiki/questions/_index.md`:
   `| questions/<filename>.md | <topic> | <date> |`
4. Git push
