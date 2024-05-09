# Circom Learning Exercises

This repository is dedicated to learning and documenting the Circom language, used for writing zero-knowledge circuits. Each directory contains solutions to various exercises, aiming to deepen understanding of writing circuits in Circom.

## Installation

### Rust Installation

The Circom compiler requires Rust. For macOS and Linux users, install Rust using the following command:

```bash
curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

### Circom Compiler Installation

Clone the Circom repository:

```bash
git clone https://github.com/iden3/circom.git
cd circom
```

Build the Circom compiler:

```bash
cargo build --release
```

Install the compiler:

```bash
cargo install --path circom
```

### Libraries

Install necessary JavaScript libraries:

```bash
npm install
```

For more information, refer to the [Circom Documentation](https://docs.circom.io/).

## Exercises

Below are the exercises included in this repository. Each exercise comes with a set of parameters, input and output specifications, and a brief description.

The following excercises are taken from: https://hackmd.io/@gubsheep/S1Hz96Yqo 

### Num2Bits

- **Parameters**: `nBits`
- **Input**: `in`
- **Output**: `b[nBits]` - Array of bits representing `in`. `b[0]` is the least significant bit.

### IsZero

- **Input**: `in`
- **Output**: `out` - `1` if `in` is zero, otherwise `0`.

### IsEqual

- **Input**: `in[2]`
- **Output**: `out` - `1` if `in[0]` is equal to `in[1]`, otherwise `0`.

### Selector

- **Parameters**: `nChoices`
- **Input**: `in[nChoices]`, `index`
- **Output**: `out` - Equals `in[index]`. `0` if `index` is out of bounds.

### IsNegative

- **Input**: `in`
- **Output**: `out` - `1` if `in` is negative by convention, otherwise `0`.

### LessThan

- **Input**: `in[2]`
- **Output**: `out` - `1` if `in[0]` is strictly less than `in[1]`, otherwise `0`.
- **Extension**: Implement variations for `LessEqThan`, `GreaterThan`, and `GreaterEqThan`.

### IntegerDivide

- **Parameters**: `nbits`
- **Input**: `dividend`, `divisor`
- **Output**: `remainder`, `quotient`
- **Extension**: Modify to handle negative dividends.

## Understanding Check

Discuss why simpler comparator circuits like `LessThan` might not suffice in certain scenarios and explore modifications to meet specific constraints.

## Contributions

Feel free to fork this repository, submit issues, and provide pull requests to suggest improvements or additional exercises.