# Bài tập trên lớp

## Bài 1 - Giải ax + b = c

```python
a = float(input("a: "))
b = float(input("b: "))
c = float(input("c: "))
if a == 0 and b == c:
    print("Vo so nghiem")
elif a == 0:
    print("Vo nghiem")
else:
    print((c - b) / a)
```

## Bài 2 - Phân loại số

```python
number = float(input("Number: "))
if number < 0:
    print("negative")
elif number == 0:
    print("zero")
else:
    print("positive")
```

## Bài 3 - Xếp loại điểm

```python
score = float(input("Score: "))
if score >= 8:
    result = "Good"
elif score >= 6.5:
    result = "Fair"
elif score >= 5:
    result = "Pass"
else:
    result = "Fail"
print(result)
```

## Bài 4 - Số lớn nhất
```python
a, b, c = 4, 9, 2
if a >= b and a >= c:
    largest = a
elif b >= c:
    largest = b
else:
    largest = c
print(largest)
```

## Bài 5 - Kiểm tra khoảng
```python
age = int(input("Age: "))
print(18 <= age <= 60)
```

## Bài 6 - Điều kiện lồng
```python
score = float(input("Score: "))
if 0 <= score <= 10:
    if score >= 5:
        print("Pass")
    else:
        print("Fail")
else:
    print("Invalid")
```