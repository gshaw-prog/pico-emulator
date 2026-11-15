# EDU PICO Simulator

A browser-based simulator for the Cytron EDU PICO V2 kit (Raspberry Pi Pico 2 W). Students write CircuitPython-style code and use the buttons, knob, buzzer and RGB LEDs without needing a board.

Made for the Year 8 **Pico Arcade** unit at British International School Phuket.

## What it simulates

| Part | Pin | Python |
|---|---|---|
| Button A (yellow) | `board.GP0` | `digitalio` (reads `False` when pressed) |
| Button B (blue) | `board.GP1` | `digitalio` (reads `False` when pressed) |
| Knob | `board.GP28` | `analogio.AnalogIn`, 0–65535 |
| Buzzer | `board.GP8` | `pwmio.PWMOut`, `simpleio.tone` |
| RGB LEDs × 5 (Grove 2) | `board.GP14` | `neopixel.NeoPixel` |
| Pico LED | `board.LED` | `digitalio` |

Supported modules: `board`, `digitalio`, `analogio`, `pwmio`, `neopixel`, `simpleio`, `rainbowio`, `time`, `random`, `math`.

## Features

- Code editor with Python highlighting and auto-indent
- Serial console, with CircuitPython-style error messages and plain-English hints
- Pico Arcade Lesson 1 starter code in the Examples menu
- A "Light show steps" record of each LED step and how long it lasted
- **Hand in** button: makes an evidence picture and text (name, success criteria, LED steps, code, output) for students to paste into Google Classroom

The OLED, sensors, servos, motors and microphone are not simulated. It runs a close copy of Python (Skulpt), not real CircuitPython, so very advanced Python features may behave differently.

## Hosting

The whole simulator is one self-contained file, `index.html`, with no build step and no outside downloads. Student code and names are saved only in the student's own browser.

## Third-party code

- [Skulpt](https://skulpt.org): Python in the browser (MIT licence)
- [CodeMirror 5](https://codemirror.net/5/): code editor (MIT licence)
