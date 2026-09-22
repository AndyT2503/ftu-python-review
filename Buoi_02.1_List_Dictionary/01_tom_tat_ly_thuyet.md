# Buổi 5 - List và dictionary

## List
`list` là một dãy có thứ tự, có thể thay đổi. List dùng `[]` và có thể chứa nhiều kiểu dữ liệu.

| Cú pháp | Ý nghĩa |
|---|---|
| `items[0]` | Lấy phần tử đầu |
| `items[-1]` | Lấy phần tử cuối |
| `items.append(x)` | Thêm `x` vào cuối |
| `items.remove(x)` | Xóa phần tử đầu tiên có giá trị `x` |
| `items.count(x)` | Đếm số lần `x` xuất hiện |
| `len(items)` | Số phần tử |
| `x in items` | Kiểm tra tồn tại |
| `sum(items)` | Tính tổng các số |
| `min(items)`, `max(items)` | Tìm nhỏ nhất, lớn nhất |

```python
numbers = [10, 20, 30]
numbers[0] = 15
numbers.append(40)
print(numbers)
```

## Dictionary
`dict` là cấu trúc lưu dữ liệu theo cặp `key: value`. Dictionary dùng `{}`. Key dùng để tra cứu value; key phải là duy nhất.

| Cú pháp | Ý nghĩa |
|---|---|
| `student["name"]` | Lấy value theo key |
| `student["age"] = 21` | Thêm hoặc cập nhật value |
| `student.get("email", default)` | Lấy value an toàn, dùng `default` nếu thiếu key |
| `student.keys()` | Lấy các key |
| `student.values()` | Lấy các value |
| `student.items()` | Lấy từng cặp key-value |
| `"name" in student` | Kiểm tra key có tồn tại |

```python
student = {"name": "Lan", "age": 20}
print(student["name"])
student["age"] = 21
student["city"] = "Hanoi"
print(student.get("email"))
print(student)
```

Khi cần tạo dictionary từ hai list có cùng độ dài, `dict(zip(keys, values))` ghép phần tử cùng vị trí thành các cặp key-value.

```python
keys = ["name", "age"]
values = ["Lan", 20]
student = dict(zip(keys, values))
print(student)
```

## Phân biệt nhanh
| Cấu trúc | Ký hiệu | Truy cập bằng | Có thay đổi được? |
|---|---|---|---|
| List | `[]` | Chỉ số | Có |
| Dictionary | `{}` | Key | Có |