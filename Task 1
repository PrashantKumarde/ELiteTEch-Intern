def caesar_cipher(text, shift, mode='encrypt'):
    result = ""
    for char in text:
        if char.isalpha():  # Check if the character is a letter
            start = 65 if char.isupper() else 97  # Determine if uppercase or lowercase
            shifted_char = chr((ord(char) - start + (shift if mode == 'encrypt' else -shift)) % 26 + start)
            result += shifted_char
        else:
            result += char  # Non-alphabetical characters remain unchanged
    return result

def main():
    print("Caesar Cipher Encryption and Decryption")
    
    message = input("Enter your message: ")
    shift = int(input("Enter the shift value (integer): "))
    mode = input("Choose mode (encrypt/decrypt): ").strip().lower()

    if mode not in ['encrypt', 'decrypt']:
        print("Invalid mode. Please choose 'encrypt' or 'decrypt'.")
        return
    
    result = caesar_cipher(message, shift, mode)
    print(f"Resulting message: {result}")

if __name__ == "__main__":
    main()
