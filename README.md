# Various PCB for playinh with Game Boy Printer emulators !

## Game Boy Printer Emulator PCB for the Arduino
Arduino Uno compatible PCB to connect cleanly different projects around the Game Boy Printer using serial cable: 
- [The original Game Boy Printer Emulator](https://github.com/mofosyne/arduino-gameboy-printer-emulator)
- [The GBCamera Android Manager](https://github.com/Mraulio/GBCamera-Android-Manager)
- [The direct PC to Game Boy Printer interface](https://github.com/Raphael-Boichot/PC-to-Game-Boy-Printer-interface)
- [The Arduino SD Game Boy Printer](https://github.com/Raphael-Boichot/The-Arduino-SD-Game-Boy-Printer)
- [The Game Boy Printer paper simulator](https://github.com/Raphael-Boichot/GameboyPrinterPaperSimulation)

![](PCB%20for%20Arduino/PCB.png)

**Parts needed:** 
- An [Arduino Uno](https://fr.aliexpress.com/item/1005006088733150.html), the cheaper the better;
- A [generic microSD shield](https://fr.aliexpress.com/item/1005006059963950.html), check the pinout to match with PCB;
- Some [GBA/GBC link plugs](https://fr.aliexpress.com/item/1005006358075502.html). Spare GBA link plugs are common while GB/GBC ones are impossible to source, both are pinout compatible for this application;
- Some [regular male pin headers](https://fr.aliexpress.com/item/1005002577212594.html). Must be soldered below the PCB as the clearance with the Uno shield is tight;
- The custom PCB, any thickness, any finish, any color. Order at [JLCPCB](https://jlcpcb.com/), it's cheap and custom clean for Eu citizens contrary to PCBWay or OSHPark;
- A [regular 5 mm LEDs](https://fr.aliexpress.com/item/32848810276.html) and a [through hole resistor](https://fr.aliexpress.com/item/32866216363.html) of about 220 Ohms (low value = high brighness).

If you use [the project with the SD card](https://github.com/Raphael-Boichot/The-Arduino-SD-Game-Boy-Printer), LED will flash when SD card is accessed as it is connected to CLK. It must be used with a **GBC compatible link cable**. GBA only purple cables are not pinout compatible with the proposed socket. The "Analog in" rows of pins can be let without pin header, it is never used here.

## Game Boy Printer Emulator PCB for the RP2040 Zero
RP2040 compatible PCB to connec cleanly this project to the Game Boy Printer serial cable:
- [The Pico GB Printer](https://github.com/untoxa/pico-gb-printer)

![](PCB%20for%20RP2040%20Zero/PCB.png)

**Parts needed:** 
- An [RP2040 Zero](https://fr.aliexpress.com/item/1005003504006451.html), with header;
- Some [GBA/GBC link plugs](https://fr.aliexpress.com/item/1005006358075502.html). Spare GBA link plugs are common while GB/GBC ones are impossible to source, both are pinout compatible for this application;
- The custom PCB, any thickness, any finish, any color. Order at [JLCPCB](https://jlcpcb.com/), it's cheap and custom clean for Eu citizens contrary to PCBWay or OSHPark;
- A [regular 5 mm LEDs](https://fr.aliexpress.com/item/32848810276.html) and a [through hole resistor](https://fr.aliexpress.com/item/32866216363.html) of about 100 Ohms (low value = high brighness).
