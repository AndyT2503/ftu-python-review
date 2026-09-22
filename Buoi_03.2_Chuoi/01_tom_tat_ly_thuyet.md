# Buổi 4 - Chuỗi

## Chuỗi là gì?
`str` là kiểu dữ liệu dùng để lưu văn bản. Chuỗi được viết trong dấu nháy đơn hoặc nháy kép. Chuỗi có thể chứa chữ, số, khoảng trắng và ký hiệu, nhưng `"123"` vẫn là chuỗi chứ chưa phải số.

```python
name = "Lan"
code = "123"
print(type(name), type(code))
```

Chuỗi là bất biến: các thao tác xử lý tạo ra chuỗi mới, không thay đổi trực tiếp chuỗi ban đầu.

## Nối chuỗi và độ dài
```python
first_name = "Nguyen"
last_name = "An"
full_name = first_name + " " + last_name
print(full_name)
print("ha" * 3)
print(len(full_name))
```

- `+` nối các chuỗi.
- `*` lặp chuỗi.
- Không thể dùng `+` trực tiếp giữa chuỗi và số; cần `str(number)` hoặc f-string.

## Indexing và slicing
Vị trí bắt đầu từ 0. `s[start:stop:step]` lấy từ `start` đến trước `stop`, theo bước `step`.

| Cú pháp | Ý nghĩa | Ví dụ với `s = "Data Python"` |
|---|---|---|
| `s[0]` | Ký tự đầu tiên | `D` |
| `s[-1]` | Ký tự cuối cùng | `n` |
| `s[:4]` | Từ đầu đến trước vị trí 4 | `Data` |
| `s[5:]` | Từ vị trí 5 đến hết | `Python` |
| `s[::2]` | Lấy cách 2 ký tự | `Dt yhn` |
| `s[::-1]` | Đảo ngược chuỗi | `nohtyP ataD` |

```python
s = "Data Python"
print(s[0], s[-1])
print(s[:4], s[5:])
print(s[::2])
print(s[::-1])
```

## Phương thức thường dùng
| Phương thức | Ý nghĩa | Ví dụ |
|---|---|---|
| `s.lower()` | Chuyển thành chữ thường | `"Py".lower()` -> `"py"` |
| `s.upper()` | Chuyển thành chữ hoa | `"Py".upper()` -> `"PY"` |
| `s.title()` | Viết hoa chữ đầu mỗi từ | `"nguyen van an".title()` -> `"Nguyen Van An"` |
| `s.strip()` | Xóa khoảng trắng đầu/cuối | `" x ".strip()` -> `"x"` |
| `s.split()` | Tách thành list các từ | `"a b".split()` -> `["a", "b"]` |
| `sep.join(items)` | Ghép các phần tử chuỗi | `"-".join(["a", "b"])` -> `"a-b"` |
| `s.replace(old, new)` | Thay phần chuỗi | `"a-b".replace("-", " ")` -> `"a b"` |
| `s.count(x)` | Đếm số lần xuất hiện | `"banana".count("a")` -> `3` |
| `s.find(x)` | Vị trí xuất hiện đầu tiên | `"banana".find("na")` -> `2` |
| `s.startswith(x)` | Kiểm tra bắt đầu bằng `x` | `"Python".startswith("Py")` -> `True` |
| `s.endswith(x)` | Kiểm tra kết thúc bằng `x` | `"file.csv".endswith(".csv")` -> `True` |

`split()` thường đi cùng `join()` khi cần chuẩn hóa nhiều khoảng trắng:
```python
text = "  Python   co ban  "
normalized = " ".join(text.strip().lower().split())
print(normalized)
```

## Kiểm tra chuỗi và duyệt từng ký tự
Toán tử `in` kiểm tra một chuỗi con có xuất hiện hay không. Vòng lặp `for` dùng để duyệt từng ký tự hoặc từng từ.

```python
text = "Python"
print("Py" in text)

for character in text:
    print(character)
```

## Nhập chuỗi và lỗi thường gặp
`input()` luôn trả về chuỗi. Dùng f-string để ghép giá trị vào câu rõ ràng hơn:
```python
name = input("Name: ").strip()
print(f"Hello, {name}!")
```

Các lỗi thường gặp:
- Nhầm chỉ số bắt đầu từ 1 thay vì 0.
- Quên rằng vị trí `stop` trong slicing không được lấy.
- Dùng `+` giữa `str` và `int` mà chưa chuyển kiểu.
- Gọi `join()` trên chuỗi không phải dấu phân cách hoặc truyền phần tử không phải chuỗi.
- Quên gán kết quả của `strip()`, `lower()` hoặc `replace()` vào biến mới.
