# 🦀 Rust Basics Cheat Sheet 🎉

Welcome to the Rust programming world! This cheat sheet is designed to teach you basic Rust concepts in an easy-to-understand way. 🚀✨ Let's dive in!

---

## 🌟 Variables

- Immutable by default (cannot change).
- Use `mut` for mutable (changeable) variables.

```rust
let name = "Rusty"; // Immutable
let mut score = 10; // Mutable
score = 20; // This works because it's mutable
println!("I am {} and my score is {}", name, score);
```

---

## 🎈 Functions

Rust functions are defined with the `fn` keyword. They can:
- Accept parameters.
- Return values!

```rust
fn greet(name: &str) {
    println!("Hello, {}! Welcome to Rust!", name);
}

fn add(x: i32, y: i32) -> i32 {
    x + y
}

fn main() {
    greet("Rustacean");
    let result = add(5, 3);
    println!("5 + 3 = {}", result);
}
```

---

## 🔀 Match Statements

No boring if-else chaining here! Use Rust's `match` for clean control flow.

```rust
fn main() {
    let fruit = "apple";

    match fruit {
        "apple" => println!("🍎 You got an apple!"),
        "banana" => println!("🍌 Yay, a banana!"),
        _ => println!("🤷‍♀️ What fruit is this?"),
    }
}
```

---

## 👫 Structs (Like Blueprints!)

We can group different properties together using `struct`.

```rust
struct Person {
    name: String,
    age: u8,
}

fn main() {
    let bob = Person {
        name: String::from("Bob"),
        age: 25,
    };

    println!("Meet {}, who is {} years old.", bob.name, bob.age);
}
```

---

## 📐 Structs + Methods (`impl`)

Associate methods/functions with structs using `impl`. Rust magic!

```rust
struct Rectangle {
    width: u32,
    height: u32,
}

impl Rectangle {
    fn area(&self) -> u32 {
        self.width * self.height
    }
}

fn main() {
    let rect = Rectangle { width: 5, height: 4 };
    println!("Area of the rectangle is: {}", rect.area());
}
```

---

## 🎡 Loops and Iterations

Rust has `loop`, `while`, and `for`.

```rust
for num in 1..4 {
    println!("Counting: {}", num); // Prints 1, 2, 3
}
```

---

## 🧳 Ownership & Borrowing

Rust is safe because of its ownership rules 🦺.

```rust
fn main() {
    let s1 = String::from("hello");
    let s2 = &s1; // Borrowing
    println!("s1: {}, s2: {}", s1, s2); // Both are valid here
}
```

---

## 🗃️ Collections (Vectors)

Use `vec!` for dynamic lists.

```rust
fn main() {
    let mut nums = vec![1, 2, 3];
    nums.push(4); // Add a number
    for n in nums {
        println!("{}", n);
    }
}
```

---

🌈 **That's it!** Rust is fun, safe, and powerful! Take small steps, write code, and have fun. 🦀💡

Made with ❤️ and Rust. Keep calm and love Rust!
