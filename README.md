# Code-Writing
import random
import string

def generate_password(length=12, use_special_chars=True):
    """Generate a random password with letters, digits, and optional special characters."""
    characters = string.ascii_letters + string.digits
    if use_special_chars:
        characters += string.punctuation

    password = ''.join(random.choice(characters) for _ in range(length))
    return password

# Example usage
if __name__ == "__main__":
    length = int(input("Enter desired password length: "))
    special = input("Include special characters? (y/n): ").strip().lower() == 'y'
    print("Generated password:", generate_password(length, special))
