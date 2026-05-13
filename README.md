# Get Next Line (GNL)

A 42 school project that implements a function to read a file descriptor line by line.

## Overview

This project provides `get_next_line()`, a function that reads and returns one line at a time from a file descriptor. It efficiently manages memory by using a static buffer (stash) to handle partial lines and optimize repeated calls.

## Features

- **Line-by-line reading**: Returns one complete line per call
- **Configurable buffer**: `BUFFER_SIZE` can be adjusted at compile time (default: 42)
- **Memory efficient**: Uses a persistent buffer to avoid unnecessary re-reads
- **Robust**: Handles edge cases like missing newlines at EOF

## Files

- `get_next_line.h` - Header file with function declarations and helper prototypes
- `get_next_line.c` - Main function implementation
- `get_next_line_utils.c` - Utility functions (string operations, memory allocation)

## Function Signature

```c
char *get_next_line(int fd);
```

Returns the next line from file descriptor `fd`, including the newline character if present. Returns `NULL` on EOF or error.

## Compilation

```
gcc -Wall -Wextra -Werror -D BUFFER_SIZE=42 *.c
```

## Usage

You can use the provided `main` function in the `get_next_line.c` file

## Grade

103/100
