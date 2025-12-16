# Python-Password-Strength-Checker
# Function to check basic password strength based on length
def check_password_strength(password):
    if len(password) >= 8:
        return "Strong (based on length)"
    else:
        return "Weak (too short, must be 8+ characters)"

# Test the function
my_pass = "p@ss123"
result = check_password_strength(my_pass)

print(f"Password: {my_pass}")
print(f"Strength: {result}")
