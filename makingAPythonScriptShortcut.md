# Tạo một Shortcut Python Script (Create a Shortcut Python Script)

Đôi khi khi bạn tạo một tập lệnh, bạn muốn có thể chạy nó một cách thuận tiện chỉ với một nút bấm. May mắn thay, có một số cách để làm điều đó.

## Đầu tiên, chúng ta có thể tạo một lối tắt Windows với các cài đặt sau:

```python
\path\to\trc-image-titler.py -o \path\to\output
```

## Tương tự, chúng ta cũng có thể tạo một tệp bó với mã sau:

```python
@echo off
\path\to\trc-image-titler.py -o \path\to\output
```

## Cuối cùng, chúng ta có thể tạo một tập lệnh bash với đoạn mã sau:

```bash
#!/bin/sh
python /path/to/trc-image-titler.py -o /path/to/output
```
