# UTF-8 Validation

This project contains a solution to a common interview coding challenge where the goal is to validate UTF-8 encoding in a data set.

## Task Overview

The primary task of this project is to create a function that checks if a given data set represents valid UTF-8 encoding. UTF-8 encoding can use between 1 and 4 bytes to represent a character, and each byte has specific rules based on its binary structure.

### Task Description

- **File**: `0-stats.py`
- **Function**: `validUTF8(data)`

### Requirements

- **Input**: A list of integers (`data`), where each integer represents 1 byte (8 bits) of data.
- **Output**: The function should return `True` if the data validates UTF-8 encoding, and `False` otherwise.

### UTF-8 Encoding Rules

1. A character in UTF-8 can be 1 to 4 bytes long.
2. For 1-byte characters, the byte starts with `0`.
3. For 2-byte characters, the first byte starts with `110`, and the second byte starts with `10`.
4. For 3-byte characters, the first byte starts with `1110`, and the next two bytes start with `10`.
5. For 4-byte characters, the first byte starts with `11110`, and the next three bytes start with `10`.

### Example

Here's an example of the function call:
```python
data = [197, 130, 1]  # Corresponds to a valid UTF-8 encoded sequence
print(validUTF8(data))  # Output: True
