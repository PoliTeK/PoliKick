<h1 align="center">
	<br>
		<img src="images/PoliKick_Sfondo.png" width="200">
	<br>
		PoliKicK
	<br>
</h1>


<h4 align="center"> PoliKick is an analog Eurorack kick drum inspired by the legendary <a href="https://en.wikipedia.org/wiki/Roland_TR-808">TR-808</a>. Based on the [<a href="https://www.ericasynths.lv/shop/diy-kits-1/edu-diy-kick-drum/">EDU DIY Kick Drum</a> by  <a href="https://www.ericasynths.lv">Erica Synths</a>, it adds a selectable distortion stage and an extended note range.

---

<p align="center">
	<a href="#key-features">Key Features</a> •
	<a href="#list-of-components">List of Components</a> •
	<a href="#how-to-use">How To Use</a> •
	<a href="#credits">Credits</a> •
	<a href="#license">License</a>
</p>

## Key Features

- **Eurorack Standard:** Designed for standard +12V/-12V Eurorack power rails with a 10-pin power header.
- **Trigger and CV Control:** Accepts standard modular trigger pulses (5V-10V) and Control Voltage inputs for dynamic parameter modulation.
- **Authentic Circuitry:** Faithful reproduction of the original analog synthesis paths using modern, easily sourced equivalent components.
- **Expanded Sound Design:** Additional parameters exposed on the front panel compared to the original desktop unit.


# Project Component List

All the components listed below can be easily found and purchased on major electronic component distributors such as Mouser and DigiKey.

## Resistors

*All resistors are through-hole Metal Film (Part Number: `MFR-25FTF52`)*

| Resistor | Value |
| -------- | ----- |
| R1       | 470k  |
| R2       | 4.7k  |
| R3       | 47k   |
| R4       | 1M    |
| R5       | 100k  |
| R6       | 14k   |
| R7       | 33k   |
| R8       | 100k  |
| R9       | 100k  |
| R10      | 22k   |
| R11      | 120k  |
| R12      | 39k   |
| R13      | 100k  |
| R14      | 1k    |
| R15      | 1k    |
| R16      | 1k    |
| R17      | 18k   |
| R18      | 1M    |
| R19      | 100k  |
| R20      | 10k   |
| R21      | 2k    |
| R22      | 330   |
| R23      | 10    |
| R24      | 10    |

## Capacitors

| Capacitor | Value   | Part Number |
| --------- | ------- | ----------- |
| C1        | 15 nF   | `MMK5153K50`  |
| C2        | 15 nF   | `MMK5153K50`  |
| C3        | 10 nF   | `C430C106K3R` |
| C4        | 68 nF   | `C320C683J5R` |
| C5        | 5.6 nF  | `MMK5332K50`  |
| C6        | 220 nF  | `MMK5224J50`  |
| C7        | 47 µF   | `ESH476M050A` |
| C8        | 100 nF  | `K104K15X7RF` |
| C9        | 47 µF   | `ESH476M050A` |
| C10       | 100 nF  | `K104K15X7RF` |

## Diodes

| Diode   | Characteristics  | Part Number |
| ------- | ---------------- | ----------- |
| D1 - D7 | Small Signal     | `1N4148`      |
| D8 - D9 | Schottky Barrier | `1N5819`      |
| DS1     | Through Hole LED | `LTL-1CHYE`   |

## ICs and Transistors

| Component  | Characteristics       | Part Number |
| ---------- | --------------------- | ----------- |
| U1         | Quad Low-Noise OP Amp | `TL074IN`     |
| Q1, Q3, Q4 | NPN Transistor        | `BC548B`      |
| Q2, Q5     | PNP Transistor        | `BC558BTA`    |

## Potentiometers

| Designator | Name      | Value     | Part Number   |
| ---------- | --------- | --------- | ------------- |
| A1         | AmpDeca   | 50k, log  | `PTV09A-4025` |
| A2         | Distortior| 100k, log | `PTV09A-4025` |
| B1         | Pitch     | 100k      | `PTV09A-4025` |
| B2         | Tone      | 50k       | `PTV09A-4025` |
| B3         | TuneDeca  | 100k      | `PTV09A-4025` |
| B4         | TuneDept  | 10k       | `PTV09A-4025` |
| B5         | PitchAmo  | 100k      | `PTV09A-4025` |

## Connectors and Switches

| Component    | Description        | Part Number  |
| ------------ | ------------------ | ------------ |
| Connector    | Power Header       | `TSW-105-07-T` |
| IN1-Gate     | 3.5 mm Stereo Jack | `SJ3-35052B`   |
| IN2-AccentCV | 3.5 mm Stereo Jack | `SJ3-35052B`   |
| IN3-PitchCV  | 3.5 mm Stereo Jack | `SJ3-35052B`   |
| OUT1         | 3.5 mm Stereo Jack | `SJ3-35052B`   |
| SW1          | Toggle Switch      | `BI_INT`       |

## Mechanical Hardware

| Component | Description | Size / Value |
| --------- | ----------- | ------------ |
| Screws    | Machine Screws | M3 |
| Standoffs | Hex Standoffs / Spacers | M3 |

## How To Use

### Hardware Installation

To install the module in your Eurorack system:
1. Ensure your Eurorack case is completely powered off.
2. Connect the 10-pin end of the ribbon cable to the header on the module's PCB. Pay strict attention to the orientation: the **red stripe** on the cable must align with the **-** marking on the PCB.
3. Connect the 16-pin end of the cable to the bus board of your case (red stripe matching -12V).
4. Secure the module to the rails using M3 screws before powering on the case.

### LTspice Simulation

To simulate the analog behavior of the  circuitry, we used LTspice.

- Inside the `Simulation` folder, you will find the `PoliKick.asc` files containing the core voice circuits.
- The trigger inputs in the simulation are modeled using a `PULSE` voltage source configured to  mimick a standard sequencer trigger.
- Run the `.tran` command to observe the envelope generation and the audio output transient response. 
- You can adjust the `.step param` commands on the simulated potentiometers to test the range of the front panel controls.

## Credits

Circuit analysis and schematic references based on the [EDU DIY Kick Drum](https://www.ericasynths.lv/shop/diy-kits-1/edu-diy-kick-drum/) by Erica Synths, which originates from the classic Roland TR-808 service manual. 

## License

[MIT](https://choosealicense.com/licenses/mit/)

---

<p align="center">
	<a href="mailto:info.politek23@gmail.com">E-Mail</a> •
	<a href="https://www.instagram.com/politek_music">Instagram</a> •
	<a href="https://t.me/+dLKMAwzNmQYxNzM0">Telegram Community</a>
</p>
