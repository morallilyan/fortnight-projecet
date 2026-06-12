# Fortnight Project

An Agda project exploring formal verification and type theory.

## Overview

The Fortnight Project is a comprehensive Agda codebase dedicated to exploring the frontiers of formal verification, dependent types, and constructive mathematics. This project serves as both a research tool and a learning resource for those interested in type-theoretic foundations of computation.

## Features

- **Formal Verification**: Prove mathematical theorems and program correctness properties
- **Dependent Types**: Leverage Agda's powerful dependent type system for precise specifications
- **Type Safety**: Catch errors at compile time through advanced static analysis
- **Interactive Development**: Use Agda's interactive mode for iterative theorem proving
- **Standard Library Integration**: Build upon Agda's comprehensive standard library

## Project Structure

```
fortnight-project/
├── Main.agda              # Entry point and main module
├── fortnight-project.agda-lib  # Library configuration
├── README.md              # This file
├── .gitignore             # Git ignore rules
├── src/                   # Main source files
│   └── (source modules)
└── lib/                   # Library modules and utilities
    └── (library code)
```

## Requirements

- **Agda** 2.6.0 or higher
- **Haskell** and **Cabal** (for building Agda)
- **Emacs** or **VSCode** with Agda mode (recommended for development)

## Setup & Installation

### Install Agda

Using Cabal:
```bash
cabal update
cabal install Agda
```

For detailed instructions, see the [official Agda documentation](https://agda.readthedocs.io/en/v2.6.3/getting-started/installation.html).

### Install Agda Standard Library

```bash
git clone https://github.com/agda/agda-stdlib.git
cd agda-stdlib
cabal install
```

### Clone and Build This Project

```bash
git clone https://github.com/morallilyan/fortnight-projecet.git
cd fortnight-projecet
agda Main.agda
```

## Building & Compilation

### Type Check Files

To check an Agda file without compilation:
```bash
agda Main.agda
```

### Compile to Haskell

To compile Agda code to executable Haskell:
```bash
agda --compile Main.agda
```

The compiled output will be generated in the `MAlonzo/` directory (which is listed in `.gitignore` to keep the repository clean).

### Interactive Mode

For interactive development and theorem proving:
```bash
emacs Main.agda
```

Then use `C-c C-l` to load and type-check the file within Emacs.

## Usage

### Basic Example

The `Main.agda` module includes a simple example:

```agda
module Main where

open import Data.Nat
open import Data.List
open import Relation.Nullary

exampleFunction : ℕ → ℕ
exampleFunction n = n + 1

main : exampleFunction 5 ≡ 6
main = refl
```

To expand on this, create new modules in the `src/` or `lib/` directories and import them into Main.

## Development Workflow

1. **Create a new module** in `src/` or `lib/` directory
2. **Define theorems and functions** with type signatures
3. **Use interactive mode** (`C-c C-l` in Emacs) to develop proofs
4. **Type check** periodically with `agda filename.agda`
5. **Commit** changes when tests pass

## Common Commands

| Command | Purpose |
|---------|---------|
| `agda file.agda` | Type-check a file |
| `agda --compile file.agda` | Compile to Haskell executable |
| `C-c C-l` (Emacs) | Load and type-check current file |
| `C-c C-n` (Emacs) | Evaluate a term in normal form |
| `C-c C-d` (Emacs) | Show type of an expression |

## Resources

- [Agda Documentation](https://agda.readthedocs.io/)
- [Agda Standard Library](https://agda.github.io/agda-stdlib/)
- [Programming Language Foundations in Agda (PLFA)](https://plfa.github.io/)
- [Type Theory Resources](https://www.andres-loeh.de/LambdaPi/)

## Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Troubleshooting

### "Module not found" errors

- Ensure the Agda standard library is installed
- Check that library paths are configured in your `.agda/libraries` file

### Compilation fails

- Verify your Agda version: `agda --version`
- Ensure all dependencies are installed and accessible
- Try clearing cache: `rm -rf MAlonzo/` and retry

### Performance issues

- Large files may take time to type-check; this is normal
- Consider breaking code into smaller, independent modules
- Use incremental compilation where possible

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

morallilyan

## Acknowledgments

- The Agda community for excellent documentation and tools
- The developers of the Agda standard library
- Contributors and maintainers of related formal verification projects
