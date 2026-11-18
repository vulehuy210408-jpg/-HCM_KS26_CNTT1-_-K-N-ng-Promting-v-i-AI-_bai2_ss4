# BÁO CÁO BÀI TẬP: SO SÁNH TRADE-OFF CÁC GIẢI PHÁP RA LỆNH PROMPT

## Bước 1: Đề xuất 2 Prompt mẫu

### Giải pháp 1: Phương án Đơn giản (Simple Prompting)
* **Đặc điểm:** Ngắn gọn, trực diện, không sử dụng khung cấu trúc phức tạp hay ràng buộc chi tiết.
* **Nội dung Prompt mẫu:**
```text
Hãy viết danh sách 3 sản phẩm smartphone nổi bật hiện nay kèm giá bán và xuất xứ dưới dạng JSON.
```
### [Context]
Bạn là một chuyên gia cơ sở dữ liệu và hệ thống thông tin thương mại điện tử chuyên cung cấp dữ liệu chuẩn hóa dạng JSON cho API.

### [Request]
Hãy trích xuất danh sách 3 sản phẩm smartphone nổi bật hiện nay theo đúng định dạng JSON thô.

### [Examples - Few-shot]
Ví dụ cấu trúc đầu ra bắt buộc:
[
  {
    "id": "SP01",
    "name": "iPhone 15 Pro",
    "price": "28990000 VNĐ",
    "origin": "Mỹ"
  }
]

### [Action & Constraints]
1. Chỉ xuất ra cấu trúc JSON thuần túy, tuyệt đối không kèm theo lời dẫn, văn bản chào hỏi hay Markdown code block (như ```json).
2. Nếu không tìm thấy thông tin của sản phẩm nào, hãy trả về mảng rỗng [].
3. Đảm bảo đúng tên trường (keys) và định dạng kiểu dữ liệu.
## Kết quả chạy thử thực tế (Simulation Output của Giải pháp 2)
[
  {
    "id": "SP01",
    "name": "iPhone 15 Pro Max",
    "price": "33990000 VNĐ",
    "origin": "Mỹ"
  },
  {
    "id": "SP02",
    "name": "Samsung Galaxy S24 Ultra",
    "price": "29990000 VNĐ",
    "origin": "Hàn Quốc"
  },
  {
    "id": "SP03",
    "name": "Xiaomi 14 Pro",
    "price": "21990000 VNĐ",
    "origin": "Trung Quốc"
  }
]