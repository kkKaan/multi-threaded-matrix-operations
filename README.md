# Multi-Threaded Matrix Operation

## Overview
This project demonstrates the use of multi-threading and synchronization in C/C++ for performing matrix operations. It involves concurrent execution of addition and multiplication on four matrices, with results synchronized using mutexes, semaphores, and condition variables.

## Key Features
- Concurrent matrix addition and multiplication.
- Thread synchronization using semaphores and mutexes.
- Dynamic memory management for matrix operations.
- Custom thread data structures for efficient computation.

## Prerequisites
- A C/C++ compiler (e.g., GCC, Clang).
- Basic understanding of threading and synchronization in C/C++.

## Code Structure

### Data Structures
- Matrices: `int **m1`, `int **m2`, `int **m3`, `int **m4` for input matrices; `int **j`, `int **l`, `int **r` for result matrices.
- Synchronization Tools: Semaphore arrays `sem_t *sem_j`, `sem_t *sem_l_row`, etc., and protected variables like `int *protected_array`.

### Threading
- Thread Functions: `add_matrices`, `multiply_matrices` for performing matrix operations.
- Thread Data: `thread_data` and `multiply_thread_data` structures to pass specific data to threads.

### Input/Output
- `take_inputs`: Function to input matrix data.
- `print_matrix`: Function to output matrix data.

### Initialization and Management
- Allocating and freeing memory for matrices and semaphores.
- Creating and joining threads for matrix operations.

## Implementation Steps

1. **Input Handling**: Customize `take_inputs` to read matrix sizes and values.
2. **Matrix Operations**: Implement `add_matrices` and `multiply_matrices` with multi-threading.
3. **Thread Synchronization**: Ensure correct use of semaphores and mutexes for accurate and synchronized results.
4. **Output Results**: Print the resulting matrices post computation.

## Usage

1. **Compilation**: Compile the code with your C/C++ compiler.
2. **Execution**: Run the executable. The program expects matrix inputs from the standard input and outputs the results of the operations.

## Cleanup

- Ensure to free all allocated memory.
- Destroy all semaphores to prevent resource leaks.
