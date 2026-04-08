# UX EXERCISE — VIETNAM AIRLINES (CHATBOT NEO)

## Sản phẩm: Vietnam Airlines — Chatbot NEO (Trợ lý ảo hỗ trợ hành khách)

## 4 PATHS

### 1. AI đúng
- User hỏi về quy định mang "Mắm tôm" hoặc "Làm thủ tục trực tuyến".
- AI hiển thị thẻ thông tin (Card) chi tiết: quy định đóng gói, link check-in trực tiếp.
- UI: Hiện thông tin chính xác, có nút bấm (button) để user đi tiếp tới website.

### 2. AI không chắc
- User gõ câu chào xã giao hoặc từ khóa ngắn như "Em ơi", "Thủ tục".
- UI: AI trả lời xã giao ("NEO rất vui được hỗ trợ...") nhưng không đưa ra menu gợi ý ngay.
- Vấn đề: Thiếu cơ chế hỏi lại hoặc Show alternatives (ví dụ: "Bạn muốn làm thủ tục tại sân bay hay trực tuyến?").

### 3. AI sai
- User đang hỏi về mắm tôm, sau đó đổi ý gõ: "Muốn gặp người thật".
- AI bị kẹt ngữ cảnh cũ, tiếp tục trả lời về mắm tôm hoặc phản hồi sai chính tả (**"abnj"**).
- Sửa: User phải gõ lại từ khóa mới hoặc nhấn "Bắt đầu lại" -> 2-3 bước.
- Vấn đề: AI không nhận diện được sự thay đổi ý định (Intent shift) và dữ liệu hiển thị còn rác (Typo).

### 4. User mất niềm tin
- Khi gặp lỗi kẹt ngữ cảnh hoặc sai chính tả, user cảm thấy bot "ngáo" và không muốn dùng tiếp.
- Không có nút "Thoát nhanh" (Exit) rõ ràng ngay tại tin nhắn lỗi.
- Fallback (Hotline) nằm ở cuối đoạn text dài, khó tìm khi đang ức chế.

---

## Path yếu nhất: Path 3 + 4
- Khả năng xử lý lỗi (Recovery flow) rất kém: AI bị "lì" trong ngữ cảnh cũ.
- Thiếu cơ chế nhận diện "Escape Intent": Khi user muốn gặp người, AI vẫn cố trả lời bằng máy.
- Lỗi hiển thị (chính tả) làm giảm uy tín của một hãng hàng không quốc gia.

---

## Gap marketing vs thực tế
- Marketing: "Trợ lý ảo thông minh", "Cá nhân hóa trải nghiệm", "Hỗ trợ tức thì".
- Thực tế: Hoạt động như một bộ FAQ Search (tìm kiếm câu hỏi thường gặp) dựa trên từ khóa. 
- Gap lớn nhất: Khả năng **Human hand-off** (chuyển giao sang người thật) không mượt mà như quảng cáo.

---

## Sketch (Hướng dẫn vẽ lên A4)

**As-is (Bên trái):**
- Vẽ khung chat: User đòi "Gặp người thật" -> AI trả lời "Quy định mắm tôm... abnj".
- Khoanh đỏ vào câu trả lời AI. Ghi chú: **"Kẹt ngữ cảnh & Lỗi Typo"**.
- User Journey gãy tại đây vì không có lối thoát.

**To-be (Bên phải):**
- Vẽ khung chat: User đòi "Gặp người thật".
- AI nhận diện Intent "Thoát" -> Hiện thông báo: "Tôi thấy bạn cần hỗ trợ trực tiếp từ nhân viên".
- UI: Xuất hiện nút bấm nổi bật **[KẾT NỐI TƯ VẤN VIÊN]**.
- Ghi rõ: **Thêm** nút Escape, **Đổi** cơ chế ưu tiên nhận diện Intent thay vì Keyword.