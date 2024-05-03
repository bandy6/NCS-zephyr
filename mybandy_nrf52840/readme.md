Create your board directory

1.You need to give your board a unique name. Run ***west boards*** for  a list of names that are laready taken, and pick something new. Let's say your board is called ***plank***.

2.start by creating the board directory  ***zephyr/boards/<ARCH>/plank*** ,where `<ARCH>` is your SoC’s architecture subdirectory. 

3.Your board directory should look like this:

```
boards/<ARCH>/plank
├── board.cmake
├── CMakeLists.txt
├── doc
│   ├── plank.png
│   └── index.rst
├── Kconfig.board
├── Kconfig.defconfig
├── plank_defconfig
├── plank.dts
└── plank.yaml
```

1. `plank.dts`: a hardware description in [devicetree](https://docs.zephyrproject.org/2.7.0/guides/dts/index.html#dt-guide) format. This declares your SoC, connectors, and any other hardware components such as LEDs, buttons, sensors, or communication peripherals (USB, BLE controller, etc).
2. `Kconfig.board`, `Kconfig.defconfig`, `plank_defconfig`: software configuration in [Configuration System (Kconfig)](https://docs.zephyrproject.org/2.7.0/guides/build/index.html#kconfig) formats. This provides default settings for software features and peripheral drivers.

- `board.cmake`: used for [Flash and debug support](https://docs.zephyrproject.org/2.7.0/guides/porting/board_porting.html#flash-and-debug-support)
- `CMakeLists.txt`: if you need to add additional source files to your build

- `plank.yaml`: a YAML file with miscellaneous metadata used by the [Test Runner (Twister)](https://docs.zephyrproject.org/2.7.0/guides/test/twister.html#twister-script).