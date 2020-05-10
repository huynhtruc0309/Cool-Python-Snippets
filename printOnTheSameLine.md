# Print trên cùng 1 Dòng
Đi cùng với dòng tương tự như việc định dạng các string, đôi lúc bạn chỉ cần để print trên cùng 1 dòng trong Python. Cũng như lệnh “ print “ hiện tại được thiết kế, nó tự động áp dụng 1 dòng mới tới cuối dòng string của bạn. May thay, có 1 vài cách bên cạnh đó:
## Chỉ với Python 2
``` python
print "Live PD",
```
## Tương thích ngược (cách nhanh nhất)
``` python
import sys
sys.stdout.write("Breaking Bad")
```
## Chỉ với Python 3
``` python
print("Mob Psycho 100", end="")
```