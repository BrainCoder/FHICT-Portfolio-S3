# Fridge Push Service


## Requirements
To use the data collected by our devices we need a service that collects and stores it.
- Energy efficent
- Multiple devices
- A large number of connected devices

## Research
To properly guide my research into this topic I have decided onto multiple subquestions.

### How to manage seperate services and make them available to all devs?
Docker

### What database is best for storing time series data? (TODO: change to the biercool context)
InfluxDB

### What communication protocol fits our requirements?
To decide on what communication protocol to use we made a seperate document explaining the pro's and con's for each of our considered protocols.
[[IoT communication protocols]]

## Design
![[ServiceDiagram.png]]

## Result
https://github.com/FontysDeeltijdICT/Bier.Cool-IoT-Service

## Reflection
I really enjoyed researching this topic