def check_password_strength(password):
    """
    Evaluates password strength based on length, 
    presence of digits, and uppercase letters.
    """
    length_check = len(password) >= 8
    digit_check = any(char.isdigit() for char in password)
    upper_check = any(char.isupper() for char in password)

    if length_check and digit_check and upper_check:
        return "Strong ✅"
    elif length_check and (digit_check or upper_check):
        return "Moderate ⚠️ (Add more variety)"
    else:
        return "Weak ❌ (Must be 8+ chars, include numbers and uppercase)"

# Test with a new password
test_pass = "SecurePass2025"
print(f"Testing Password: {test_pass}")
print(f"Final Evaluation: {check_password_strength(test_pass)}")
