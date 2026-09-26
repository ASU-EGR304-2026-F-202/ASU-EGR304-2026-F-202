---
title: Ideation and Concept Generation
---

# Ideation and Concept Generation

## Project Goal and Audience

The goal of this project is to develop a compact environmental-monitoring device that measures relative humidity, atmospheric pressure, and ambient light, then displays those readings clearly to the user. The device must also exchange signals safely with the team's other subsystems, operate from a regulated power source, and protect its electronics during outdoor use.

The primary audience is a person who needs quick, local environmental readings in an outdoor or semi-outdoor setting. The design must therefore be readable, weather-resistant, easy to mount, and simple to maintain. A secondary audience is the project team, which must assemble, test, integrate, and troubleshoot the device.

## 1. Prioritization Method

The brainstorm was based on the team's User Needs and Benchmarking and Product Requirements assignments. Requirements with priority scores from P8 through P10 received the most attention because they represent the device's primary functions and the greatest integration risks.

The team prioritized:

1. Accurate humidity, pressure, and light measurements
2. A simple, readable display
3. Reliable 9 V-to-5 V power regulation
4. Safe communication with teammates' subsystems
5. Basic protection from water and outdoor conditions
6. Replaceable batteries and accessible components
7. PCB features that are easy to assemble and test
8. Components that are affordable and currently available

Wireless communication, solar charging, touchscreens, mobile applications, and custom charging circuits were considered but were not prioritized because they would add cost and integration difficulty without improving the core required functions.

## 2. Initial Brainstorm Capture

The team generated 100 feature ideas. The image below preserves the initial capture before the features were reorganized into ranked groups and product concepts.

![Initial brainstorm capture showing the original 100 ideas](ideation-assets/brainstorm-initial-capture.jpg)

### Complete Brainstorm, Grouped and Ranked

Within each group, Rank 1 is the team's highest-ranked feature, followed by Rank 2 and Rank 3. The remaining two ideas were retained as alternatives rather than discarded.

| No. | Requirement / need | Rank | Feature | Detail |
|---:|---|:---:|---|---|
| 1 | Multi-sensor measurement | 1 | Three separate digital sensors | Use one sensor each for humidity, pressure, and light so every measurement can be tested separately. |
| 2 | Multi-sensor measurement | 2 | Combined humidity and pressure sensor | Use one module for humidity and pressure and a separate module for light to reduce component count. |
| 3 | Multi-sensor measurement | 3 | I2C sensor modules | Select sensors that share the same data and clock wires. |
| 4 | Multi-sensor measurement | - | Labeled sensor connectors | Allow sensors to be removed easily during testing or replacement. |
| 5 | Multi-sensor measurement | - | Sensor breakout-board prototypes | Test sensors on breakout boards before placing them on the custom PCB. |
| 6 | Humidity measurement | 1 | Factory-calibrated humidity sensor | Use a digital sensor calibrated by the manufacturer. |
| 7 | Humidity measurement | 2 | Humidity range warning | Display a warning if a reading falls outside 0-100% RH. |
| 8 | Humidity measurement | 3 | Software humidity offset | Allow a small correction value to be added or subtracted in software. |
| 9 | Humidity measurement | - | Average multiple readings | Average several readings to reduce small measurement changes. |
| 10 | Humidity measurement | - | Protected humidity opening | Place the sensor behind a vent so it can sample air without direct water exposure. |
| 11 | Pressure measurement | 1 | Digital pressure sensor | Use a common pressure sensor capable of approximately 300-1100 hPa. |
| 12 | Pressure measurement | 2 | Small pressure vent | Include an enclosure opening so outside air can reach the pressure sensor. |
| 13 | Pressure measurement | 3 | Local pressure display | Show the atmospheric pressure measured at the device. |
| 14 | Pressure measurement | - | Software pressure offset | Allow adjustment against a trusted reference. |
| 15 | Pressure measurement | - | Sea-level pressure option | Let the user enter an altitude correction to estimate sea-level pressure. |
| 16 | Ambient-light measurement | 1 | Digital lux sensor | Use a ready-made sensor that reports light level directly in lux. |
| 17 | Ambient-light measurement | 2 | Bright-light warning | Warn when the light exceeds the selected sensor's measurement range. |
| 18 | Ambient-light measurement | 3 | Automatic light range | Use a sensor library that automatically changes sensitivity. |
| 19 | Ambient-light measurement | - | Clear sensor window | Place a clear plastic opening above the light sensor. |
| 20 | Ambient-light measurement | - | Diffuser cover | Add a translucent cover to reduce directional variation. |
| 21 | Measurement updates | 1 | Two-second updates | Refresh the display every two seconds to meet the requirement exactly. |
| 22 | Measurement updates | 2 | One-second updates | Collect and display a new set of measurements every second. |
| 23 | Measurement updates | 3 | Timer-based sampling | Use a software timer to take measurements at regular intervals. |
| 24 | Measurement updates | - | Separate sensing and display functions | Use one software function for sensing and another for screen updates. |
| 25 | Measurement updates | - | Last valid reading | Continue showing the last valid value if a sensor briefly fails. |
| 26 | Display selection | 1 | Character LCD | Show all three readings with a basic text display. |
| 27 | Display selection | 2 | Display brightness setting | Offer two or three screen-brightness levels. |
| 28 | Display selection | 3 | Display hood | Add a small 3D-printed hood to improve outdoor visibility. |
| 29 | Display selection | - | Monochrome OLED | Use a common I2C OLED that is easy to connect and program. |
| 30 | Display selection | - | Color TFT | Use a color display if the team wants a more visual interface. |
| 31 | User interface | 1 | Three labeled rows | Show humidity, pressure, and light on separate rows. |
| 32 | User interface | 2 | Sensor error message | Show `Sensor Error` instead of an incorrect number. |
| 33 | User interface | 3 | Large numbers | Use the largest font that still fits all three readings. |
| 34 | User interface | - | Measurement icons | Place a droplet, gauge, or sun icon beside each reading. |
| 35 | User interface | - | Trend arrows | Show whether each measurement rose, fell, or remained stable. |
| 36 | Water-resistant enclosure | 1 | Two-piece 3D-printed enclosure | Use printable front and back enclosure sections. |
| 37 | Water-resistant enclosure | 2 | Downward-facing air vents | Reduce direct water entry while preserving airflow. |
| 38 | Water-resistant enclosure | 3 | Rubber gasket | Seal the joint between the enclosure halves with rubber or foam. |
| 39 | Water-resistant enclosure | - | Raised enclosure edges | Add overlapping seam edges to resist splashed water. |
| 40 | Water-resistant enclosure | - | Covered cable opening | Protect the ribbon-cable opening with a cover or downward-facing path. |
| 41 | Sensor placement / heat control | 1 | Sensors near an enclosure vent | Place humidity and pressure sensors close to outside airflow. |
| 42 | Sensor placement / heat control | 2 | Sensors away from the regulator | Separate sensors from heat-producing power components. |
| 43 | Sensor placement / heat control | 3 | Sensors away from the display | Separate the humidity sensor from heat produced by the screen. |
| 44 | Sensor placement / heat control | - | PCB sensor extension | Place environmental sensors near the PCB edge. |
| 45 | Sensor placement / heat control | - | White enclosure material | Use a light-colored enclosure to absorb less solar heat. |
| 46 | Replaceable batteries | 1 | Standard AAA batteries | Use smaller cells when enclosure size matters more than battery life. |
| 47 | Replaceable batteries | 2 | Commercial battery holder | Use a ready-made holder instead of custom contacts. |
| 48 | Replaceable batteries | 3 | Standard AA batteries | Use inexpensive, widely available batteries. |
| 49 | Replaceable batteries | - | Screw-mounted battery door | Secure a small access cover with one or two screws. |
| 50 | Replaceable batteries | - | Low-battery icon | Measure battery voltage and warn the user when it is low. |
| 51 | Power regulation | 1 | Power switch | Add a slide or rocker switch between the power source and circuit. |
| 52 | Power regulation | 2 | Decoupling capacitors | Place capacitors near the microcontroller and sensors to reduce noise. |
| 53 | Power regulation | 3 | Ready-made buck converter | Prototype with a commercial 9 V-to-5 V regulator module. |
| 54 | Power regulation | - | Buck-converter IC on PCB | Integrate a common regulator circuit on the final board. |
| 55 | Power regulation | - | 5 V power indicator LED | Show when the regulated supply is operating. |
| 56 | Electrical protection | 1 | Resettable fuse | Limit excessive current and reset after the fault is removed. |
| 57 | Electrical protection | 2 | Reverse-polarity diode | Protect the circuit from a reversed supply connection. |
| 58 | Electrical protection | 3 | 5.1 V protection diode | Use a Zener or TVS diode to clamp voltage spikes. |
| 59 | Electrical protection | - | Input-current test point | Provide a location for measuring total current draw. |
| 60 | Electrical protection | - | Main power fuse | Add an inexpensive fuse rated below the 1.5 A limit. |
| 61 | Ribbon-cable connection | 1 | Keyed 2x4 IDC header | Prevent the ribbon cable from being installed backward. |
| 62 | Ribbon-cable connection | 2 | Strain-relief clip | Keep cable tension from stressing the connector. |
| 63 | Ribbon-cable connection | 3 | Pin-one marking | Clearly mark pin one on the PCB and cable. |
| 64 | Ribbon-cable connection | - | Printed pin labels | Label five digital pins, two analog pins, and ground. |
| 65 | Ribbon-cable connection | - | Test pads for all eight wires | Add accessible pads beside the connector. |
| 66 | Receive teammate signals | 1 | Analog input reading | Use the microcontroller ADC for teammate analog signals. |
| 67 | Receive teammate signals | 2 | UART receiving | Receive short text messages through a serial connection. |
| 68 | Receive teammate signals | 3 | Digital input | Read basic HIGH and LOW signals from another subsystem. |
| 69 | Receive teammate signals | - | Input voltage divider | Reduce an incoming analog voltage to a safe level. |
| 70 | Receive teammate signals | - | Missing-data timeout | Display an error when new information does not arrive in time. |
| 71 | Send teammate signals | 1 | Labeled text message | Send a format such as `H:45 P:1008 L:650`. |
| 72 | Send teammate signals | 2 | Comma-separated message | Send a simple format such as `45,1008,650`. |
| 73 | Send teammate signals | 3 | Fixed message order | Always transmit humidity, pressure, and light in the same order. |
| 74 | Send teammate signals | - | Basic checksum | Add transmitted values to create a simple error check. |
| 75 | Send teammate signals | - | Data-ready output | Set a digital pin HIGH when a new group of readings is ready. |
| 76 | PCB design / assembly | 1 | Mounting holes | Securely attach the PCB to the enclosure. |
| 77 | PCB design / assembly | 2 | Components on one side | Keep most parts on the top side to simplify assembly. |
| 78 | PCB design / assembly | 3 | Programming header | Provide an accessible connector for firmware uploads and debugging. |
| 79 | PCB design / assembly | - | 0805 passive components | Use components large enough for student soldering and repair. |
| 80 | PCB design / assembly | - | Clearly labeled connectors | Print connector names and pin functions on the PCB. |
| 81 | Component availability | 1 | Common sensor modules | Select popular sensors available from several suppliers. |
| 82 | Component availability | 2 | Supplier stock check | Verify inventory before finalizing the PCB. |
| 83 | Component availability | 3 | Updated bill of materials | Record part numbers, prices, suppliers, and backup options. |
| 84 | Component availability | - | Backup sensor option | Identify a second sensor capable of the same measurement. |
| 85 | Component availability | - | Standard passive values | Use common resistor and capacitor values. |
| 86 | Mounting options | 1 | Wall-mounting holes | Attach the device to a wall or fence. |
| 87 | Mounting options | 2 | Pole-mounting holes | Provide holes for zip ties or hose clamps. |
| 88 | Mounting options | 3 | Tabletop stand | Add a fixed or fold-out stand for a desk or patio table. |
| 89 | Mounting options | - | Garden stake | Attach the enclosure to a wooden, metal, or 3D-printed stake. |
| 90 | Mounting options | - | Removable bracket | Replace one small bracket for different mounting methods. |
| 91 | Metric / imperial units | 1 | Stored unit setting | Save the selected units in nonvolatile memory. |
| 92 | Metric / imperial units | 2 | Unit label beside every reading | Always display the correct unit beside its number. |
| 93 | Metric / imperial units | 3 | Unit-selection button | Use one button to change the displayed units. |
| 94 | Metric / imperial units | - | Long-press unit selection | Require a held button to prevent accidental changes. |
| 95 | Metric / imperial units | - | Startup unit choice | Ask for units when the device is first turned on. |
| 96 | Safety / test / documentation | 1 | Covered conductive parts | Keep the PCB and exposed traces inside the enclosure. |
| 97 | Safety / test / documentation | 2 | Setup instruction sheet | Explain how to power and operate the device. |
| 98 | Safety / test / documentation | 3 | Rounded enclosure corners | Avoid sharp edges on the finished enclosure. |
| 99 | Safety / test / documentation | - | Troubleshooting screen | Display basic sensor and communication error messages. |
| 100 | Safety / test / documentation | - | Built-in test mode | Show raw sensor values, supply voltage, and communication status at startup. |

## 3. Sorting, Ranking, and Refinement

The team first sorted the ideas by function. This produced 20 groups: sensing architecture, humidity, pressure, ambient light, update timing, display choice, user interface, enclosure protection, sensor placement, batteries, power regulation, electrical protection, ribbon-cable connection, received signals, transmitted signals, PCB construction, component availability, mounting, units, and safety/testing/documentation.

Each teammate highlighted preferred ideas in an individual color. The team then discussed the alternatives one at a time and reached a unanimous ranking. The first three ideas shown in each group above are the ranked selections; lower-ranked ideas remain available for later design revisions.


### Ranked Shortlist

| Group | Rank 1 | Rank 2 | Rank 3 |
|---|---|---|---|
| Sensor architecture | Separate digital sensors | Combined humidity/pressure sensor | I2C sensor modules |
| Humidity | Factory-calibrated sensor | Range warning | Software offset |
| Pressure | Digital pressure sensor | Pressure vent | Local pressure display |
| Ambient light | Digital lux sensor | Bright-light warning | Automatic range |
| Update method | Two-second updates | One-second updates | Timer-based sampling |
| Display | Character LCD | Brightness setting | Display hood |
| Interface | Three labeled rows | Sensor error message | Large numbers |
| Enclosure | Two-piece printed enclosure | Downward-facing vents | Rubber gasket |
| Sensor placement | Sensors near vent | Sensors away from regulator | Sensors away from display |
| Batteries | AAA batteries | Commercial holder | AA batteries |
| Power | Power switch | Decoupling capacitors | Ready-made buck converter |
| Protection | Resettable fuse | Reverse-polarity diode | 5.1 V protection diode |
| Ribbon cable | Keyed IDC header | Strain relief | Pin-one marking |
| Receive data | Analog input | UART | Digital input |
| Send data | Labeled text | CSV message | Fixed field order |
| PCB | Mounting holes | One-sided assembly | Programming header |
| Availability | Common modules | Stock check | Updated BOM |
| Mounting | Wall holes | Pole holes | Tabletop stand |
| Units | Stored setting | Labels beside values | Selection button |
| Safety/testing | Covered conductors | Setup sheet | Rounded corners |

## 4. Three Product Concepts

The ranked features were recombined into three distinct product concepts. Features not selected for a concept remain in the master brainstorm for future revisions.

### Concept A: Outdoor Wall/Pole Mount 

![Annotated outdoor wall and pole mount concept](ideation-assets/concept-brendan-outdoor-mount.png)

This concept emphasizes a polished, weather-resistant outdoor unit. A clear top panel lets ambient light reach the lux sensor, while downward-facing louvers expose the humidity and pressure sensors to airflow without direct rain entry. A hooded LCD presents all three measurements. A large mounting base supports wall, rail, or pole installation, and the rear contains a screw-mounted AA battery door and a power switch.

| Design area | Selected brainstorm features | How the selection satisfies needs |
|---|---|---|
| Sensing | 1, 6, 10-13, 16, 19, 21 | Separates the three measurements, keeps sensors exposed to the correct medium, and updates every two seconds. |
| Display | 26, 28, 31, 32 | Provides a readable outdoor display with separate rows and clear error feedback. |
| Enclosure | 36-45, 98, 101 | Adds vents, gasketed/overlapping seams, light-colored material, safe corners, and debris filtering. |
| Power and protection | 47-49, 51, 52, 56-58 | Supports replaceable AA batteries, switching, noise control, and electrical protection. |
| Integration and build | 61, 62, 66, 71, 76, 77, 81-83 | Provides a keyed cable, strain relief, analog input, labeled transmitted data, serviceable PCB layout, and available parts. |
| Installation and use | 87, 88, 91, 96, 97 | Supports pole/tabletop use, retained units, covered electronics, and setup documentation. |

### Concept B: Modular Ventilated Enclosure 

![Annotated modular ventilated enclosure concept](ideation-assets/concept-branden-modular-enclosure.png)

This concept emphasizes modular construction and flexible installation. Its two-piece 3D-printed enclosure separates the vented sensor region from the angled LCD interface. Large rear holes support wall mounting, while the removable top simplifies access during assembly and testing.

| Design area | Selected brainstorm features | How the selection satisfies needs |
|---|---|---|
| Sensing | 1, 6, 11, 12, 16, 21 | Uses independent calibrated digital sensors with outdoor air access and two-second updates. |
| Display | 26, 31, 32 | Uses a simple LCD with three labeled rows and an explicit error state. |
| Enclosure and placement | 36, 37, 41, 42 | Uses a two-piece ventilated form and separates sensors from regulator heat. |
| Compact power | 46, 47, 51, 52, 56, 57 | Uses AAA batteries, a commercial holder, a switch, decoupling, and fault protection. |
| Communications | 61, 62, 67, 72, 73 | Adds a keyed, strain-relieved cable and a predictable UART/CSV data format. |
| Build and installation | 76, 81-83, 86, 92, 96, 97 | Uses common stocked parts, documented units, enclosed conductors, wall mounting, and setup instructions. |

### Concept C: Isolated Sensor-Chamber CAD Enclosure 

![CAD concept with isolated sensor chambers](ideation-assets/concept-zander-isolated-chambers.png)

This concept emphasizes measurement isolation and serviceability. Each sensor sits in its own chamber to reduce interference. The humidity and pressure chambers use turned-down vents, and the light sensor receives a dedicated window. The front includes an LCD bezel; the enclosure also includes countersunk lid holes, threaded PCB inserts, and separate wall-mounting holes.

| Design area | Selected brainstorm features | How the selection satisfies needs |
|---|---|---|
| Sensing | 1, 6, 10-13, 16, 17, 19 | Gives each measurement a separate, protected sensing path and adds a bright-light warning. |
| Display | 26, 31, 99 | Shows local readings in labeled rows and supports troubleshooting messages. |
| Enclosure and thermal control | 36, 37, 41-43, 45, 98 | Protects sensor openings, isolates sources of heat, reduces solar heating, and removes sharp corners. |
| Power and connection | 46, 47, 52, 57, 61 | Uses compact replaceable batteries, decoupling, polarity protection, and a keyed cable. |
| Construction and installation | 76, 77, 86, 91, 96 | Adds PCB inserts/mounting holes, one-sided assembly, wall mounting, retained units, and enclosed conductors. |

## 5. Ideation Process

On September 24, 2026, Group 202 met virtually using FaceTime. The full team - Branden, Sidra, Brendan, and Zander - participated. The group unanimously selected Google Docs as the shared tool for collecting and organizing ideas.

The session began with a review of the team's earlier User Needs and Benchmarking and Product Requirements work. The team used the stated priorities, the rankings from those assignments, and the frequency of user-review comments to decide where to spend the most brainstorming effort. Because accurate sensing, display readability, power regulation, subsystem communication, and basic outdoor protection were the highest-priority areas, the team generated the greatest number of alternatives around those functions. More complex additions were preserved as possibilities but were not allowed to distract from the core requirements.

Next, the team discussed possible categories and agreed on functional groupings. Ideas were recorded without criticism so that conventional, unconventional, and incremental options could all be captured. For example, the need to measure light produced ideas involving sensor selection, automatic ranging, optical windows, diffusers, warnings, and display behavior. The need to communicate with other PCBs produced alternatives involving analog inputs, digital inputs, UART, message formats, checksums, and data-ready signals.

After the initial 100 ideas were recorded, the team reorganized them by intended function. No ideas were deleted. Each participant independently highlighted preferred features in a different color. The team then reviewed the ideas one at a time; each person explained the reasoning behind their choices, and the group discussed feasibility, importance, cost, testability, and compatibility with the required system. The group reached a unanimous decision on the top three ideas in each category. This discussion also led to refinements, including a mesh filter behind the ventilation openings to keep debris out while maintaining airflow.

Finally, the team recombined the strongest features into three different full-device concepts. Brendan's concept prioritizes a polished outdoor wall/pole mount with strong weather protection and a clear user interface. Branden's concept prioritizes modular construction, a compact battery system, and flexible wall installation. Zander's concept prioritizes isolated sensor chambers, threaded PCB mounting points, and a clearly annotated CAD enclosure. Comparing these alternatives makes the tradeoffs visible without discarding features that may be useful during later development.

