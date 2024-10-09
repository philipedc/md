
There are three different ways a program can be executed: **compiled**, **interpreted** and through **virtual machines**. These tools provide a way to simulate the semantics of a program in hardware. Any programming language can be be compiled or interpreted. 

# Compiled Programs

Compilers transforms a high-level language to a low-level language tailored to a computer architecture

#change the image isn't great
![[compiler-overview.png]]

**Pros**:
- Faster (binary code is already done)
- Safer (errors occur during compilation)

**Cons**:
- Hardware specific
## Frontend Phase: 

#change
**Preprocessing**: 

**Lexical analysis (lexing):** source code is broken into a sequence of small pieces called lexical tokens. Common token categories include identifiers, keywords, separators, operators, literals and comments. Typically the lexemes form a regular language, so a finite state automata can be constructed to verify errors.

**Syntax analysis (parsing)**: the tokens are used to build a parse tree according to the formal grammar that defines the language's syntax. 

**Semantic analysis**: add information to the parse tree and build the symbol table. Performs semantic checks such as type checking, object binding (associating variable and function references with their definitions) and definite assignment (requiring all local variables to be initialized before use), rejecting or issuing warnings.

## Optimize Phase:



## Backend Phase:


## Code:

Create a **preprocessed** file:
```
gcc -E hello.c > hello.p.c
cat hello.p.c
```

Generate the **assembly**:
```
gcc -S hello.p.c -o hello.p.s
cat hello.p.s
```

Build the **binary** code:
#change
```
as hello.p.s -o hello.o
coredump
```

Link the binary code to its **libraries**:
```
ld hello.o -o a.out
coredump
```

# Interpreted Programs

#question 
Interpreters execute the code in memory (is tree-walk interpreter the only one?)

**Pros**:
- Hardware agnostic (if the machine has an interpreter it will work)
**Cons**:
- Slow (code is read, analyzed and executed in run time)
- Resource-intensive 


First we'll create 

**Abstract syntax tree**: 

# Virtual Machine Programs

#change 
Virtual machines are a mid ground between compiled and interpreted programs. The compilation phase generates a bytecode, it is then interpreted by a virtual machine

