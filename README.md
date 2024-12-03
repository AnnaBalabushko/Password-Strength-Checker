PasswordStrengthChecker
# Password Strength Checker - Python Program

## Overview

This Python program checks the strength of a user's password based on certain criteria and provides feedback to help improve it. The program checks if the password meets the following requirements:

1. Minimum length of 8 characters.
2. Maximum length of 20 characters.
3. At least one uppercase letter.
4. At least one lowercase letter.
5. At least one digit.
6. At least one special character (e.g., !, @, #, $, %, etc.).

If the password meets all the requirements, it is considered strong. Otherwise, the program will give detailed feedback on what needs to be improved.

## Features

- **Checks password strength**: Evaluates the password against multiple criteria (length, character types).
- **Feedback mechanism**: Provides clear feedback for users to strengthen their passwords.
- **Customizable criteria**: The password strength criteria (such as minimum length, required characters) are set in the code and can be modified easily.

## Requirements

- **Python 3.x**: This program is written in Python 3.x, so make sure you have Python installed.
- **No external libraries required**: The program only requires Python’s built-in `re` library for regular expressions, which is included by default in Python 3.x installations.

## How to Use

1. **Run the Program**:
   - Open a terminal or command prompt.
   - Navigate to the directory where the `password_strength_checker.py` file is located.
   - Run the script using the following command:
     ```bash
     python password_strength_checker.py
     ```
   
2. **Enter Password**:
   - When prompted, enter the password that you want to check for strength.

3. **View Feedback**:
   - The program will evaluate the password and print out feedback on whether the password is strong or suggestions for improvement.

### Example Usage

1. **Strong Password**:
   ```bash
   Welcome to the Password Strength Checker!
   Please enter your password: SuperStrong123!
   
   Password Strength Report:
   Password is strong!
   ```

2. **Weak Password**:
   ```bash
   Welcome to the Password Strength Checker!
   Please enter your password: weakpass
   
   Password Strength Report:
   Password should be at least 8 characters long.
   Password should contain at least 1 uppercase letter(s).
   Password should contain at least 1 digit(s).
   Password should contain at least 1 special character(s) (e.g., !@#$%).
   ```

## Code Explanation

### `check_password_strength(password)` Function

This function takes the password as input and evaluates it against several criteria using regular expressions and simple checks:

1. **Length Check**: Ensures the password is between 8 and 20 characters.
2. **Uppercase Check**: Ensures the password contains at least one uppercase letter.
3. **Lowercase Check**: Ensures the password contains at least one lowercase letter.
4. **Digit Check**: Ensures the password contains at least one digit.
5. **Special Character Check**: Ensures the password contains at least one special character (e.g., `!@#$%`).

It returns a string of feedback messages, or a success message if the password is strong.

### `main()` Function

This function is the entry point of the program:
- It prompts the user to enter a password.
- It calls the `check_password_strength` function to evaluate the password.
- It prints the password strength report to the console.

### Regular Expressions Used

- `[A-Z]`: Matches any uppercase letter.
- `[a-z]`: Matches any lowercase letter.
- `[0-9]`: Matches any digit.
- `[\W_]`: Matches any non-word character (special characters like `!@#$%`).

### Error Handling

- The program does not explicitly handle input errors since the `input()` function takes user input as a string. However, if users enter a password that doesn't meet the criteria, the program will provide appropriate feedback.

## Customization
The password strength criteria can be easily modified by changing the values of the following variables inside the `check_password_strength` function:

- `min_length`: Minimum length of the password.
- `max_length`: Maximum length of the password.
- `min_uppercase`: Minimum number of uppercase letters required.
- `min_lowercase`: Minimum number of lowercase letters required.
- `min_digits`: Minimum number of digits required.
- `min_special`: Minimum number of special characters required.

Example:
```python
min_length = 10
min_uppercase = 2
```

This would change the criteria to:
- Minimum length of 10 characters.
- Minimum of 2 uppercase letters.
