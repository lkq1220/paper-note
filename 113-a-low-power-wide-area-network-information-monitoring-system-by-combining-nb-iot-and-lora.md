### 1.13 A Low-Power Wide-Area Network Information Monitoring System by Combining NB-IoT and LoRa

#### 0.Abstract
- Detail
    - Zhang, X., et al. (2019). "A low-power wide-area network information monitoring system by combining NB-IoT and LoRa." IEEE Internet of things Journal 6(1): 590-598.
![](/assets/factors.jpg)
![](/assets/journal.jpg)
- Aim
    - Long range
    - A small amount of data transmission
    - Low power
    - Low cost of the Internet of Things (IoT) in actual applications
- Method
    - Multiple subnodes(LoRa node)
    - Main node(NB-IoT && LoRa gateway)
    - A could Server
    - Computer System
    - Optical-electric conversion technology
- Advantage
    - Improves transmission distance
    - Reduces the operating costs of the WAN information monitoring system
- Results 
    - the communication distance in a complex environment is up to 1.6 km
    - the minimum working current is 2 mA
    - the system communication packet loss rate is approximately 3%
    
#### 1. Introduction
- Application Fields
    - Intelligent Agriculture
    - Industrial Automation
    - Smart City
    - Smart Home
- Traditional Communication Technology
    - ZigBee, Bluetooth(short-range radio technologies and not suitable for long-range transmission scenarios)
    - 2G, 3G, 4G, and other solutions based on cellular communication (provide a wider coverage, but they consume too much energy and increase the operating costs)
- LPWAN
    - LoRa 
        - high stability
        - ultralong transmission
        - ultralow power
        - low cost 
    - NB-IoT
        - high QoS 
        - low latency 
        - strong links
        - high coverage,
        - low power
        - low cost 
        
#### 2. LPWAN Technology
##### 2.1 LoRa
- A physical layer technology
- A proprietary spread spectrum technique
- 868 MHz in Europe, 915 MHz in North America, 433 MHz in Asia
- signal
    - low noise levels, 
    - high interference resilience 
    - be difficult to detect or jam
    
##### 2.2 NB-IoT
- A new 3GPP wireless access technology 
- Three deployment modes
    - stand-alone
    - guardband
    - in-band
    
    
![](/assets/nb-iot.jpg)

#### 3. System Desgin and Implementation
- Subnode
    - collects sensor information through analog-to-digital converter (ADC) or serial communication
    - conducts point-to-point or multihop communications with the main node by the LoRa communication module. 
- Main Node
    - receive information sent by subnode 
    - process received information
    - sends information in itself and in other subnodes to the server through the NB-IoT communication module
- Server
    - receive and process data
    - store the data in a database
- User
    - access and download the data through HTTPS protoco
    
![](/assets/wholeSystem.jpg)

##### 3.1 Hardware Design of the System 
- Subnode
    - Function
        - sensor information collection
        - LoRa communication
        - low power
        - solar power supply.
    - Component
        - microcontroller unit (MCU)
            - STM32F103ZET6(Cortex M3)
            - Mode
                - sleep
                - shutdown
                - standby 
        - communication unit
            - LoRa communication module
                - general mode*
                - wake mode
                - power save mode
                - sleep mode* 
            - RS232 and RS485 communication
        - information collection unit
            - ADC collection
            - RS232 and RS485 communication 
        - power unit
            - solar paneL
            - solar panel control circuit
            - dc–dc converter
            
![](/assets/hardware.jpg) 
![](/assets/truehard.jpg)  

- Main node(an LoRa–NB-IoT gateway)

##### 3.2 Software Design of the System 

#### 4. System Test and Analysis
##### 4.1 Point-to-Point Communication Distance Test
##### 4.2 Multihop Communication Distance Test
#### 5. Conclusion