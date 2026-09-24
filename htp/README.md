# Heat pump htp

See also
* Battery, bty
* Condenser cdr
* Micro grid mgd, use of DDS

## Notes

Objectives - primary
* COTS component build, shortest time to market, fast prototyping, understand domain, proven component parts, integration
* Greenfield component build, aka from scratch development, ground up development, recreating from first principles, learning by doing, interest 

Objectives - secondary
* Satellite spacecraft temperature regulating systems for use as air cooling systems on Earth. 
* Aerospace thermal engineering
* Data Distribution Services DDS, OMG, for internal component interoperability and componentization separatoin of concerns

## Status
TODO
* <todo: consider, sample pruduced by Brave search, confirm this it true, confirm these are best, >
* <todo: consider, which is best overall, as a component for all types of heat transfer, heat pump, >
* <todo: consider, which is best specifically for cooling water, >
* <todo: consider, which is best for refrigeration, >
* <todo: consider, if C02 how could these heat transfer units be part of C02 extraction from the atmosphere, as opposed to buring fossile fuels to make C02 for example, carbon dioxide removal cdr, direct air capture dac, >
* <todo: consider, LaTeX diagramming for; mechancial engineering, power eingineering, >
* <todo: consider, DDS OMG as internal componentization capability, that is plug and play component architecture, more expensive to start with but enable components to be replaced as standalone units, compressor as example, or controller unit, or controle panel, ...  >

DONE
* <done: consider, intent to commit>

## Bill of Materials BoM
First project to build your own heat pump byohp
* <todo: consider, which if any of the hardware component could be 3d printed, >
* <todo: consider, using c02 as a refigerant incrased cost  by x2 x3 due to hight pressure requirements, component BoM changes as a consequence, ponder on refrigerant more, >

Dependency
* electrical engineering tool set, helping hands, soldering iron, electric guage, mats of various kinds, 
* work room and work bench 

Estimated cost
* components; £800 to £2500
* efficiency; COP 3.0 to 4.0, for every 1 unit of electrical energy consumed produces 3-4 units of heat energy
* tools; separate tools BoM, vacuum pump, manifold guage set, leak detector, torque wrenches, flaring tool, brazing kit

Safety and legal codes
* refrigerants
* high voltage
* pressure risks, shields for testing, 
* permits
* ..

Hardware components
* Compressor, to ? heating load, rotoary or scroll kinds, 2 to 5 kw for single room, heart of system, 
* Heat exchangers, evaoporator coil - to capture heat from air outside, condensor coil - to release heat inside
* Reversing valve, to switch between heating and cooling modes
* Expansion device, to regulate refrigerant flow and pressure drop, thermal expansion valve TXV
* Refrigerant, 
* Controls and sensors, to manage temperature pressure and defrost cycles, microcontroller or single board computer, advanced HVAC? , 
* Fans and motors, to move air across coils, high energy EC fans, 

Design and Build
* OpenEnergyMonitor, to simulate performance and size components
* Sizing, to calculate heating load based on room size and insulation
* Coil fabrication, to create copper coils for evaporator and condensor, bend copper tubing into tight even coils, 
* Brazing, to create leak proof high pressure joints, oxy-acetylene brazing, use nitorgen purge to prevent internal oxidation, to join; compressor, coils, valve, expansion device
* Vacuum and leak testing, to remove all air and moisture with vacuum pump, down to or below <500 microns, pressurize with nitrogen, use leak detector to find any leaks, 
* Charging, fill system with refrigerant to specific weight, likely require certification UK/EU for handling certain refrigerants
* Electrical component and controls, to wire everything together, micro electronics and programming, safety cut-offs and defrost cycle, high pressure, over temperature ... 
* Commissioning, to measure and refine coefficient of performance COP, working system, 
* ..

Third party supliers of modular diy kits
* Open Ecology, heat pump, water heat pump

## Refrigerants

| Refrigerant | Type | GWP | ODP | Safety Class | Flammability |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **R-717 (Ammonia)** | Inorganic (Natural) | **0** | 0 | B2L | Mild |
| **R-744 (CO₂)** | Inorganic (Natural) | **1** | 0 | A1 | **None** |
| **R-1234yf** | HFO (Synthetic) | **<1** | 0 | A2L | Mild |
| **R-1234ze** | HFO (Synthetic) | **<1** | 0 | A2L | Mild |
| **R-290 (Propane)** | Hydrocarbon (Natural) | **3** | 0 | A3 | **High** |
| **R-32** | HFC (Synthetic) | **675** | 0 | A2L | Mild |

## References

Terms
* Heat pump, [WP](https://en.wikipedia.org/wiki/Heat_pump), electrical power source, mechanical heat pump, 
* Absorption heat pump. thermal power, air, geothermally heated water, steam solar heated water, natural gas burning, more complex, larger
* Borehole field, ground, 
* Heat transfer
* Heat pump and refrigeration cycle [WP](https://en.wikipedia.org/wiki/Heat_pump_and_refrigeration_cycle)
* Vapor Compression Refrigeration [WP](https://en.wikipedia.org/wiki/Heat_pump_and_refrigeration_cycle)
* Carrot Cycle, 
* Global Warming Potential GWP , refrigerants, lower the better, 
* Ozone Depletion Potential ODP, refrigerants, zero is better,
* POE, lubricants, refrigerants, 
* <todo: other kinds of thing to be sourced, >

Kinds
* air to air
* water to water
* ..

Papers - heat pumps
* Unlocking heat pump flexibility to deliver low-carbon heating and support the electricity grid [WS](https://www.imperial.ac.uk/grantham/publications/all-publications/unlocking-heat-pump-flexibility-to-deliver-low-carbon-heating-and-support-the-electricity-grid.php), August 2026, Hui Yan, Jacek Pawlack, Aruna Sivakumar, Stephen Agyeman, Han Wang, etal, Energy and Low-Carbon Futures, Mitigation, Resources and Pollution, Grantham Institute, Imperial, [DIO](https://doi.org/10.25560/131725)

Papers - refrigerants
* CO2 as a refrigerant for heating and cooling systems [PDF](https://assets.danfoss.com/documents/latest/356557/BE470937803806en-000101.pdf), Danfoss
