# tada68-bootloader-restore
This is the fix that I used to repair a bricked Tada68 keyboard

# Usage
Download the files, connect the pins of your ISP to the keyboard, I used a USBasp clone so you can change the commands as you need. The first step is to flash the hex file and then disconnect the ISP and connect the keyboard via USB. Then put it in to mass storage mode and drag the .BIN file to the keyboard and press ESC. DO NOT PRESS EJECT ON YOUR COMPUTER. If you press eject you will need to reflash the keyboard again using the ISP.

# Commands
To flash th Atmel chip with the ISP using a USBasp clone use this command

avrdude -c usbasp-clone -p atmega32u4 -F -e -U flash:w:mass_bootloader_tada68.hex

You bootloader is now flashed and you just have to put the keyboard in to mass storage mode, drag the .bin file to your keyboard and press ESC! You now have a functioning keyboard again!
