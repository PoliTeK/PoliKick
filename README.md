# PoliKick
Circuit-level study of the [EDU DIY Kick Drum][Kick Drum] by [Erica Synths](https://www.ericasynths.lv), based off of the legendary [TR-808][TR-808].

[Kick Drum]: https://www.ericasynths.lv/shop/diy-kits-1/edu-diy-kick-drum/
[TR-808]: https://en.wikipedia.org/wiki/Roland_TR-808

## LTSpice simulation
This project uses [LTSpice][LTSpice] to simulate the kick drum. The simulation for each stage can be found under the `spice` directory.

Some simulations use external components, such as the TL072, which must be added manually to one of the folders where LTSpice looks up schematics and symbols.

[LTSPice]: https://www.analog.com/en/resources/design-tools-and-calculators/ltspice-simulator.html

## Documentation
The documentation for the kick is split between two documents, the Cookbook and the PoliKick, located under `docs/cookbook` and `docs/polikick` respectively.
The purpose of this separation is as follows:
- the PoliKick is meant to be a qualitative overview of the design with a brief explanation of the design choices that were made;
    its purpose is to quickly guide through the circuit and give a rough understanding of how everything plays together.

- the Cookbook provides a quantitative analysis for each block of the circuit taken by itself and lists the resulting formulas for quick use and future reference.

Both documents make use of some `circuitikz` files located in the `docs/circuits` folder.