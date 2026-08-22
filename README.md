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
