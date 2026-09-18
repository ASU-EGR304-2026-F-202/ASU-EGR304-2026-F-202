---
title: Product Requirements
---

## Project Objective

This project aims to design and develop a compact environmental monitoring device capable of measuring and displaying atmospheric pressure, relative humidity, and ambient light levels in real time. The system will integrate multiple environmental sensors, a microcontroller, and a display onto a custom PCB to provide users with clear and easily accessible environmental measurements. The device will target a relative humidity measurement range of 0–100% RH with an accuracy of approximately ±3% RH, an atmospheric pressure range of approximately 300–1100 hPa with an accuracy of approximately ±1 hPa, and an ambient light measurement range of at least 0–10,000 lux. Measurements will be updated and displayed at least once every two seconds. The product will prioritize reliable sensor operation, measurement accuracy, readability, compact size, and ease of use. Components will be selected based on cost, availability, power requirements, and compatibility with the PCB design. The primary goal is to successfully integrate the sensors, microcontroller, power circuitry, and display into a functional PCB-based prototype.

## Stakeholders

* **Target group** Middle-income adults approximately 20–50 years old who have an interest in gardening, meteorology, environmental monitoring, or electronics.
* **Target purchaser** Gardening and meteorology enthusiasts or hobbyists who want an affordable way to monitor local environmental conditions.
* **Customer service** Responsible for providing users with instructions for setup, operation, troubleshooting, and interpretation of sensor measurements through an instruction manual and instructional video.
* **Marketing & Sales division** Responsible for advertising the product to gardening and weather enthusiasts through locations such as botanical gardens, nurseries, garden centers, and online hobbyist communities.
* **Retailers** Require a product that can be safely transported and stored under reasonable variations in temperature, humidity, atmospheric pressure, and vibration.
## Use Cases

### User Story #1: Janelle

Janelle is a 42-year-old mother who lives in a mountainous valley outside of Seattle. The surrounding terrain creates several microclimates, causing light, humidity, and atmospheric pressure to vary throughout the area. As a gardening enthusiast, Janelle wants to better understand the environmental conditions affecting her personal garden. She uses the environmental monitoring device to measure the ambient light, relative humidity, and atmospheric pressure around her plants. By viewing these measurements on the device's display, Janelle can observe changes in her garden's local environment and use the information to better understand the conditions in which her plants are growing. 

### User Story #2: Marcus

Marcus lives in the Valley of the Sun, where extreme heat, low humidity, intense sunlight, and seasonal monsoon storms create rapidly changing weather conditions. As a meteorology enthusiast, Marcus enjoys observing these changes and wants a convenient way to collect environmental measurements around his home. He uses the environmental monitoring device to measure atmospheric pressure, relative humidity, and ambient light throughout the day. By viewing these measurements on the device's display, Marcus can observe how local environmental conditions change as weather systems move through the valley and compare his observations with local weather reports.
...

## Aspects

The new product design will be based on that of the AirPods with improvements based on the following requirements. The **P1 - P10** is the "code" to indicate the priority of the requirement, from low to high.

1. **Product Design**
   * 1.1 The product shall contain sensors capable of measuring pressure, humidity, and ambient light. (P9)
   * 1.2 The product will be in a completely contained unit to prevent water damage. (P8)
   * 1.3 The product will have access and replace batteries. (P7)
   * 1.4 The product shall connect to teammates' subsystems via an 8-wire ribbon cable using a 2x4 IDC header, following the team's shared pinout (5 digital I/O, 2 analog I/O, 1 ground). (P9)
   * 1.5 The product shall regulate incoming 9V power to stable 5V supple for the microcontroller and sensors. (P10)
2. **Functionality**
      * 2.1 The product shall measure relative humidity from 0–100% RH with a target accuracy of ±3% RH. (P10)
      * 2.2 The product shall measure an atmospheric pressure range of approximately 300–1100 hPa with an accuracy of approximately ±1 hPa (P10)
      * 2.3 The product shall measure an ambient light measurement range of at least 0–10,000 lux. (P9)
      * 2.4 Measurements will be updated and displayed at least once every two seconds (P8)
      * 2.5 The microcontroller shall be capable of receiving and correctly interpreting signals sent by teammates' subsystems over shared ribbon connector. (P8)
      * 2.6 The microcontroller shall be capable of transmitting correctly formatted signals to teammates' subsystems over shared ribbon connector. (P8)
        
3. **Interactivity & User Experience**
      * 3.1 The product shall display current humidity, pressure and ambient light readings simultaneously on a single screen, legible in direct sunlight. (P8)
      * 3.2 The product shall use a display format that is understandable to a non technical enthusiast (P6)
           
4. **Customization**
     * 4.1 The product shall be offered with a mounting option suitable for outdoor garden placement (P4)
     * 4.2 The product shall allow the user to select between metric and imperial display units (P3)
     * 4.3 The enclosure shall be offered in at least one weather resistant finish suited to prolonged outdoor exposure. (P2)

5. **Manufacturing**
     * 5.1 The PCB shall be producible using standard surface mount assembly processes available to the team. (P9)
     * 5.2 All components shall be sourced from suppliers with verified availability at time of order to avoid production delays. (P7)
     * 5.3 The enclosure shall be manufacturable within the courses budget. (P6)


  6. **Safety**
     * 6.1 The product shall limit input current draw to no more than 1.5A to prevent damage to the regulator and connected subsystems. (P10)
     * 6.2 The products power regulation circuitry shall prevent voltage above 5.5V from reaching the microcontroller or sensors under normal operating conditions. (P10)
     * 6.3 The product shall not exposure users to sharp edges, pinch points, or exposed conductive traces during normal handling. (P7)
       
## Requirement Criteria Specifications
1. **Product Design**
* 1.1.1 Confirm Via data sheet review that selected sensor ICs cover the required pressure, humidity, and light range
* 1.2.1 Apply light water spray to assembled enclosure for 60seconds, visually inspect internals for moisture entrance
* 1.3.1 Remove and replace batteries using only fingers
* 1.4.1 Compare connector pin assignment against the team block diagram pinout table
* 1.5.1 Measure regulator output voltage under no load and full load conditions with a multimeter, confirm output stays within range.

  
2. **Functionality**
* 2.1.1 Check the device's humidity readings against a trusted humidity reader at a few different moisture levels and conifrm error stays within +/- 3%RH
* 2.2.1 Compare device pressure readings against known altitude points and confirm error stays within +/- 1hPa.
* 2.3.1 Expose light sensor to calibrated light sources from 0–10,000 lux; confirm readings track within acceptable tolerance.
* 2.4.1 Use a timer to confirm display refresh interval does not exceed 2 seconds across 10 consecutive cycles.
* 2.5.1 Send test signals from a teammate's board on each ribbon pin and confirm correct interpretation.
* 2.6.1 Trigger microcontroller to transmit signals on each ribbon pin andd confirm correct format via receiving board


  3. **Interactivity & User Experience**

* 3.1.1 View display outdoors in direct sunlight and confirm a test user can read all three values
* 3.2.1 Have an untrained test user view the display and correctly state each reading without instruction

  4. **Customization**
* 4.1.1 Confirm mounting hardware is included and physically compatible with the enclosure.
* 4.2.1 Toggle unit setting and confirm all three measurements convert correctly
* 4.3.1 Apply water spray to coated enclosure and inspect for finish degradation 
  5. **Manufacturing**
*5.1.1 Review PCB design files to confirm all components are compatible with standard surface-mount assembly
*5.2.1 Cross-check BOM part numbers against supplier stock at time of order
*5.3.1 Total projected enclosure material cost against the defined budget limit
  6. **Safety**
*6.1.1 Apply short-circuit/over-current condition at regulator output and confirm current draw is limited to <1.5A without component damage.
*6.2.1 Vary input voltage at the barrel jack and measure voltage at sensor supply pins and confirm it never exceeds 5.5V.
*6.3.1 Physically handle the assembled unit and enclosure and check for exposed traces or pinch points.
  
## Open Questions

* Can we move towards a recyclable and repairable product, for example, with ZIF connectors and glue-free assembly?
* Can we improve on failing or self-igniting batteries?
