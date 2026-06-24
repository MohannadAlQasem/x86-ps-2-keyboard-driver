# PS/2 Keyboard Driver for x86 Educational OS

A PS/2 keyboard driver written in C for a 32-bit x86 educational operating system.

## Features

- IRQ1 keyboard interrupt handling
- PIC remapping and EOI management
- IDT integration
- Lock-free ring buffer for scancode collection
- Top-half and bottom-half processing model
- Scancode-to-ASCII translation
- Shift key support
- VGA text console output

## Architecture

1. Keyboard generates IRQ1.
2. Interrupt handler reads scancode from I/O port `0x60`.
3. Scancode is pushed into a ring buffer.
4. Bottom-half processing translates scancodes into ASCII.
5. Characters are displayed through the VGA text driver.

## Learning Goals

This project was built to understand:

- x86 interrupt architecture
- PS/2 keyboard protocols
- Linux driver design concepts
- Low-level systems programming
- Operating system development

## Inspiration

Inspired by studying the Linux i8042/AT keyboard driver architecture and reimplementing the core concepts in a simplified educational kernel.
