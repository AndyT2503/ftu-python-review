# Buổi 8 - Tài liệu tự ôn tổng hợp

Buổi này dùng để tự rà lại các mẫu code và lỗi thường gặp. Hãy chạy từng ví dụ, thay đổi dữ liệu và giải thích kết quả bằng lời của mình.

## Checklist trước khi nộp
- Có nhập dữ liệu bằng `input()` ở câu cần nhập.
- Đã ép kiểu số.
- Slicing chuỗi đúng vị trí.
- Điều kiện có xử lý trường hợp đặc biệt.
- Hàm có `return`.
- List comprehension đúng khoảng `1..100`.
- Pandas dùng đúng `head`, `iloc`, thống kê, `corr`.
- Hồi quy có `fit`, `coef_`, `intercept_`, `score`.

## Quy trình làm bài
1. Đọc kỹ yêu cầu và gạch chân tên biến bắt buộc.
2. Viết từng câu trong một ô riêng, chạy thử với dữ liệu đơn giản.
3. Kiểm tra kiểu dữ liệu, chỉ số chuỗi và khoảng `range`.
4. Với Pandas, kiểm tra tên cột trước khi tính.
5. In kết quả trung gian để tìm lỗi, sau đó mới rút gọn code.

## Thứ tự tự ôn
1. Biến, `str`, `int`, `float`, `bool`, `input`, ép kiểu và toán tử.
2. Điều kiện: so sánh, `and/or/not`, thụt lề và trường hợp đặc biệt.
3. Vòng lặp: `range` không lấy `stop`, cập nhật `while`, `break`, `continue`.
4. Chuỗi: chỉ số bắt đầu từ 0, slicing không lấy vị trí `stop`, phương thức xử lý chuỗi.
5. Hàm: tham số, `return` và khác biệt giữa `return` với `print`.
6. List comprehension: đúng mẫu `[expression for item in iterable if condition]`.
7. Pandas: `DataFrame`, `head`, `iloc`, thống kê, `corr` và hồi quy.

## Cách tự kiểm tra
- Đổi dữ liệu đầu vào và chạy lại.
- Kiểm tra kiểu bằng `type()` trước khi sửa lỗi.
- In từng biến trung gian khi kết quả sai.
- Đọc lỗi từ dòng cuối của traceback và kiểm tra đúng tên biến/hàm.