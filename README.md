import random

print("🎮 Chào mừng đến với game đoán số!")
print("Tôi đã chọn một số từ 1 đến 100.")

# Tạo số random
secret_number = random.randint(1, 100)

attempts = 0

while True:
    try:
        guess = int(input("Nhập số bạn đoán: "))
        attempts += 1

        if guess < secret_number:
            print("🔻 Số bạn đoán nhỏ hơn!")
        elif guess > secret_number:
            print("🔺 Số bạn đoán lớn hơn!")
        else:
            print(f"🎉 Chính xác! Bạn đã đoán đúng sau {attempts} lần.")
            break
    except:
