# Embedded_Interrupts
AVR Interrupt-Based LED &amp; Buzzer Control using ATmega2560 — Demonstrates maskable interrupt (INT0) and Non-maskable Interrupt , startup behavior, and real-time hardware interaction with LEDs and buzzer.

## 🚀 Features
- 🔄 Startup sequence triggered by RESET (Non-Maskable Interrupt concept)
- ⚡ External interrupt handling using INT0 (Maskable Interrupt)
- 💡 LED indication for different system states
- 🔊 Buzzer alert during interrupt handling
- 🔁 Continuous LED blinking during normal operation

## 🧠 Concepts Covered
- Maskable Interrupts (INT0)
- Non-Maskable Interrupt (Reset behavior)
- Interrupt Service Routine (ISR)
- Embedded C for AVR Microcontrollers
- GPIO configuration and control

## 🔌 Hardware Used
- ATmega2560 Microcontroller
- LEDs (2x)
- Buzzer
- Push Button (INT0)
- Reset Push Button (for Non-Maskable behavior)
- Resistors

## ⚙️ Working
### 🔹 Non-Maskable Interrupt (RESET)
- When the reset button is pressed:
  - MCU restarts immediately
  - Startup sequence runs (LEDs + buzzer blink)
  - Cannot be disabled (Non-Maskable behavior)

### 🔹 Maskable Interrupt (INT0)
- When INT0 button is pressed:
  - Interrupt is triggered (can be enabled/disabled)
  - LED2 turns ON
  - Buzzer activates for 1 second
  - System resumes normal operation

### 🔹 Normal Operation
- LED1 continuously blinks indicating system is running

## 🛠️ Tools & Environment
- AVR-GCC Compiler
- Atmel Studio / Microchip Studio / VS Code
- Proteus (for simulation)

## 📷 Applications
- Learning interrupt systems in embedded programming
- Understanding real-time hardware interaction
- Academic projects and demonstrations

## Simple Definations :-
- There are Two types of the Interrupts one is Maskable and another is the Non - Maskable.
- Maskable Interrupt :- Means those interrupt which are Ignored for Such time Being by the Programmer like we Do here we use the spst Push button at PD0 and Learned Functionality of the Maskable Interrupt.
- Non - Maskable Interrupt :- Means those type of the Interrupts which is not ignored and must be Passed in the CPU. and we Learn this one using the Reset Functionality.

## 📌 Author
Vivek Chaudhary 


