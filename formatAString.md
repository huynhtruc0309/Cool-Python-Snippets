# Định dạng 1 String
Dù thích hay không, chúng ta cũng sẽ tự thấy rằng mình mình hay vùi dập các lệnh print xuyên suốt dòng code cho mục đích debug nhanh hơn. Sau tất cả, 1 lệnh print được đặt đúng chỗ có thể giúp bạn tiết kiệm được khá nhiều thời gian. Tuy nhiên, không phải lúc này cũng dễ dàng và tiện lợi để hiển thị đúng thứ ta muốn. Nhưng không sao cả, Python có khá nhiều lựa chọn cho ‘format’: 
``` python
name = "Truc Huynh"
age = 21
```
## Định dạng chuỗi bằng cách sử dụng concatenation
``` python
print("My name is " + name + ", and I am " + str(age) + " years old.")
```
## Định dạng chuỗi bằng nhiều lệnh print
``` python
print("My name is ", end="")
print(name, end="")
print(", and I am ", end="")
print(age, end="")
print(" years old.")
```
## Định dạng chuỗi bằng cách sử dụng join
``` python
print(''.join(["My name is ", name, ", and I am ", str(age), " years old"]))
```
## Định dạng chuỗi bằng cách sử dụng toán tử '%'
``` python
print("My name is %s, and I am %d years old." % (name, age))
```
## Định dạng chuỗi bằng cách sử dụng hàm format với tham số truyền theo thứ tự
``` python
print("My name is {}, and I am {} years old".format(name, age))
```
## Định dạng chuỗi bằng cách sử dụng hàm format với tham số được đặt tên
``` python
print("My name is {n}, and I am {a} years old".format(a=age, n=name))
```
## Định dạng chuỗi bằng cách sử dụng f-Strings (Python 3.6+)
``` python
print(f"My name is {name}, and I am {age} years old")
```
Hãy nghĩ rằng các giải pháp này không cần phải được dùng với lệnh print. Nói cách khác, bạn cứ thoải mái sử dụng các cách giải này như f-string bất kỳ đâu mà bạn cần.