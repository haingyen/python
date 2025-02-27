# BASIC
# 0. Install and setup Python
# 1. Kiểu dữ liệu - Data Types
Các kiểu dữ liệu cơ bản trong Python:
- `str`: Chuỗi ký tự 
```
name = 'Vi'

print(name)             #> output: Vi
print(f"Hello, {name}") #> output: Hello, Vi
print(type(name))       #> output: `str`
```
- `int`: Integer - Số Nguyên 
```
age = 22

print(age)          #> output: 22
print(type(age))    #> output: `int`
```
- `float`: Số thực
```
gpa_score = 3.66 

print(gpa_score)        #> output: 3.66
print(type(gpa_score))  #> output: `float`
```
- `bool`: True or False | 1 or 0
```
is_goal = True

print(is_goal)          #> output: True
print(is_goal + 9)      #> output: 10
print(type(is_goal))    #> output: `bool`

```
- `None`: Tương đương False
```
email_address = None

print(email_address)        #> None
print(type(email_address))  #> output: `None`
```
**NOTE**:
- `name`, `age`, `gpa_score`, `is_goal`, `email_address`: biến - variable
- `=`: phép gán
- `str`, `int`, `float`, `bool`, `None`: kiểu dữ liệu - data types
- `print()`: hàm in giá trị 
- `type()`: hàm kiểm tra kiểu dữ liệu của một biến
- `f""`: dùng để kết hợp chuỗi ký tự với biến
- **Các quy tắc đặt tên biến trong Python**:
  - a
  - b
  - c
  - d
# 2. TEST
# 3. Arthimetic & Math

**Các phép toán cơ bản trong Python**:
- `+`: cộng `print(6+4) => 10`
- `-`: trừ `print(8-2) => 6`
- `*`: nhân `print(6*11) => 66`
- `**`: mũ `print(2**3) => 8`
- `/`: chia `print(10/3) => 3.33333`
- `//`: chia lấy phần nguyên `print(10//3) => 3`
- `%`: chia lấy phần dư `print(10%3) => 1`
**Basic Funtion (Hàm cơ bản)**:
- `pow()`: hàm mũ `print(pow(2, 3)) => 8`
- `abs()`: hàm trị tuyệt đối `print(abs(-10)) => 10`
- `round()`: hàm làm tròn `print(round(5.69)) => 6`
  - Làm tròn đến số thập phân thứ 1 `print(round(6.582, 1)) => 6.6`
- `bin()`: hàm chuyển sang số nhị phân 
- `hex()`: hàm chuyển sang số lục phân 
# 4. Typecasting
# 5. User input()
# 6. String and String methods - Chuỗi ký tự và hàm xử lý chuỗi ký tự
String được để trong `' '` hoặc `" "`: 
```
my_string = 'Hello!'
print(my_string, type(my_string))   #> Hello `str`

var_a = "I'm a Data Analyst"
print(var_a)                        #> I'm a Data Analyst

var_b = 'I\'m a "Beginner"'         #> I'm a "Beginner"
```

Để truy cập đến ký tự hoặc phần tử con trong String có thể dùng index - index trong Python bắt đầu từ số 0
```
my_string = 'Hello, World!'
# index      0123456789...

# Truy cập index 0 trong chuỗi `my_string` và lưu vào biến `char`
char = my_string[0]
print(char)             #> H

print(my_string[7])     #> W
print(my_string[5])     #> ,

# index -1 tương đương ký tự cuối của chuỗi
print(my_string[-1])    #> !
print(my_string[-2])    #> d
print(my_string[-3])    #> l
```

Truy cập một đoạn trong chuỗi dùng: [index bắt đầu: index kết thúc] nhưng không bao gồm ký tự của index kết thúc:

```
my_string = 'Hello, world!'
             0123456789...
# Lấy đoạn `Hello` index bắt đầu là 0, index kết thúc là 5 (không bao gồm ký tự `,`)

sub_string = my_string[0:5]
print(sub_string)       #> Hello

print(my_string[:6])    #> Hello,
print(my_string[2:6])   #> llo,
print(my_string[7:-1])  #> world
print(my_string[7:])    #> world!
print(my_string[::-1])  #> Đảo ngược chuỗi
print(my_string[::2])   #> Hlo o l! 
```
Nối chuỗi với `+`
```
greeting = 'Hello'
name = 'Vi'

concatenate = greeting + ' cac ban, toi la ' + name
print(concatenate) #> Hello cac ban, toi là Vi
```
Nối chuỗi với `join()`
```
my_list = ['anh', 'em']
concatenate = ' '.join(my_list)
print(concatenate)    #> anh em

concatenate = '&'.join(my_list)
print(concatenate)    #> anh&em 
```
Xóa khoảng trống đầu và cuối chuỗi `strip()`
```
var_a = '  Hello  '
print(var_a.strip())    #> Hello
```
Tách các phần tử trong chuỗi thành mảng phần tử `split()`
```
var_b = 'Life is good'
var_c = 'Hello, world abc xyz '
print(var_b.split())    #> ['Life', 'is', 'good']
print(var_c.split(',')) #> ['Hello', 'world abc xyz']
```

Thay thế chuỗi `replace()`
```
var_u = 'Hate you'
# Thay chuỗi `Hate` = `Love`
print(var_u.replace('Hate', 'Love))  #> Love you 
```

Kiểm tra chuỗi có bắt đầu/kết thúc bằng ký tự cụ thể nào không `startswith()`/`endswith()`
```
var_s = 'Love you'

# Kiểm xem chuỗi có bắt đầu bằng `Love` hay không
print(var_s.startswith('Love'))    #> True

# Kiểm xem chuỗi có kết thúc bằng `water` hay không
print(var_s.endswith('water'))    #> False
```
Xem vị trí của ký tự trong chuỗi `index()` và `find()`
```
var_i = 'See you again!'
         0.2...6
# Xem index của ký tự `u` trong chuỗi
print(var_i.index('u'))     #> 6
print(var_i.find('u'))      #> 6
```
IN HOA ký tự trong chuỗi `upper()`
```
var_x = 'abc'
print(var_x.upper())    #> ABC
```
in thường ký tự trong chuỗi `lower()`
```
var_y = 'XYZ'
print(var_y.lower())    #> xyz
```
In hoa các ký tự đầu trong chuỗi `title()`
```
var_f = 'how are you'
print(var_f.title())    #> How Are You
```
Chỉ in hoa ký tự đầu trong chuỗi `capitalize()`
``` 
var_h = 'how are you'
print(var_h.capitalize())    #> How are you
```
Đếm ký tự trong chuỗi `count()`
``` 
var_c = 'how are you'
# Điếm ký tự `o`
print(var_c.count('o'))    #> 2
```
String Formatting - Định dạng chuỗi `%`, `format()` hoặc `f""`
```
# f-strings 

height = 175.262  #float
name = 'H'        #str
age = 25          #int

my_string = f"Hello, My name is {name}, {age} year old and my height is {height:.2f} cm"
#> Hello, My name is H, 25 year old and my height is 175.26 cm
# {height:.2f} `f` có nghĩa kiểu dữ liệu của `height` là float và `.2` làm tròn đến số thập phân thứ 2

```
<!-- # 7. String indexing -->
# 8. Format specifier
# 9. if statements
# 10. Logical Operators
# 11. For loops
# 12. While loops
# 13. Nested loops
# 14. Lits, Tuples, Sets
# 15. Dictionaries
# 16. Random Number
# 17. Functions
# 18. Default arguments 
# 19. Keyword arguments
# 20. *args & **kwargs
# 21. Iterables 
# 22. Membership operators 
# 23. List comprehensions 
# 24. Match-case statements 
# 25. Modules 
# 26. Scope resolution
# 27. if name == 'main':
# 28. File detection 
# 29. Writing files 
# 30. Reading files 
# 31. Dates & times 
# 32. Exception handling 

# ADVANDED
# 33. Python Object Oriented Programming 
# 34. Class variables 
# 35. Inheritance 
# 36. Multiple inheritance 
# 37. super() 
# 38. Polymorphism 
# 39. Duck typing 
# 40. Static methods 
# 41. Class methods 
# 42. Magic methods 
# 43. @property 
# 44. Decorators 
# 45. Multithreading 
# 46. Request API data 

