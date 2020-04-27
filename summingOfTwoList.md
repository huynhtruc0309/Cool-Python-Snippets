# Tổng các phần tử của 2 danh sách liên kế (Summing of two list)
Hãy nói rằng bạn có hai danh sách liên kết(list) và bạn muốn hợp nhất chúng thành một danh sách liên kết (list) theo từng phần tử. Nói cách khác, bạn muốn thêm phần tử đầu tiên của danh sách đầu tiên vào phần tử đầu tiên của danh sách liên kết(list) thứ hai và lưu kết quả vào một danh sách liên kết (list) mới. Vâng, có một số cách để làm điều đó:

## Cách dài dòng (nên tránh)

``` python
ethernet_devices = [1, [7], [2], [8374163], [84302738]]
usb_devices = [1, [7], [1], [2314567], [0]]
print(all_devices)
```

```python
[2, [7, 7], [2, 1], [8374163, 2314567], [84302738, 0]]
```

## Cú pháp comprehension (dành riêng cho python)

```python 
all_devices = [x + y for x, y in zip(ethernet_devices, usb_devices)]
print(all_devices)
```

```python
[2, [7, 7], [2, 1], [8374163, 2314567], [84302738, 0]]
```

## Sử dụng ánh xạ (map)
```python
import operator 
all_devices = list(map(operator.add, ethernet_devices, usb_devices))
print(all_devices)
```
```python
[2, [7, 7], [2, 1], [8374163, 2314567], [84302738, 0]]
```

## Thư viện numpy 

```python
import numpy as np 
all_devices = np.add(ethernet_devices, usb_devices)
print(all_devices)
```

```python
[2, [7, 7], [2, 1], [8374163, 2314567], [84302738, 0]]
```
