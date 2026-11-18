# AVR Interrupts · LED and Buzzer Demo

An ATmega2560 demonstration of external interrupts, GPIO outputs, and startup behavior. Two LEDs and a buzzer make each execution path visible.

![AVR interrupt demo](<Screenshot 2026-03-23 205834.png>)

[Watch the demo](<Screen Recording 2026-03-23 204832.mp4>)

| Event | Observable behavior |
| --- | --- |
| Normal operation | LED1 blinks while the main loop runs. |
| INT0 push button | The interrupt service routine turns on LED2 and activates the buzzer for about one second. |
| RESET push button | The MCU restarts and runs the LED and buzzer startup sequence. |

INT0 is a maskable external interrupt. RESET restarts execution through the reset vector.

## Verification in the demo

Observe the normal blink first. Trigger INT0 and watch for the brief LED and buzzer response, then press RESET to see the startup sequence repeat.

## Hardware and tools

ATmega2560 · Two LEDs · Buzzer · Two push buttons · Resistors · AVR-GCC · Proteus

**Author** · Vivek Chaudhary
