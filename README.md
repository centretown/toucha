# toucha

---

PlatformIO setup for the Freenove Touch Screen (4") paint program.

---

## Setup

---

1.  Clone this repository.

```bash
git clone --depth=1 https://github.com/centretown/toucha.git
```

1.  Install [udev rules](https://docs.platformio.org/en/latest/core/installation/udev-rules.html)

1.  Install [platformio](https://docs.platformio.org/en/latest/core/installation/index.html)
    - Select [installer script](https://docs.platformio.org/en/latest/core/installation/methods/installer-script.html)
    - Select [Local Download (macOS / Linux / Windows)](https://docs.platformio.org/en/latest/core/installation/methods/installer-script.html#local-download-macos-linux-windows)

1.  Activate from the terminal

```bash
source activate
```

1.  Install the TFT_eSPI library

```bash
pio pkg install --library "bodmer/TFT_eSPI@^2.5.43"
```

1.  Copy and replace the existing setup selection file in the TFT_eSPI library directory.

```bash
cp TFT_eSPI_Setups/User_Setup_Select.h .pio/libdeps/ESP32-32E/TFT_eSPI
```

1.  Copy the setups folder to make it accessible from TFT_eSPI library.

```bash
cp -R TFT_eSPI_Setups  .pio/libdeps/ESP32-32E
```

1.  Compile

```bash
pio run
```

    If successful upload

```bash
pio run -t upload
```

1.  To Monitor

```bash
pio device monitor
```
