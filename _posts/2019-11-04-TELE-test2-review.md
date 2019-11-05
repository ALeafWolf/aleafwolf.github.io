---
title: TELE25892 Test 2 Review
category: Self-review
tag: TELE25892
---
# Chapter 9: 802.11 MAC Architecture
## Data-Link Layer
- sublayers:
 - LLC (upper)
 - MAC (lower)
### MAC Service Data Unit (MSDU)
- contains data from the LLC and upper layers
- the data payload that contains the IP packet pluse some LLC data
### MAC Protocol Data Unit (MPDU)
- it’s a 802.11 frame
- it consists of a MAC header, MSDU and FCS (frame check sequence)

## Physical Layer
- sublayers
 - PLCP (upper): prepares the frame for transmission by taking the frame from the MAC sublayer and creating the PLCP Protocol Data Unit (PPDU)
 - PMD (lower): modulates PPDU and transmits the data as bits
### PLCP Service Data Unit (PSDU)
- it’s MPDU which is recognized by the physical layer side
### PLCP Protocal Data Unit (PPDU)
- PPDU add a PHY header to the PSDU

## 802.11 and 802.3 Interoperability
- 802.3 frames are encapsulated within 802.11 frames for transmission
 - 802.3 frame size: 1518 bytes with 1500 bytes data payload
 - 802.11 frame size: 2347 bytes with 2304 bytes MSDU payload
- difference in MAC address fields
 - 802.3 only have a source address (SA) and destination address (DA)
 - 802.3 have more, receiver address (RA), transmitter address (TA) and basic service set identifier (BSSID)

## 802.11 Frame Types
* All have many subtypes
### Management frames
- is used by wireless stations to join and leave the basic service set (BSS)
- not necessary for the wired networking
- ex. subtypes:
 - association/reassociation request and response
 - action with/without ACK
 - beacon
### Control frames
- assist with the delivery of the data frames
- clear the channel
- acquire the channel
- provide unicast frame acknoledgments
- contain only header information
- ex. subtypes:
 - Clear to sent (CTS)
 - Acknowledgment (ACK)
 - Request to send (RTS)
### Data frames
- carry the actual data which is passed down form the higher layer protocols
- not all data frame will carry a MSDU payload
- ex. subtypes:
 - data
 - null function (no data)
 - QoS Data/Null (HCF)

## Beacon Management Frame
- the AP of a BSS send the beacons while the clients listen for the beacon frames
 - the only situation client send the beacon frame is when it’s in the Ad Hoc mode
- the beacon frame contains all the necessary information for a client station to learn about the parameters of the basic service set before joining the BSS
- ex. info:
 - time stamp: synchronization information 
 - channel information (channel used by the AP or IBSS)
 - SSID: logical WLAN name
 - Robust Security Network Capabilities: TKIP or CCMP cipher information and authentication method
 - QoS capabilities

## Passive Scanning
- listen for beacon frames from the AP
## Active Scanning
- transmits probe request/reponse frames between client and AP

## ACK Frame
* Every unicast frame must be followed by an ACK frame
- if the frame is corrupted, Frame check sequence(FCS) will fail, receiving station will not send an ACK, the frame will be retransmitted

## RTS and CTS Frames
* ready to send/clear to send is the mechanism that performs a NAV distribution and helps prevent collisions from occuring
![Example](/assets/images/post_images/tele-test2-1.png)
* CTS-to-Self: a 802.11g protection mechanisms

# Chapter 8: Media Access
## CSMA/CA
![Example](/assets/images/post_images/tele-test2-2.png)
* CSMA/CA vs. CSMA/CD
![Example](/assets/images/post_images/tele-test2-3.png)
## Distributed Coordination Function (DCF)
* fundamental/mandatory access mode of 802.11 standard
### Interframe Spacing (IFS)
* time period between wireless transmissions
* five types of IFS
- low priority = more wait time
* actual time vary depending on the transmission speed of the network
### Duration/ID Field
* field in the MAC header of an 802.11 unicast frame
- time in microseconds to transmit
* other station alter their transmit time based on this
### carrier sense
* physical
- performed by stations not transmitting or receiving
- listening for any 802.11 traffic
* virtual
- use a logical timer (NAV)
- stations cannot transmit unless the nav value is 0
### random back-off timer
* final timer used prior to transmission
## PCF
* **optional** 802.11 media access method
## HCF
* combined capabilities from DCF and PCF
* frame brust
- several frames then one ACK (old is one frame with one ACK)
