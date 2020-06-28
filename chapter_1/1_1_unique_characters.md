# Question
Implement an algorithm to determine if a string has all unique characters. What if you cannot use additional data structures?

# Answer

## With additional data structures

```python
def string_has_unique_characters(string):
    unique_characters = {}
    for char in string:
        if unique_characters.get(char):
            return False
        else:
          unique_characters.update({f"{char}": True})
    return True

# alternatively...

def string_has_unique_chars(string):
    return len(string) == len(set(string))
```

## Without additional data structures

The most obvious way without additional data structures is to sort the string
and then use two pointers to compare each character with the previous one to
see if they match.

```python
def string_has_unique_characters(string):
    sorted_string = sorted(string)

    for index in range(1, len(sorted_string)):
        if sorted_string[index] == sorted_string[index -1]:
            return False
    return True
```
