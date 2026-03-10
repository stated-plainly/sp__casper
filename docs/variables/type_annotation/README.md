[Casper :: Docs](https://github.com/stated-plainly/sp__casper/tree/main/docs) :: [Variables](https://github.com/stated-plainly/sp__casper/tree/main/docs/variables)
# Type Annotation
A foundational rule of **casper** is that:
> **ALL** variables must be type annotated

The reasoning for this is simply that it's **safer** than the alternative.

With implicit typing, the programmer is trusting that the function/method being called won't change its return type in the future, which **they cannot guarantee**. Generally this is *okay*, because a change in return type tends to break downstream logic, which'll get flagged by the compiler, but this isn't guaranteed.

In contrast, if the programmer **must** specify the type of data that they're expecting in all cases, then any upstream change **is** guaranteed to be flagged by the compiler and brought to the attention of the programmer.

As such, in **casper** all variable declarations must be annotated, using the following syntax:
```casper
name : (?)Char = prompt_user_for_name(); -- here, we specify explicitly that we're expecting a string of characters, of unknown length, to be returned
```
