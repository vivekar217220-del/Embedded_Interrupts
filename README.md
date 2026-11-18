# AVR Interrupts | ATmega2560 LED and Buzzer Demo

A Proteus demonstration of how an ATmega2560 responds to a button on its external interrupt input. Two LEDs and a buzzer make the startup routine, the main loop, and interrupt handling visible.

![Proteus circuit for the AVR interrupt demonstration](<Screenshot 2026-03-23 205834.png>)

[Watch the simulation recording](<Screen Recording 2026-03-23 204832.mp4>)

## What the circuit demonstrates

| Input or output | Role |
| --- | --- |
| ATmega2560 | Runs the startup code, main loop, and external interrupt service routine. |
| INT0 push button | Sends a request through the maskable external interrupt input. The project notes identify PD0 as the input. |
| RESET push button | Restarts execution through the reset vector. |
| LED1 | Blinks during normal operation to make progress through the main loop visible. |
| LED2 and buzzer | Provide visible and audible feedback during the INT0 event. |

## Execution flow

```text
Power-on or RESET ── Startup indication ── Main loop: LED1 blinks
                                             │
                                            INT0
                                             ▼
                                   ISR: LED2 and buzzer
                                             │
                                             └── Return to the main loop
```

### Startup and normal operation

At startup, the demo runs an LED and buzzer sequence. The application then enters its repeating LED1 blink loop. Pressing the reset button repeats initialization through the reset vector.

### External interrupt

When INT0 and global interrupts are enabled, a configured event on the INT0 pin causes the processor to enter its interrupt service routine (ISR). In this demonstration the ISR turns on LED2 and activates the buzzer for roughly one second. The main loop resumes when the handler completes.

An interrupt request uses the configured interrupt vector and can be masked. A reset restarts execution through the reset vector, so the visible startup sequence starts over.

## How to review the demonstration

1. Observe the startup indication, then look for the repeating LED1 blink.
2. Trigger INT0 during the normal blink. Check for LED2 and buzzer activity, then look for LED1 operation to resume.
3. Trigger RESET and compare the response with the initial power-on sequence.
4. Use the schematic screenshot to identify the two independent button inputs and the assigned outputs.

## Tools and project material

The documented setup uses the ATmega2560, two push buttons, two LEDs, resistors, and a buzzer in Proteus. The original notes list AVR-GCC as the toolchain for Embedded C. This repository provides the circuit screenshot and demonstration recording. A reproducible build would also require the source, the Proteus project, and the interrupt trigger configuration.

**Author** · Vivek Chaudhary
