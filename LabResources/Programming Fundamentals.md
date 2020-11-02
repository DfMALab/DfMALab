# Summarization of the Programming Fundamentals - A Modular Structured Approach, 2nd Edition book

**IPO**: Inputs – Processing – Outputs

**Pseudocode**: English-like statements used to convey the steps of an algorithm or function.

****

**Programming Quality**
  - **Reliability**: how often the results of a program are correct.
  - **Robustness**: how well a program anticipates problems due to errors (not bugs).
  - **Usability**: the ergonomics of a program.
  - **Portability**: the range of computer hardware and operating system platforms on which the source code of a program can be compiled/interpreted and run.
  - **Maintainability**: the ease with which a program can be modified by its present or future developers in order to make improvements or customizations, fix bugs and security holes, or adapt it to new environments.
  - **Efficiency/performance**: the measure of system resources a program consumes (processor time, memory space, slow devices such as disks, network bandwidth and to some extent even user interaction): the less, the better.
  - **Readability**: the ease with which a human reader can comprehend the purpose, control flow, and operation of source code.

****

**Pseudocode** is an informal high-level description of the operating principle of a computer program or other algorithm.

**Flowcharts** is a type of diagram that represents an algorithm, workflow or process.

****

**Integrated Development Environment (IDE)**

The IDE does the following steps:
  1. If there are any unsaved changes to the source code file it has the **test editor** save the changes.
  2. The **compiler** opens the source code file and does its **first step** which is executing the **pre-processor** compiler directives and other steps needed to get the file ready for the second step. The #include will insert header files into the code at this point. If it encounters an error, it stops the process and returns the user to the source code file within the text editor with an error message. If no problems encountered it saves the source code to a temporary file called a translation unit.
  3. The **compiler** opens the translation unit file and does its **second step** which is **converting** the programming language code to machine instructions for the CPU, a data area, and a list of items to be resolved by the linker. Any problems encountered (usually a syntax or violation of the programming language rules) stops the process and returns the user to the source code file within the text editor with an error message. If no problems encountered it saves the machine instructions, data area, and linker resolution list as an object file.
  4. The **linker** opens the program object file and links it with the library object files as needed. Unless all linker items are resolved, the process stops and returns the user to the source code file within the text editor with an error message. If no problems encountered it saves the linked objects as an executable file.
  5. The IDE directs the operating system’s program called the **loader** to load the executable file into the computer’s memory and have the Central Processing Unit (CPU) start processing the instructions. As the user interacts with the program, entering test data, he or she might discover that the outputs are not correct. These types of errors are called logic errors and would require the user to return to the source code to change the algorithm.

  ****

  **Version Control**

  **Version control**, also known as revision control or source control, is the management of changes to documents, computer programs, large websites, and other collections of information.

  - **Branch**: A separate working copy of files under version control which may be developed independently from the origin.
  - **Clone**: Create a new repository containing the revisions from another repository.
  - **Commit**: To write or merge the changes made in the working copy back to the repository.
  - **Merge**: An operation in which two sets of changes are applied to a file or set of files.
  - **Push**: Copy revisions from the current repository to a remote repository.
  - **Pull**: Copy revisions from a remote repository to the current repository.

****

## DATA AND OPERATORS

***

**Constants and Variables**

  - **Constant**: A data item whose value cannot change during the program’s execution.
    - **Literal constant**: A **value** you type into your program wherever it is needed.
    - **Symbolic constants or Named constants**: A constant represented by a name.
  - **Variable**: A data item whose value can change during the program’s execution.

****

**Identifier Names**

- Meaningful
- Case consistent

- **camelCase**: The practice of writing compound words or phrases such that each word or abbreviation in the middle of the phrase begins with a capital letter, with no intervening spaces or punctuation.
- **PascalCase**: The practice of writing compound words or phrases such that each word or abbreviation in the phrase begins with a capital letter, including the first letter, with no intervening spaces or punctuation.
- **Snake_case**: The practice of writing compound words or phrases in which the elements are separated with one underscore character (_) and no spaces, with each element’s initial letter usually lowercased within the compound and the first letter either upper or lower case.
- **Reserved word**: Words that cannot be used by the programmer as identifier names because they already have a specific meaning within the programming language.

****

**Scope**

- **Scope**: The area of a source code file where an identifier name is recognized.
- **Global scope**: Data storage defined outside of a function.
- **Local scope**: Data storage defined inside of a function.
- **Data area**: A part of an object code file used for storage of data.
- **Stack**: A part of the computer’s memory used for storage of data.

****

**Data Types**

A **data type** is a classification of data which tells the compiler or interpreter how the programmer intends to use the data.

| Data Type | Represents    | Examples     |
|-----------|---------------|--------------|
| integer   | whole numbers | `-5, 0, 123` |
| floating point (real) | fractional numbers | `-87.5, 0.0, 3.14159` |
| string | A sequence of characters | `"Hello world!"` |
| Boolean   | logical true or false | `true, false` |
| nothing   | no data       | `null`       |
| void      | no values and no operations | `void` |


- **ASCII**: American Standard Code for Information Interchange
character
- **double quote marks**: Used to create string type data within most programming languages.
- **single quote marks**: Used to create character type data within languages that differentiate between string and character data types.
- **Void**: Has no values and no operations. It’s a data type that represents the lack of a data type.

****

**Data Type Conversions**

Changing a data type of a value is referred to as “**type conversion**”. There are two ways to do this:
  1. **Implicit** – the change is implied
  2. **Explicit** – the change is explicitly done with an operator or function

The value being changed may be:
  1. **Promotion** – going from a smaller domain to a larger domain
  2. **Demotion** – going from a larger domain to a smaller domain

- **Demotion**: Going from a larger domain to a smaller domain.
- **Explicit**: Changing a value’s data type with the cast operator.
- **Implicit**: A value that has its data type changed automatically.
- **Promotion**: Going from a smaller domain to a larger domain.
- **Truncation**: The fractional part of a floating-point data type that is dropped when converted to an integer.

****

**Integer Overflow**

**Integer overflow** occurs when an arithmetic operation attempts to create a numeric value that is outside of the range that can be represented with a given number of bits – either larger than the maximum or lower than the minimum representable value.

The most common result of an overflow is that the least significant representable bits of the result are stored; the result is said to wrap around the maximum (i.e. modulo power of two). An overflow condition may give results leading to unintended behavior. In particular, if the possibility has not been anticipated, overflow can compromise a program’s reliability and security.

**Implications When Executing Loops**

If a programmer sets up a counting loop incorrectly, usually one of three things happen:
  - Infinite loop – usually caused by missing update attribute.
  - Loop never executes – usually, the text expression is wrong with the direction of the less than or greater than relationship needing to be switched.
  - Loop executes more times than desired – update not properly handled. Usually, the direction of counting (increment or decrement) need to be switched.

****

**Assignment**

An **assignment** statement sets and/or re-sets the value stored in the storage location(s) denoted by a variable name; in other words, it copies a value into the variable.

****

**Order of Operations**

  - Parentheses
  - Exponents
  - Multiplication / Division
  - Addition / Subtraction

A valid expression consists of operand(s) and operator(s) that are put together properly.
  1. Unary – only have one operand
  2. Binary – have two operands, one on each side of the operator
  3. Trinary – have two operator symbols that separate three operands

- **Associativity**: Determines the order in which the operators of the same precedence are allowed to manipulate the operands.
- **Evaluation**: The process of applying the operators to the operands and resulting in a single value.
- **Expression**: A valid sequence of operand(s) and operator(s) that reduces (or evaluates) to a single value.
- **Operand**: A value that receives the operator’s action.
- **Operator**: A language-specific syntactical token (usually a symbol) that causes an action to be taken on one or more operands.
- **Parentheses**: Change the order of evaluation in an expression. You do what’s in the parentheses first.
- **Precedence**: Determines the order in which the operators are allowed to manipulate the operands.

****

**Arithmetic Operators**

| Action         | Common Symbol |
|----------------|:-------------:|
| Addition       | `+`           |
| Subtraction    | `-`           |
| Multiplication | `*`           |
| Division       | `/`           |
| Modulus (associated with integers) | `%` |

Many programming languages support a combination of the assignment (`=`) and arithmetic operators (`+, -, *, /, %`).

****

**Unary Operations**

A **unary operation** is an operation with only one operand.

- **minus**: Aka unary negative.
- **plus**: Aka unary positive.
- **unary negative**: An operator that causes negation.
- **unary positive**: A worthless operator almost never used.

****

**Lvalue and Rvalue**

Some programming languages use the idea of **l-values** and **r-values**, deriving from the typical mode of evaluation on the left and right hand side of an assignment statement. An lvalue refers to an object that persists beyond a single expression. An rvalue is a temporary value that does not persist beyond the expression that uses it.

- **Lvalue**: The requirement that the operand on the left side of the assignment operator is modifiable, usually a variable.
- **Rvalue**: Pulls or fetches the value stored in a variable or constant.

****

**Relational Operators**

A **relational operator** is a programming language construct or operator that tests or defines some kind of relation between two entities. These include numerical equality (e.g., 5 = 5) and inequalities (e.g., 4 ≥ 3).

| Operator | Meaning                  |
|----------|--------------------------|
| <        | less than                |
| >        | greater than             |
| <=       | less than or equal to    |
| >=       | greater than or equal to |
| ==       | equality (equal to)      |
| != or <> | inequality (not equal to)|

**Assignment vs Equality**

**Assignment** sets and/or re-sets the value stored in the storage location denoted by a variable name. **Equality** is a relational operator that tests or defines the relationship between two entities.

***

**Logical Operators**

A **logical operator** is a symbol or word used to connect two or more expressions such that the value of the compound expression produced depends only on that of the original expressions and on the meaning of the operator. Common logical operators include AND (`&&`), OR (`||`), and NOT (`!`).

**Truth Tables**

A common way to show logical relationships is in truth tables.

| x     | y     | x and y | x or y |
|-------|-------|---------|--------|
| false | false | false   | false  |
| false | true  | false   | true   |
| true  | false | false   | true   |
| true  | true  | true    | true   |

| x     | not x |
|-------|-------|
| false | true  |
| true  | false |

****

## FUNCTIONS

****

**Modular Programming**

**Modular programming** is a software design technique that emphasizes separating the functionality of a program into independent, interchangeable modules, such that each contains everything necessary to execute only one aspect of the desired functionality.

Generally, functions fall into two categories:
  1. **Program Control** – Functions used to simply sub-divide and control the program. These functions are unique to the program being written. Other programs may use similar functions, maybe even functions with the same name, but the content of the functions are almost always very different.
  2. **Specific Task** – Functions designed to be used with several programs. These functions perform a specific task and thus are usable in many different programs because the other programs also need to do the specific task. Specific task functions are sometimes referred to as building blocks. Because they are already coded and tested, we can use them with confidence to more efficiently write a large program.

Program Control functions normally do not communicate information to each other but use a common area for variable storage. 

Specific Task functions are constructed so that data can be communicated between the calling program piece (which is usually another function) and the function being called. 

This ability to communicate data is what allows us to build a specific task function that may be used in many programs. The rules for how the data is communicated in and out of a function vary greatly by programming language, but the concept is the same. The data items passed (or communicated) are called **parameters**. Thus the wording: **parameter passing**. The four data communication options include:
  1. no communication in with no communication out
  2. no communication in with some communication out
  3. some communication in with some communication out
  4. some communication in with no communication out

**Program Layout**

Most programs have several items before the functions, including:
  1. Documentation – Most programs have a comment area at the start of the program with a variety of comments pertinent to the program.
  2. Include or import statements used to access standard library functions.
  3. Language-specific code such as namespace references or function prototypes. 
  4. Global or module-level constants and variables, when required.

- **Function**: What modules are called in many predominant programming languages of today.
- **Function call**: A function’s using or invoking of another function.
- **Function definition**: The code that defines what a function does.
- **Function prototype**: A function’s communications declaration to a compiler.
- **Identifier name**: The name given by the programmer to identify a function or other program items such as variables.
- **Modularization**: The ability to group some lines of code into a unit that can be included in our program.
- **Parameter passing**: How the data is communicated in to and out of a function.
Modular
- **Program control**: Functions used to simply subdivide and control the program.
- **Specific task**: Functions designed to be used with several programs.

| Function         | Purpose      | Parameters (input) | Return Value (output) |
|------------------|--------------|---------------------|-----------------------|
| Main             | main program | none                | none                  |
| GetFahrenheit    | input        | none                | fahrenheit            |
| CalculateCelsius | processing   | fahrenheit          | celsius               |
| DisplayResult    | output       | fahrenheit, celsius | none                  |

****

**Parameters and Arguments**

A **parameter** is a special kind of variable used in a function to refer to one of the pieces of data provided as input to the function. These pieces of data are the values of the **arguments** with which the function is going to be called/invoked. An ordered list of parameters is usually included in the definition of a function, so that, each time the function is called, its arguments for that call are evaluated, and the resulting values can be assigned to the corresponding parameters.

- **Argument**: A value provided as input to a function.
- **Parameter**: A variable identifier provided as input to a function.

****

**Call by Value vs. Call by Reference**

In **call by value**, a parameter acts within the function as a new local variable initialized to the value of the argument (a local (isolated) copy of the argument). In **call by reference**, the argument variable supplied by the caller can be affected by actions within the called function.

`Call by value <--Exact-- Original value --Modified--> Call by reference`

- **Call by reference**: Parameters passed by calling functions may be modified by called functions.
- **Call by value**: Parameters passed by calling functions cannot be modified by called functions.

****

**Return Statement**

- **Return**: A branching control structure that causes a function to jump back to the function that called it.

****

**Programming Style**

**Programming style** is a set of rules or guidelines used when writing the source code for a computer program.
  1. Documentation: At the top of the program
  2. Vertical Alignment
  3. Comments
  4. Indentation
  5. Meaningful Identifier Names Consistently Typed
  6. Appropriate use of Typedef

```
float length, width, height;
```
```
// Some programmers list them in alphabetic order.

float length;
float height; 
float width; 
```

****

**Standard Libraries**

Many common or standard functions, whose definitions have already been written, are ready to be used in any program. They are organized into a group of functions (think of them as several books) and are collectively called a **standard library**.

The main program must establish the existence of functions used in that program. Depending on the programming language, there is a formal way to:
  1. define a function
  2. declare a function (a prototype is a declaration to a compiler)
  3. call a function

When we create functions in our program, we usually see them in the following order in our source code listing:
  1. declare the function (prototype)
  2. call the function
  3. define the function

When we use functions created by others that have been organized into a library, we include a header file in our program which contains the prototypes for the functions. Just like functions that we create, we see them in the following order in our source code listing:
  1. declaring the function (prototype provided in the include file)
  2. call the function (with parameter passing of values)
  3. define the function (it is either defined in the header file or the linker program provides the actual object code from a Standard Library object area)

In most cases, the user can look at the prototype and understand exactly how the communications (parameter passing) into and out of the function will occur when the function is called. Let’s look at the math example of absolute value.

****

## CONDITIONS

****

**Structured Programming**

**Structured programming** is a programming paradigm aimed at improving the clarity, quality, and development time of a computer program by making extensive use of the structured control flow constructs of selection (if/then/else) and repetition (while and for), block structures, and subroutines in contrast to using simple tests and jumps such as the go to statement, which can lead to “**spaghetti code**” that is potentially difficult to follow and maintain.

The mechanisms that allow us to control the flow of execution are called **control structures**.

  - **Sequence** – Very boring. Simply do one instruction then the next and the next. Just do them in a given sequence or in the order listed. Most lines of code are this.
  - **Selection** – This is where you select or choose between two or more flows. The choice is decided by asking some sort of question. The answer determines the path (or which lines of code) will be executed.
  - **Iteration** – Also known as **repetition**, it allows some code (one to many lines) to be executed (or repeated) several times. The code might not be executed at all (repeat it zero times), executed a fixed number of times or executed indefinitely until some condition has been met. Also known as **looping** because the flowcharting shows the flow looping back to repeat the task.

A fourth category describes unstructured code.
  - **Branching** – An uncontrolled structure that allows the flow of execution to jump to a different part of the program. This category is rarely used in modular structured programming.

****

**Selection Control Structures**

In **selection control structures**, conditional statements are features of a programming language which perform different computations or actions depending on whether a programmer-specified Boolean condition evaluates to true or false.

  - **If Then Else Control Structure**: `if, else`
  - **Case Control Structure**: `switch, case, break, default`

****

**Code Blocks**

A **code block**, sometimes referred to as a compound statement, is a lexical structure of source code which is grouped together. Blocks consist of one or more declarations and statements. A programming language that permits the creation of blocks, including blocks nested within other blocks, is called a block-structured programming language. Blocks are fundamental to structured programming, where control structures are formed from blocks.

**The Need for a Compound Statement**

Within many programming languages, there can be **only one statement listed as the action part of a control structure**

Often, we will want to do more than one statement. This problem is overcome by creating a code block or compound statement. For programming languages that use curly braces `{}` or `:` or `end` to designate code blocks.
```
if(expression) 
  { 
    statement; 
    statement; 
  } else 
  { 
    statement; 
    statement; 
  }
```

- **Block**: Another name for a compound statement.
- **Compound statement**: A unit of code consisting of zero or more statements.

****

**Nested If Then Else**

Two-way selection structures may be **nested** inside other two-way selection structures, resulting in **multi-way selection**.

```
if age is less than 18 
  you can't vote 
    if age is less than 16 
      you can't drive 
    else 
      you can drive 
else 
  you can vote 
    if age is less than 21 
      you can't drink 
    else 
      you can drink
```

```
// Multiway Selection

if age equal to 18 
  you can now vote 
else 
  if age equal to 39 
    you are middle-aged 
  else 
      if age equal to 65 
        you can consider retirement 
      else 
        your age is unimportant
```

****

**Case Control Structure**

A **case** or **switch** statement is a type of selection control mechanism used to allow the value of a variable or expression to change the control flow of program execution via a multiway branch.

```
switch (age) { 
  case 18: 
    message = "You can vote."; 
  break; 
  case 39: 
    message = "You're middle-aged.";
  break; 
  case 65: 
    message = "Consider retirement."; 
  break; 
  default: 
    message = "Age is unimportant."; 
    break; 
}
```

****

## LOOPS

***

**Iteration Control Structures**

In **iteration control structures**, a statement or block is executed until the program reaches a certain state, or operations have been applied to every element of a collection. This is usually expressed with keywords such as `while`, `repeat`, `for`, or `do..until`.

```
count assigned zero 
While count < 5 
  Display "I love computers!" 
  Increment count 
End
```
```
count assigned five 
Do 
  Display "Blast off is soon!" 
  Decrement count 
While count > zero
```
```
count assigned five 
Repeat 
  Display "Blast off is soon!" 
  Decrement count 
Until count < one
```
```
For x starts at 0, x < 5, increment x 
  Display "Are we having fun?" 
End
```

****

**Flag Concept**

**Flags** are commonly used to control or to indicate the intermediate state or outcome of particular operations.

Any variable or constant that holds data can be used as a flag. You can think of the storage location as a flagpole. The value stored within the variable conveys some meaning and you can think of it as being the flag. An example might be a variable named: gender which is of the character data type. The two values commonly stored in the variable are: ‘F’ and ‘M’, meaning female and male. Then, somewhere within a program we might look at the variable to make a decision:

flag controlling an if then control structure
```
if gender equals 'F' 
  display "Are you pregnant?" 
  get answer from user store in pregnant variable
```
Looking at the flag implies comparing the value in the variable to another value (a constant or the value in another variable) using a relational operator (in our above example: equality).

Control structures are “controlled” by using a **test expression** which is usually a **Boolean expression**. Thus, the flag concept of “looking” at the value in the variable and comparing it to another value is fundamental to understanding how all control structures work.

**Two Flags with the Same Meaning**

Sometimes we will use an iteration control structure of do while to allow us to decide if we want to do the loop action again. A variable might be named “loop_response” with the user prompted for their answer of ‘y’ for yes or ‘n’ for no. Once the answer is retrieved from the keyboard and stored in our flag variable of “loop_response” the test expression to control the loop might be:

simple flag comparison
```
loop_response equals 'y'
```
This is fine but what if the user accidentally has on the caps lock. Then the response of ‘Y’ would not have the control structure loop and perform the action again. The solution lies in looking at the flag twice. Consider:

complex flag comparison
```
loop_response equals 'y' or loop_response equals 'Y'
```
We look to see if the flag is either a lower case y or an upper case Y by using a more complex Boolean expression with both relational and logical operators.

**Multiple Flags in One Byte**

Within assembly language programming and in many technical programs that control special devices; the use of a single byte to represent several flags is common. This is accomplished by having each one of the 8 bits that make up the byte represent a flag. Each bit has a value of either 1 or 0 and can represent true and false, on or off, yes or no, etc.

****

**Branching Statements**

A branch is an instruction in a computer program that can cause a computer to begin executing a different instruction sequence and thus deviate from its default behavior of executing instructions in order. Common branching statements include `break`, `continue`, `return`, `goto`, and `exit`.

```
counter = 0; 
While counter < 8 
  Output 
    counter 
  If counter == 4 
    break 
  counter += 1
```
```
For counter = 0, counter < 8, counter += 1 
  If counter == 4 
    continue 
  Output counter
```
```
Function DoSometing 
  statements 
Return <optional return value>
```
```
some lines of code; 
goto label;                  // jumps to the label 
some lines of code; 
some lines of code; 
some lines of code; label: 
some statement;              // Declared label 
some lines of code;
```

****

**Increment and Decrement**

**Increment (`++`) and decrement (`--`) operators** are unary operators that add or subtract one from their operand, respectively. They are commonly implemented in imperative programming languages.

- **Decrement**: Subtracting one from the value of a variable.
- **Increment**: Adding one to the value of a variable.
- **Postfix**: Placing the increment or decrement operator to the right of the operand. `age = oldest++;`
- **Prefix**: Placing the increment or decrement operator to the left of the operand. `age = ++oldest;`

****

**Nested For Loops**

**Nested for loops** places one for loop inside another for loop. The inner loop is repeated for each iteration of the outer loop.

```
For row = 1, row <= 3, row += 1 
  For column = 1, column <= 3, column += 1 
    Output row * column 
    Output "\t" 
  Output "\n"
```

- **Complex logic**: Often solved with nested control structures.

****

## ARRAYS

****

**Arrays and Lists**

An **array** is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key.

Depending on the language, array types may overlap (or be identified with) other data types that describe aggregates of values, such as **lists** and **strings**. Array types are often implemented by array data structures, but sometimes by other means, such as **hash tables**, **linked lists**, or **search trees**.

Arrays can have multiple axes (more than one axis). Each axis is a **dimension**. Thus a single-dimension array is also known as a **list**. A two-dimension array is commonly known as a **table** (a spreadsheet like Excel is a two dimension array). In real life, there are occasions to have data organized into **multiple-dimension arrays**. Consider a theater ticket with section, row, and seat (three dimensions). Most single-dimension arrays are visualized vertically.

Most programmers are familiar with a special type of array called a **string**. Strings are basically a single dimension array of characters. Unlike other single dimension arrays, we usually envision a string as a horizontal stream of characters and not vertically as a list.

We refer to the individual values as **members** (or elements) of the array. Programming languages implement the details of arrays differently. Because there is only one identifier name assigned to the array, we have operators that allow us to reference or access the individual members of an array. The operator commonly associated with referencing array members is the **index** operator. It is important to learn how to define an array and initialize its members.

```
// C++

int ages[] = {49, 48, 26, 19, 16};

ages[0] = 49;
```

This is the **defining of storage space**. The square brackets [] are used here to create the array with five integer members and the identifier name of ages. The assignment with braces (that is a block) establishes the initial values assigned to the members of the array. Note the use of the sequence or comma operator.

- **Dimension**: An axis of an array.
- **List**: A single dimension array.
- **Table**: A two-dimension array.

****

**Index Notation**

**Index notation** is used to specify the elements of an array. Most current programming languages use square brackets [] as the array index operator. Older programming languages, such as FORTRAN, COBOL, and BASIC, often use parentheses () as the array index operator.

- **Array member**: An element or value in an array.
- **Index**: An operator that allows us to reference a member of an array.
- **Offset**: The method of referencing array members by starting at zero.

****

**Displaying Array Members**

To **display** all **array members**, visit each element using a for loop and output the element using index notation and the loop control variable.

One of the principles of software development is **don’t repeat yourself (DRY)**. Violations of the DRY principle are typically referred to as **WET solutions**, which is commonly taken to stand for either “**write everything twice**”, “**we enjoy typing**” or “**waste everyone’s time**”.

```
Declare Integer Array ages[5] 
Declare Integer index 
Assign ages = [49, 48, 26, 19, 16] 
For index = 0 to Size(ages) - 1 
  Output ages[index] 
End
```

****

**Arrays and Functions**

In modular programming, specific task functions are often created and used or reused for array processing. Array processing functions are usually passed the array and any data necessary to process the array for the given task.

It should be noted that arrays are passed by reference in most current programming languages. Array processing functions must take care not to alter the array unless intended.

Arrays are an important **complex data type** used in almost all programming.

- **Array function**: A user-defined specific task function designed to process an array.

****

**Math Statistics with Arrays**

Statistics is a branch of mathematics dealing with the collection, organization, analysis, interpretation, and presentation of data. Common statistical methods include mean (or average) and standard deviation, sum, etc.

****

**Searching Arrays**

**Linear search** or **sequential search** is a method for finding a target value within a list. It sequentially checks each element of the list for the target value until a match is found or until all the elements have been searched.

Finding a specific member of an array means searching the array until the member is found. It’s possible that the member does not exist and the programmer must handle that possibility within the logic of his or her algorithm.

“The linear search is a very simple algorithm. Sometimes called a sequential search, it uses a loop to sequentially step through an array, starting with the first element. It compares each element with the value being searched for, and stops when either the value is found or the end of the array is encountered. If the value being searched for is not in the array, the algorithm will search to the end of the array.”

Two specific linear searches can be made for the maximum (largest) value in the array or the minimum (smallest) value in the array. Maximum and minimum are also known as max and min. Note that the following max and min functions assume an array size >= 1.

- **Linear search**: Using a loop to sequentially step through an array.
- **Maximum**: Aka max or the largest member of an array.
- **Minimum**: Aka min or the smallest member of an array.

****

**Sorting Arrays**

A **sorting** algorithm is an algorithm that puts elements of a list in a certain order. The most frequently used orders are numerical order and lexicographical order. Most current programming languages include built-in or standard library functions for sorting arrays.

****

**Parallel Arrays**

A group of **parallel arrays** is a form of implicit data structure that uses multiple arrays to represent a singular array of records. It keeps a separate, homogeneous data array for each field of the record, each having the same number of elements. Then, objects located at the same index in each array are implicitly the fields of a single record.

For example, if there are two arrays, one for names and one for ages, the array elements at `names[2]` and `ages[2]` would describe the name and age of the third person.

```
Function Main 
  Declare String Array names[5] 
  Declare Integer Array ages[5] 
  
  Assign names = ["Lisa", "Michael", "Ashley", "Jacob", "Emily"]
  Assign ages = [49, 48, 26, 19, 16] 
  
  DisplayArrays(names, ages) 
End 
  Function DisplayArrays (String Array names, Integer Array ages) Declare Integer index 
  
  For index = 0 to Size(array) - 1
    Output names[index] & " is " & ages[index] & " years old" 
  End 
End
```

****

**Multidimensional Arrays**

The number of indices needed to specify an element is called the **dimension** or **dimensionality** of the array. A two-dimensional array, or table, may be stored as a one-dimensional array of one-dimensional arrays (rows of columns) and accessed with double indexing (`array[row][column]` in typical notation).

****

**Fixed and Dynamic Arrays**

A **fixed array** is an array for which the size or length is determined when the array is created and/or allocated.

A **dynamic array** is a random access, variable-size list data structure that allows elements to be added or removed. It is supplied with standard libraries in many modern programming languages. Dynamic arrays overcome a limit of static arrays, which have a fixed capacity that needs to be specified at allocation.

Dynamic arrays allow elements to be added and removed at runtime. Most current programming languages include built-in or standard library functions for creating and managing dynamic arrays.

****

## STRINGS AND FILES

****

**Strings**

A **string** is traditionally a sequence of characters, either as a literal constant or as some kind of variable. The latter may allow its elements to be mutated and the length changed, or it may be fixed (after creation). A string is generally considered a data type and is often implemented as an array data structure of bytes (or words) that stores a sequence of elements, typically **characters**, using some character encoding.

A **buffer overflow**, or buffer overrun, is an anomaly where a program, while writing data to a buffer, overruns the buffer’s boundary and overwrites adjacent memory locations.

****

**String Functions**

**String functions** are used in computer programming languages to manipulate a string or query information about a string. (case, comparison, concatenation, find, join, length, replace, reverse, split, substring, trim)

****

**String Formatting**

**String formatting** uses a process of string interpolation (variable substitution) to evaluate a string literal containing one or more placeholders, yielding a result in which the placeholders are replaced with their corresponding values. (`format()`)

- **Code injection**: The exploitation of a computer bug that is caused by processing invalid data.
- **Formatting**: Modifying the way the output is displayed.
- **String interpolation**: Evaluating a string literal containing one or more placeholders, yielding a result in which the placeholders are replaced with their corresponding values.

****

**File Input and Output**

A computer file is a computer resource for recording data discretely in a computer storage device. Just as words can be written to paper, so can information be written to a computer file.
There are different types of computer files, designed for different purposes. A file may be designed to store a picture, a written message, a video, a computer program, or a wide variety of other kinds of data. Some types of files can store several types of information at once.
By using computer programs, a person can open, read, change, and close a computer file. Computer files may be reopened, modified, and copied an arbitrary number of times.

- **Close**: Your program requesting the operating system to release a file that was previously opened.
- **Device token**: A key value provided by the operating system to associate a device to your program.
- **Filename**: The name and its extension.
- **Filespec**: The location of a file along with its filename.
- **Open**: Your program requesting the operating system to let it have access to an existing file or to open a new file.
- **Read**: Moving data from a device that has been opened into a memory location defined in your program.
- **Stream**: A sequence of data elements made available over time.
- **stdin**: Standard input stream, typically the keyboard.
- **stderr**: Standard output error stream, typically the monitor.
- **stdout**: Standard output stream, originally a printer, but now typically the monitor.
- **text file**: A file consisting of characters from the ASCII character code set.
- **using / with**: A wrapper around a processing block that will automatically close opened resources.
- **Write**: Moving data from a memory location defined in your program to a device that has been opened.

****

**Loading an Array from a Text File**

Loading an array from a text file requires several steps, including: opening the file, reading the records, parsing (splitting) the records into fields, adding the fields to an array, and closing the file. The file may be read all at once and then parsed, or processed line by line. The array must either be at least as large as the number of records in the file, or must be generated dynamically.
  - Static Array Processing
  - Dynamic Array Processing

- **Dynamic memory**: Aka stack created memory associated with local scope.
- **Static memory**: Aka data area memory associated with global scope.

****

## OBJECT-ORIENTED PROGRAMMING

****

**Objects and Classes**

**Object-oriented programming (OOP)** is a programming paradigm based on the concept of “**objects**”, which may contain data, in the form of **fields**, often known as **attributes**; and code, in the form of **procedures**, often known as **methods**. A feature of objects is that an object’s procedures can access and often modify the data fields of the object with which they are associated (objects have a notion of “**this**” or “**self**”). There is significant diversity of OOP languages, but the most popular ones are **class-based**, meaning that **objects are instances of classes, which typically also determine their type**.

Object-oriented programming instead breaks down a programming task into objects that expose behavior (methods) and data (members or attributes) using interfaces. The most important distinction is that while procedural programming uses procedures to operate on separate data structures, object-oriented programming bundles the two together, so an “object”, which is an instance of a class, operates on its “own” data structure. Larger programs benefit from better code and data isolation and reuse provided by an object-oriented approach.

Objects and classes are often designed to represent real-world objects. Consider a door as an example of a real-world object. Most doors have limited functionality. They may be opened and closed, and locked and unlocked. In procedural programming, we might design functions to open, close, lock, and unlock a door, such as:
```
// Procedural Programming - Functions 

OpenDoor(door) 
CloseDoor(door) 
LockDoor(door) 
UnlockDoor(door)
```
Object-oriented programming combines code and data, so that, rather than having separate functions act on doors, we design doors that have methods that can act on themselves. Methods represent something the object can do, and are typically defined using verbs. Object-oriented door pseudocode might look like:
```
// Object-Oriented Programming - Methods 

door.Open() 
door.Close() 
door.Lock() 
door.Unlock()
```
Objects may also have attributes, something the object **is** or **has**, and are typically defined using **nouns** or **adjectives**. Door attributes might include:
```
// Object-Oriented Programming - Attributes

door.Height 
door.Width 
door.Color 
door.Closed 
door.Locked
```
When we write code to define a generic door, we would create a door class. The door class would contain all of the methods a door can perform and all of the attributes a door might have. We would then create instances of the class (objects) to represent specific doors, such as a front door, back door, or room door on a house, or a left door and right door on a car.

- **Attribute**: A specification that defines a property of an object.
- **Class**: An extensible program-code-template for creating objects, providing initial values for state (member variables) and implementations of behavior (member functions or methods).
- **Instance**: A concrete occurrence of an object.
- **Method**: A specification that defines a procedure or behavior of an object.
- **Object**: A particular instance of a class where the object can be a combination of variables, functions, and data structures.
- **this, self, or Me**: Keywords used in some computer programming languages to refer to the object, class, or other entity that the currently running code is part of.

****

**Encapsulation**

**Encapsulation** is one of the fundamentals of OOP (object-oriented programming). It refers to the bundling of data with the methods that operate on that data. Encapsulation is used to hide the values or state of a structured data object inside a class, preventing unauthorized parties’ direct access to them. Publicly accessible methods are generally provided in the class (so-called getters and setters) to access the values, and other client classes call these methods to retrieve and modify the values within the object.

- **Abstraction**: A technique for arranging complexity of computer systems so that functionality may be separated from specific implementation details.
- **Accessor**: A method used to return the value of a private member variable, also known as a getter method.
- **Encapsulation**: A language mechanism for restricting direct access to some of an object’s components.
- **Information hiding**: The principle of segregation of the design decisions in a computer program from other parts of the program. See encapsulation.
- **Mutator**: A method used to control changes to a private member variable, also known as a setter method.
- **Private**: An access modifier that restricts visibility of a property or method to the class in which it is defined.
- **Public**: An access modifier that opens visibility of a property or method to all other classes.

****

**Inheritance and Polymorphism**

In object-oriented programming, **inheritance** is the mechanism of basing an object or class upon another object (prototypical inheritance) or class (class-based inheritance), retaining similar implementation. In most class-based object-oriented languages, an object created through inheritance (a “child object”) acquires all the properties and behaviors of the parent object (except: constructors, destructor, overloaded operators and friend functions of the base class). Inheritance allows programmers to create classes that are built upon existing classes, to specify a new implementation while maintaining the same behaviors (realizing an interface), to reuse code and to independently extend original software via public classes and interfaces.

- **Inheritance**: An object or class being based on another object or class, using the same implementation or specifying a new implementation to maintain the same behavior.
- **Polymorphism**: The provision of a single interface to entities of different types.

****

**_Reference_**: [**Programming Fundamentals**: A Modular Structured Approach, 2nd Edition](https://press.rebus.community/programmingfundamentals)