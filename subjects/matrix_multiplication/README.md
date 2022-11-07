## matrix_multiplication

### Instructions

- Define a `struct` named `Matrix` as a tuple of 2 tuples. The nested tuple will contain 2 `i32`s.

- Create a **function** named `multiply` that receives a Matrix and an i32 and returns the Matrix with each number multiplied by the second argument. 
```rust
pub fn multiply(m: Matrix, val: i32) -> Matrix {
}
```

`Matrix` must implement `Debug`, `PartialEq` and `Eq`. You can use `derive`.

> Remember that you are defining a library, so any element that can be called from an external crate must be made public.

### Usage

Here is a possible program to test your function

```rust
use matrix_multiplication::multiply;
use matrix_multiplication::Matrix;

fn main() {
    let matrix = Matrix((1, 3), (4, 5));
    let val = 3;
    println!("Original matrix {:?}", matrix);
    println!("Matrix after multiply {:?}", multiply(matrix, val));
}
```

And its output:

```console
$ cargo run
Original matrix Matrix((1, 3), (4, 5))
Transpose matrix Matrix((3, 9), (12, 15))
$
```

### Notions

- [Defining a struct](https://doc.rust-lang.org/stable/book/ch05-01-defining-structs.html)

- [The Tuple Type](https://doc.rust-lang.org/stable/book/ch03-02-data-types.html?highlight=accessing%20a%20tuple#compound-types)

- [Tuples](https://doc.rust-lang.org/rust-by-example/primitives/tuples.html)

- [Tuple Structs without Named Fields](https://doc.rust-lang.org/stable/book/ch05-01-defining-structs.html?highlight=tuple#using-tuple-structs-without-named-fields-to-create-different-types)

- [Adding Useful Functionality with Derived Traits](https://doc.rust-lang.org/stable/book/ch05-02-example-structs.html?highlight=debug%20deriv#adding-useful-functionality-with-derived-traits)

- [Chapter 7](https://doc.rust-lang.org/stable/book/ch07-03-paths-for-referring-to-an-item-in-the-module-tree.html)
