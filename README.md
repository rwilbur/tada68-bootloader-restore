# tada68-bootloader-restore
This is the fix that I used to repair a bricked Tada68 keyboard

# Usage
Download the files, connect the pins of your ISP to the keyboard, I used a USBasp clone so you can change the commands as you need. The first step is connect the ISP. ![Tada68](https://rileywilbur.com/projects/tada68.jpg "tada68") 

The next step will be to flash the hex file. To flash th Atmel chip with the ISP using a USBasp clone use this command:

```bash
avrdude -c usbasp-clone -p atmega32u4 -F -e -U flash:w:mass_bootloader_tada68.hex
```
Then disconnect the ISP and connect the keyboard via USB. Then put it in to mass storage mode and drag the .BIN file to the keyboard and press ESC. DO NOT PRESS EJECT ON YOUR COMPUTER. If you press eject you will need to reflash the keyboard again using the ISP.
