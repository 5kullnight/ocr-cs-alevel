Preconditions are requirements that must be met before a program can be executed. If the preconditions are not met, the program will fail to execute or return an invalid answer. Specifying preconditions means that a subroutine can safely expect the arguments passed to it to meet certain criteria, as defined by the preconditions. Preconditions can be tested for within the code but are more often included in the documentation accompanying a particular subroutine, library, or program.

Consider, for example, the function `pop()`, which removes the last item added to a stack:
```
function pop():
    if top = 0 then
        print “No items in the stack.”
    else:
        element = stack[top]
        top = top - 1
    endif
endfunction

```
The function first checks that the stack is not empty by checking whether the top pointer, `top`, is greater than 0. Clearly, without this condition being met, no items can be removed from the stack. It is important that this is tested within the code, as popping from an empty stack would otherwise produce an error that would cause the program to crash.
Preconditions can also be included within the documentation, in which case it is the user’s responsibility to ensure inputs meet the requirements specified by these preconditions. A common example of this is the factorial function, which can only be called upon positive numbers. Rather than checking that the arguments passed to the function must be non-negative, this is specified within the documentation accompanying this function. Including preconditions within the documentation reduces the length and complexity of the program as well as saving time needed to debug and maintain a longer program.
The purpose of preconditions is to ensure that the necessary checks are carried out before the execution of a subroutine, either by the user or as part of the subroutine. By explicitly ensuring these conditions are met, subroutines are made more reusable.