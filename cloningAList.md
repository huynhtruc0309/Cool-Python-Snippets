# Tạo bản sao cho  danh sách liên kết (cloning a list)

Một trong những môn học yêu thích của tôi trong lập trình là sao chép các loại dữ liệu. Xét cho cùng, nó không bao giờ dễ dàng trong thế giới dựa trên tham chiếu này, và điều đó cũng đúng với Python. May mắn thay, nếu chúng ta muốn sao chép một  danh sách liên kết
, có một vài cách để làm điều đó:

## Sao chép  danh sách liên kết bằng cách duyệt trâu

```python
my_list = [27, 13, -11, 60, 39, 15]
my_duplicate_list = [item for item in my_list]
print(my_duplicate_list)
```

```python
[27, 13, -11, 60, 39, 15]
```

## Sao chép  danh sách liên kết với một lát

```python
my_duplicate_list = my_list[:]
print(my_duplicate_list)
```

```python
[27, 13, -11, 60, 39, 15]
```

## Sao chép  danh sách liên kết với hàm tạo  danh sách liên kết

```python
my_duplicate_list = list(my_list) 
print(my_duplicate_list)
```

```python
[27, 13, -11, 60, 39, 15]
```

## Sao chép  danh sách liên kết với chức năng sao chép (Python 3.3+)

```python
my_duplicate_list = my_list.copy()
```

```python
[27, 13, -11, 60, 39, 15]
```

## Sao chép  danh sách liên kết với gói sao chép

```python
import copy
my_duplicate_list = copy.copy(my_list)
my_deep_duplicate_list = copy.deepcopy(my_list)
print(my_duplicate_list)
print(my_deep_duplicate_list)
```

```python
[27, 13, -11, 60, 39, 15]
[27, 13, -11, 60, 39, 15]
```

Và sự khác biệt của copy và deepcopy 

```python
import copy

a = my_list
shallow = copy.copy(my_list)
deep = copy.deepcopy(my_list)
```

![Minh họa](/image/deepcopy.png)
- a là dùng danh sách liên kết cũ chỉ tạo mới biến trỏ đến danh sách liên kết cũ 

- shallow là taọ dùng danh sách liên kết mới nhưng các không tạo mới địa chỉ của phần tử trong danh sách liên kết 

- deep là tạo mới hoàn toàn

## Sao chép một  danh sách liên kết với phép nhân? (nên tránh)

```python
my_duplicate_list = my_list * 1  
```

```python
[27, 13, -11, 60, 39, 15]
```
