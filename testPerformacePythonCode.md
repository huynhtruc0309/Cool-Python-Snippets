# Kiểm tra Hiệu năng
Bạn đôi lúc chỉ muốn so sánh 1 vài đoạn code. Và Python có vài sự lựa chọn đơn giản dành cho bạn
## Cách Brute force
``` python
import datetime
start_time = datetime.datetime.now()
[(a, b) for a in (1, 3, 5) for b in (2, 4, 6)] 
# example snippet
end_time = datetime.datetime.now()
print end_time - start_time
```
## Sử dụng timeit
``` python
import timeit
min(timeit.repeat("[(a, b) for a in (1, 3, 5) for b in (2, 4, 6)]"))
```
## Sử dụng cProfile 
``` python
cProfile.run("[(a, b) for a in (1, 3, 5) for b in (2, 4, 6)]")
```