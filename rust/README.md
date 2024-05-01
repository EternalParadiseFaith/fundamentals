# Rust

Rust is a fast & powerful system programming language which can also be used for web developement and web3.
No garbage collector

## Hello World

```rust
fn main() {
    println!("Hello, World\n");
}
```

## Variables

### Immutability

- Variables declared by the `let` keyworrd are immutable by default.
- Use the `mut` keyword to make it mutable. Example, `let mut x = 5;`.
- If a variable is mutable, only its value can change and not its type.

```rust
let mut x = 100;
let x = "Stringy"; // This will raise an error
```

### Shadowing

- Variable with the same name can be redefined in the same scope and can have different data type.

```rust
fn main() {
    let mut x = 5;
    let x = "Hello";
}
```

- Inner scope variables look for variables in the outer scope if not defined.

```rust
fn main() {
    let mut x = 5;
        println!("{}", x);
    {
        x = x*2;
        println!("{}", x);
    }
    x = x+1;
    println!("{}", x);
}
/* OUTPUT
 * 5
 * 10
 * 11
 */
```

### Const

- The type must be mentioned while initializing a `const` variable.
- We cannot only declare a `const` variable.
- Const variabels cannot be shadowed.
- Const cannot be made mutable with `mut`

```rust
const UPPER_VALUE: i32 = 1_000;
```
