# Buổi 6 - Hàm và list comprehension

## Hàm
Hàm là một khối lệnh có tên, dùng để thực hiện một nhiệm vụ và có thể gọi lại nhiều lần.

| Thành phần | Ý nghĩa |
|---|---|
| `def` | Bắt đầu khai báo hàm |
| Tham số | Dữ liệu đầu vào của hàm |
| `return` | Trả kết quả về nơi gọi |
| `print` | Chỉ hiển thị kết quả |

```python
def square(number):
	return number ** 2

result = square(4)
print(result)
```

`return` khác `print`: kết quả từ `return` có thể gán vào biến hoặc dùng tiếp trong phép tính.

## List là gì?
`list` là một dãy có thứ tự, có thể chứa nhiều giá trị và có thể thay đổi sau khi tạo. List viết trong ngoặc vuông, các phần tử ngăn cách bằng dấu phẩy.

```python
numbers = [10, 20, 30]
numbers[0] = 15
numbers.append(40)
print(numbers)
```

| Cú pháp | Ý nghĩa |
|---|---|
| `numbers[0]` | Lấy phần tử đầu |
| `numbers[-1]` | Lấy phần tử cuối |
| `numbers.append(x)` | Thêm `x` vào cuối list |
| `len(numbers)` | Độ dài list |
| `x in numbers` | Kiểm tra `x` có tồn tại |
| `sum(numbers)` | Tính tổng |
| `min(numbers)`, `max(numbers)` | Tìm nhỏ nhất, lớn nhất |

## List comprehension
List comprehension là cách viết ngắn để tạo một list từ một dãy giá trị. Chỉ học phần này sau khi đã hiểu `for` và list thông thường.
```python
numbers = [10, 20, 30]
numbers[0]
len(numbers)
20 in numbers

squares = [number ** 2 for number in range(1, 6)]
evens = [number for number in range(1, 11) if number % 2 == 0]
```

Cấu trúc `[expression for item in iterable if condition]`: duyệt từng `item`, tính `expression`, chỉ giữ item thỏa `condition` nếu có.

## Ví dụ
```python
numbers = list(range(1, 11))
evens = [number for number in numbers if number % 2 == 0]
squares = [number ** 2 for number in evens]
print(numbers)
print(evens)
print(squares)
```