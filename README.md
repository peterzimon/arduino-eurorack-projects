Arduino Eurorack projects
=========================

DIY Eurorack projects with Arduino and common C++ libraries.

> 🛒 *Some of these modules are for sale on **[Reverb](https://reverb.com/shop/joeseggiola)** and **[Tindie](https://www.tindie.com/stores/joeseggiola/)**!*

Modules
-------

Each module has its own detailed README file.

- [Clock divider](clock-divider/): clock divider in 4HP.
- [Forks](forks/): two Bernoulli gates, clone of Mutable Instruments Branches.
- [In CV](in-cv/): virtual ensemble that plays Terry Riley's "In C" on CV/gate outputs.
- [MIDI 4+1](midi4plus1/): polyphonic and monophonic MIDI to 4x CV/gate interface in 6HP.

Libraries and tools
-------------------

- [Button class](lib/Button.cpp): convenient reading methods, debouncing, combined single and long-press, internal pull-up usage.
- [Knob class](lib/Knob.cpp): analog value reading with low/high thresholds.
- [LED class](lib/Led.cpp): handles minimum duration to ensure visibility, implements blinking, toggle, flash.
- [MCP4728 class](lib/MCP4728.cpp): extends [Hideaki Tai's lib](https://github.com/hideakitai/MCP4728) to include DACs calibration and optional LDAC. Sketches for [setting I2C address (device ID)](tools/mcp4728_addr) and [guiding the calibration process](tools/mcp4728_calibration) are provided.
- [MM74HC595M class](lib/MM74HC595M.cpp): simple wrapper around `shiftOut()` to handle 74HC595 shift registers.

### Note about the library folder

There's a symbolic link to the `lib/` folder in every module folder. If the link doesn't work for you, you won't be able to compile: try to manually copy and paste the entire `lib/` folder from the root next to the sketch you are trying to compile. Unfortunately the Arduino compiler does not allow including source files from parent folders.

License
-------

Code: [GPL 3.0](LICENSE), hardware: [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).
