from PIL import Image
import numpy as np

def encrypt_image(image_path, key):
    """
    Encrypts an image by applying a simple mathematical operation on each pixel.

    :param image_path: The path to the input image file.
    :param key: An integer key used for encryption.
    :return: An encrypted image as a NumPy array.
    """
    # Open the image
    img = Image.open(image_path)
    img_array = np.array(img)

    # Encrypt the image by applying the key to each pixel value
    encrypted_array = (img_array + key) % 256

    return encrypted_array


def decrypt_image(encrypted_array, key):
    """
    Decrypts an image by reversing the encryption operation.

    :param encrypted_array: The encrypted image as a NumPy array.
    :param key: An integer key used for decryption (should be the same as for encryption).
    :return: A decrypted image as a NumPy array.
    """
    # Decrypt the image by reversing the encryption operation
    decrypted_array = (encrypted_array - key) % 256

    return decrypted_array


def save_image(image_array, output_path):
    """
    Saves a NumPy array as an image file.

    :param image_array: The image data as a NumPy array.
    :param output_path: The path where the image will be saved.
    """
    img = Image.fromarray(image_array.astype('uint8'))
    img.save(output_path)


def main():
    """
    Main function to handle image encryption and decryption based on user input.
    """
    print("Image Encryption Tool")

    # Get the operation mode from the user
    mode = input("Choose mode ('encrypt' or 'decrypt'): ").lower()
    if mode not in ['encrypt', 'decrypt']:
        print("Invalid mode! Please choose 'encrypt' or 'decrypt'.")
        return

    # Get the image path and key from the user
    image_path = input("Enter the path to the image file: ")
    try:
        key = int(input("Enter an integer key for encryption/decryption: "))
    except ValueError:
        print("Invalid key! Please enter an integer.")
        return

    # Perform encryption or decryption
    if mode == 'encrypt':
        encrypted_image = encrypt_image(image_path, key)
        output_path = "encrypted_image.png"
        save_image(encrypted_image, output_path)
        print(f"Image encrypted and saved as {output_path}")
    elif mode == 'decrypt':
        encrypted_img = Image.open(image_path)
        encrypted_array = np.array(encrypted_img)
        decrypted_image = decrypt_image(encrypted_array, key)
        output_path = "decrypted_image.png"
        save_image(decrypted_image, output_path)
        print(f"Image decrypted and saved as {output_path}")


if __name__ == "__main__":
    main()
