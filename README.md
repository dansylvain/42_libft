# Libft Project Documentation
A custom C library project designed to provide a set of essential functions for various programming tasks

## Introduction
The "libft" project is a library of custom C functions created to supplement the standard C library. It provides a wide range of utility functions for common programming tasks, such as string manipulation, memory allocation, and list handling. The name "libft" stands for "Library Functions" and serves as a foundational toolkit for C programming projects.

The "libft" library is designed to be modular and extensible, allowing users to easily incorporate the provided functions into their own projects. Each function in the library is carefully implemented to adhere to standard conventions and best practices, ensuring robustness, efficiency, and portability across different platforms.

The primary goal of the "libft" project is to enable C programmers to streamline their development process by offering a comprehensive set of reusable functions. By using "libft," developers can reduce the amount of time spent on repetitive coding tasks and focus on solving higher-level problems in their projects.

## Execution
### Cloning the Repository

To use the "libft" library in your project, clone the repository containing the library files from GitHub:

```bash
git clone <https://github.com/dansylvain/42_libft>
```
### Compiling the Library
Navigate to the project directory and compile the library using the provided Makefile. Here's how:
```bash
cd libft
make
```
This will compile the library and create a static library file named libft.a in the project directory.
## Dependencies

My implementation of the "libft" project includes all necessary dependencies within the source code, requiring no additional installations.

## Adding "libft" as a Dependency

To add "libft" as a dependency in your project, follow these steps:

* Copy the "libft" directory into your project directory, or specify its location in your project's Makefile.
* Modify your project's Makefile to include rules for compiling "libft" along with your project. Here's an example of how to do it:

```make
LIBFT_DIR = path/to/libft

$(NAME): $(OBJ) $(LIBFT_DIR)/libft.a
    gcc -o $(NAME) $(OBJ) -L$(LIBFT_DIR) -lft

$(LIBFT_DIR)/libft.a:
    make -C $(LIBFT_DIR)
```
Replace path/to/libft with the actual path to the "libft" directory in your project.
* Update your project's compilation rules to ensure that "libft" is compiled before your project.

### Using the Library Functions
Once you've added "libft" as a dependency in your project's Makefile, you can use the library functions in your source code as needed. Include the libft.h header file in your source files and call the desired functions.

This approach allows for seamless integration of "libft" into your project's build process, ensuring that the library is compiled and linked automatically whenever your project is built.
### include the header file
Don't forget to include the libft.h header file in your source file:
```c
#include "libft.h"
#include <stdio.h>

int main() {
    char *str = "Hello, world!";
    int len = ft_strlen(str);
    
    printf("Length of the string: %d\n", len);
    
    return 0;
}
```
In this example:

* We include the standard <stdio.h> header for using printf.
* We include "libft.h" to access the function prototypes provided by the "libft" library.
* We call the ft_strlen function from "libft" to calculate the length of the string "Hello, world!".
* We print the length of the string using printf.
