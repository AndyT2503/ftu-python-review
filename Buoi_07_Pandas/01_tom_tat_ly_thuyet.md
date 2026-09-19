# Buổi 7 - Pandas và hồi quy tuyến tính

## Pandas và DataFrame
Pandas là thư viện xử lý dữ liệu dạng bảng. `DataFrame` giống một bảng gồm hàng và cột; mỗi cột thường có một kiểu dữ liệu. `Series` là một cột dữ liệu.

## Tạo và xem DataFrame
```python
import pandas as pd

df = pd.DataFrame(data)
df.head(3)
df.iloc[1:3]
df["population"].mean()
df["population"].std()
df["population"].min()
df["population"].max()
df[["population", "gdp"]].corr()
```

```python
from sklearn.linear_model import LinearRegression
X = df[["population"]]
y = df["gdp"]
model = LinearRegression()
model.fit(X, y)
coefficient = model.coef_[0]
intercept = model.intercept_
r_square = model.score(X, y)
```

- `X` phải là DataFrame hai chiều, `y` là Series.
- `iloc[1:3]` lấy dòng chỉ số 1 và 2.

## Đọc dữ liệu từ dictionary, CSV và SQL
### Từ dictionary
Dictionary phù hợp với dữ liệu nhỏ được viết trực tiếp trong code. Các list làm giá trị nên có cùng độ dài.

```python
data = {
	"city": ["Hanoi", "Da Nang"],
	"population": [8000000, 1200000]
}
df = pd.DataFrame(data)
```

### Từ file CSV
CSV là file dạng bảng, thường có dòng đầu là tên cột và các giá trị được ngăn cách bằng dấu phẩy. `read_csv` đọc file và trả về DataFrame.

```python
df = pd.read_csv("data.csv")
print(df.head())
```

Nếu file dùng dấu phân cách khác, truyền thêm `sep`, ví dụ `pd.read_csv("data.csv", sep=";")`. Đường dẫn tương đối được tính từ thư mục đang chạy notebook.

### Từ SQL
Có thể dùng `sqlite3` để kết nối một database SQLite rồi dùng `pd.read_sql_query` đọc kết quả truy vấn vào DataFrame.

```python
import sqlite3

connection = sqlite3.connect("school.db")
df = pd.read_sql_query("SELECT * FROM students", connection)
connection.close()
print(df.head())
```

`connect` mở kết nối, câu lệnh `SELECT` chỉ đọc dữ liệu, `read_sql_query` biến kết quả thành DataFrame và `close` đóng kết nối. Khi dùng database khác, cần cài driver tương ứng.

| Nguồn dữ liệu | Hàm thường dùng | Kết quả |
|---|---|---|
| Dictionary | `pd.DataFrame(data)` | DataFrame |
| CSV | `pd.read_csv(path)` | DataFrame |
| SQL | `pd.read_sql_query(query, connection)` | DataFrame |

| Lệnh | Ý nghĩa |
|---|---|
| `pd.DataFrame(data)` | Tạo DataFrame |
| `df.head(n)` | Lấy `n` dòng đầu |
| `df.tail(n)` | Lấy `n` dòng cuối |
| `df.shape` | Số hàng và số cột |
| `df["column"]` | Chọn một Series |
| `df[["a", "b"]]` | Chọn nhiều cột |
| `df.iloc[1:3]` | Lấy dòng vị trí 1 và 2 |

## Thống kê và tương quan
| Phương thức | Ý nghĩa |
|---|---|
| `mean()` | Trung bình |
| `std()` | Độ lệch chuẩn |
| `min()`, `max()` | Nhỏ nhất, lớn nhất |
| `corr()` | Ma trận tương quan |

## Hồi quy tuyến tính
Mô hình tìm quan hệ gần dạng `y = intercept + coefficient * x`. `X` là biến đầu vào dạng DataFrame hai chiều, `y` là biến cần dự đoán. `fit` học mô hình; `coef_` là hệ số, `intercept_` là hệ số chặn và `score` trả về R-square.

## Code mẫu hoàn chỉnh
```python
import pandas as pd
from sklearn.linear_model import LinearRegression

data = {"cities": ["Glasgow", "Edinburgh", "Aberdeen", "Dundee", "Hanoi"],
	"gdp": [50, 40, 30, 25, 60],
	"population": [54490, 16940, 44950, 24260, 34560],
	"year": [2013] * 5}
df = pd.DataFrame(data)
df["size"] = [450, 560, 230, 240, 340]
print(df.head(3))
print(df.iloc[1:3])
print(df["population"].mean())
print(df["population"].std())
print(df["population"].min(), df["population"].max())
print(df[["population", "gdp"]].corr())

X = df[["population"]]
y = df["gdp"]
model = LinearRegression().fit(X, y)
print(model.coef_[0], model.intercept_, model.score(X, y))
```