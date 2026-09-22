# Buổi 2 - Điều kiện

## Điều kiện là gì?
Điều kiện là một biểu thức cho kết quả `True` hoặc `False`. Python dùng kết quả đó để quyết định có chạy một khối lệnh hay không.

## Cú pháp
```python
if condition:
    ...
elif another_condition:
    ...
else:
    ...
```

| Nhóm | Toán tử | Ý nghĩa |
|---|---|---|
| So sánh | `==` | Bằng |
| So sánh | `!=` | Khác |
| So sánh | `<`, `>` | Nhỏ hơn, lớn hơn |
| So sánh | `<=`, `>=` | Nhỏ hơn/bằng, lớn hơn/bằng |
| Logic | `and` | Cả hai điều kiện đúng |
| Logic | `or` | Ít nhất một điều kiện đúng |
| Logic | `not` | Đảo `True` thành `False` và ngược lại |
- `and` đúng khi cả hai vế đúng; `or` đúng khi ít nhất một vế đúng; `not` đảo giá trị logic.
- Python dùng thụt lề để xác định khối lệnh. Các dòng cùng khối phải thẳng hàng.

## Mẫu giải ax + b = c
```python
if a == 0 and b == c:
    print("vo so nghiem")
elif a == 0:
    print("vo nghiem")
else:
    x = (c - b) / a
    print(x)
```

## Ví dụ
```python
score = float(input("Score: "))
if score < 0 or score > 10:
    print("Invalid score")
elif score >= 8:
    print("Good")
elif score >= 5:
    print("Pass")
else:
    print("Fail")
```

Với phương trình `ax + b = c`, phải kiểm tra `a == 0` trước khi chia để tránh chia cho 0:

```python
if a == 0 and b == c:
    print("vo so nghiem")
elif a == 0:
    print("vo nghiem")
else:
    print((c - b) / a)
```