# XGLCD-LVGL Library for RA8875

This library is designed to use a RA8875 LCD module with <a href="http://www.littlevgl.com" target="_blank"> LittleVGL </a>, especially using an ESP32 as MCU (but it will also works with MKR family - Pycom family - Particle family - Adafruit Feather - plain old Arduino).

It's not a full RA8875 library but a light weight version dedicated to LittleVGL (You need to install <a href="https://github.com/littlevgl/" target="_blank"> LittleVGL </a> to use this library).

XGLCD-LVGL can drive 5.0", 7.0" and 9.0" 800x480 TFT LCD with capacitive touchscreen controlled by either FT5206 or GSL1680, so you need the <a href="https://github.com/sumotoy/FT5206" target="_blank">FT5206 library from Sumotoy</a> or <a href="https://github.com/Skallwar/GSL1680">GSL1680 for Arduino from Skallwar</a> depending on your display. The code for resistive touchscreen directly managed by the RA8875 is commented but available). Make sure you select your touchscreen driver in XGLCD.h.

XGLCD-LVGL is based on <a href="https://github.com/xgraph/XGLCD" target="_blank">XGLCD from XGraph</a> witch is based on <a href="https://github.com/sumotoy/RA8875" target="_blank">RA8875 from Sumotoy</a>.

Power supply consideration : RA8875 usually control large displays witch needs lot of current, USB will not provide enough energy to feed an ESP32, the LCD and the touch panel, please use an external power supply to avoid weird behaviors.

Wiring consideration : The code provided for esp32 works with DOIT ESP32 DEVKIT V1 and the Adafruit Feather Huzzah ESP32, if you want to use another board edit XGLCD.h and modify the defines to use the right pins for the SPI port you want to use.

Licence GNU GPL v3.0.

