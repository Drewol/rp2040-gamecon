# RP2040 Game Controller
Modified tinyusb HID example to make the Raspberry Pi Pico appear as an USB HID Gamepad.

## Build instructions
Insturctions based on Ubuntu 20.04.1 LTS tested under WSL2

1. Install CMake (at least version 3.13), and GCC cross compiler
```
sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi
```

2. Download the pico-sdk and set the `PICO_SDK_PATH` environment variable. Also set the variable in your `.bashrc` for future use.
```
git clone https://github.com/raspberrypi/pico-sdk
cd pico-sdk
git submodule update --init
export PICO_SDK_PATH=$PWD
cd ..
```

3. Clone and build this repository
```
git clone https://github.com/Drewol/rp2040-gamecon
cd rp2040-gamecon
mkdir build
cd build
cmake ..
make
```

4. Upload the `gamecon.uf2` that was created in your build directory.