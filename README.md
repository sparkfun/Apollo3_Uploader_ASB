![generate executables](https://github.com/sparkfun/Apollo3_Uploader_ASB/workflows/generate%20executables/badge.svg)

# Apollo3 Uploader - Ambiq Secure Bootloader (ASB)


# Usage

* prerequisites
  * Python is installed on your computer
  * your program is compiled + linked to support the ASB (binary offset ```0xC000```)
* use the ASB loader script to upload to the board
  
  ```python asb.py [flags (all required)]```
  
  * ```--load-address-blob``` **load address**: 0x20000
  * ```--magic-num``` **magic**: 0xCB
  * ```--version``` **version**: 0x0
  * ```--load-address-wired``` **load address wired**: 0xC000
  * ```-i``` **i**: 6
  * ```--options``` **options**: 0x1
  * ```-b``` **baud rate**: 115200 or 921600 depending on your board (Artemis boards are 115200)
  * ```-v``` **verbose**: turn on verbose output
  * ```-o``` **intermediate file path**: where to place intermediate files
  * ```-port``` **serial port**: the serial port to connect over (*/dev/\** on \*nix or *COMX* on windows)
  * ```--bin``` **filepath**: path to the binary image of your program to upload
  
* easy copy/paste
  * ```--load-address-blob 0x20000 --magic-num 0xCB --version 0x0 --load-address-wired 0xC000 -i 6 --options 0x1 -v -o ./temp -port ${YOUR_PORT_HERE} --bin ${YOUR_BIN_HERE}```