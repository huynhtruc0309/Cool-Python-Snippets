# Sắp xếp danh sách liên kết các chuỗi

Sắp xếp là một nhiệm vụ phổ biến mà bạn mong đợi để biết cách thực hiện trong Khoa học máy tính. Mặc dù tập trung mạnh mẽ vào các thuật toán sắp xếp trong hầu hết các chương trình giảng dạy, không ai thực sự cho bạn biết cách sắp xếp phức tạp thực sự có thể có được. Chẳng hạn, việc sắp xếp các số rất đơn giản, nhưng còn việc sắp xếp các chuỗi thì sao? Làm thế nào để chúng ta quyết định một thứ tự thích hợp? May mắn thay, có rất nhiều tùy chọn trong Python:

## Duyệt trâu với sắp xếp nổi bọt

```python
my_list = ["leaf", "cherry", "fish"]
size = len(my_list)
for i in range(size):
    for j in range(size):
        if my_list[i] < my_list[j]:
            temp = my_list[i]
            my_list[i] = my_list[j]
            my_list[j] = temp

print(my_list)
```

```python
['cherry', 'fish', 'leaf']
```

## Sắp xếp bằng phương thức

```python
my_list.sort()
print(my_list)
```

```python
['cherry', 'fish', 'leaf']
```

## Sắp xếp bằng phương thức với con trỏ hàm

```python
my_list.sort(key=str.casefold)
print(my_list)
```

```python
['cherry', 'fish', 'leaf']
```

## Sắp xếp bằng phương thức sorted với con trỏ hàm

```python
my_list = sorted(my_list, key=str.casefold) 
print(my_list)
```

```python
['cherry', 'fish', 'leaf']
```

## Sắp xếp bằng package functools 

``` python
import locale
from functools import cmp_to_key
my_list = sorted(my_list, key=cmp_to_key(locale.strcoll))
print(my_list)
```

```python
['cherry', 'fish', 'leaf']
```

## Sắp xếp giảm dần

```python
my_list = sorted(my_list, key=str.casefold, reverse=True)
print(my_list)
```

```python
['cherry', 'fish', 'leaf']
```