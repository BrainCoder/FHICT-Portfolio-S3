# Integration Tests

## Requirements
Om bekender te worden met integration tests heb ik besloten een integratie test te schrijven voor de fridge pull service die ik eerder gebouwd heb.

## Keuzes
Omdat mijn service bestaat uit verschillende onderdelen geschreven door anderen had ik nog geen test framework na wat googlen kwam ik er achter een framework bedoeld voor nodejs dat erg geschikt lijkt om verschilende services te testen.

### Mocha
Mocha is een test framework geschreven in nodejs hierdoor is het makelijk om asynchrone tests te schrijven.

### Chai
Chai is een assertion libary in node die goed samenwerkt met Mocha. Dankzij deze libary zijn de tests makelijker te schrijven en lezen.

## Result
After a few days of figuring out how this framework worked I had to write a few stubs & drivers to act as data sources & data clients.

### Stubs - HardwareDeviceStub
The HardwareDeviceStub is a module that emulates a device by sending the correct json payload over MQTT to the Fride push service.

### Drivers - InfluxDriver
The InfluxDriver acts as an influx client and houses the code needed to querry data stored by the Fridge push service.

### Output
![[Pasted image 20210611231443.png]]

### Code Repo
https://github.com/FontysDeeltijdICT/Bier.Cool-IoT-IntegrationTest
![[files/Bier.Cool-IoT-IntegrationTest-master.zip]]

## Reflection
I feel like my method was a little overkill due to it's lose coupeling with the services under test. I however do believe that this testing methodology with it's universal framework, external stubs & drivers has it's benefits when testing services consisting of smaller services.