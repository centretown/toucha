# toucha
## freenove touch screen paint program from example scripts

### Setup
1. Install [udev rules](https://docs.platformio.org/en/latest/core/installation/udev-rules.html)

1. Install [platformio](https://docs.platformio.org/en/latest/core/installation/index.html)
  
    - Select [installer script](https://docs.platformio.org/en/latest/core/installation/methods/installer-script.html)
  
    - Select [Local Download (macOS / Linux / Windows)](https://docs.platformio.org/en/latest/core/installation/methods/installer-script.html#local-download-macos-linux-windows)

2. Activate from the terminal

      `source activate`

3. Compile first attempt to load TFT_eSPI library
      
      pio run

4. Copy the file TFT_eSPI_Setups/User_Setup_Select.h => .pio/libdeps/ESP32-32E/TFT_eSPI and replace the existing file.

5. Copy the folder TFT_eSPI_Setups => .pio/libdeps/ESP32-32E as this will now be referenced from the TFT_eSPI build.

6. Re-compile and upload
  
    pio run -t upload

7. To Monitor
    
    pio device monitor
