# Bài tập trên lớp

## Bài 1 - Dạng đúng đề thi

```python
python_list = [number for number in range(1, 101)]
print(137 in python_list)
print(22 in python_list)
```

## Bài 2 - Số chia hết cho 2 và 5
Tham khảo bài list comprehension trong Lecture 4.

```python
numbers = [2, 3, 30, 4, 5, 10, 15, 20]
answer = [number for number in numbers if number % 2 == 0 and number % 5 == 0]
print(answer)
```

## Bài 3 - Chuẩn hóa danh sách chữ

```python
words = ["python", "pandas", "sql"]
upper_words = [word.upper() for word in words]
print(upper_words)
```

## Bài 4 - Bình phương số lẻ
```python
squares = [number ** 2 for number in range(1, 11) if number % 2 != 0]
print(squares)
```

## Bài 5 - Lọc số chia hết cho 5
```python
numbers = [number for number in range(1, 51) if number % 5 == 0]
print(numbers)
```

## Bài 6 - Dùng hàm trong list comprehension
```python
def square(number):
	return number ** 2

squares = [square(number) for number in range(1, 6)]
print(squares)
```