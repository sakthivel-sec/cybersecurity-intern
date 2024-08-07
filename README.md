# cybersecurity-intern
This project is Python project
This script defines two main functions: encrypt and decrypt. The encrypt function shifts each letter in the input text by a specified amount, wrapping around it if necessary. The decrypt function simply calls the encrypt function with a negative shift value to reverse the process.
The main function provides a simple command-line interface for the user to choose between encryption and decryption, enter a message, and specify a shift value.

STEPS:
Open Command Prompt:
Press Win + R, type cmd, and press Enter.
Check the Python version:
Type the following command and press Enter:
python --version
Alternatively, you can use:
python -V
Example:
C:\Users\YourUsername> python --version
Python 3.8.5

OUTPUT:
C:\Users\********\Desktop>python encrypt.py
Do you want to (E)ncrypt or (D)ecrypt?: e
Enter your message: cyber security
Enter the shift value: 10
Encrypted message: milob comebsdi

C:\Users\*********\Desktop>python encrypt.py
Do you want to (E)ncrypt or (D)ecrypt?: d
Enter your message: milob comebsdi
Enter the shift value: 10
Decrypted message: cyber security
