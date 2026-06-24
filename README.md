# x86-ps-2-keyboard-driver
A small PS/2 keyboard subsystem for a 32-bit x86 educational operating system.


Keyboard
   ↓
IRQ1
   ↓
IDT[33]
   ↓
irq_handler()
   ↓
keyboardirq()
   ↓
Ring Buffer
   ↓
keyboard_process()
   ↓
ASCII Translation
   ↓
VGA Driver
