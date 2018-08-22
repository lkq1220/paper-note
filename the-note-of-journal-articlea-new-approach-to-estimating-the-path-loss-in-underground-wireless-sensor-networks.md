##  A New Approach to Estimating the Path Loss in Underground Wireless Sensor Networks
### 0. Abstract
- ##### Why
  - Due to the complexity of soil, accurate estimation of the underground signal attenuation is challenging.
- ##### What
  - In this paper, two existing models for estimating the path loss in soil (i.e., the CRIM-Fresnel and Modified-Friis models) are compared with measurements obtained at three locations. In addition,an improved method is proposed for estimating the path loss based on a new approach for calculating the dielectric properties of soil from Time Domain Reflectometry (TDR) measurements.
- ##### New approach 
  - Calculates the complex permittivity values from TDR waveform based on a new modified
method and subsequently use them as inputs into the Modified-Friis model.
- ##### Result
  - The results of this comparison showed that the proposed estimation technique provides a better estimation of Radio Frequency (RF) attenuation than the existing models.
  
### 1. Introduction
- ##### Main Challennes For WUSNs
  - the lack of available power
  - large path loss(caused by the poor radio frequency transmission throngh soil)

- ##### Three Categories Of Signal Transmission(Figure 1 shows a schematic of a typical WUSN used for pipeline monitoring.)
  - UG2UG
    - the topsoil(0-30cm depth)
    - the subsoil(>30cm depth)*
        - majority of buried infrastructure (e.g., water pipes) is placed in the subsoil region
  - UG2AG
  - AG2UG
  
  ![](/assets/8220.jpg)
  ###### Figure 1. Schematic of a typical WUSN for pipeline monitoring
  
- ##### affect the attenuation of EM signals by changing the dielectric properties of soil
  - soil water content*
  - soil composition*
    - air
    - water
    - bulk soil
  - soil density
  - these properties are not constant and can vary due to environmental factors*

- ##### Two method to estimate the Dielectric properties
  - Time Domain Reflectometry (TDR)
  - Vector Network Analyser (VNA) measurements

- ##### Field Test
  - Compares the accuracy of common models for the estimation of RF attenuation with experimental measurements of attenuation in soil that have been undertaken at three separate field trial locations each having different soil compositions and conditions.
  - A new approach for the TDR extracted permittivity values are then applied to the Modified-Friis model

### 2. RF Signals in Soil
#### 2.1  Dielectric Properties of Soil
- ##### The key dielectrics parameters(Underground path loss estimation models)
  - soil complex dielectric permittivity
    -  signifies the ability of a dielectric medium to permit the transmission of an electric field
    - the main parameters affecting the permittivity
      -  water content
      - the frequency of the signal
      - the soil composition 
      - the soil conductivity(土壤电导率)
  - soil electrical conductivity 
    -  the ability of the material to conduct electrical currents
  - soil magnetic permeability（the relative magnetic permeability）
    -  the ratio between the magnetic permeability of soil and free space（For most common types of soil the relative magnetic permeability of soil can beassumed to be 1）

#### 2.2. Propagation Models
- ##### The two main models in the literature are the CRIM-Fresnel model and the Modified-Friis model. Both of these models are based on the “link budget” formula. 
$$
P_r = P_t + G_r + G_t − L_0 − L_m
$$
where $$L_m$$ is the path loss in soil (medium) due to material absorption (dB), $$L_0$$ is the path loss infree space (dB), $$G_t$$ and $$G_r$$ are the transmitter and receiver antenna gains (dB) and $$P_t$$ and $$P_r$$ are thetransmitter and receiver powers (dB).
- ##### Based on the Modified-Friis model,the total losses of an EM signal in soil(Lp)
$$
L_p = 6.4 + 20 log(d) + 20 log(β) + 8.68αd
$$
- ##### The CRIM-Fresnel model also considers losses due to reflection in the calculations of total attenuation，$$A_(tot)$$ in soil.However,the CRIM-Fresnel model itself was developed based on a very limited soil types and conditions. 
$$
A_(tot) = α_cd + R_c
$$
- ##### A common drawback of both of these models
  -  their accuracy is largely dependent on the accuracy of the mixing model used
  -  require a sample of the soil to be analysed in the laboratory which makes them unsuitable for scenarios
  - a large discrepancy between the estimated attenuation of EM signals determined from these models

### 3. TDR and Field Trials
#### 3.1. Proposed Path Loss Estimation Method
#### 3.2. Trial Setup
### 4. Results and Discussion
### 5. Conclusion
A robust, reliable and easy-to-use method for approximation of the attenuation in soil can hugely benefit the development and deployment of WUSNs. 