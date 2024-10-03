# PHOTON-WAND
Designed an LED display circuit using a 555 timer, 4-bit counter, 3-to-8 decoder, and LEDs. Created schematics and PCB layouts in Circuit Maker with integrated AAA battery holders and adjustable frequency. Powered by 4.5V from three AAA batteries. Focused on Gerber file generation and prototyping for design verification.

Working : 
The magic wand project operates by using a 555 timer as a clock source, creating a regular pulse (heartbeat) for the system. The frequency of this pulse is determined by two resistors (RA, RB) and a capacitor, but instead of fixed resistors, potentiometers are used to allow the frequency to be adjusted manually. This clock signal, running at a human-perceivable speed (around 10-50 Hz), is sent to a 4-bit counter.

The 4-bit counter counts from 0 to 15 in binary, cycling through these values continuously. The outputs from the counter represent binary values, which are used to create a sequence of signals that can be used to control LEDs. However, instead of simply lighting up the LEDs in binary, the goal is to create a "chasing" sequence, where the LEDs light up one at a time in a visually appealing pattern.

To achieve this, a 3-to-8 decoder (74HC138) is used. The counter's 4-bit output is reduced to 3 bits (QA, QB, QC) for input into the decoder, which converts these binary inputs into a single active output. The decoder is designed to have only one active output at a time, which is used to drive an LED. The LEDs are connected through current-limiting resistors to the decoder's active-low outputs. As the counter cycles through its values, the decoder selects different LEDs to turn on, creating the chasing effect.

The LEDs are powered by a simple battery pack (three AAA batteries providing 4.5V), with no voltage regulation, which powers the entire circuit.

In summary, the wand uses a 555 timer to generate clock pulses, a 4-bit counter to cycle through binary values, and a 3-to-8 decoder to light up LEDs in sequence, creating a visual "chasing" pattern.
