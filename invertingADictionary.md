# Đảo ngược một từ điển (Inverting a dictionary)
Đôi khi khi chúng ta có một từ điển(dictionary), chúng ta muốn có thể  đảo ngược các khóa (keys) và giá trị (values) của nó. Tất nhiên, có những lo ngại như "làm thế nào để chúng ta đối phó với các giá trị trùng lặp?" và "nếu giá trị(value) không có thể băm(aren't hashable) thì sao?" Điều đó nói rằng, trong trường hợp đơn giản, có một vài giải pháp(solution):


## Đảo ngược từ điển (invert dictionary) có giá trị duy nhất (unique key).
``` python
my_dict = {
  'Phuong Truc': 'is hard-working', 
  'Truong Le': 'is smart', 
  'HCMUS': 'is one of most university in Vietnam'
}
my_inverted_dict = dict(map(reversed, my_dict.items()))
print(my_inverted_dict)
print()
my_inverted_dict = {value: key for key, value in my_dict.items()}
print(my_inverted_dict)
```

```python 
{'is hard-working': 'Phuong Truc', 'is smart': 'Truong Le', 'is one of most university in Vietnam': 'HCMUS'}

{'is hard-working': 'Phuong Truc', 'is smart': 'Truong Le', 'is one of most university in Vietnam': 'HCMUS'}
```

## Đảo ngược từ điển(invert dictionary) có giá trị không duy nhất(non-unique key).

``` python 
my_dict = {'a': 1, 'b': 1, 'c': 1, 'd': 2, 'e': 2, 'f': 2}
from collections import defaultdict
my_inverted_dict = defaultdict(list)
{my_inverted_dict[v].append(k) for k, v in my_dict.items()}
print(my_inverted_dict)
print()

my_inverted_dict = dict()
for key, value in my_dict.items():
    my_inverted_dict.setdefault(value, list()).append(key)
print(my_inverted_dict)
```

```python
defaultdict(<class 'list'>, {1: ['a', 'b', 'c'], 2: ['d', 'e', 'f']})

{1: ['a', 'b', 'c'], 2: ['d', 'e', 'f']}
```

## Đảo ngược từ điển có danh sách các giá trị

```python 
my_inverted_dict = {1: ['a', 'b', 'c'], 2: ['d', 'e', 'f']}
my_dict = {value: key for key in my_inverted_dict for value in my_inverted_dict[key]}
print(my_dict)
```

```
{'a': 1, 'b': 1, 'c': 1, 'd': 2, 'e': 2, 'f': 2}
```
