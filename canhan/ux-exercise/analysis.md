# PHÂN TÍCH UX AI CHATBOT - VIETNAM AIRLINES (NEO)

## PHẦN 1 — KHÁM PHÁ (EXPLORE)
* **Marketing hứa hẹn:** Trợ lý ảo AI thông minh, hỗ trợ 24/7, cá nhân hóa hành trình, giải quyết thủ tục nhanh chóng.
* **Thực tế trải nghiệm:** * Giao diện Card/Thẻ thông tin trực quan.
    * Phản ứng nhanh với các từ khóa tra cứu (FAQ).
    * **Vấn đề:** Chưa thực sự "thông minh" trong việc hiểu ý định thay đổi đột ngột; giao diện không đổi khi gặp lỗi.

---

## PHẦN 2 — PHÂN TÍCH 4 PATHS (FRAMEWORK)

| Path | Câu hỏi & Phân tích thực tế |
| :--- | :--- |
| **1. Khi AI đúng** | **Thấy:** Text chi tiết + Thẻ Card + Link điều hướng. <br> **Confirm:** Nhắc lại đúng keyword (Vd: "Mắm tôm", "20/5"). |
| **2. Khi AI không chắc** | **Xử lý:** Trả lời xã giao ("Chào bạn"). <br> **Vấn đề:** Thiếu "Show alternatives" (Gợi ý menu chức năng) để user chọn lại. |
| **3. Khi AI sai** | **Dấu hiệu:** AI trả lời lạc đề, lỗi chính tả (**"abnj"**). <br> **Sửa:** User phải xóa/gõ lại. **Mất 3 bước** để thoát context cũ. |
| **4. Khi user mất tin** | **Exit:** Nút thoát ẩn/khó tìm. <br> **Fallback:** AI không nhận diện được lệnh "Gặp người thật" khi đang kẹt luồng cũ. |

### **Tự phân tích (Insights)**
* **Path xử lý tốt nhất:** **Path 1** (Tra cứu FAQ tĩnh). Hệ thống có cơ sở dữ liệu quy định bay rất sâu và chính xác.
* **Path yếu nhất:** **Path 3 & 4**. AI bị "lì", không có khả năng tự sửa lỗi (Self-correction) và không nhận diện được ý định thoát (Escape Intent).
* **Gap Marketing vs Thực tế:** Marketing định vị "AI", thực tế là **Keyword-Bot**. Khoảng cách nằm ở khả năng nhận diện cảm xúc (Sentiment) và sự kết nối tức thời với con người.

---

## PHẦN 3 — SKETCH "LÀM TỐT HƠN" (PATH 4 - ESCAPE PATH)

### 1. As-is (Hiện tại)
* **Luồng:** User ức chế gõ "Gặp người thật" -> AI trả lời quy định mắm tôm (Lỗi kẹt ngữ cảnh) -> User bế tắc.
* **Điểm gãy:** Không nhận diện được yêu cầu kết nối con người; lặp lại dữ liệu rác/lỗi chính tả ("abnj").

### 2. To-be (Đề xuất)
* **Luồng:** User yêu cầu gặp người thật -> AI nhận diện Intent "Thoát" -> Ngắt luồng FAQ cũ -> Hiển thị nút hỗ trợ trực tiếp.
* **Thêm:** Nút bấm **[Kết nối nhân viên ngay]**.
* **Bớt:** Các câu trả lời FAQ dài dòng khi user đang cần hỗ trợ khẩn cấp.
* **Đổi:** Chuyển từ ưu tiên "Khớp từ khóa" sang "Nhận diện ý định thoát".

---
*Người thực hiện: Nguyễn Thanh Bình - 2A202600484*