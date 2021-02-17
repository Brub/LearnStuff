# Code Styling

The Python language has some programming guidelines outlined in PEP8  
[https://www.python.org/dev/peps/pep-0008/](https://www.python.org/dev/peps/pep-0008/)

## Code Lay-out  
### Indentation  
Use 4 spaces per indentation level.

### Maximum Line Length  
Limit all lines to a maximum of 79 characters.  

For flowing long blocks of text with fewer structural restrictions (docstrings or comments), the line length should be limited to 72 characters.  

If the exeed 79 characters of code you need to use \

### One Statement per Line
Use one statement per line

### Blank Lines
Top-level function and classes are separated by two blank lines.  
Method definitions inside classes should be separated by one blank line.

## Class names
By convention, class names use CamelCase.

## Constants
Constants are usually defined on a module level and written in all capital letters with underscores separating words. Examples include MAX_OVERFLOW

## Source File Encoding
Python 3, UTF-8 is the default source encoding.  
Python 2, ASCII is the default source encoding.

## Imports
You should always import libraries at the start of your script.  
If you do many imports, you should make sure to state each import on a single line.

You should take into account that there is an order that you need to respect when you're importing libraries.  
In general, you can follow this order:

1. Standard library imports.
2. Related third-party imports.
3. Local application/library specific imports.
