# Arduino AVR Boards

This repository contains modified source code and configuration files of the Arduino AVR Boards 
[platform](https://arduino.github.io/arduino-cli/latest/platform-specification/). The original can be found [here](https://github.com/arduino/ArduinoCore-avr).

This repo was modified to allow for precompiling the core library for several platforms.
For this, some autotools files and one header were added.

## Instructions
I assume that GCC targeting avr is already installed. In that case, make sure 
that `avr-gcc` is in your `PATH` and then do the normal
```sh
./configure --prefix=$PREFIX
make
make install
```
You'll want to set `PREFIX` to wherever `avr-gcc` is installed.