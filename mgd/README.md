# Micro grid mgd

Small power grid, mobile, system of system

## Notes

Objectives
* How to use for AGW project
* Extreme weather event emergency management response and recovery
* Climate refugee camps
* Distributed federated power supply systems
* National Disaster Management Agency, mobile power capability, 
* National resillence and civil preparednes, NATO Article III
* Interoperability with NATO equipment for micro grids, this will be getting rough global heating wise and all the interoperability possible will be required
* Home Grid, Building Grid, Community Grid, Local Grid, add new Storage, Source, Controller, Load, ... hospitals, 

Use cases - currently require protocol gateway for mixed environments, of TMS and IEEE/IEC, however any genset, battery, inverter can be made TMS compliant by addding a gateway, with modifying the OEM's internal firmware, i.e. drop in tmsi module concept
* TMS, tactical microgrid system, mobile, islanded, tactical, military, potentially for emergency services in extreme civilian grid failure scenario likely nato articel iii related, which might be extreme weather global heating scenario
* IEEE/IEC, fixed, grid interconnected, commercial/industrial, civilian, requires a TMS interface module, and likely assimilation into TMS network for the durration, 

## Status
TODO
* <todo: consider, first cut resources available, >
* <todo: consider, similar micro grid solutions to us-army mil std 3071, system of systems, plug and play, what is the au ca de fr jp kr nz uk etal  equivalent? is this the defacto of dejure NATO standard, >
* <todo: consider, determine when test tool set for mil std 3071 to be open sourced? eta?,  >
* <todo: consider, how best to interoperate with renewably energy sources, solar, wind, tidal, hydrogen fuel cell, >
* <todo: consider, how to conform to NATO interop and wider global resillence and civil preparedness, >
* <todo: consider, find ISO standard in this domain is any exist, >
* <todo: consider, how to weave this into global heating resillience frameworks emerging from UN, BRICS, P4M, others, >
* <todo: consider, other DDS based defence standards SOSA MOSA etal >
* <todo: consider, controller hardware MCU SBC are concern regarding emerging multipolar world, seperation of concern regarding civiliam and military use cases, even if the standards based approach makes systems of systems the dominant frame of reference, actual conrete use cases mean different hardware and software options my be required, >

DONE
* <done: consider, intent to commit>

## Libs

Standards - power general
* <todo: consider, which of these are micro grid or could be used for same or interoperate with same, so what are interfaces and handoff, >
* OpenFMB, 
* SGIP
* Smart Electic Power Alliance
* TMSC tactical microgrid standard, <todo: consider, same as usm 3071?>

Standards - microgrid
* IEEE 2030.7, microgrid control system, ems microgrid energy management system
* IEEE 1547-2018, interconnection & interoperability, poi point of interconnection with der unit
* IEEE 2030.8, microgrid controller & utility communication
* IEEE P2030.11, der management system derms
* IEEE P2030.12, microgrid protection system design, 
* MIL STD 3071, us army, nato, micro grid, <todo: consider, how closely does 3071 follow the IEEE standards, not very much, different use case see use cases above>

Standards - component
* IEC 61850, substation automation, intelligent electronic device ied (MMXU = three phase measuring, XCBR = circuit breaker), microgird device protection/monitoring
* IEEE C37.2, device numbering, relay number/protection, (50 = overcurrent, 25 = sync check, 87 = differential)
* ASME Y14.44, successor to IEEE 200, reference designators electrical/electronic parts, for schematics (U = IC, CB = circuit breaker, T = transformer, M = motor)
* IEC 81346, general identification system for industrial products, used by IEC 61859 object naming
* ...

Standards - teccnnical
* Data Distribution Service DDS, [WS](https://www.omg.org/omg-dds-portal/), OMG
* Real Time Publish Subscribe RTPS, 

Organisations
* DDS Foundation, [WS](https://www.dds-foundation.org/) 
* EDM Association, 
* ISO, 
* OMG, Object Management Group, 

Certification - compute controller safety certs
* Directive 2014/34/EU, ATEX certification
* UKCA Explosive Atmosphere Regulations 2019 <todo: consider, uk equivalent >
* US <todo: consider, us equivalent >
* <todo: consider, equivalents for au ca jp kr nz ua others, cert once and use in many juresdictions >

## Output

Context diagram - distributed generation dg
* attempt to replace base load fossil fuel power sources with storage and h2 to replace natural gas and deisel and other fossil fuels
* depends on use case, civ, mil, building, vehicle, fixed, mobile, strategic, tactical
```
                                                      base load        base load
   source     source       source         source      source           source
   pv solar   small wind   microturbine   fuel cell   chp              genset
                                          h2          h2/natural gas   h2/ng/deisel

```

Context diagram - distributed storage ds
```
  storage          storage    storage         storage   storage   storage
  BESS (BMS+PMS)   Flywheel   Supercapacitor  thermal   gravety   ...

```

Context diagram - OEM TMS connection module and OEM IEC/IEEE connection module for OEM device
* the tms connection module is provided by the OEM as bridge between external TMS network and OEM device internal ECU control system CAN/CAN FD/Modbus/...
* the tmsi does not reach into and override inernal OEM device control system operation
* IEC 62898 series (Parts 1–4) — planning, operation, protection/dynamic control, use cases
* IEC 62786 series — DER connection with the grid
* IEEE 1547 — DER interconnection
* IEEE 2030.7 / 2030.8 — microgrid controller specification and testing
* IEC 61850 — device-level data modelling 
* MIL STD 3071 — tactical microgrid system
* It is incumbent on the OEM device to have bridge interface to interoperate with both stacks of standards
```
   UNSDG 1,9,11,13,15   
   NATO A.V,A.III       
   MIL/NDMA TMS          OEM device                   OEM device
   MIL STD 3071          3071 to OEM bus bridge       CAN/CAN FD/Modbus/...
   TMS network           TMS coonection module        Device internal bus
   ethernet dds          ethernet dds to ECU NCS      Device networked control system   

   CIV MG                OEM device                   OEM device
   <todo: stuff>         IEC/IEEE to OEM bus bridge   as above                 
   <todo: stuff>         MG connection module         as above
   <todo: stuff>         <todo: stuff>                as above
 
```

Context diagram - de facto device unit naming convention in the wild civ
* there is currently, of this writing 2026.09.28, and de jure standard
* functional name acronyms fna some overlap in standardised naming accross; IEEE 1547 / 2030.7 and IEC 61850
* fna including amoungst others; BMS, PCS, EMS/MEMS, DER, POI, PCC, ...
* there is no single unified glossary accross the different standards, and the standard operate at different levels of abstraction
```
   < site >_< area/bus  >_< device kind >_< sequence >
   
    e.g.
   SITE1_BMS_A_01
   SITE1_PCS_A_01
   SITE1_PV_INV_01
   SITE1_GEN_01
   SITE1_BREAKER_TIE_01
```

## References

* Micro grid
* Distributed energy resource der, distributed source, distributed storage, 


