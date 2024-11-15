# 42Cursus - Libft

This repository contains **Libft**, the first project of the **42Cursus**. It involves creating a custom C library that replicates many essential functions of the standard C library (`libc`), as well as additional functions for working with linked lists. This project serves as a foundation for all future C projects at **42**.

---

## Repository Structure

```plaintext
.
├── Makefile         # Build system to compile the library
├── libft.h          # Header file containing function prototypes
├── ft_*.c           # C source files implementing the library's functions
```

---

## Implemented Functions

### Part 1 - Standard Library Functions
| **Function**        | **Description**                                      |
|---------------------|-----------------------------------------------------|
| `ft_isalpha`        | Checks if a character is alphabetic.                |
| `ft_isdigit`        | Checks if a character is a digit.                   |
| `ft_isalnum`        | Checks if a character is alphanumeric.              |
| `ft_isascii`        | Checks if a character is an ASCII character.        |
| `ft_isprint`        | Checks if a character is printable.                 |
| `ft_strlen`         | Computes the length of a string.                    |
| `ft_memset`         | Fills memory with a constant byte.                  |
| `ft_bzero`          | Sets memory to zero.                                |
| `ft_memcpy`         | Copies memory from one location to another.         |
| `ft_memmove`        | Copies memory with overlap handling.                |
| `ft_strlcpy`        | Copies a string with size limitation.               |
| `ft_strlcat`        | Appends a string with size limitation.              |
| `ft_toupper`        | Converts a character to uppercase.                  |
| `ft_tolower`        | Converts a character to lowercase.                  |
| `ft_strchr`         | Locates a character in a string.                    |
| `ft_strrchr`        | Locates the last occurrence of a character in a string. |
| `ft_strncmp`        | Compares two strings up to a given length.          |
| `ft_memchr`         | Locates a byte in memory.                           |
| `ft_memcmp`         | Compares two memory areas.                          |
| `ft_strnstr`        | Locates a substring in a string.                    |
| `ft_atoi`           | Converts a string to an integer.                    |
| `ft_calloc`         | Allocates and zeroes memory.                        |
| `ft_strdup`         | Duplicates a string.                                |

---

### Part 2 - Additional Functions
| **Function**        | **Description**                                      |
|---------------------|-----------------------------------------------------|
| `ft_substr`         | Extracts a substring from a string.                 |
| `ft_strjoin`        | Joins two strings into one.                         |
| `ft_strtrim`        | Trims characters from the start and end of a string.|
| `ft_split`          | Splits a string into an array of strings.           |
| `ft_itoa`           | Converts an integer to a string.                    |
| `ft_strmapi`        | Applies a function to each character of a string.   |
| `ft_striteri`       | Iterates over a string with an index-aware function.|
| `ft_putchar_fd`     | Outputs a character to a file descriptor.           |
| `ft_putstr_fd`      | Outputs a string to a file descriptor.              |
| `ft_putendl_fd`     | Outputs a string with a newline to a file descriptor.|
| `ft_putnbr_fd`      | Outputs an integer to a file descriptor.            |

---

### Bonus - Linked List Functions
| **Function**        | **Description**                                      |
|---------------------|-----------------------------------------------------|
| `ft_lstnew`         | Creates a new linked list node.                     |
| `ft_lstadd_front`   | Adds a node to the beginning of a linked list.       |
| `ft_lstadd_back`    | Adds a node to the end of a linked list.            |
| `ft_lstdelone`      | Deletes a single node from a linked list.           |
| `ft_lstclear`       | Clears an entire linked list.                       |
| `ft_lstiter`        | Iterates through a linked list and applies a function.|
| `ft_lstmap`         | Creates a new list by applying a function to each node.|
| `ft_lstsize`        | Returns the size of a linked list.                  |
| `ft_lstlast`        | Returns the last node of a linked list.             |

---

## How to Compile and Use

1. **Compile the Library**  
   Use the provided `Makefile` to build the library:  
   ```bash
   make
   ```
   This will generate a `libft.a` file, which is the compiled static library.

2. **Link the Library**  
   To use the library in your project, include `libft.h` and link `libft.a`:  
   ```c
   #include "libft.h"

   int main(void) {
       char *str = ft_strdup("Hello, Libft!");
       ft_putstr_fd(str, 1);
       free(str);
       return (0);
   }
   ```
   Compile with:  
   ```bash
   gcc -Wall -Wextra -Werror main.c -L. -lft
   ```

3. **Clean Up**  
   Use `make clean` to remove object files or `make fclean` to remove the library.