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
- Permittivity estimation through velocity of wave propagation in soil
  - Power delay profile (PDP) are measured to get velocity of the wave propagation
  - Relative permittivity in soil is calculated from the difference of transmission and arrival time of the direct component in the soil
  ![](/assets/319-2.jpg)
- Di-Sense soil moisture sensing
    - soil permittivity depends on the soil moisture only, soil water content can be determined from soil permittivity

#### 3. Model validation techniques

#### 4. Empirical setup
#### 5. Performance analysis, model validation, and error analysis
#### 6. Di-Sense applications and future work