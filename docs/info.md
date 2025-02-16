<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

A simple capacitive touch keyboard.

Basic idea:

1. The user can press eight capacitive buttons to play sounds on the keyboard.
1. The state of the buttons are stored in registers.
1. Each register is accessible via uart.
1. If a register is set via uart, it will only reset via uart OR a button press and release.
1. Based on which registers are set, a PWM signal will be sent to a buzzer.
1. An additional register allows the user to modify the debouncing period for the buttons. Default value is 50 ms.

## How to test

Run the clock at 50 MHz. The clock will be strobed internally to generate a 2.5 MHz clock for the tone playing, while 50 MHz will be used for PWM reference waveform.

## External hardware

List external hardware used in your project (e.g. PMOD, LED display, etc), if any
