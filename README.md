# ocaml-calculator-cli
A simple calculator application built using OCaml, demonstrating basic arithmetic operations (addition, subtraction, multiplication, and division) through functional programming. This project serves as an introduction to OCaml syntax, functional programming concepts, and basic CLI development.


It's common to separate concerns into different files for better organization and modularity. The goal is to keep different parts of the program focused on specific tasks. Here's how each file fits into this idea:


-  calculator.ml  : This file contains purely functional logic—the actual operations or calculations. It's the place where the basic arithmetic functions (like sum, subtract, etc.) are implemented. This file is a module that exposes functions that can be used in other parts of the program.


-  simple_calculator.ml:   This file is more about interacting with the user and handling input/output. It contains the code for reading user input, selecting the right operation, and printing the result. It is essentially the driver program that connects the logic (from calculator.ml) to the user interface.


How Dune Works with Both Files:

Dune is a build system for OCaml projects. It helps organize and build the project by defining how to build each part of the project and how the parts (modules) depend on each other. Dune knows how to compile all the .ml files into an executable.

Dune Build Process: When we run dune build, Dune will:

    + Compile calculator.ml and produce a compiled object file for the Calculator module.
    + Compile simple_calculator.ml, linking it with the Calculator module (since simple_calculator.ml uses functions like sum from calculator.ml).
    + Build the executable (likely simple_calculator.exe), which is a program that can run and interact with the user.

How Dune Knows About the Files:

In Dune, we specify which files are part of the project and how they should be compiled. The relevant dune file is looking like this:  

(executable
  (name simple_calculator)
  (modules simple_calculator calculator))  (* This tells dune to include both files *)


This dune file tells Dune that:

    + We are building an executable called simple_calculator.
    + The source code for this executable is split into two modules: simple_calculator.ml and calculator.ml.
    + When Dune compiles the code, it will first compile the calculator.ml module and then compile simple_calculator.ml, linking them together into one         final executable.






    
