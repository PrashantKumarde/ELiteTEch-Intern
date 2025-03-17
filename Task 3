import re

def check_password_strength(password):
    # Criteria for strong password
    length_criteria = len(password) >= 8
    uppercase_criteria = bool(re.search(r'[A-Z]', password))
    lowercase_criteria = bool(re.search(r'[a-z]', password))
    number_criteria = bool(re.search(r'[0-9]', password))
    special_char_criteria = bool(re.search(r'[^A-Za-z0-9]', password))

    # Feedback messages
    feedback = []
    
    if not length_criteria:
        feedback.append("Password should be at least 8 characters long.")
    if not uppercase_criteria:
        feedback.append("Password should contain at least one uppercase letter.")
    if not lowercase_criteria:
        feedback.append("Password should contain at least one lowercase letter.")
    if not number_criteria:
        feedback.append("Password should contain at least one number.")
    if not special_char_criteria:
        feedback.append("Password should contain at least one special character (e.g., !@#$%^&*()).")

    # Determine password strength
    if length_criteria and uppercase_criteria and lowercase_criteria and number_criteria and special_char_criteria:
        strength = "Strong"
    elif length_criteria and (uppercase_criteria or lowercase_criteria) and number_criteria:
        strength = "Medium"
    else:
        strength = "Weak"
    
    # Output the feedback
    return strength, feedback

def main():
    print("Password Strength Checker")
    
    password = input("Enter a password to check its strength: ")
    
    strength, feedback = check_password_strength(password)
    
    print(f"\nPassword Strength: {strength}")
    if feedback:
        print("Feedback on password strength:")
        for item in feedback:
            print(f"- {item}")
    else:
        print("Password meets all the criteria.")

if __name__ == "__main__":
    main()
