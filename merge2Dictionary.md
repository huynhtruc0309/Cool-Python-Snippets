# Gộp 2 Dictionary
Trong bộ sưu tập này, ta đã nói rất nhiều về việc xử lý các cấu trúc data như list và dictionary. Vâng, cái này cũng sẽ tương tự. Cụ thể hơn là, chúng ta đang xem về việc gộp 2 dictionary lại với nhau. Dĩ nhiên, việc hợp nhất 2 dictionary sẽ mang vài rủi ro. Ví dụ: Nếu có các key bị lặp (duplicate key) thì sẽ ra sao? Thật may vì ta sẽ có các giải pháp cho nó:
``` python
truc_power = {"Phuong Truc": "Spirit Gun"}
truong_power = {"Nhut Truong": "Jagan Eye"}
powers = dict()
```
## Brute force
``` python
for dictionary in (truc_power, truong_power): 
  for key, value in dictionary.items(): 
    powers[key] = value
```
## Dictionary Comehension
``` python
powers = {key: value for d in (yusuke_power, hiei_power) for key, value in d.items()}
```
## Sao chép và cập nhật
``` python
powers = yusuke_power.copy()
powers.update(hiei_power)
```
## Giải nén Dictionary (Python 3.5+)
``` python
powers = {**yusuke_power, **hiei_power}
```
## Hàm tương thích ngược cho bất kỳ số lượng dicts
``` python
def merge_dicts(*dicts: dict): 
  merged_dict = dict() 
  for dictionary in dicts: 
    merge_dict.update(dictionary) 
  return merged_dict
```