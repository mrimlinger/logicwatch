# Logicwatch

Course: EPFL - EE110 - Logic systems (autumn semester 2017/2018)

Project: a digital multifunction watch implemented using only logic gates

## Physical constraints

- Two push buttons A and B
- Six seven-segment displays (SSDs)
- Ten LEDs
- One power-on-reset button
- One clock (2KHz crystal oscillator)

The project is meant to run on a Terasic DE10-Lite FPGA board.

## Features

The watch has five distinct operation modes (time, stopwatch, alarm, time setting, countdown). The user can switch between the modes by pressing A and B simultaneously for a longer period of time. The first five LEDs (n°0-4) indicate which mode is currently active.

### Mode 1 - Time

Time is kept with the format {month - day of the week - date - hours - minutes - seconds}. Pressing on A allows to change from the display of {month - day of the week - date} to {hours - minutes - seconds} and vice-versa. Pressing on B changes the time format from european to american and vice-versa.

### Mode 2 - Stopwatch

Pressing on B resume/pause the chronometer. Pressing on A while the chronometer is paused will reset it at zero. Pressing A while the chronometer is working will do nothing.

### Mode 3 - Alarm

The SSD of the field being modified blinks
When the alarm "sounds", a special LED animation is triggered. To stop it, any button can be pressed.

### Mode 4 - Time setting

### Mode 5 - Countdown

## Notable technical solutions

- Various finite state machines
- Switch debouncing system
- Simultaneous button press detector
- (...)

## How to use it

Launch `logisim-evolution-2.13.19.jar` and from there open `MAIN.circ`. Then you can start the simulation. Depending on your computer performance and the settings of the simulation, time will most likely not be accurate. It can however be calibrated by modifying certain logic circuits.


