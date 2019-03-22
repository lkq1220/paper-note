### In situ real-time permittivity estimation and soil moisture sensing using wireless underground communications

#### 0. Abstract
- Detail
    - Salam, A., et al. (2019). "Di-Sense: In situ real-time permittivity estimation and soil moisture sensing using wireless underground communications." Computer Networks 151: 31-41.
- Method(real-time in situ estimation of relative permittivity of soil, and soil moisture)
    - be determined from the propagation path loss, and velocity of wave propagation of an underground (UG) transmitter and receiver link in wireless underground communications
- Result
    - The estimated soil parameters have less than 8% estimation error from the ground truth measurements and semi-empirical dielectric mixing models
    
#### 1. Introduction
- Why
    - one major bottleneck in the current laboratory-based permittivity estimation techniques is off-line measurement of the collected soil samples
- Electromagnetic (EM) waves propagates through the soil
   - depth
   - distance
   - frequency
   - soil moisture
   - properties of the soi
- How 
    1. a transmitter antenna buried at a certain depth in soil transmits a wideband signal in frequency range of 100–500 MHz, which propagates through the UG channel. 
    2. the received signal is measured at the receiver to determine the path loss. 
    3. estimate the soil moisture and permittivity based on path loss using Di-Sense
- Verification
    - Ground truth measurements
    - Semiempirical Peplinski dielectric mixing model
    - Topp mode

#### 2. System models
- Aim 
    - estimate the soil permittivity and moisture at a distance range of 1–15 m
- Quantities
    - propagation path loss in soil
    - velocity of wave propagation in soil
- Quetion
    - given the path loss of communication link in the soil medium
    - derive a function that estimates the permittivity, and soil moisture of understudy soil medium.
![](/assets/319-1.jpg)
- Propagation path loss approach
  - Path loss
  - The frequency of the minimum pathloss
  - Soil factor
  - Wavelength 
  - Relative permittivity
  
  ![](/assets/319-10.jpg)
- Permittivity estimation through velocity of wave propagation in soil
  - Power delay profile (PDP) are measured to get velocity of the wave propagation
  - Relative permittivity in soil is calculated from the difference of transmission and arrival time of the direct component in the soil
  
  ![](/assets/319-11.jpg)
  ![](/assets/319-2.jpg)
- Di-Sense soil moisture sensing
    - soil permittivity depends on the soil moisture only, soil water content can be determined from soil permittivity
    ![](/assets/319-12.jpg)
    
#### 3. Empirical setup
- Empirical VWC range, depth, and particle size distribution and classification of testbed soil
![](/assets/319-3.jpg)

##### 3.1 Outdoor/field software-defined radio (SDR) testbed development and measurements
- Testbed development
    - four sets of buried dipole antennas in silt loam soil（10cm, 20cm, 30cm, 40cm）
        - Each set contains four antennas buried at 50 cm, 2 m, and 4 m distance from the first antenna
        
![](/assets/319-4.jpg)

- Experiment methodology 
    - A Gaussian signal RF waveform of 2 MHz bandwidth is transmitted from an UG dipole antenna, buried at 40 cm depth, by using the transmitter USRP
    - Signal is received on the receiver USRPs, connected to dipole antennas buried at four different depths
    - Experiment are repeated for all these depth for the distances of 2 m and 4 m
    - This process is repeated for frequency range of 100–500 MHz
    - Post-processing is done in Matlab
    
![](/assets/319-5.jpg)

#####3.2 PDP measurements
- PDPs are measured by using the Keysight Technologies N9923A FieldFox VNA

#### 4. Performance analysis, model validation, and error analysis
##### 4.1 Path loss in wireless underground communications
- change in lowest path loss frequency of the UG channel at different soil moisture levels is shown in sandy soil, silt loam, and silty clay loam soil. 
- change in the lowest path frequency over depth in silt loam, silty clay loam, and sandy soil
- time of arrival of the direct component is shown as a function of change in soil moisture. 
![](/assets/319-6.jpg)
- ##### pic(a)
    - frequency of the lowest path loss decrease with increase in soil moisture, because of the fact that permittivity of soil is greater than the air, and it increases with increase in soil moisture, hence frequency of the lowest path loss shifts to the lower frequency end
- ##### pic(b)
    - This difference in lowest frequency with depth is caused by the reflected wave from the soil–air interface that induces a current on the antenna and changes the impedance which results in changes in lowest path loss frequency of the wireless UG channel.  
    - At higher depths, the distance to the soil–air interface is higher. Hence, the intensity of the reflected wave is less due to higher soil absorption. Furthermore, interaction of antenna fields with the soil causes changes in the lowest path loss frequency of the UG channel.h
    - It can be seen that the lowest path loss is not corresponding to minimum operating frequency, so frequency needs to be adjusted to the current soil conditions automatically in field.
    ![](/assets/319-9.jpg)
- ##### pic(c)
    - velocity of wave propagation in soil decrease with increase in soil moisture
    
##### 4.2 Model validation
- Di-Sense VWC is compared with ground truth VWC measurements 
- Di-Sense VWC is compared with Topp model
- Di-Sense permittivity is compared with Peplinski model
- DiSense permittivity by time-domain velocity of propagation method is compared with Di-Sense path loss propagation permittivity method 
![](/assets/319-7.jpg)
- ##### Results:With decrease in lowest path loss frequency, soil permittivity increase rapidly, which also lead to increase in soil moisture. 

##### 4.3 Model error analysis
![](/assets/319-8.jpg)

##### 4.4 Di-Sense transfer functions
- effects of changes in soil permittivity with change in depth are likely to be reduced at higher depths due to the fact that intensity of the reflected wave from soil–air interface is reduced at the deeper depths
    - Determine the lowest path loss frequency.
    - Estimate soil permittivity using (5) and (6).
    - Estimate soil moisture using (7).
    ![](/assets/319-13.jpg)
    
#### 5. Di-Sense applications
- precision agriculture(IOUTs)
- determine the health of the buildings and bridges structures
- detect dynamic variations in the soil properties
- improve the performance of landmines detection approaches
- improve the design of wave propagation systems for tunnels through cognitively adjusting the communication parameters based on the sensing of moisture and permittivity
- in the area of the geophysical prospecting, where IOUT can be used simultaneously for sensing, communications, and permittivity estimation of the ice and rocks.

#### 6. Conclusion
- wireless UG channel path loss and velocity of wave propagation in soil medium have been utilized to determine the permittivity and soil moisture
- Di-Sense is based on estimation of the frequency of the lowest path loss of the direct communication link between the buried antennas in soil