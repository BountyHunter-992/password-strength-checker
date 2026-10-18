password = input("Enter your password: ")
length_ok = len(password) >= 8
upper_ok = any(ch.isupper() for ch in password)
lower_ok = any(ch.islower() for ch in password)
digit_ok = any(ch.isdigit() for ch in password)
special_ok = any(not ch.isalnum() for ch in password)

score = sum([length_ok, upper_ok, lower_ok, digit_ok, special_ok])

if score == 5:
    print("Strong password! ✅")
elif score >= 3:
    print("Moderate password. Add more variety. ⚠️")
else:
    print("Weak password. Use at least 8 characters with uppercase, lowercase, numbers, and symbols. ❌")

print(f"Password score: {score}/5")
print(f"Length: {len(password)} characters")
