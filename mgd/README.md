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
* TMG civilian equivalent open source, iso standard required, how to maintain compatiblity?
* A microgrid ontology, glossary, data dictionary, canonical data model cdm, there does not appear to be one circa 2026.10.02

Use cases - currently require protocol gateway for mixed environments, of TMS and IEEE/IEC, however any genset, battery, inverter can be made TMS compliant by addding a gateway, with modifying the OEM's internal firmware, i.e. drop in tmsi module concept
* TMG, tactical microgrid system, mobile, islanded, tactical, military, potentially for emergency services in extreme civilian grid failure scenario likely nato articel iii related, which might be extreme weather global heating scenario
* IEEE/IEC, fixed, grid interconnected, commercial/industrial, civilian, requires a TMS interface module, and likely assimilation into TMS network for the durration, 

Risk mitigation - human health, pollution, ghg emmisions, pure hydrogen combustion best case, 
* Best case. Hydrogen combustion produces; nitrogen oxides (NOx) only produced with oxidizer, zero particulate matter, zero carbon based pollutants, water vapour h2o primary byproduct of pure hydrogen combustion
* Worst case. Diesel combustion produces; particulate matter pm2.5 very harmful, nitrogen oxides (NOx) significant amounts at high temperature reacting in atmosphere to form ground level ozon and seconcary PM2.5, carciogens nitroarenes and polycyclic aromatic hydrocarbons pah's, black carbon major component of pm2.5 repitory mortality and climate warming

Risk mitigation - NOx, NOx can be catalyzed and removed; SCR, EGR, H2-SCR
* h2 selective catalytic reduction H2-SCR, uses hydrogen as reducing agent
* selective catalytic reduction SCR, uses amonia as reducing agent
* exhaust gas recirculation EGR, 
* <todo: consider, what other solutions are there for NOx to water h2o, >

## Status
TODO
* <todo: consider, first cut resources available, >
* <todo: consider, similar micro grid solutions to us-army mil std 3071, system of systems, plug and play, what is the au ca de fr jp kr nz uk etal  equivalent? is this the de facto or de jure NATO standard, what would a civilian equivalent look like, iso, >
* <todo: consider, determine when test tool set for mil std 3071 to be open sourced? eta?,  >
* <todo: consider, how best to interoperate with renewably energy sources, solar, wind, tidal, hydrogen fuel cell, >
* <todo: consider, how to conform to NATO interop and wider global resillence and civil preparedness, >
* <todo: consider, find ISO standard in this domain is any exist, >
* <todo: consider, how to weave this into global heating resillience frameworks emerging from UN, BRICS, P4M, others, >
* <todo: consider, other DDS based defence standards SOSA MOSA etal >
* <todo: consider, controller hardware MCU SBC are concern regarding emerging multipolar world, seperation of concern regarding civiliam and military use cases, even if the standards based approach makes systems of systems the dominant frame of reference, actual conrete use cases mean different hardware and software options my be required, >
* <todo: consider, for itar compatibility define the european standards set, and au ca nz uk no is similar, >

DONE
* <done: consider, intent to commit>

## Libs

Standards - power general
* <todo: consider, which of these are micro grid or could be used for same or interoperate with same, so what are interfaces and handoff, >
* OpenFMB, [WS](https://openfmb.gitlab.io/), us centric power wrapper round IEC 61850 and IEC 61968/61970 (Common Information Model)
* SGIP, 
* Smart Electic Power Alliance, 
* TMSC tactical microgrid standard consortium, <todo: consider, same as usm 3071?>

Standards - microgrid management
* ISO ...
* ISO ...
* ...

Standards - microgrid
* IEEE 2030.7, microgrid control system, ems microgrid energy management system
* IEEE 1547-2018, interconnection & interoperability, poi point of interconnection with der unit
* IEEE 2030.8, microgrid controller & utility communication
* IEEE P2030.11, der management system derms
* IEEE P2030.12, microgrid protection system design, 
* MIL STD 3071, us army, nato, micro grid, <todo: consider, how closely does 3071 follow the IEEE standards, not very much, different use case see use cases above>

Standards - component
* IEC 61850, substation automation, intelligent electronic device ied (MMXU = three phase measuring, XCBR = circuit breaker), microgird device protection/monitoring
* IEC 61968/61970 (Common Information Model), 
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
* necessary for human health and planetary safety for capex investment for as rapid as possible horizon for 100% H2 base load source and retire fossil fuel base load source
* the diagram below show intermediate state in change to 100% H2 for all base load
```
                           base load      base load   base load        base load
   source     source       source         source      source           source
   pv solar   small wind   microturbine   fuel cell   chp              genset
                           h2             h2          h2/natural gas   h2/ng/deisel

<todo: consider, remove natural gas ng & deisel as these are very harmful, transitional only untill all base load source is 100% h2, >
<todo: conside, 100% h2 ice, internal combution engine, >
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
* It is incumbent on the OEM device to have bridge interface to interoperate with both stacks of standards,
* Device unit interoperability between CIV SMG and MIL/NDMA TMG and likely requirement for CIV/NDMA TMG internationl standard while still retaining interop with MIL TMG, so a CIV/NDMA TMG standard/solution required but not to reinvent the wheel, emergency services which would be NDMA members are civilian organisations, this muddle need to be sorted, as does related itar free concern, 
* <todo: consider, these last two statements need revision, conflating things, use least impact on OEM device for tms capabiltiy addition, use case one - OEM retrofits current device with tms capabilty, use case two - OEM new design for future devices tbc best solution in that instance, device retrofit vs new device design build >
* Likely two seperte externally facing code bases, both deployed to the same controller hardware, via user panel or cli initiate one or other,
* LIkely one single internally facing code base, deployed to its own controller hardward MCU sepration of concern modulairty, accessed by which ever microgrid facing module was initiated
```
   UNSDG 1,9,11,13,15   
   NATO A.V,A.III       
   MIL NATO/CIV NDMA TMG   OEM device controller        OEM device
   MIL STD 3071            3071 to OEM bus bridge       CAN/CAN FD/Modbus/...
   TMG network             TMG coonection module        Device internal bus
   ethernet dds            ethernet dds to ECU NCS      Device networked control system   

   CIV SMG                 OEM device controller        OEM device
   IEC/IEEE stack          IEC/IEEE to OEM bus bridge   as above                 
   SMG network             SMG connection module        as above
   <todo: stuff>           <todo: stuff>                as above
 
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

* Microgrid MG
* Distributed energy resource der, distributed source, distributed storage, 
* Tactical Microgrid TMG, mobile, might be civilian NDMA or military NATO
* Stretegic Microgrid SMG, fixed, what does a smg dds equivalent to tmg look like

H2 power
* <todo: consider, first pass at h2 power generation technology, >
* Jenbacher engines, [WS](https://www.jenbacher.com/en/energy-solutions/energy-sources/hydrogen/) chp 100% h2 operation
* H2Genset, [WS](https://www.h2-genset.com/en/) 100% h2
* gas turbines, [WS](https://hydrogeneurope.eu/siemens-and-others-test-first-100-h2-gas-turbine-in-france/) using 100% h2 as fuel source
* ...

H2 generation
* electrolyzers, 

News papers - microgrids
* Understanding Microgrids and Their Future Trends, [WS](https://ieeexplore.ieee.org/document/8754952), 13-15 February  2019, IEEE, International Conference on Idustrial Technology ICIT, [DOI](https://doi.org/10.1109/ICIT.2019.8754952)
* Drop-in Modular Solution for MIL-STD-3071 Tactical Microgrid Standard (TMS) Compliance, [WS](https://aegispower.com/mil-std-3071-tactical-microgrid-interface-module/), Aegis, product, what is an itar free alternative, 

Reports
* The Grid We Need Now, Independent Review of AI Deployment in the Electricity Networks, [PDF](https://assets.publishing.service.gov.uk/media/6a9fea93c5796a7a179c641f/the-grid-we-need-now-independent-review.pdf), September 2026, Lucy Yu, Granthan Institute, Imperial, UK Gov, 
