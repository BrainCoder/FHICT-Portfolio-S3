# Service Deployment
For our project we need to deploy multiple services and software packages to our production and development infrastructure. We need a way to automate the deployment of these services to reduce the development overhead caused by a multi service architecture.

## Solutions
### HTTP RESTfull
**The HyperText Transfer Protocol** (**HTTP**) is widely used as a document-centric protocol that transmits messages which are formatted as webpages requested by the client from the Server. It operates on TCP/IP and supports TLS (Transport Layer Security) in the form of HTTPs. It’s widely used in client-server models for REST API between two different platforms or interfaces.

### Docker
 **Docker** is an open and standard lightweight, publish-subscribe network protocol that transports messages between devices. The protocol usually runs over TCP; however, any network protocol that provides ordered, lossless, bi-directional connections can support MQTT. It is designed for connections with remote locations where a "small code footprint" is required and/or the network bandwidth is limited.

### CoAP
**Constrained Application Protocol** (**CoAP**) is an IoT protocol for use on constrained devices. CoAP is based on the popular REST model making it easy to learn for people allready familiar with this technology.

## Comparison matrix
| Feature  | HTTP  | MQTT  | CoAP  |
|---|---|---|---|
| **UDP/TCP**  | TCP | TCP  | UDP  |
| **Ease of use**  | High | High | Medium |
| **Bandwidth consumption**  | High | Low | Low |
| **Energy efficent**  | No | Yes | Yes |
| **Not blocked by firewall / NAT**  | Yes | Yes | No |
| **Flexible**  | Yes | Yes | Yes |
| **Secure**  | No<sup>1</sup> | No<sup>1</sup> | Yes |
| **Easy to maintain**  | Yes | Yes | Maybe |
| **Reliability**  | High | High<sup>2</sup> | Medium |
| **Realtime**  | No | Yes | Yes |
| **Scalable**  | Yes | Yes | Yes |
| **Open Standard**  | Yes | Yes | Yes |

<sup>1</sup> Can be made secure using TLS.
<sup>2</sup> Reliability can be selected using 3 QoS levels.

## Conclusion
Due to the requirements of our project and the skill level within our team. We have decided that MQTT is the best option for this project. The main deciding factors where its **Energy efficency, Ease of use, NAT support & Realtime communication**.


## Sources
### HTTP
https://www.prolim.com/mqtt-v-s-http-rest/

### MQTT
https://www.pickdata.net/news/mqtt-vs-coap-best-iot-protocol

### CoAP
https://coap.technology/

#fontys #portfolio