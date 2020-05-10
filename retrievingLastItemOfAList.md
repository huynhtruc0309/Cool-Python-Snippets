# Truy xuất vào phần tử cuối của danh sách liên kết
Vì chúng tôi về chủ đề của danh sách liên kết, hãy nói về việc lấy mục cuối cùng của danh sách liên kết. Trong hầu hết các ngôn ngữ, điều này liên quan đến một số biểu thức toán học phức tạp liên quan đến độ dài của danh sách. Điều gì sẽ xảy ra nếu tôi nói với bạn rằng có một số giải pháp thú vị hơn trong Python?

## Lấy vật phẩm cuối cùng bằng vũ lực bằng cách sử dụng len

```python 
my_list = ['red', 'blue', 'green']
last_item = my_list [len (my_list) - 1]
print(last_item)
```

```python
green
```

## Xóa mục cuối cùng khỏi danh sách bằng pop

```python
last_item = my_list.pop()
print(last_item)
print(my_list)
```

```python
green
['red', 'blue']
```

## Nhận mục cuối cùng bằng chỉ số phủ định * phương pháp ưa thích & nhanh nhất *

```python
last_item = my_list [-1]
print(last_item)
```

```python
blue
```

## Nhận mục cuối cùng bằng cách sử dụng giải nén lặp

```python
* _, last_item = my_list
print(last_item)
```

```python
blue
```
