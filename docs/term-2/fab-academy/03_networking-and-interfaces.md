---
hide:
    - toc
---

# 03_networking-and-interfaces_

## section a
*intro to networks*

During the networking class with Victor, we received an introduction to creating a network using the Arduino software and local server. Working in teams, we attempted to connect to Victor's computer through the local server and Arduino software interface, particularly the serial monitor.

To establish a connection with Victor's computer, we had to modify specific parts of the code on Arduino. Firstly, we downloaded the PunSubClient library and changed the Wifi name and password in the code to connect to the local network. Additionally, we modified the mqttClientuser (Victor), topicToSub, and mqttClientName (our team name). Marielle made some changes to the code as well, but I couldn't follow those parts. Nevertheless, we successfully modified the message we sent to Victor's computer and avoided using the generic "hello!" greeting.

__AY