# Chuyển đổi hai danh sách liên kết (list) thành một từ điển (dictionary)

Trước đây, chúng tôi đã nói về việc tóm tắt hai danh sách liên kết trong Python. Hóa ra, có rất nhiều thứ chúng ta có thể làm với hai danh sách liên kết. Ví dụ: chúng ta có thể thử ánh xạ cái này sang cái khác để tạo một từ điển.

Cũng như nhiều vấn đề này, có một vài lo ngại. Chẳng hạn, nếu hai danh sách này có cùng kích thước thì sao? Tương tự như vậy, nếu các khóa không duy nhất (aren't unique) hoặc không có thể băm(aren't hashable) thì sao? Trong trường hợp đơn giản, có một số giải pháp đơn giản:

## Chuyển đổi hai danh sách liên kết thành một từ điển với zip và hàm khởi tạo dict

```python
column_names = ['id', 'color', 'style']
column_values = [1, 'red', 'bold']
name_to_value_dict = dict(zip(column_names, column_values))
print(name_to_value_dict)
```

```python
{'id': 1, 'color': 'red', 'style': 'bold'}
```

## Chuyển đổi hai danh sách liên kết thành một từ điển

```python
column_names = ['id', 'color', 'style',  'id', 'id']
column_values = [1, 'red', 'bold', 4, 5]

name_value_tuples = zip(column_names, column_values) 
name_to_value_dict = {} 
for key, value in name_value_tuples:
    name_to_value_dict.setdefault(key, list()).append(value)
print(name_to_value_dict)
```

```python
{'id': [1, 4, 5], 'color': ['red'], 'style': ['bold']}
```
