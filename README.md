# Application-level-Postfix-to-Infix-program-11


# Postfix to Infix Conversion - Calculator Application

def postfix_to_infix(expression):
    stack = []

    for ch in expression:
        if ch.isalnum():
            stack.append(ch)
        else:
            op2 = stack.pop()
            op1 = stack.pop()
            new_exp = "(" + op1 + ch + op2 + ")"
            stack.append(new_exp)

    return stack[0]


# Application Example
postfix = "AB+C*"

print("Postfix Expression:", postfix)
print("Infix Expression:", postfix_to_infix(postfix))



Postfix Expression: AB+C*
Infix Expression: ((A+B)*C)
