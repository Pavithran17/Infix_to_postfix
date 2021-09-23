# Infix_to_postfix
## The function to convert an expression from infix to postfix consists following steps:
1. Every character of the expression string is scanned in a while loop until the end of the expression is reached. 
2. Following steps are performed depending on the type of character scanned. 
3. If the character scanned happens to be a space then that character is skipped. 
4. If the character scanned is a digit or an alphabet, it is added to the target string pointed to by t. 
5. If the character scanned is a closing parenthesis then it is added to the stack by calling push( ) function. 
6. If the character scanned happens to be an operator, then firstly, the topmost element from the stack is retrieved. Through a while loop, the priorities of the character scanned and the character popped ‘opr’ are compared.  
   
   Then following steps are performed as per the precedence rule. 
i. If ‘opr’ has higher or same priority as the character scanned, then opr is added to the target string. 
ii.If opr has lower precedence than the character scanned, then the loop is terminated. Opr is pushed back to the stack. Then, the character scanned is also added to the stack. 

7. If the character scanned happens to be an opening parenthesis, then the operators present in the stack are retrieved through a loop.  The loop continues till it does not encounter a closing parenthesis.  The operators popped, are added to the target string pointed to by t. 

8. Now the string pointed by t is the required postfix expression. 
