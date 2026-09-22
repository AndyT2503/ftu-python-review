# Bài tập trên lớp

## Bài 1 - Tổng và đếm

```python
numbers = [2, 3, 30, 4, 5, 6, 7, 8, 9, 10]
total = 0
count_even = 0
for number in numbers:
    total += number
    if number % 2 == 0:
        count_even += 1
print(total, count_even)
```

## Bài 2 - In số từ 1 đến 100 chia hết cho 5

```python
for number in range(1, 101):
    if number % 5 == 0:
        print(number)
```

## Bài 3 - Vòng lặp nhập hợp lệ

```python
while True:
    score = float(input("Score 0-10: "))
    if 0 <= score <= 10:
        break
print(score)
```

## Bài 4 - Tổng từ 1 đến n
```python
n = int(input("n: "))
total = 0
for number in range(1, n + 1):
    total += number
print(total)
```