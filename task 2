from PIL import Image
import numpy as np

def encrypt_image(image_path):
    try:
        # Open the image file
        image = Image.open(image_path)
        
        # Convert the image to a NumPy array (this will contain pixel values)
        img_array = np.array(image)
        
        # Define a key for encryption (can be any integer, e.g., 5)
        key = 5
        
        # Encrypt the image by modifying the pixel values
        encrypted_pixels = img_array + key
        
        # Clip values to ensure they stay within the valid range of 0-255
        encrypted_pixels = np.clip(encrypted_pixels, 0, 255)
        
        # Convert the NumPy array back to an image
        encrypted_image = Image.fromarray(encrypted_pixels.astype(np.uint8))  # Ensure dtype is uint8
        
        # Save the encrypted image
        encrypted_image.save("encrypted_image.jpg")
        print("Image encrypted successfully!")
    
    except Exception as e:
        print(f"Error: {e}")

def decrypt_image(image_path):
    try:
        # Open the encrypted image file
        image = Image.open(image_path)
        
        # Convert the image to a NumPy array (this will contain pixel values)
        img_array = np.array(image)
        
        # Define the key for decryption (same as encryption key)
        key = 5
        
        # Decrypt the image by reversing the encryption process
        decrypted_pixels = img_array - key
        
        # Clip values to ensure they stay within the valid range of 0-255
        decrypted_pixels = np.clip(decrypted_pixels, 0, 255)
        
        # Convert the NumPy array back to an image
        decrypted_image = Image.fromarray(decrypted_pixels.astype(np.uint8))  # Ensure dtype is uint8
        
        # Save the decrypted image
        decrypted_image.save("decrypted_image.jpg")
        print("Image decrypted successfully!")
    
    except Exception as e:
        print(f"Error: {e}")

def main():
    action = input("Choose an action (encrypt/decrypt): ").strip().lower()
    image_path = input("Enter the image file path: ").strip()  # Input the correct image path
    
    if action == "encrypt":
        encrypt_image(image_path)
    elif action == "decrypt":
        decrypt_image(image_path)
    else:
        print("Invalid action!")

if __name__ == "__main__":
    main()
