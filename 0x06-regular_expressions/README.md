### Regular Expressions in Python:

1. **What are Regular Expressions?**
   - Regular expressions (regex or regexp) are powerful tools for pattern matching and text manipulation.
   - They provide a concise and flexible means to search, match, and manipulate strings.

2. **Using the `re` Module:**
   - Python's `re` module provides support for regular expressions.
   - Import it using: `import re`.

3. **Basic Patterns:**
   - A regular expression pattern is a sequence of characters that defines a search pattern.
   - Examples:
     - `abc`: Matches the literal characters 'abc'.
     - ` \d`: Matches any digit.
     - `.`: Matches any character except a newline.

4. **Common Functions:**
   - `re.search(pattern, string)`: Searches for the pattern in the string.
   - `re.match(pattern, string)`: Checks if the pattern occurs at the beginning of the string.
   - `re.findall(pattern, string)`: Returns a list of all occurrences of the pattern in the string.

5. **Special Characters:**
   - `.` (dot): Matches any character except a newline.
   - `^`: Anchors the regex at the start of the string.
   - `$`: Anchors the regex at the end of the string.
   - `*`: Matches 0 or more occurrences of the preceding character.
   - `+`: Matches 1 or more occurrences of the preceding character.
   - `?`: Matches 0 or 1 occurrence of the preceding character.
   - `[]`: Matches any single character within the brackets.
   - `|`: Acts like an OR operator.

6. **Quantifiers:**
   - `{n}`: Matches exactly n occurrences.
   - `{n,}`: Matches n or more occurrences.
   - `{n, m}`: Matches between n and m occurrences.

7. **Character Classes:**
   - `\d`: Any digit (0-9).
   - `\w`: Any alphanumeric character (word character).
   - `\s`: Any whitespace character.
   - `\D`, `\W`, `\S`: Negations of `\d`, `\w`, `\s` respectively.

8. **Example: Matching Email Addresses:**
   ```python
   import re

   pattern = r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b'
   email = "user@example.com"

   if re.match(pattern, email):
       print("Valid email address!")
   else:
       print("Invalid email address.")
   ```

9. **Modifiers:**
   - `re.IGNORECASE` or `re.I`: Ignores case when matching.

10. **Escape Characters:**
    - To match special characters like `.` or `*`, use the backslash `\` as an escape character.

11. **Grouping and Capturing:**
    - Use parentheses `()` to create groups. Capturing groups allow extracting matched portions.

12. **Replace and Substitution:**
    - `re.sub(pattern, replacement, string)`: Replace occurrences of the pattern with the specified replacement
