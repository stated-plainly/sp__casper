# Casper :: Variables :: Declaration Keywords
There are two aspects to the mutability of a variable:
- Internal Mutability => A value within the instance that the variable holds is changed
- External Mutability => The instance that the variable itself holds is changed

**casper** captures these inter-related states using the following declaration keywords:
- `{immut}` => Internally Immutable :: Externally Immutable
- `mut:in` => Internally Mutable :: Externally Immutable
- `mut:ex` => Internally Immutable :: Externally Mutable
- `mut` => Internally Mutable :: Externally Mutable

`{immut}` is wrapped in `{}` to indicate its implicit nature i.e. a variable declared without a declaration keyword is `{immut}`:
```casper
age : Int = (10); -- this variable is {immut}
```
