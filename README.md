# mcu-cpp

[![Build](https://github.com/yh-sb/mcu-cpp/actions/workflows/build.yml/badge.svg)](https://github.com/yh-sb/mcu-cpp/actions/workflows/build.yml)

One C++ project for different microcontrollers types

See [examples](examples/).

## How to build
```bash
git clone --recursive https://github.com/yh-sb/mcu-cpp.git
cd mcu-cpp

make
```
**Other targets:**
* `make flash` - Upload firmware to the target
* `make erase` - Erase all memory on the target
* `make reset` - Reset the target
* `make debug` - Start debug session

## Requirements
* [GNU Arm Embedded Toolchain](https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads)
* [CMake](https://github.com/Kitware/CMake/releases)
* [Make](https://github.com/maweil/MakeForWindows/releases)
* [Ninja](https://github.com/ninja-build/ninja/releases)
* [JLink](https://www.segger.com/downloads/jlink) for debug and uploading firmware to all ARM Cortex-M

  or just for STM32 only: **STM32CubeProgrammer** and **ST-LINK gdbserver** from [STM32CubeCLT](https://www.st.com/en/development-tools/stm32cubeclt.html?dl=redirect) package

## Requirements for ESP32 project
* [GNU Xtensa esp-elf toolchain](https://github.com/espressif/crosstool-NG/releases/tag/esp-13.2.0_20240530)
* [Python](https://www.python.org/downloads)
* Install python dependencies:
    ```sh
    python -m pip install --upgrade pip
    python third_party/esp-idf/tools/idf_tools.py install-python-env
    python -m pip install -r third_party/esp-idf/tools/requirements/requirements.core.txt
    ```
