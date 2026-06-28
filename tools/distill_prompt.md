# PROMPT DISTILL SÁCH

## Nguyên tắc bắt buộc
- Không tóm tắt theo chương, không kể lại cốt truyện.
- Mỗi câu là thông tin mới. Không padding, không lặp ý đã nói ở field khác.
- Chỉ extract những gì sách thực sự viết. Nếu sách không có dữ liệu cho một field optional, bỏ field đó — không bịa cho đủ format.
- Nếu không tìm được 6 knowledge unit độc lập thực sự có trong sách, viết ít hơn 6. Không tạo unit giả cho đủ số lượng.
- Trigger situations viết như câu người dùng thực sự gõ vào, không phải topic label.
  - Sai: "Quản lý thời gian"
  - Đúng: "Tao thấy ngày nào cũng kín lịch mà vẫn cảm thấy chưa làm được gì quan trọng"
- Toàn bộ output viết bằng tiếng Việt.
- Tổng giới hạn: 2500–3000 từ. Phân bổ tham khảo:
  - Metadata + Cuốn sách giải quyết + Core Thesis: ~400–500 từ
  - Knowledge Units (phần payload chính — không cắt ngắn để nhường chỗ cho phần đầu): ~1800–2200 từ
  - Index Entries: ~100–200 từ (sinh tự động từ nội dung trên, không tính vào từ phân tích)

---

# [Tên sách đầy đủ]
**Tác giả:** [Tên]
**Năm:** [năm xuất bản]
**Thể loại:** [Business / Psychology / Self-help / Philosophy / ...]
**Loại bằng chứng:** [Trải nghiệm cá nhân tác giả / Case study tổng hợp / Nghiên cứu — data-driven / Hỗn hợp]
*(Field này quyết định độ tin cậy khi advice của sách này mâu thuẫn với sách khác trong kho kiến thức. Đừng bỏ qua field này.)*
**Distilled:** [ngày hôm nay]

---

## Cuốn sách này giải quyết
[Liệt kê 7-10 problem statements. Ngôi thứ nhất "Tôi đang...". Bao gồm cả những vấn đề không obvious mà cuốn sách giải quyết. Đây là phần quan trọng nhất — AI dùng phần này để biết khi nào cần pull cuốn sách này ra.]
- Tôi ...
- Tôi đang hỏi về ...
- Tôi không hiểu tại sao ...

**Không phù hợp khi:**
[1-3 câu: hoàn cảnh hoặc loại người mà lời khuyên trong sách này KHÔNG áp dụng tốt, hoặc dễ bị áp dụng sai. Ví dụ kiểu: sách viết cho người đã có sản phẩm/đang vận hành, không dành cho người chưa từng launch gì. Bỏ qua field này nếu sách áp dụng phổ quát, không có giới hạn rõ ràng — không tự suy diễn giới hạn nếu sách không gợi ý điều đó.]

---

## Core Thesis
[2-3 câu. Sau khi đọc xong cuốn này, người đọc nên nghĩ khác về điều gì? Câu khẳng định trực tiếp, không phải "tác giả thảo luận về X".]

**Myth nó phá vỡ:**
[1-2 câu — niềm tin phổ biến mà cuốn sách này chứng minh là sai hoặc không đầy đủ. Khác với "vấn đề giải quyết" ở trên: đây là lúc người đọc đang vận hành theo một giả định SAI mà chính họ không biết đó là giả định. Bỏ qua nếu cuốn sách không thực sự đối đầu với một niềm tin phổ biến cụ thể nào.]

---

## Knowledge Units
[Extract 6-10 units thực sự tồn tại độc lập trong sách. Mỗi unit là một framework, mental model, hoặc insight dùng được mà không cần đọc unit khác.]

### [Tên concept — đặt tên ngắn gọn, dễ nhớ]

**Trigger situation:**
[Người dùng đang gặp tình huống nào, hoặc đang hỏi câu gì, thì cần đọc unit này? 2-3 trigger cụ thể, viết bằng ngôn ngữ tự nhiên như người dùng thật sự gõ.]

**Core insight:**
[1-3 câu. Đọc một mình vẫn hiểu được, không cần context trước. Câu khẳng định trực tiếp, không phải "tác giả nói rằng".]

**Cơ chế:**
[Tại sao nó đúng? Giải thích bằng logic, không phải "research cho thấy".]

**Dẫn chứng cụ thể:**
[Optional. Số liệu, ví dụ, hoặc tình huống cụ thể mà sách đưa ra để neo insight này vào thực tế — cái này tăng độ thuyết phục khi dùng để tư vấn downstream. Bỏ qua nếu sách chỉ lý luận trừu tượng, không có gì cụ thể.]

**Áp dụng:**
Nếu [tình huống X] → thì [làm Y / nghĩ theo hướng Z]

**Không dùng khi:**
[Exception hoặc điều kiện mà advice này không work hoặc backfire. Bỏ qua nếu không có exception rõ ràng — không tự bịa exception cho đủ format.]

---
[Lặp lại schema trên cho mỗi knowledge unit]
---

## Index Entries

> Block này dùng để paste thẳng vào bảng Problem → Source Map trong `_index.md`.
> Mỗi dòng = 1 problem statement từ section "Cuốn sách này giải quyết" ở trên, ghép với đúng Knowledge Unit tương ứng và góc nhìn riêng của sách này.
> Không thêm dòng nào không có trong "Cuốn sách này giải quyết". Không bịa góc nhìn — lấy từ Core Thesis hoặc core insight của unit tương ứng.

| Người dùng đang hỏi hoặc đang gặp... | Đọc | Section ưu tiên | Góc nhìn |
|---------------------------------------|-----|-----------------|----------|
| [Problem statement 1 — copy từ "Cuốn sách này giải quyết", chuyển sang ngôi "Tôi"] | `wiki/sources/[ten-file].md` | Knowledge Units > [Số]. [Tên unit] | [3–5 từ: lăng kính riêng của sách này cho vấn đề đó] |
| [Problem statement 2] | `wiki/sources/[ten-file].md` | Knowledge Units > [Số]. [Tên unit] | [3–5 từ] |
| [Lặp lại cho mỗi problem statement — 7-10 dòng tương ứng với số problem statements ở trên] |
