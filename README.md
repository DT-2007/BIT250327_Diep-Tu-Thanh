# BIT250327_Diep-Tu-Thanh
#%%
#Bài 1
n = int(input("Nhập một số từ 1 đến 9: "))

#Điều Kiện
if 1 <= n <= 9:
    print(f"Bảng cửu chương của {n}:")
    for i in range(1, 10):
        print(f"{n} x {i} = {n * i}")
else:
    print("Số không hợp lệ! Vui lòng nhập số từ 1 đến 9.")
#%%
#Bài 2
n = int(input("Nhập một số dương: "))

if n <= 1:
    print(f"{n} không phải là số nguyên tố.")
else:
    is_prime = True
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            is_prime = False
            break

    if is_prime:
        print(f"{n} là số nguyên tố.")
    else:
        print(f"{n} không phải là số nguyên tố.")
#%%
#Bài 3
n = int(input("Nhập số n: "))

a, b = 0, 1
print("Dãy Fibonacci:")

for _ in range(n):
    print(a, end=" ")
    a, b = b, a + b
#%%
#Bài 4
n = input("Nhập một số: ")
tong = 0

for ch in n:
    tong += int(ch)

print("Tổng các chữ số là:", tong)
#%%
#Bài 5
chuoi = input("Nhập chuỗi: ")
ky_tu = input("Nhập ký tự cần đếm: ")

dem = 0
for ch in chuoi:
    if ch == ky_tu:
        dem += 1

print(f"Ký tự '{ky_tu}' xuất hiện {dem} lần")
#%%
#Bài 6
def giai_thua(n):
    if n == 0 or n == 1:
        return 1
    return n * giai_thua(n - 1)

n = int(input("Nhập số n: "))
print("Giai thừa của", n, "là:", giai_thua(n))
#%%
#Bài 7
a = int(input("Nhập số a: "))
b = int(input("Nhập số b: "))

while b != 0:
    a, b = b, a % b

print("Ước số chung lớn nhất là:", a)
#%%
#Bài 8
n = input("Nhập số: ")
dao = n[::-1]

print("Số sau khi đảo:", dao)
#%%
#Bài 9
n = input("Nhập số nguyên dương 5 chữ số: ")

max_digit = n[0]
for ch in n:
    if ch > max_digit:
        max_digit = ch

print("Chữ số lớn nhất là:", max_digit)
#%%
#Bài 10
def tong(n):
    if n == 1:
        return 1
    return n + tong(n - 1)

n = int(input("Nhập số n: "))
print("Tổng từ 1 đến", n, "là:", tong(n))
#%%
#Bài 11
diem = float(input("Nhập điểm trung bình: "))

if diem >= 8:
    print("Xếp loại: Giỏi")
elif diem >= 6.5:
    print("Xếp loại: Khá")
elif diem >= 5:
    print("Xếp loại: Trung bình")
else:
    print("Xếp loại: Yếu")
#%%
#Bài 12
n = int(input("Nhập số n: "))
tong = 0

for i in range(1, n + 1, 2):
    tong += i

print("Tổng các số lẻ từ 1 đến", n, "là:", tong)
#%%
#Bài 13
mat_khau = ""

while mat_khau != "python123":
    mat_khau = input("Nhập mật khẩu: ")

print("Đăng nhập thành công!")
#%%
#Bài 14
n = int(input("Nhập số n: "))

if n <= 1:
    print(n, "không phải là số nguyên tố")
else:
    la_nguyen_to = True
    for i in range(2, n):
        if n % i == 0:
            la_nguyen_to = False
            break

    if la_nguyen_to:
        print(n, "là số nguyên tố")
    else:
        print(n, "không phải là số nguyên tố")
#%%
 #Bài 15
n = int(input("Nhập số nguyên dương: "))
tong = 0

while n > 0:
    tong += n % 10
    n //= 10

print("Tổng các chữ số là:", tong)
