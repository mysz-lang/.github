# Mysz-Lang

A mouse-loving mouse-based mouse-enthusiastic programming language project.

## Repositories
- **mysz-core** – main implementation of the language

## Mysz

Mysz is a compiled, statically-typed programming language designed to be simple.

### Type System
Mysz features a straightforward static type system that maps cleanly to native machine types:
* `int` – 64-bit signed integer (`i64`)
* `char` – 8-bit ASCII character/byte (`i8`)
* `bool` – Boolean value (`true`/`false`)
* `str` – Immutable string reference / C character pointer
* `[T; N]` – Fixed-size array of type `T` and length `N`

### Example Code

Here is a simple program demonstrating array initialization, loop control structures, and interaction with foreign functions:

```mysz
extern fn print_char(a: char, newline: bool);

fn main(): int {
    // Fixed-size character array allocation
    var x: [char; 12] = ['H', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd', '!']; 
    
    // Iterating and printing each character
    for (var i = 0; i < 12; i = i + 1) {
        print_char(x[i], false);
    };
    
    return 0;
}
```

```
> ./out
Hello world!
```

## Contributing
Contributions are welcome. By contributing, you agree your work will be licensed under the Apache License 2.0 in the relevant repository.

See individual repositories for details.

## License
Most repositories are licensed under Apache License 2.0.
