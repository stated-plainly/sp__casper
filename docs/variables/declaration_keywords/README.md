[Casper :: Docs](https://github.com/stated-plainly/sp__casper/tree/main/docs) :: [Variables](https://github.com/stated-plainly/sp__casper/tree/main/docs/variables)
# Declaration Keywords
There are two aspects to the mutability of a variable:
- **Internal** Mutability → A value within the instance that the variable holds is changed e.g. the car's front-right tyre is replaced
- **External** Mutability → The instance that the variable itself holds is changed e.g. the car itself is replaced

**casper** captures these inter-related states using the following declaration keywords:
- `{immut}` → Internally Immutable :: Externally Immutable
- `inmut` → **Internally Mutable** :: Externally Immutable
- `exmut` → Internally Immutable :: **Externally Mutable**
- `mut` → **Internally Mutable** :: **Externally Mutable**

`{immut}` is wrapped in `{}` to indicate its **implicit** nature i.e. a variable declared without a declaration keyword is `{immut}`:
```casper
age : u8 = 10; -- this variable is {immut}
```
