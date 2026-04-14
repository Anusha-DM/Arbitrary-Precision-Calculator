# Arbitrary-Precision-Calculator
📌 Arbitrary Precision Calculator (APC)
🧾 Project Overview

The Arbitrary Precision Calculator (APC) is a C-based application designed to perform arithmetic operations on extremely large integers that exceed the limits of standard data types. Instead of relying on built-in numeric types, this project uses doubly linked lists to store and manipulate each digit individually.

This approach enables accurate computation of very large numbers without overflow issues.

⚙️ Features
Supports large integer operations:
Addition (+)
Subtraction (-)
Multiplication (x or *)
Division (/)
Handles both positive and negative numbers
Uses doubly linked list representation for digit-wise processing
Efficient carry and borrow handling
Command-line based execution
🏗️ Data Structure Used

The project uses a doubly linked list where:

Each node stores a single digit
Nodes are connected using prev and next pointers
Enables traversal in both directions (important for arithmetic operations)
typedef struct apc
{
    int data;
    struct apc *prev;
    struct apc *next;
} APC;

🧠 Working Principle
Input numbers are taken as command-line arguments
Each digit is stored in a linked list
Arithmetic operations are performed digit-by-digit:
Addition handles carry
Subtraction handles borrow
Multiplication uses repeated addition with shifting
Division uses repeated subtraction
Result is stored in another linked list and printed
🚀 How to Run
🔧 Compilation
gcc *.c -o a.out
▶️ Execution
./a.out <number1> <operator> <number2>
📌 Examples
./a.out -12 + 5
./a.out 123456789 x -987654321
./a.out -100 / 25
./a.out -12 - -3
✅ Sample Output
-7
-121932631112635269
-4
-9

📂 Project Modules
main.c → Input parsing and operation control
add.c → Addition logic with carry handling
sub.c → Subtraction with borrow logic
mul.c → Multiplication using partial products
div.c → Division using repeated subtraction
compare.c → Compares two large numbers
Utility files:
insert_first.c, insert_last.c
get_len.c
free.c
print_list.c
⚠️ Limitations
Division is implemented using repeated subtraction, which is not optimized for very large numbers
No support for decimal numbers (only integers)
No GUI (command-line only)
🔮 Future Enhancements
Implement faster division (e.g., long division algorithm)
Support floating-point numbers
Add user interface (GUI)
Optimize memory usage
👩‍💻 Author
Anusha M
