<div align="center">

# Roz — Terminal Logic Gate Simulator for Windows and Linux

**Learn and experiment with AND, OR, NOT, NAND, NOR, XOR and XNOR gates in a simple, programming-language-like terminal.**

[![Platform: Windows and Linux](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-blue.svg)](https://github.com/Thirtexe/Roz/releases)
[![License: PolyForm Noncommercial 1.0.0](https://img.shields.io/badge/License-PolyForm%20Noncommercial-blue.svg)](LICENSE)

English | [فارسی](README.fa.md)

</div>

---

## What is Roz?

Roz is a free logic gate simulator that runs in a terminal. You type gate expressions such as `AND(1, 1)`, nest gates inside each other, and run the lines to see the result. It is built for students, hobbyists and anyone who wants to understand how digital logic works without wiring a real circuit.

Roz runs on Windows (64-bit) and Linux (64-bit) and works like a small programming language: every line starts with a gate name, and gates can be combined to build larger expressions.

## What are logic gates?

Logic gates are the basic building blocks of electronic circuits. They take inputs of `0` and `1` and produce an output according to a fixed rule, which is how a circuit decides whether current flows (think of a smart water valve).

## Features

- **Built-in editor:** write and edit multi-line gate code without leaving the terminal.
- **Syntax highlighting:** gate names and keywords are colored so your code is easier to read.
- **File operations:** open and save your code as files.
- **Quick exit:** close Roz quickly when you are done.
- **Variables:** store a value under a name and reuse it in later lines.
- **Undo and redo:** reverse or reapply your recent edits.

## Installation

Download the file for your operating system from the [Releases page](https://github.com/Thirtexe/Roz/releases):

| OS | File |
|----|------|
| Windows (64-bit) | `Roz-Full.exe` |
| Linux (64-bit) | `Roz-Full.AppImage` |

### Windows

Right-click the downloaded `Roz-Full.exe` and run it. Roz opens a terminal window where you can enter commands.

### Linux

Make the file executable, then run it from a terminal opened in the file's folder:

```bash
chmod +x Roz-Full.AppImage
./Roz-Full.AppImage
```

## Quick start

1. Start Roz.
2. Type `help` to list every command.
3. Type one line of code per row and press Enter to move to the next line.
4. Run all the lines together when you are ready.

```text
LOG(AND(1, 1))
LOG(XOR(1, 0))
LOG(NOT(0))
```

## Syntax

Every line must start with one of these gates:

`AND` | `OR` | `NOT` | `NAND` | `NOR` | `XOR` | `XNOR` | `LOG`

Each gate takes exactly as many inputs as its real-world counterpart, separated by commas.

- Too many inputs: the gate uses only the number it needs.
- Too few inputs: Roz shows an error.

```text
AND(1, 1)  ✅ Correct
AND(1)     ❌ Incorrect
```

The result of one gate can be used as an input to another:

```text
AND(AND(1, 1), 0)
```

Every input must be `1` or `0`. Any number greater than `1` is always read as `1`.

### The `LOG` command

`LOG` is specific to Roz and has no real-world equivalent. It takes one input and prints it in the terminal. Without `LOG`, the calculation still runs but nothing is displayed.

## Logic gate reference

| Gate | Inputs | Output is 1 when… |
|------|--------|-------------------|
| `AND` | 2 | both inputs are 1 |
| `OR` | 2 | at least one input is 1 |
| `NOT` | 1 | the input is 0 (it outputs the opposite) |
| `NAND` | 2 | at least one input is 0 (the opposite of AND) |
| `NOR` | 2 | both inputs are 0 (the opposite of OR) |
| `XOR` | 2 | the inputs are different |
| `XNOR` | 2 | the inputs are equal |

### Truth table

| A | B | AND | OR | NAND | NOR | XOR | XNOR |
|---|---|-----|----|------|-----|-----|------|
| 0 | 0 | 0 | 0 | 1 | 1 | 0 | 1 |
| 0 | 1 | 0 | 1 | 1 | 0 | 1 | 0 |
| 1 | 0 | 0 | 1 | 1 | 0 | 1 | 0 |
| 1 | 1 | 1 | 1 | 0 | 0 | 0 | 1 |

`NOT` takes a single input: `NOT(0)` is `1` and `NOT(1)` is `0`.

## FAQ

**What is Roz?**
A terminal-based simulator for working with logic gates, designed so that a regular user can learn how gates behave without any hardware.

**Which operating systems does Roz support?**
Windows (64-bit) and Linux (64-bit).

**Which gates are supported?**
AND, OR, NOT, NAND, NOR, XOR and XNOR, plus the Roz-specific `LOG` command for printing a value.

**Can I nest gates?**
Yes. Any input can be the result of another gate, for example `AND(AND(1, 1), 0)`.

**Why do I see an error when I use a gate?**
The most common cause is giving a gate fewer inputs than it needs, such as `AND(1)`.

**Why is nothing printed when I run my code?**
Roz only displays a result when you pass it to `LOG`.

**What license does Roz use?**
[PolyForm Noncommercial 1.0.0](LICENSE).

## Contact

[![GitHub](https://img.shields.io/badge/GitHub-Thirtexe-black?style=flat-square&logo=github)](https://github.com/Thirtexe)
[![Telegram](https://img.shields.io/badge/Telegram-Thirtexe-blue?style=flat-square&logo=telegram)](https://t.me/Thirtexe)
[![Email](https://img.shields.io/badge/Email-Thirtexe@gmail.com-red?style=flat-square&logo=gmail)](mailto:Thirtexe@gmail.com)
[![Telegram Community](https://img.shields.io/badge/Telegram-@DotChatc-yellow?style=flat-square&logo=telegram)](https://t.me/DotChatc)
