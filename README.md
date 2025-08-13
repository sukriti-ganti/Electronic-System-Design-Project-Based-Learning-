# Smart Gas Leak Detection and Ventilation System using Raspberry Pi and MQTT
This project is a smart **gas leakage detection and ventilation system** designed using a **Raspberry Pi**, an **MQ-2 gas sensor**, an **exhaust fan**, and **MQTT-based communication via HiveMQ Cloud**.

## Problem Statement
Gas leakage incidents in kitchens, factories, and mining environments can be fatal if not detected and addressed in real-time. Manual monitoring is unreliable and cannot ensure timely evacuation or control. There is a need for:
- Real-time gas monitoring
- Instant alerts to stakeholders
- Automatic ventilation control

## Proposed Solution
This project detects LPG gas leaks using an **MQ-2 sensor**, activates an **exhaust fan**, and sends **real-time MQTT alerts** to subscribed devices via **HiveMQ Cloud**. The system is compact, low-cost, and designed with a **custom PCB** for deployment-ready form factor.

## Features
- Gas leak detection using MQ-2
- Automatic fan control via transistor switch
- Real-time alert over HiveMQ (MQTT)
- Raspberry Pi GPIO-based control
- Compact PCB design with EasyEDA

##  Components Used

| Component              | Function                                  |
|------------------------|-------------------------------------------|
| Raspberry Pi (any)     | Controller + MQTT publisher               |
| MQ-2 Gas Sensor        | Detects LPG/propane concentration         |
| DC Exhaust Fan         | Disperses leaked gas                      |
| Transistor (e.g., BC547)| Switch fan ON/OFF                        |
| 1kΩ Resistor, Diode    | Discrete control circuitry                |
| PCB                    | Compact hardware integration              |
| HiveMQ Cloud           | MQTT broker for remote alerting           |


## Block diagram:
[MQ-2 Sensor] ---> [Raspberry Pi GPIO]
                         |
                         v
                 [Transistor Switch]
                         |
                    [Exhaust Fan]

        [Wi-Fi] ---> [HiveMQ Broker] ---> [Subscriber Device]

