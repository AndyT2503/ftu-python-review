# Bài tập trên lớp

## Bài 1 - DataFrame đúng dạng đề

```python
import pandas as pd
from sklearn.linear_model import LinearRegression

data = {"cities": ["Glasgow", "Edinburgh", "Aberdeen", "Dundee", "Hanoi"], "gdp": [50, 40, 30, 25, 60], "population": [54490, 16940, 44950, 24260, 34560], "year": [2013] * 5}
df = pd.DataFrame(data)
df["size"] = [450, 560, 230, 240, 340]
print(df.head(3))
print(df.iloc[1:3])
print(df["population"].mean())
print(df["population"].std())
print(df["population"].min(), df["population"].max())
print(df[["population", "gdp"]].corr())
```

## Bài 2 - Hồi quy

```python
X = df[["population"]]
y = df["gdp"]
model = LinearRegression()
model.fit(X, y)
print(model.coef_[0])
print(model.intercept_)
print(model.score(X, y))
```

## Bài 3 - Đọc dữ liệu từ CSV

Tạo file `cities.csv` có các cột `city`, `gdp`, `population`, sau đó đọc file.

```python
import pandas as pd

df_csv = pd.read_csv("cities.csv")
print(df_csv.head())
```

## Bài 4 - Đọc dữ liệu từ SQL

Ví dụ với SQLite. Database phải có bảng `cities` gồm các cột `city`, `gdp`, `population`.

```python
import sqlite3
import pandas as pd

connection = sqlite3.connect("cities.db")
df_sql = pd.read_sql_query(
	"SELECT city, gdp, population FROM cities",
	connection
)
connection.close()
print(df_sql.head())
```

## Bài 5 - Thực hành chọn cột
Tạo `df_small` chỉ gồm `cities`, `gdp`, `population` và in 2 dòng cuối bằng `tail(2)`.

```python
df_small = df[["cities", "gdp", "population"]]
print(df_small.tail(2))
```