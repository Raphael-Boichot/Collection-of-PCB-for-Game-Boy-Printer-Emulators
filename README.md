# PCBs for various Game Boy Printer emulator projects
PCB designs can be edited with [EasyEDA Standard Edition](https://easyeda.com). Schematics follows the associated projects. All these boards must be used with a **GBC compatible link cable**. GBA only purple cables are not pinout compatible with the proposed socket. 

Eu citizens are advised to order PCBs at [JLCPCB](https://jlcpcb.com/) to avoid additional prohibitive taxes with customs (taxes paid at order). I've never had a quality problem with them, unlike other well-known manufacturers whose printed circuit boards were of fairly average quality, with the added bonus of a gift from customs.

## Game Boy Printer Emulator PCB for the Arduino Uno
Arduino Uno compatible PCB to connect cleanly different projects around the Game Boy Printer: 
- [The original Game Boy Printer Emulator](https://github.com/mofosyne/arduino-gameboy-printer-emulator)
- [The GBCamera Android Manager](https://github.com/Mraulio/GBCamera-Android-Manager)
- [The direct PC to Game Boy Printer interface](https://github.com/Raphael-Boichot/PC-to-Game-Boy-Printer-interface)
- [The Arduino SD Game Boy Printer](https://github.com/Raphael-Boichot/The-Arduino-SD-Game-Boy-Printer)
- [The Game Boy Printer paper simulator](https://github.com/Raphael-Boichot/GameboyPrinterPaperSimulation)

![](PCB_Arduino_Uno/PCB.png)

**Parts needed:** 
- An [Arduino Uno](https://fr.aliexpress.com/item/1005006088733150.html), the cheaper the better;
- A [generic microSD shield](https://fr.aliexpress.com/item/1005006059963950.html) if needed, check the pinout to match with PCB;
- Some [GBA/GBC link plugs](https://fr.aliexpress.com/item/1005006358075502.html). Spare GBA link plugs are common while GB/GBC ones are impossible to source, both are pinout compatible for this application;
- Some [male pin headers](https://fr.aliexpress.com/item/1005006104110168.html). The clearance with the Arduino Uno shield is tight, but by triming pins below the PCB regular 11 mm pin headers are OK;
- The [custom PCB](/PCB_Arduino_Uno), any thickness, any finish, any color. Order at [JLCPCB](https://jlcpcb.com/);
- A [regular 5 mm LEDs](https://fr.aliexpress.com/item/32848810276.html) and a [through hole resistor](https://fr.aliexpress.com/item/32866216363.html) of about 220 Ohms (low value = high brighness).

### For Game Boy Printer emulator and and PC to printer direct interface, without SD shield adapter
![](/PCB_Arduino_Uno/Arduino_shield.jpg)

### For SD printer, with micro SD shield adapter
![](/PCB_Arduino_Uno/Arduino_Shield_with_SD.jpg)

If you use [SD card based project](https://github.com/Raphael-Boichot/The-Arduino-SD-Game-Boy-Printer), LED will flash when SD card is accessed as it is connected to CLK. For non SD based projects, just left the SD stuff unpopulated. The "Analog in" rows of pins can also be let without pin header if you want to spare some, it is never used here. The Arduino Uno is overall the most reliable device for playing with the Game Boy/Game Boy Printer.

## Game Boy Printer Emulator PCB for the Arduino Nano
Arduino Nano compatible PCB to connect cleanly different projects around the Game Boy Printer: 
- [The original Game Boy Printer Emulator](https://github.com/mofosyne/arduino-gameboy-printer-emulator)
- [The GBCamera Android Manager](https://github.com/Mraulio/GBCamera-Android-Manager)
- [The direct PC to Game Boy Printer interface](https://github.com/Raphael-Boichot/PC-to-Game-Boy-Printer-interface)
- [The Game Boy Printer paper simulator](https://github.com/Raphael-Boichot/GameboyPrinterPaperSimulation)

I must admit that the Arduino Nano is particularly fancy as Game Boy Printer emulator device (cute and flashy as I like).

![](PCB_Arduino_Nano/PCB.png)

**Parts needed:** 
- An [Arduino Nano](https://fr.aliexpress.com/item/1005006053215107.html), the cheaper the better;
- Some [GBA/GBC link plugs](https://fr.aliexpress.com/item/1005006358075502.html). Spare GBA link plugs are common while GB/GBC ones are impossible to source, both are pinout compatible for this application;
- Some [regular male pin headers](https://fr.aliexpress.com/item/1005002577212594.html). Must be soldered below the PCB as the clearance with the Uno shield is tight;
- The [custom PCB](/PCB_Arduino_Nano), any thickness, any finish, any color. Order at [JLCPCB](https://jlcpcb.com/);
- A [regular 5 mm LEDs](https://fr.aliexpress.com/item/32848810276.html) and a [through hole resistor](https://fr.aliexpress.com/item/32866216363.html) of about 220 Ohms (low value = high brighness).

![](PCB_Arduino_Nano/Nano_shield.jpg)

## Game Boy Printer Emulator PCB for the Waveshare RP2040 Zero
RP2040 compatible PCB to connect cleanly:
- [the Pico GB Printer](https://github.com/untoxa/pico-gb-printer) 

![](PCB_RP2040_Zero/PCB.png)

**Parts needed:** 
- An [RP2040 Zero](https://fr.aliexpress.com/item/1005003504006451.html), **with pin header** (or add some);
- Some [GBA/GBC link plugs](https://fr.aliexpress.com/item/1005006358075502.html). Spare GBA link plugs are common while GB/GBC ones are impossible to source, both are pinout compatible for this application;
- A [4 gates bidirectionnal level shifters](https://fr.aliexpress.com/item/1005004560297038.html). Any similar one in another seller will do the job.
- The [custom PCB](/PCB_RP2040_Zero), any thickness, any finish, any color. Order at [JLCPCB](https://jlcpcb.com/);
- A [regular 5 mm LEDs](https://fr.aliexpress.com/item/32848810276.html) and a [through hole resistor](https://fr.aliexpress.com/item/32866216363.html) of about 100 Ohms (low value = high brighness).
- A [6x6 push button](https://fr.aliexpress.com/item/1005003938244847.html)  whatever height, that can be harvested on any dead electronic suff so it is common.

For full support with the **pico-gb-printer**, you have to recompile the code to activate the external LED and the "paper tearing" functions. LED is indeed routed by default to GPIO25 which is the internal one (if any...) and "paper tearing" is routed by default to GPIO23 which is not reachable on a regular board. The device works anyway with the default build, tearing paper button and LED are just optional (and installing the Pico SDK was a real hassle on my side).

![](/PCB_RP2040_Zero/Pi_Zero_shield.jpg)

**Sidenote:**
This board id also partly compatible with the Arduino based projects if you compile them with the [Earle Philhower RP2040 core](https://github.com/earlephilhower/arduino-pico) installed on Arduino IDE. Just route LED to pin D8 instead of D13 and GBP_SO_PIN to D0 instead of D4. However, the serial output format is not exactly the same (not sure why) and the code needs a bit of rewrite to be directly compatible with the various image decoders. On the other hand, driving the printer with it seems working after a quick trial on my side. Anyway, I won't make any further try but it looks possible to use this board with other Game Boy Printer emulators.
