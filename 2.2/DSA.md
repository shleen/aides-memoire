## Deallocating Memory
- Use the `delete` operator i.e. `delete myPtr`.
- Point the 'deleted' pointer to NULL i.e. `myPtr = NULL`

## Evaluate Postfix
- Next Char, **Operand Stack**, Evaluation
- Steps
  - Iterate through each character in the expression.
  - If it's an operand, **push** onto the top of the stack.
  -  If it's an operator, **pop 2** elements off the top of the stack & apply the operator. i.e. second_from_top <operator\> top. Then push the evaluation back onto the stack.

## Infix to Postfix
- Next Char, Postfix Expression, **Operator** Stack
- Steps
  - Iterate through each character in the expression.
  - If it's an operand, **append** to the postfix expression.
  - If it's an operand, **push** onto the top of the stack **iff** s.peek() has equal or lower precedence than next char. else, pop & append to expression until the condition is satisfied & next char can be pushed onto the operator stack.
- Note: open parentheses are **always** pushed onto the operator stack & can only be popped off by a closing parentheses.

## Tracing a Recursive Function
Use a call stack! Push each call onto the stack with subscript denoting which call it stopped at. When a call terminates, cancel out the relevant call & write its return value to the right of the function call in the stack. Then, proceed.

<img src="https://i.imgur.com/6klH1YX.png" width="600px">

**Note!** Integral division in C++ **always rounds down**!
