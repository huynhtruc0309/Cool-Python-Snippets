# Kiểm tra danh sánh liên kết (list) rỗng (empty)

Nếu bạn bắt đầu một ngôn ngữ được gõ tĩnh như Java hoặc C, bạn có thể bị làm phiền bởi việc thiếu các kiểu tĩnh trong Python. Chắc chắn, không biết loại biến đôi khi có thể gây bực bội, nhưng cũng có những đặc quyền. Chẳng hạn, chúng ta có thể kiểm tra xem một danh sách có trống không bởi loại linh hoạt của nó trong số các phương thức khác:

## Kiểm tra xem danh sách có trống không theo chiều dài của nó

```python
if len(my_list) == 0:
    pass  # danh sách liên kết rỗng
```

## Kiểm tra xem danh sách có trống không bằng cách so sánh trực tiếp (chỉ hoạt động cho danh sách)

```python
if my_list == []:
    pass  # danh sách liên kết rỗng
```

## Kiểm tra xem danh sách có trống không bởi tính linh hoạt của loại (phương thức ưa thích)

```python
if not my_list:
    pass  # danh sách liên kết rỗng
```