# CS50P
# Welcome To My journey Through Harvard's CS50 Introduction to Programming with Python

## Lecture 0 what i have learned :

```
- Core Python fundamentals: variables, input(), print(), f-strings
- Functions: def, parameters, arguments, return, side effects, and scope
- Type conversion: int(), float()
- String methods: .strip(), .capitalize(), .title(), .split()
- Operators: % (modulo), round()
- String formatting: format specifiers (.2f, , for thousands separators)
- Escape characters (\n, \t, \", etc.)
- Command line basics and Python's interactive mode
- Debugging fundamentals — reading tracebacks, fixing syntax and logic errors
```

## Lecture 1 what I have learned :

```
- Conditionals: if, elif, else
- Boolean expressions and boolean values (True, False)
- Logical operators: and, or
- return True / return False from a function
- String method: .replace()
- match, case, case _ (pattern matching)
- Using | inside case to match multiple values
```

## Lecture 2 what I have learned :

```
- for loops: looping through each item in a list, string, or range
- while loops, while True, and using break/continue to control them
- range() to generate a sequence of numbers to loop through
- Lists: ordered collections of multiple values
- Dictionaries: key-value pairs, accessed by key (e.g. student["Name"])
- String methods: .isalpha(), .isdigit(), .isalnum() for checking character types
- enumerate() to loop through a string/list while getting both index and value
- String slicing (n[i:]) to grab part of a string from an index to the end
- not keyword to flip a boolean condition
- Structuring a program into multiple small helper functions, each checking one rule
```

## Lecture 3 what I have learned :

```
- try / except for handling errors without crashing the program
- Common exceptions: ValueError, ZeroDivisionError
- raise to manually trigger an exception
- Combining multiple exception types: except ValueError or ZeroDivisionError
- pass as a placeholder that does nothing (vs. continue, which skips the rest of a loop iteration)
- Structuring input validation with if/elif chains, and why condition order matters
- Combining related conditions with or inside a single elif instead of repeating branches
- round() to round a number to the nearest integer (or to n decimal places)
- Splitting user input and converting each piece separately with int()
```

## Lecture 4 what I have learned :

```
- Modules and import, reusing pre-written code instead of rewriting it
- Built-in modules: random (choice, randint, shuffle), statistics (mean, median), sys
- sys.argv for command line arguments, sys.exit() to stop the program immediately
- Slices (n[start:end]), including negative numbers on either side to count from the end
- Packages vs. modules, a package bundles multiple modules together
- pip install to fetch packages from PyPI, then import to use them
- APIs, requesting and receiving data from an external service
- requests.get(url) and .json() to fetch and parse API data into a dict
- from module import function, importing just one specific function instead of the whole module
- __name__ and __main__, code outside a function runs immediately on import unless guarded
```
## Lecture 5 what I have learned :

```
- Unit testing, writing separate code that automatically checks whether functions behave correctly, instead of testing by hand
- assert, checks that an expression is true; raises AssertionError if it's false
- AssertionError, a built-in exception automatically raised when an assert fails
- pytest, a library that finds functions starting with test_, runs their asserts, and reports pass/fail with details
- with, runs setup code before a block and cleanup code after it automatically, even if an error happens inside (not just for files)
- Saving results before a with block ends, since the resource itself (like a file) becomes unusable right after closing
- pytest.raises(ExceptionType), used inside a with block to confirm a specific error is expected to happen; fails if it doesn't
- Packages need an __init__.py to be recognized as a package; this can accidentally break simple imports if added where it shouldn't be
- .append(item), list method that adds one item to the end of a list, modifying it in place
- .join(list), string method that combines a list of strings into one string using a separator
- Global variables outside a function don't reset between calls, causing state to leak across multiple calls (found this bug in twttr.py)
- Good tests need to cover edge cases (capitals, numbers, punctuation), not just the simplest case, to actually catch bugs
```
## Lecture 6 what I have learned:
```
- open(filename, mode), a built-in function that opens a file and returns a file object; needs to be stored in a variable to be used
- Modes: "r" (read, default, errors if file doesn't exist), "w" (write, overwrites the whole file), "a" (append, adds to the end)
- with, runs setup code before a block and cleanup code after it automatically, even if an error happens inside — the error still stops the program, but the file still gets closed on the way out
- .write(text), .read(), .readline(), .readlines(), .close() — the main file object methods
- .strip(), .lstrip(), .rstrip() — remove whitespace from both/left/right sides of a string
- "".join(list), combines a list of strings into one string using the string it's called on as the separator
- csv.reader(file), parses a file line by line into lists of values, splitting on commas automatically
- csv.DictReader(file), same idea but returns each row as a dictionary, using the header row as keys
- csv.writer(file) and .writerow(list), write a single row of values to a file as CSV
- csv.DictWriter(file, fieldnames=[...]), writes rows from dictionaries instead of lists; fieldnames sets both column order and expected keys
- newline="" in open(), prevents Windows from double-adding line breaks when writing CSVs with the csv module
- key=, an optional parameter for sorted(), max(), and min() that takes a function; that function is called separately on each item (not the whole list) to decide what to compare by
- lambda, a way to write a small unnamed function in one line: lambda variables: return_value — useful for short throwaway functions like a sorted() key, but limited to a single expression (no loops, no multiple statements)
- PIL / Pillow, a third-party image library; installed with pip install pillow but imported as PIL
- Image.open(filename), opens an image file and returns an Image object (needs to be stored in a variable)
- .save(filename, ...), writes an Image object to a file; save_all=True, append_images=, duration=, and loop= are used together to build an animated GIF from multiple images
```
## Lecture 7 what I have learned:
```
- re, a built-in module for pattern matching in strings; imported with import re
- raw strings, r"...", tell Python to treat backslashes literally instead of as escape sequences; needed for regex patterns
- escape sequences, backslash + character combos in normal strings that get special meaning, like \n (newline), \t (tab), \\ (literal backslash)
- re.search(pattern, string, flags=0), scans the whole string looking for a match anywhere; returns a match object if found, None if not
- re.match(pattern, string, flags=0), only checks for a match starting at position 0 of the string; doesn't require the match to reach the end
- re.fullmatch(pattern, string, flags=0), requires the entire string to match the pattern, start to finish, like having ^ and $ automatically wrapped around it
- re.sub(pattern, replacement, string, count=0, flags=0), replaces every match of a pattern in a string with a replacement, returns the new string (original is unchanged)
- re.split(pattern, string, maxsplit=0, flags=0), splits a string into a list wherever the pattern matches, instead of a fixed separator
- re.findall(pattern, string, flags=0), returns a list of every match found in the string, instead of stopping at the first one
- ., matches any single character except a newline
- *, zero or more times
- +, one or more times
- ?, zero or one time
- {m}, exactly m times
- {m,n}, between m and n times
- {m,}, m or more times
- {,n}, up to n times
- [...], a character class, matches one character that's in the set listed
- [^...], a negated character class, matches one character that's NOT in the set
- [a-z], a range inside a character class
- \d / \D, a digit / not a digit
- \w / \W, a word character (letter, digit, underscore) / not a word character
- \s / \S, a whitespace character / not a whitespace character
- ^, anchors to the start of the string (different meaning than ^ inside [...], where it negates instead)
- $, anchors to the end of the string
- (...), a capturing group; groups characters together and saves the matched text for later use
- (?:...), a non-capturing group; groups characters together but doesn't save the matched text
- |, means "or" between two alternatives, only inside a regex pattern (different from | in normal Python, which is the bitwise operator)
- \, escapes a special character so it's treated literally, like \. for an actual period
- flags, optional settings passed to regex functions via flags=, like re.IGNORECASE, re.MULTILINE, re.DOTALL; combine multiple with |
- .group() / .group(0), returns the whole match from a match object
- .group(1), .group(2), etc., returns one specific captured group
- .groups(), returns all captured groups at once, as a tuple
- the walrus operator, :=, assigns a value to a variable and uses it in the same expression at once, e.g. if matches := re.search(pattern, string):
- .removeprefix(prefix), removes a given prefix from the start of a string if present, returns the string unchanged if it isn't there
- .removesuffix(suffix), same idea but removes from the end of the string instead
