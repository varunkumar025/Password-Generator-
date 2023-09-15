# Password-Generator-
Java Password Generator
This Java code defines a program called `GeneratePassword` that generates random passwords with certain constraints. Here's an explanation of the code:

1. **Import Statement**: The code imports the `SecureRandom` class from the `java.security` package. `SecureRandom` is used for generating cryptographically secure random numbers, which are suitable for password generation.

2. **Constants**:
   - `LOWERCASE_CHARS`, `UPPERCASE_CHARS`, `DIGITS`, `SPECIAL_CHARS`: These constants store strings containing characters from different character sets: lowercase letters, uppercase letters, digits, and special characters, respectively.
   - `ALL_CHARS`: This constant combines all the character sets to create a pool of characters from which the password will be generated.
   - `DEFAULT_LENGTH`: This constant represents the default length for generated passwords (set to 14 characters).

3. **`main` Method**:
   - The `main` method serves as the entry point of the program.
   - It calls the `generatePassword` method with a length of 14 (specified as an argument) and prints the generated password to the console.

4. **`generatePassword` Method**:
   - This method takes an integer `length` as a parameter, which represents the desired length of the generated password.
   - If the specified length is less than 4, it sets the length to the `DEFAULT_LENGTH` (which is 14).
   - An instance of `SecureRandom` is created to generate secure random numbers.
   - The method ensures that the generated password contains at least one uppercase letter, one digit, and one special symbol. It appends these characters to the `password` StringBuilder.
   - A loop generates the remaining characters by randomly selecting characters from `ALL_CHARS` and appending them to the `password`.
   - Finally, it shuffles the characters in the password using the `shuffleString` method to ensure randomness.

5. **`shuffleString` Method**:
   - This method shuffles the characters in a string to enhance the randomness of the password.
   - It takes an input string, converts it to an array of characters, and then performs a Fisher-Yates shuffle to rearrange the characters randomly.

When you run this program, it will print a random password of the specified length (or the default length if none is provided) to the console. The generated password will meet the constraints of containing at least one uppercase letter, one digit, and one special symbol in addition to the remaining characters.
