# Bài tập trên lớp

Các bài luyện list và dictionary, không dùng hàm tự định nghĩa hoặc list comprehension vì hai nội dung đó học ở Buổi 6.

## Bài 1 - List cơ bản

```python
numbers = [10, 20, 30]
print(numbers[0], numbers[-1])
numbers.append(40)
print(len(numbers))
print(20 in numbers)
```

## Bài 2 - Cập nhật dictionary sinh viên

```python
student = {"name": "Lan", "age": 20}
print(student["name"])
student["age"] = 21
student["city"] = "Hanoi"
print(student)
```

## Bài 3 - Dictionary từ hai list

```python
keys = ["name", "age", "city"]
values = ["Lan", 20, "Hanoi"]
student = dict(zip(keys, values))
print(student)
```

## Bài 4 - Thống kê list

```python
numbers = [12, 7, 20, 5, 18]
print(sum(numbers))
print(min(numbers), max(numbers))
print(10 in numbers)
```

## Bài 5 - Truy cập dictionary an toàn

```python
student = {"name": "Lan", "age": 20}
print(student.get("email", "Chua co email"))
print("name" in student)
student["email"] = "lan@example.com"
print(student)
```

## Bài 6 - Danh sách sản phẩm

```python
products = ["book", "pen", "book", "bag"]
print(products.count("book"))
products.remove("pen")
products.append("notebook")
print(products)
```

## Bài 7 - Xử lý list dữ liệu

```python
scores = [8.5, 7.0, 9.0, 6.5]
scores[1] = 7.5
print(scores)
print(sum(scores) / len(scores))
```

## Bài 8 - Cập nhật nhiều bản ghi

```python
students = {
    "A01": {"name": "Lan", "score": 8.5},
    "A02": {"name": "Minh", "score": 7.0}
}
students["A02"]["score"] = 7.5
students["A03"] = {"name": "An", "score": 9.0}
print(students)
```

## Bài 9 - Tổng hợp list và dictionary

```python
numbers = [10, 15, 20, 25]
summary = {
    "count": len(numbers),
    "total": sum(numbers),
    "minimum": min(numbers),
    "maximum": max(numbers)
}
print(summary)
```
