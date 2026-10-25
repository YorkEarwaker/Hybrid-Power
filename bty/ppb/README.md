# Portable power bank ppb

From chocolate bar size to mobile phone size to shoe box size to moving box size, stackable, backup power for personal devices to household. 

## Notes

Objectives
* Portable power bank for AGW project, what capacity Wattage T shirt S M L which use cases
* COTS components, breakout boards, MCU, ...
* Design and build own PCB, passives, actives, ...
* Integrate with a solar pv panel, high priority
* Integrate with H2 fuel cell, high priority
* Integrate with small wind turbine, high priority
* Integrate with small H2 turbine, medium priority
* Integrate with EVB as storage, medium priority, 
* Integrate with DDS system of systems see microgrid, large mg as sink, in home mg as storge

Out of scope
* Build a battery not in scope, another differnt project, 

Use Cases
* ...

## Status
TODO
* <todo: conider, what qaulifies as a hello world start minimum viable product PoC>
* <todo: consider, battery management system BMS >
* <todo: consider, moving some of the general battery kinds references elsewhere, top level? >

DONE
* <done: consider, intent to commit >

## BoM - bill of materials

* Heatshrink tubing, exposed terminal cover
* Kapton tape, exposed terminal cover
* Li ion, LiFePO4 batteries, 
* Al ion, ??? batteries, MOF? quasi solid state, graphite? tbd future state, <todo: consider, monitor progress of technology for Al ions>

## Output

Context diagram - circuit electron flow, battery ion flow
* charge, ions transfer electrons within the battery from anode to cathode through electrolyte to maintain charge balance
* work, electrons from the battery cathode travel through the external circit taking a longer path to complete the circuit with the battery anode, 
* energy, some of the energy may be lost to heat due to work
```
 electron flow through external wires in circuit, ion flow through internal electrolyte in battery
 <todo: consider, first use of LaTeX circuit diagram? >
```

## References

* Battery management system BMS, prevent over charging, over discharging, short circuits,  ...
* Boost converter, step up battery 3.7V to V for device
* Charging modeule, 
* Regarchable battery
* Regarchable battery kinds, lithium ion, other tbc

Battery - Lithium ion battery kinds, Li ion flow via electrolyte, products from sepecific manufactureres elsewhere
* <todo: consider, LiFePo4 product of choice, is there any better safety and longevity wise thatn LiFePO4 >
* Lithium ion battery 
* LiFePO4, [WP](https://en.wikipedia.org/wiki/Lithium_iron_phosphate_battery), Lithium Li Iron Fe Phosphate P O4 oxides, low cost, low toxicity, long life cycle, stable, safe, + 
* NMC, [WP](), Lithium Li Nickle Ni Magnesium Mn Cobolt Co O2 oxides
* NCA, [WP](https://en.wikipedia.org/wiki/Lithium_nickel_cobalt_aluminium_oxides), Lithium Li Nickle Ni Cobalt Co Aluminium Al O2 oxides
* LiCoO2 Lithium Li Cobalt Co O2 oxide
* ...

Battery - Aluminium ion battery kinds, Al ion flow via electrolyte
* Aluminium ion battery, [WP](https://en.wikipedia.org/wiki/Aluminium-ion_battery), low cost, low flamability, high capacity, more charge discharge cycles than Li ion batteries
* Aluminium air battery, oxygen reaction in atmosphere, 
* ...

Battery - Lead acid battery kinds
* Lead acid, flooded battery
* AGM, absorbant glass mat, kind of valve-regulated lead acid battery, non flooded battery, spill proof, highly resistant to vibration and shock, 
* VRLA, valve regulated lead acid battery, non flooded battery, start stop car vehicle battery, <todo: consider, vrla battery with H2 vehicles? >
* ...

Battery - other
* Lynden jar

Risks
* overcharging, thermal runaway

Metrics - energy density, per battery kind
* mAh/g, milliampere-hour, over gram, mass based gavimetric capacity
* mAh/ml, milliampere-hour, over millileter, volume based volumetric capacity
* ...

News Papers - how to
* How to Build a DIY Power Bank, [WS](https://www.logotech.com/blog/post/how-to-build-a-diy-power-bank), logotech
* How to Build a DIY Power Bank, [WS](https://cellsaviors.com/blog/diy-power-bank), cellaviors, 
* DIY Power Bank!, [WS](https://www.instructables.com/DIY-Power-Bank-2/), Instructables
* Homemade Power Bank: An Easy DIY Guide, [WS](https://www.ourpcb.com/homemade-power-bank.html), OurPCB
* Build Your Own Power Bank, [WS](https://circuitdigest.com/electronic-circuits/18650-battery-diy-power-bank), circuit digest
* How to Build a Portable Power Bank from Scratch, [WS](https://www.prasunbarua.com/2025/09/how-to-build-portable-power-bank-from.html) - this site looks interesting
* Build a Power Bank in $2 [WS](https://www.instructables.com/Build-a-Power-Bank-in-2/) Autodesk Instructables
* How To Make Your Own Portable Power Bank Using Common Components, [WS](https://commercialtoolry.com/home/how-to-make-your-own-portable-power-bank-using-common-components), CommercialToolry 
* How to Make Power Bank on Your Own Easily, [WS](https://www.instructables.com/How-to-Make-Power-Bank-on-Your-Own-Easily/), Autodesk Instructables
