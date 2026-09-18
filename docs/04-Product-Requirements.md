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

### User Story #2

Marcus lives in the Valley of the Sun, where extreme heat, low humidity, intense sunlight, and seasonal monsoon storms create rapidly changing weather conditions. As a meteorology enthusiast, Marcus enjoys observing these changes and wants a convenient way to collect environmental measurements around his home. He uses the environmental monitoring device to measure atmospheric pressure, relative humidity, and ambient light throughout the day. By viewing these measurements on the device's display, Marcus can observe how local environmental conditions change as weather systems move through the valley and compare his observations with local weather reports.
...

## Aspects

The new product design will be based on that of the AirPods with improvements based on the following requirements. The **P1 - P10** is the "code" to indicate the priority of the requirement, from low to high.

1. **Producer Design**
   * 1.1 The product shall be visually easy to distinguish from existing AirPods as well as main competitors Sony WF-1000XM3, Jabra Elite, Amazon Echo Buds, Samsung Galaxy Buds, and Bose SoundSport Free, and Urbanista Stockholm. (P10)
   * 1.1 The product shall be easy to recognize as an Apple product without needing a logo on its exterior. (P10)
   * 1.2. The product shall avoid styling elements from our Powerbeats over-ear wireless headphones since those address a different market segment. (P8)
  
1. **Functionality**
      * 2.1 The product shall incorporate one or more optical proximity sensors to detect the user wearing it. (P10)
      * 2.2 The product shall offer a dual microphone in each earbud. (P10)

## Requirement Criteria Specifications

* 1.1.1 - Regulate system power from 9 volts to 5 volts
* 1.1.2 - Provide over-amperage project to not exceed 1.5 amps.

## Open Questions

* Can we move towards a recyclable and repairable product, for example, with ZIF connectors and glue-free assembly?
* Can we improve on failing or self-igniting batteries?
