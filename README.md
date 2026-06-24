#PS/2 Keyboard Driver for 32-bit x86 educational operating system. 



Features
IRQ1 keyboard interrupt handling
PIC remapping and EOI management
IDT integration
Lock-free ring buffer for scancode collection
Top-half and bottom-half processing model
Scancode-to-ASCII translation
Shift key support
VGA text console output
Architecture
Keyboard generates IRQ1.
Interrupt handler reads scancode from I/O port 0x60.
Scancode is pushed into a ring buffer.
Bottom-half processing translates scancodes into ASCII.
Characters are displayed through the VGA text driver.
Learning Goals

This project was built to understand:

x86 interrupt architecture
PS/2 keyboard protocols
Linux driver design concepts
Low-level systems programming
Operating system development

Inspired by studying the Linux i8042/AT keyboard driver architecture and reimplementing the core concepts in a simplified educational kernel.
