# Buổi 1 - Biến, kiểu dữ liệu, nhập liệu và datetime

## Biến là gì?
Biến là một tên dùng để lưu một giá trị. Dấu `=` là phép gán: vế phải được tính trước rồi lưu vào tên ở vế trái.

```python
width = 5
height = 3
area = width * height
print(area)
```

Tên biến nên mô tả dữ liệu, dùng chữ thường và dấu gạch dưới: `birth_year`, `total_price`. Không dùng dấu cách và không đặt tên bắt đầu bằng số.

## Các kiểu dữ liệu cơ bản
| Kiểu | Ý nghĩa | Ví dụ | Ghi chú |
|---|---|---|---|
| `str` | Chuỗi ký tự/văn bản | `"Python"`, `"123"` | `"123"` chưa phải số |
| `int` | Số nguyên | `10`, `-3` | Không có phần thập phân |
| `float` | Số thực | `3.14`, `10.0` | Dùng cho giá trị có phần lẻ |
| `bool` | Giá trị logic | `True`, `False` | Dùng trong điều kiện |

```python
name = "Lan"          # str
age = 20               # int
height = 1.62          # float
is_student = True      # bool
print(type(name))
```

`type(value)` cho biết kiểu dữ liệu của `value`.

## Nhập và xuất dữ liệu
`input(prompt)` hiển thị lời nhắc và luôn trả về một giá trị kiểu `str`. Vì vậy dữ liệu nhập để tính toán phải được chuyển kiểu.

```python
name = input("Name: ")
age = int(input("Age: "))
height = float(input("Height: "))
print(f"{name} is {age} years old")
```

f-string đặt chữ `f` trước chuỗi và cho phép đưa biến vào trong `{}`.

## Ép kiểu và chuyển kiểu
| Hàm | Chuyển thành | Ví dụ |
|---|---|---|
| `int(value)` | Số nguyên | `int("25")` -> `25` |
| `float(value)` | Số thực | `float("3.5")` -> `3.5` |
| `str(value)` | Chuỗi | `str(25)` -> `"25"` |
| `bool(value)` | Logic | `bool(0)` -> `False` |

Ép kiểu là tạo giá trị mới thuộc kiểu mong muốn:

```python
text_number = "25"
number = int(text_number)       # str -> int
decimal = float(text_number)    # str -> float
text = str(25)                  # int -> str
logic = bool(1)                 # 1 -> True
```

`int("3.5")` gây lỗi vì chuỗi đó không biểu diễn trực tiếp một số nguyên. Dùng `int(float("3.5"))` nếu muốn bỏ phần thập phân. `bool(0)` là `False`, hầu hết giá trị khác 0 là `True`; chuỗi rỗng là `False`, chuỗi không rỗng là `True`.

## Toán tử số học
| Toán tử | Ý nghĩa | Ví dụ | Kết quả |
|---|---|---|---|
| `+` | Cộng | `5 + 2` | `7` |
| `-` | Trừ | `5 - 2` | `3` |
| `*` | Nhân | `5 * 2` | `10` |
| `/` | Chia thường | `5 / 2` | `2.5` |
| `//` | Chia lấy phần nguyên | `5 // 2` | `2` |
| `%` | Lấy số dư | `5 % 2` | `1` |
| `**` | Lũy thừa | `2 ** 3` | `8` |

```python
print(17 / 4)   # 4.25
print(17 // 4)  # 4
print(17 % 4)   # 1
print(2 ** 3)   # 8
```

Python tính ngoặc trước, rồi `**`, rồi `* / // %`, sau đó `+ -`. Dùng ngoặc để biểu diễn rõ ý định.

## Ngày và giờ
```python
from datetime import date, datetime, timedelta

today = date.today()
exam_date = date(2026, 10, 9)
print(today)
print(exam_date - today)
print(datetime.now().strftime("%d/%m/%Y %H:%M"))
print(today + timedelta(days=1))
```

`date` biểu diễn ngày, `datetime` biểu diễn ngày và giờ, `timedelta` biểu diễn một khoảng thời gian. `date(2026, 10, 9)` là ngày 09/10/2026. `strftime` định dạng ngày thành chuỗi: `%d` ngày, `%m` tháng, `%Y` năm, `%H` giờ, `%M` phút. Đổi chuỗi thành ngày bằng:

```python
text = "09/10/2026"
exam_date = datetime.strptime(text, "%d/%m/%Y").date()
```

## Lỗi thường gặp
- Quên ép kiểu cho kết quả của `input()`.
- Dùng `/` trong khi cần chia lấy phần nguyên.
- Nhầm `"10"` là số 10; một bên là `str`, một bên là `int`.
- Dùng sai định dạng khi gọi `strptime`.