# Minimal AVR ASM LDI Compiler & Tutorial 🚀
A lightweight, single-page web tool built to compile basic AVR Assembly (`LDI` instruction) directly into 16-bit machine code opcodes, featuring an interactive educational guide on hardware bitfields.


🌐 **Live Demo:**      https://costycnc.github.io/minimal-avr-asm-compiler-uploader


---## 💡 About the Project
This project demonstrates the core relationship between high-level code illusions and true hardware reality. While compilers often mask how a microcontroller processes instructions, this tool takes an Assembly statement and breaks it down to its raw binary and hexadecimal representation.

The concept and core compiler logic were developed entirely from scratch to show how an instruction word is constructed bit-by-bit inside an 8-bit AVR chip (like the ATmega328P on the Arduino Nano). 

*(Note: AI was utilized exclusively as a digital assistant to clean up UI/UX styling and handle English text translation).*
---## 🛠️ Key Features
* **Interactive LDI Compiler:** Input a target register (`R16` to `R31`) and a 2-digit hex value to instantly generate the real `E_ _ _` execution opcode.
* **Error Handling:** Built-in validation prevents illegal hardware assignments (e.g., attempting an `LDI` on registers lower than `R16`).* **Bitfield Educational Guide:** A visual breakdown showing how the CPU control unit parses the 16-bit instruction word during the **Fetch** and **Read** phases.
* **Opcode Architecture Examples:** Includes real microarchitecture comparisons featuring `LDI`, `ORI`, and `ADD` structural definitions.
---## 🔬 How the Hardware Logic Works
When an AVR CPU fetches a 16-bit instruction from Flash memory, it analyzes specific bitfields to drive its internal state machine:

1. **The Opcode Bits (15–12):** Bound to `1110` (Hex `E`). This fixed prefix signals the execution unit to configure hardware paths for a *Load Immediate* command.
2. **The Destination Register Bits (7–4):** The chip maps indexes `0000` to `1111` to trigger physical registers `R16` through `R31`.3. **The Operand Bits (11–8 and 3–0):** The 8-bit constant value is split into two separate 4-bit chunks wrapped tightly around the register address to maximize bit efficiency.
---## 🚀 Quick Start1. Clone or download this repository.
2. Open `index.html` in any standard web browser.3. Select your registers, compile, and see the architecture come to life!
---## 👤 Author* **CostyCNC** - https://github.com](https://github.com/costycnc


C'è qualche altra funzione o istruzione che ti piacerebbe aggiungere al compilatore prima di chiudere il cerchio?

