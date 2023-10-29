# Infix-Postfix
An infix expression is an expression in which operators (+, -, *, /) are written between the two operands. The postfix operator also contains operator and operands. In the postfix expression, the operator is written after the operand. It is also known as Reverse Polish Notation. 


# **AIM**

Infix and Postfix expression solving using stack.

Menu options - i) Push ii) Pop iii) Display iv) Exit

## **THEORY**

Infix expression: The expression of the form “a operator b” (a + b) i.e., when an operator is in-between every pair of operands.

Postfix expression: The expression of the form “a b operator” (ab+) i.e., When every pair of operands is followed by an operator.

Infix – Any operation of format a op b format example a + b is called an infix operation

Postfix – An operation or expression can also be written in the format of a b op i.e. a b + which is similar to writing a + b in infix. All we are doing is shifting operator to the right of operands

Why we need postfix operator?

For a compiler, it is easier to read postfix or prefix operation. As a compiler either reads from right to left or left to right. Let us understand this with the help of an example –
Imagine the following - a + b * c + d

Let us assume compiler starts reading from right to left

It reads c + d the operation first and it would be efficient if it could’ve implemented it, but, it can’t as next operation is c * b which has higher precedence and must be implemented first.

Thus, if the compiler reads a notation in which, it can keep on implementing operations as soon as it sees them right!

The corresponding Postfix would be: abc*+d+

Steps to convert

Any infix op1 oper op2 can be written as op1 op2 oper

Where op1 = Operand 1

op2 = Operand2

oper = Operation

Example a + b can be written as ab+ in postfix

Problem

Infix: a + b * c + d can be written as a + (b * c) + d

Now, for all + – / * associativity is left to right we will write it as

(a + (b * c)) + d and thus further ((a + (b * c)) + d)

Solving and converting innermost bracket to postfix

Step 1 –((a + bc*)+ d)

Step 2 – Consider bc* as separate operand x the innermost bracket now looks like ((a + x)+ d)

Applying postfix it looks like – (ax+ + d)replacing x here (abc*+ + d)

Step 3 – Consideringabc*+as separate operand z, the final bracket looks like – (z + d)the result would be zd+

replacing z value = abc*+d+

## **ALGORITHM**

Here's the algorithm of the provided C++ program, which allows users to push infix expressions onto a stack, convert them to postfix expressions, and display the stack:

1.Include necessary header files:

iostream for input and output.

stack for stack data structure.

string for handling string data.

2.Define utility functions:

isOperator(char c): Checks if a character is one of the operators (+, -, *, /).

getPrecedence(char op): Determines the precedence of an operator (+, -, *, /).

infixToPostfix(string infix): Converts an infix expression to postfix using a stack.

Inside the main function, create a stack of strings to hold infix expressions, and initialize variables for infix and postfix expressions.

3.Use an infinite loop for the program menu:

Display menu options (Push, Pop, Display, Exit).

Read the user's choice.

4.Implement the menu options:

5.Push (Infix Expression):

Prompt the user to enter an infix expression.

Push the infix expression onto the stack.

Display a confirmation message.

Pop (Convert and Display Postfix Expression):

Check if the stack is empty; if empty, inform the user.

Otherwise, pop the top infix expression from the stack.

Convert the infix expression to postfix using the infixToPostfix function.

6.Display the resulting postfix expression.

7.Display (Current Stack):

Check if the stack is empty; if empty, inform the user.

Otherwise, display the current stack's infix expressions.

8.Exit:

9.Display an exit message and terminate the program.

Provide a default case to handle invalid menu choices.

10.End the program.

This algorithm outlines how the C++ code manages infix expressions, postfix conversion, and stack display based on user menu selections.

## **OUTPUT**

![Screenshot 2023-10-29 at 5 53 25 PM](https://github.com/sanskkriti/Infix-Postfix/assets/140137289/9bca0967-c2e6-4950-8430-8f58a95bd51b)

![Screenshot 2023-10-29 at 5 53 33 PM](https://github.com/sanskkriti/Infix-Postfix/assets/140137289/e8513f87-6e4c-48dd-bc8c-73f3e1e51bd4)


