# Buổi 3 - Vòng lặp

## Vòng lặp là gì?
Vòng lặp chạy một khối lệnh nhiều lần. Dùng `for` khi duyệt qua một dãy hoặc biết số lượt; dùng `while` khi lặp theo điều kiện.

## Vòng lặp `for` và `range`
```python
for number in range(1, 6):
    print(number)

total = 0
for number in numbers:
    total += number
```

- `range(start, stop, step)` không bao gồm `stop`.
- `range(5)` tạo các số `0, 1, 2, 3, 4`; `range(1, 6)` tạo `1..5`.

| Cú pháp | Ý nghĩa | Ví dụ |
|---|---|---|
| `range(stop)` | Từ `0` đến trước `stop` | `range(5)` |
| `range(start, stop)` | Từ `start` đến trước `stop` | `range(1, 6)` |
| `range(start, stop, step)` | Tăng/giảm theo bước | `range(10, 0, -2)` |

## Vòng lặp `while`, `break`, `continue`
`while` kiểm tra điều kiện trước mỗi lượt. Phải thay đổi biến điều khiển để vòng lặp có thể kết thúc. `break` thoát hẳn; `continue` bỏ qua phần còn lại của lượt hiện tại.

```python
number = 1
while number <= 5:
    print(number)
    number += 1
```

## Ví dụ tổng và đếm
```python
numbers = [2, 3, 4, 5, 6]
total = 0
even_count = 0
for number in numbers:
    total += number
    if number % 2 == 0:
        even_count += 1
print(total, even_count)
```