# ocaml-calculator-cli
A simple calculator application built using OCaml, demonstrating basic arithmetic operations (addition, subtraction, multiplication, and division) through functional programming. This project serves as an introduction to OCaml syntax, functional programming concepts, and basic CLI development.


It's common to separate concerns into different files for better organization and modularity. The goal is to keep different parts of the program focused on specific tasks. Here's how each file fits into this idea:


-  calculator.ml  : This file contains purely functional logic—the actual operations or calculations. It's the place where the basic arithmetic functions (like sum, subtract, etc.) are implemented. This file is a module that exposes functions that can be used in other parts of the program.


-  simple_calculator.ml:   This file is more about interacting with the user and handling input/output. It contains the code for reading user input, selecting the right operation, and printing the result. It is essentially the driver program that connects the logic (from calculator.ml) to the user interface.
