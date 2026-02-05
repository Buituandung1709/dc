### NHIỆM VỤ 1:
```python
def Select(A,x):
    B = []
    for k in range(len(A)):
        if float(A[k]) >= x:
            B.append(A[k])
    return B
a=input('Nhập các số bất kì cách nhau bởi dấu cách: ')
A=a.split(' ')
b=float(input('Nhập số bất kì: '))
B=Select(A,b)
print('Các phần tử trong danh sách lớn hơn', b, 'là:', ' '.join(B))
```
### NHIỆM VỤ 2:
```python
def Tach_tu(Str, c):
    A = Str.split()
    for k in range(len(A)):
        if c == 0:
            A[k] = A[k].upper()
        if c == 1:
            A[k] = A[k].lower()
        if c == 2:
            A[k] = A[k].title()
    return A
a=input('Nhập kí tự bất kì: ')
b=int(input("""Chọn phương thức chuyển đổi kí tự:
[0]: Chuyển thành chữ in hoa
[1]: Chuyển thành chữ in thường
[2]: Chuyển thành in hoa kí tự đầu còn lại in thường
Nhập phương thức vào đây [0-2]: """))
B=Tach_tu(a, b)
print('Kí tự được chuyển đổi là: ', ' '.join(B))
```
### LUYỆN TẬP 2:
```python
def Tach_day(a):
    B=[]
    C=[]
    A=a.split(' ')
    for i in range(len(A)):
        if int(A[i]) % 2 == 0:
            B.append(A[i])
        else:
            C.append(A[i])
    return B, C
a=input('Nhập các số nguyên bất kì cách nhau bởi dấu cách: ')
B, C = Tach_day(a)
print('Danh sách các số chẵn là:', ' '.join(B))
print('Danh sách các số lẻ là:', ' '.join(C))
```
### VẬN DỤNG 1:
```python
def UCLN(m, n):
    while m != n:
        if m < n:
            n = n - m
        else:
            m = m - n
    return m
a=int(input('Nhập số nguyên thứ nhất bất kì: '))
b=int(input('Nhập số nguyên thứ hai bất kì: '))
ucln=UCLN(a, b)
bcnn=(a*b)/ucln
print('ƯCLN và BCNN của 2 số tương ứng là:', ucln, 'và', bcnn)
```
### VẬN DỤNG 2:
```python
def namnhuan(d, m, y):
    a='Ngày hợp lệ'
    if m in [1, 3, 5, 7, 8, 10, 12]:
        if d < 1 or d > 31:
            a='Ngày không hợp lệ'
    elif m == 2:
        if d < 1 or d > 29:
            a='Ngày không hợp lệ'
    elif m in [4, 6, 9, 11]:
        if d < 1 or d > 30:
            a='Ngày không hợp lệ'
    else:
        a='Tháng không hợp lệ'
    return a
def namkhongnhuan(d, m, y):
    a='Ngày hợp lệ'
    if m in [1, 3, 5, 7, 8, 10, 12]:
        if d < 1 or d > 31:
            a='Ngày không hợp lệ'
    elif m == 2:
        if d < 1 or d > 28:
            a='Ngày không hợp lệ'
    elif m in [4, 6, 9, 11]:
        if d < 1 or d > 30:
            a='Ngày không hợp lệ'
    else:
        a='Tháng không hợp lệ'
    return a
a=input('Nhập ngày, tháng, năm cách nhau bởi dấu cách: ')
A=a.split(' ')
day=int(A[0])
month=int(A[1])
year=int(A[2])
if (year % 4 == 0 and year % 100 != 0) or year % 400 == 0:
    kq=namnhuan(day, month, year)
    print(kq)
else:
    kq=namkhongnhuan(day, month, year)
    print(kq)
```
