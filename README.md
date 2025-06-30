# learning_make_OS
# 🧵 My Custom OS from Scratch: Development Roadmap ✅

I'm building my own operating system with a simple GUI. This roadmap tracks all the essential phases, learning goals, implementation steps, and key resources.

---

## 📦 Phase 0: Toolchain and Emulator Setup

- [ ] Install GCC Cross-Compiler (`x86_64-elf-gcc`)
  - 📖 [OSDev: GCC Cross-Compiler](https://wiki.osdev.org/GCC_Cross-Compiler)
- [ ] Install QEMU for emulation
  - 📖 [QEMU OSDev Setup](https://wiki.osdev.org/QEMU)
- [ ] Install GDB (for debugging)
- [ ] Set up `make` and `nasm`/`ld` toolchain

---

## 🧭 Phase 1: Bootloader and Kernel Entry

### 🛠 Goals:
Get your kernel to boot and print something.

- [ ] Write a custom bootloader OR use GRUB multiboot
  - 📖 [GRUB Multiboot Specification](https://wiki.osdev.org/Multiboot)
  - 🎥 [Writing an OS from scratch - low-level bootloading (YouTube)](https://youtu.be/FN4Y8Zl5lH8)
- [ ] Create linker script (`linker.ld`)
- [ ] Set up 32-bit or 64-bit protected mode
- [ ] Print "Hello, World!" to screen using VGA text mode
  - 📖 [OSDev VGA](https://wiki.osdev.org/VGA_Text_Mode)

---

## 🧠 Phase 2: CPU and Memory Setup

### 🛠 Goals:
Enable protected mode, handle interrupts, and manage memory.

- [ ] Set up GDT (Global Descriptor Table)
  - 📖 [OSDev GDT](https://wiki.osdev.org/GDT)
- [ ] Set up IDT (Interrupt Descriptor Table)
  - 📖 [OSDev IDT](https://wiki.osdev.org/IDT)
- [ ] Enable IRQ handling (keyboard, timer)
- [ ] Set up a basic timer using PIT
  - 📖 [OSDev Timer](https://wiki.osdev.org/Programmable_Interval_Timer)
- [ ] Implement a basic memory manager (malloc/free)
  - 📖 [Writing a Memory Allocator](https://arjunsreedharan.org/post/148675821737/memory-allocation-strategies-in-operating-systems)

---

## 🧮 Phase 3: Paging and Virtual Memory

### 🛠 Goals:
Isolate memory and simulate modern memory layout.

- [ ] Enable paging
- [ ] Implement virtual to physical mapping
- [ ] Create page tables and switch pages
  - 📖 [OSDev Paging](https://wiki.osdev.org/Paging)
  - 🎥 [Paging Explained Simply - Jacob Sorber](https://youtu.be/3EkbYEDK12c)

---

## 🎛️ Phase 4: Drivers and Input Devices

### 🛠 Goals:
Interact with user through keyboard/mouse.

- [ ] Write PS/2 Keyboard driver
- [ ] Handle keyboard input (scancodes → ASCII)
  - 📖 [OSDev Keyboard](https://wiki.osdev.org/PS2_Keyboard)
- [ ] Implement mouse driver
  - 📖 [OSDev Mouse](https://wiki.osdev.org/Mouse_Input)

---

## 📁 Phase 5: Filesystem and Disk I/O

### 🛠 Goals:
Read files from disk using a real filesystem.

- [ ] Implement ATA PIO disk driver
  - 📖 [ATA PIO](https://wiki.osdev.org/ATA_PIO_Mode)
- [ ] Read sectors from disk
- [ ] Implement FAT12/FAT32 filesystem
  - 📖 [FAT File System](https://wiki.osdev.org/FAT)
- [ ] Read a file and print its contents

---

## 🧍 Phase 6: User Mode & Multitasking

### 🛠 Goals:
Run programs in user mode and switch between them.

- [ ] Switch to user mode (ring 3)
  - 📖 [User Mode](https://wiki.osdev.org/Entering_User_Mode)
- [ ] Add support for system calls
- [ ] Implement a simple scheduler (round robin)
  - 📖 [Context Switching](https://wiki.osdev.org/Context_Switching)

---

## 🖼️ Phase 7: Graphics Mode & Simple GUI

### 🛠 Goals:
Enable framebuffer graphics and build a GUI.

- [ ] Switch to VBE graphics mode (VGA/VESA)
  - 📖 [Setting VBE Mode](https://wiki.osdev.org/VBE)
- [ ] Draw pixels, rectangles, text (bitmap fonts)
- [ ] Implement a mouse cursor
- [ ] Design a minimal windowing system
- [ ] Create basic GUI apps: calculator, text viewer
  - 🎥 [Write a GUI for your OS - PonchoDev](https://youtu.be/itG2beCmgCk)

---

## 🖥️ Phase 8: Shell and Basic Applications

### 🛠 Goals:
Create a command-line interface and simple userland programs.

- [ ] Build a basic shell with command parsing
- [ ] Support launching built-in apps
- [ ] Implement simple text editor or file browser

---

## 💡 Phase 9: Advanced (Optional)

- [ ] Implement multitasking with paging isolation
- [ ] ELF loader for user applications
- [ ] Networking stack (TCP/IP)
- [ ] Port to ARM (e.g., Raspberry Pi)
  - 📖 [Raspberry Pi Bare Metal](https://github.com/bztsrc/raspi3-tutorial)

---

## 🛠 Tools Recap

- Emulator: `QEMU`
- Compiler: `x86_64-elf-gcc`
- Debugger: `GDB`
- Editor: `VS Code`, `CLion`, or `Vim`
- File image: `mtools`, `dd`

---

## 💬 Communities and References

- 💬 [https://forum.osdev.org](https://forum.osdev.org) – Ask questions
- 📚 [https://wiki.osdev.org](https://wiki.osdev.org) – Core documentation
- 🎥 YouTube channels: Jacob Sorber, Low Level Learning, PonchoDev

---

> ✅ Check each box once you complete the step.
> 🎯 Build iteratively: you don’t need everything perfect before moving on.

