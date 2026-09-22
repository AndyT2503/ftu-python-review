# Bài tập trên lớp

## Bài 1 - Diện tích nhà
Nhập `width`, `height`, tính và in `area`.

```python
width = float(input("Width: "))
height = float(input("Height: "))
area = width * height
print(f"Area = {area}")
```

## Bài 2 - Tiền sau giảm giá
Nhập giá và phần trăm giảm, in số tiền phải trả.

```python
price = float(input("Price: "))
discount = float(input("Discount (%): "))
final_price = price * (1 - discount / 100)
print(final_price)
```

## Bài 3 - Đổi nhiệt độ

```python
celsius = float(input("Celsius: "))
fahrenheit = celsius * 9 / 5 + 32
print(fahrenheit)
```

## Bài 4 - Đổi giây

```python
total_seconds = int(input("Seconds: "))
hours = total_seconds // 3600
minutes = (total_seconds % 3600) // 60
seconds = total_seconds % 60
print(hours, minutes, seconds)
```

## Bài 5 - Ngày mai

```python
from datetime import date, timedelta

tomorrow = date.today() + timedelta(days=1)
print(tomorrow)
```

## Bài 6 - Đếm ngày tới kỳ thi

```python
from datetime import datetime, date

text = input("Exam date (dd/mm/yyyy): ")
exam_date = datetime.strptime(text, "%d/%m/%Y").date()
days_left = exam_date - date.today()
print(days_left.days)
```