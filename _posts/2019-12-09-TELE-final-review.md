---
title: TELE25892 Final Review
category: Self-review
tag: TELE25892
---
# RF Measurement
1. Main components of an RF communication link? What do you understand by IR and EIRP?
* transmitter
* antenna: interface between electrical and EM signals
* receiver
* Intentional Radiator (IR): the device that intentionally emits RF enery by radiation or induction
* Equivalent Isotropically Radiated Power (EIRP): power * antenna gain
2. SNR, Noise Floor and Receive sensitivity?
* SNR
* Noise Floor
* Receive sensitivity
8. Antenna beamforming: use an antenna array for the directional signal transission or reception

# 3G, 4G and Beyond
1. List 4 key 3G vision statements.
* universal global roaming
* multimedia (voice, data and video)
* increased capacity
* approach for worldwide standaradization and IP-based architecuture
2. Draw and label 3GPP architecture for 3G
* ![3GPP 3G](..\assets\images\post_images\tele-w14-2.png)
3. Draw and label UMTS (WCDMA) Rel 99 architecture for 3G
* ![UTMS](..\assets\images\post_images\tele-w14-1.png)
4. What improvements are move in HSDPA and HSUPA, over base 3G?
* Higher data speed
* reduced latency
* higher system capacity
5. Draw and label LTE architecture. Briefly describe the functions of the key elements.
* ![LTE](..\assets\images\post_images\tele-w14-3.png)
* eNodeB
* serving gateway: helps mobility, maintains data path between eNodeB and PDN GW
* MME: provide mobile related services (tracking, handover, paging, temp ID)
* HSS: database that storing subscriber info
* PDN Gateway: provides connectivity for the UE to external packet data networks
* PCRF: detects the service flow and enforce charging policy
6. What are the key technologies used in LTE that makdes it stand out compared to other versions of cellular systems?
* multiple antenna technology
* multi-carrier technology
* Packet Switched Radio Interface Technology
7. What are the visions of 5G and key improvements over 4G networks?
* New Radio
* 5 Gbps - 50 Gbps downlink throughput
* massive MIMO and beamforming
* ability to support either FDD or TDD modes for 5G radio bands

# Others
1. Wireless Connectivity
* Transmission error
* Low bandwidth
* Long or variable latency
* Asymmetry in bandwidth and error characteristics
2. 802.11e: enhanced medium access methods to support QoS requirements
3. Distributed Coordination Function
* interframe space:period of time exist between wireless frame transmissions
* duration/ID field: the time required to transmit the ACK and SIFS
* carrier sense:check if the medium is busy
* random back-off timer