Logfind
---

Logfind is a simple version of grep. Search for a string and receive a list of files in the current
directory containing that string.

# Features
* Written with Python 2.7.6
* Specify what file types to search via Regular Expressions in ~/.logfind file (you create this!)
* Searches files in current directory for string specified at the command line
* Returns a list of files containing the search string
* Default search uses AND logic, use -o flag to use OR logic instead

# Installing
For now, follow these steps:

1. Download the source code
2. Run `$ python setup.py sdist`
3. Run `$ pip install dist/logfind-0.1.tar.gz`

And you're good to go!

# Usage
Search for a single word using default (AND) logic:

`$ logfind apple`

Search for a string of text using default (AND) logic:

`$ logfind "string to find"`

Search using OR logic:

`$ logfind apple -o`

Example ~/.logfind file:

```
[a-zA-Z0-9_-]+[.]txt
[a-xA-Z_-]+[.]log
```

# Uninstalling
Just run:

`pip uninstall logfind`

# Source
Source is available here: http://github.com/tylerm-/logfind

# To Do List
* Add RegEx parsing for command line args