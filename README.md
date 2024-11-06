
# libft

## Project Overview
`libft` is a custom C library developed as part of the 42 School curriculum. This project involves reimplementing standard C library functions, providing a foundational toolkit for future projects, and reinforcing low-level programming skills. By creating `libft`, we gain a deeper understanding of memory management, pointer manipulation, string operations, and efficient algorithm design.

## Features
This library includes:
- **Libc Functions**: Reimplementations of essential standard C library functions.
- **Additional Utility Functions**: New functions that extend the standard library, helping with everyday tasks like string manipulation, memory management, and data structure handling.
- **Bonus Part**: Implementations of basic data structures and algorithms, like linked lists.

## Functions
### Part 1 - Libc Functions
These are reimplemented standard library functions from `<string.h>` and `<ctype.h>`:
- **Character Checks and Conversions**:
  - `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint` - Check for character types.
  - `ft_toupper`, `ft_tolower` - Convert characters to uppercase or lowercase.
- **String Manipulation**:
  - `ft_strlen` - Returns the length of a string.
  - `ft_strchr`, `ft_strrchr` - Locates a character in a string.
  - `ft_strncmp` - Compares specified characters in two strings.
  - `ft_strnstr` - Finds the first occurrence of a substring within length-limited search.
- **Memory Manipulation**:
  - `ft_memset` - Fills a block of memory with a specific byte.
  - `ft_bzero` - Clears a block of memory.
  - `ft_memcpy`, `ft_memmove` - Copies memory from one location to another.
  - `ft_memchr` - Searches for a byte in memory.
  - `ft_memcmp` - Compares two blocks of memory.
- **Standard Library-Compatible Functions**:
  - `ft_atoi` - Converts a string to an integer.
  - `ft_strlcpy`, `ft_strlcat` - Safer versions of string copy/concat.
- **Memory Allocation**:
  - `ft_calloc` - Allocates and zeroes out memory.
  - `ft_strdup` - Duplicates a string.

### Part 2 - Additional Utility Functions
Functions added to handle tasks and extend libc functionalities:
- **String Manipulation**:
  - `ft_substr` - Extracts a substring from a string.
  - `ft_strjoin` - Concatenates two strings.
  - `ft_strtrim` - Trims characters from start and end of a string.
  - `ft_split` - Splits a string by a delimiter into an array of strings.
  - `ft_itoa` - Converts an integer to a string.
  - `ft_strmapi` - Applies a function to each character in a string.
  - `ft_striteri` - Applies a function in-place on each character of a string.
- **File Descriptor Functions**:
  - `ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd` - Write characters, strings, and numbers to specified file descriptors.

### Part 3 - Linked List Functions (Bonus)
If enabled, `libft` also includes functions for working with singly linked lists using the `t_list` structure:
- `ft_lstnew` - Creates a new node.
- `ft_lstadd_front` - Adds a node at the beginning of the list.
- `ft_lstsize` - Counts the nodes in a list.
- `ft_lstlast` - Returns the last node of a list.
- `ft_lstadd_back` - Adds a node to the end of the list.
- `ft_lstdelone` - Frees the memory of a single node.
- `ft_lstclear` - Deletes and frees the entire list.
- `ft_lstiter` - Applies a function to each list node.
- `ft_lstmap` - Applies a function to each node to create a new list.

## Installation
To compile `libft`:
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/libft.git
   ```
2. Navigate to the project directory:
   ```bash
   cd libft
   ```
3. Run `make` to compile the library:
   ```bash
   make
   ```
4. After compiling, include `libft.a` in your project and `#include "libft.h"` in your C files to use the library.

## Usage
Here’s an example of how to use `libft` in a project:

```c
#include "libft.h"
#include <stdio.h>

int main() {
    char *str = ft_strdup("Hello, world!");
    printf("Duplicated string: %s\n", str);
    free(str); // Freeing memory after use
    return 0;
}
```

Compile with:
```bash
cc main.c -L. -lft -o main
```

## Learning Objectives
This project focuses on:
- **C Programming Mastery**: Reinforces essential skills like memory management, pointer manipulation, and string handling.
- **Data Structures and Algorithms**: Introduces linked lists and related algorithms.
- **Custom Library Building**: Provides hands-on experience in building, organizing, and linking a reusable library.

## Acknowledgments
Special thanks to 42 School for the rigorous curriculum, which includes building this library from scratch to solidify low-level programming concepts in C.
