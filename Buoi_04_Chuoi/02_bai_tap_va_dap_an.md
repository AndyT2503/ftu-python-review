# Bài tập trên lớp

Các bài được sắp xếp từ thao tác cơ bản đến bài tổng hợp. Dành khoảng 8-12 phút cho mỗi bài, sau đó chữa các lỗi chỉ số, kiểu dữ liệu và cách chuẩn hóa dữ liệu.

## Bài 1 - Cắt và đảo chuỗi
Với `s = "Data Python"`, in từ đầu, từ cuối, độ dài, hai từ bằng slicing và chuỗi đảo ngược.

```python
s = "Data Python"
print(s[:4])
print(s[5:])
print(len(s))
print(s[::-1])
```

## Bài 2 - Phân tích ký tự
Đếm số chữ cái `a`, số khoảng trắng và in ký tự đầu/cuối của chuỗi.

```python
text = "Data Python"
lower_text = text.lower()
print(lower_text.count("a"))
print(text.count(" "))
print(text[0], text[-1])
```

## Bài 3 - Chuẩn hóa họ tên
Xóa khoảng trắng thừa ở đầu/cuối và viết hoa chữ cái đầu mỗi từ.

```python
name = "  nguyen van an  "
clean_name = name.strip().title()
print(clean_name)
```

## Bài 4 - Chuẩn hóa câu
Đưa câu về chữ thường và chỉ giữ một khoảng trắng giữa các từ.

```python
text = "  Python   co ban  "
normalized_text = " ".join(text.strip().lower().split())
print(normalized_text)
```

## Bài 5 - Tách và ghép dữ liệu
Tách họ tên thành danh sách từ, in danh sách và ghép lại bằng dấu gạch ngang.

```python
name = "Nguyen Van An"
words = name.split()
print(words)
print("-".join(words))
```

## Bài 6 - Tìm và thay thế
Kiểm tra câu có chứa từ `python`, tìm vị trí của từ đó và thay bằng `programming`.

```python
text = "I learn Python programming"
lower_text = text.lower()
print("python" in lower_text)
print(lower_text.find("python"))
print(text.replace("Python", "Programming"))
```

## Bài 7 - Thống kê từ trong câu
Nhập một câu, chuẩn hóa khoảng trắng, đếm số từ và in từ dài nhất.

```python
text = input("Sentence: ")
words = " ".join(text.strip().split()).split()
print("Word count:", len(words))
if words:
    longest_word = max(words, key=len)
    print("Longest:", longest_word)
```

## Bài 8 - Kiểm tra chuỗi đối xứng
Nhập một chuỗi, bỏ khoảng trắng và chuyển về chữ thường. Kiểm tra chuỗi có đọc xuôi và ngược giống nhau không.

```python
text = input("Text: ")
clean_text = "".join(text.lower().split())
if clean_text == clean_text[::-1]:
    print("Palindrome")
else:
    print("Not palindrome")
```
