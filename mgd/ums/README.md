# US military standard ums

MIL STD 3071, US Army, micro grid interoperability FOB, other uses many for civilian use cases

See also
* DDS, application []() <todo: consider, get github hyperlink>
* Heat pump, []() <todo: consider, get github hyperlink>
* NEXUS-1, []() composability for discrete system examples dds <todo: consider, get github hyperlink>

## Notes

Objectives
* Find interoperability with other standards
* Promote this as for adoption as an ISO standard
* Use as interoperability with NATO Article III

## Status
TODO
* <todo: consider, first project with this for civilian use for heat pump or hydrogen fuel cell or solar panel or hydron hot water boiler home product ... >
* <todo: consider, CAN bus chip sets MCU's SBC's for genset controller unit >

DONE
* <done: consider, intent to commit>

## Libs
Use cases civilian civ vs military mil compounded by current global security concerns.

Implementations - oss, foss, middleware, dds, rtps, ...
* Cyclone DDS, Eclipse Foundation, EPL 2.0, ITAR free, S RTOS (64 MB min), M/L Linux
* Fast DDS, eProsima (Spain), Apache 2.0, ITAR free, No RTOS  (Linux only), M/L Linux (128 MB min)
* HDDS, Verify origin, Apache 2.0 / MIT, ITAR verify, S RTOS TBD, M/L Linux TBD
* ZeroDDS, Verify origin, Apache 2.0, ITAR verify, S RTOS TBD, M/L Linux TBD

Implementatons - commercial, proprietary, lisensed, ...
* tbd

Standards
* Controller Area Network CAN, de facto 
* Data Distribution Service DDS, [WS](https://www.omg.org/omg-dds-portal/), OMG
* Real Time Publish Subscribe RTPS, 
* Tactical Microgrid Standard TMS, [WS](https://battery.army.mil/system-integrator-hub/tms/), MIL STD 3071, US Army
* <todo: consider, other similar standards, >

Organisations
* DDS Foundation, [WS](https://www.dds-foundation.org/) 
* EDM Association, 
* Object Management Group, 
* US Army, repurposing military grade system solutions based on open standards for civilian use

## Hardware
Use cases civilian civ vs military mil compounded by current global security concerns.

Civilian, no military use cases, generic use global, - prototyping more resarch required!
* <todo: consider, first cut prototpying options, >
* <todo: consider, arduino as excuse to buy fist instance >
* <todo: consider, rpi + hat for testing with arduino p2p>
* <todo: consider, central ems controller, per source controller, scenario, >
* Arduino, + Copperhill CAN Shield, or Seeed CANBed, Seeed CANBed M4, CANDuino v3, prototyping
* Raspberry Pi, + PiCAN3, or PiCAN2 Duo or similar, prototyping

US - itar
* <todo: consider, identify components>

EU - itar free, safe, candidate list smd's 
* <todo: consider, more research required, first cut only, >
* CompuLab UCM-iMX95 8 GB (5× CAN), SBC, [](), industrial, central ems controller, circa # £500
* nRF54H20, SoC [WS](https://www.nordicsemi.com/Products/nRF54H20), per source, field controller, circa ~£15
* STM32H743, SoC [](), per source, field controller, circa ~£15 
* nRF54LM20A (BLE uplink), [](), per source, telemtry, wireless gateway,  circa ~£10
* TJA1051, [](), CAN transceiver, isolation,  circa ~£5
* STM32740 [](), CAN transceiver, isolation,  circa ~£5

EU - itar free, pre built pcb's, itar free, cots products, 
* tbd

## References

Terms
* Micro grid, tactical

News Papers - presentations
* Modernizing Tactical Microgrids with TMS & DDS, [WS](https://www.brighttalk.com/webcast/12231/673028), Sep 23 2026, Nina Tucker Twin Oaks Computing and Gerardo Pardo RTI, BrightTalk

News Papers - CAN
* A Simple Intro to CAN [WS](https://www.csselectronics.com/pages/can-bus-simple-intro-tutorial), 2026, scc electronics
