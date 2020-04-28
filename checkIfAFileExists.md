# Kiểm tra nếu một file có tồn tại

Một trong những đặc quyền tuyệt vời của Python là việc quản lý tệp dễ dàng như thế nào. Không giống như Java, Python có cú pháp tích hợp để đọc và ghi tệp. Kết quả là, kiểm tra nếu một tập tin tồn tại là một nhiệm vụ khá ngắn gọn:

## Duyệt trâu (Brute force) với try-except

``` python
try: 
    with open('/path/to/file', 'r') as fh:
        pass
except FileNotFoundError: 
    pass
```

## Tận dụng gói OS (có thể  tranh đoạt tiến trình (possible race condition))

``` python
import os 
exists = os.path.isfile('/path/to/file')
```

## Bọc đường dẫn trong một đối tượng để tái sử dụng những hàm có sẵn trong đối tướng 

```python
from pathlib import Path
config = Path('/path/to/file') 
if config.is_file(): 
    pass
```

