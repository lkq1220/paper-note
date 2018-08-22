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
-  Estimat the effective frequency of the TDR signal in the soil, which is the frequency that contains the majority of the energy of the signal, by calculating the rise time of the signal at the end of the TDR probe (Figure 2). The rise time of the signal is commonly calculated based on the 10% to 90% increase in the reflection coefficient at the end of the probe.Figure 2 illustrates the proposed method for calculating the rise time of a waveform when there are multiple end reflections with rise time, tr, and travel time, t1, of the signal indicated.
![](/assets/8221.jpg)
###### Figure 2. The proposed method of calculating the rise time in TDR waveforms with end reflections
- The permittivity is then used as an input to the Modified-Friis model to estimate the attenuation, which eliminats potential inaccuracies associated with this mixing model. 

#### 3.2. Trial Setup
- During this research,the attenuation of RF signals in soil were measured at three separate locations to provide a varied set of data for testing the performance of the models.The locations of the trials were selected to have different soil types and conditions.
- During this project a WUSN node developed during the research was used as the transmitter with fixed frequencies of 433 MHz and 868 MHz. 
-  Figure 3 shows a schematic of the trials
![](/assets/8222.jpg)
###### Figure 3. Schematic of the RF trials
- The main parameters that can potentially negatively affect RF trials
  - antenna orientation
  - soil disturbance 
  - instrument characteristics
### 4. Results and Discussion
- ##### The results from the soil characterisation tests for all of the locations (A, B and C) are presented in Table 1.
###### Table 1. Soil characteristic of location A, B and C (GWC: gravimetric water content, "’ real part of the permittivity, "” imaginary part of the permittivity, σDC bulk conductivity).
![](/assets/8223.jpg)
- ##### Figures 4–6 illustrate the measured attenuation of the signal at locations A, B and C respectively. 
![](/assets/8224.jpg)
###### Figure 5. Comparison of the measured attenuation with the propagation models (location A)
![](/assets/8225.jpg)
###### Figure 5. Comparison of the measured attenuation with the propagation models (location B)
![](/assets/8226.jpg)
###### Figure 5. Comparison of the measured attenuation with the propagation models (location C)

### 5. Conclusion
- A robust, reliable and easy-to-use method for approximation of the attenuation in soil can hugely benefit the development and deployment of WUSNs. 
- The Modified-Friis model for estimating signal attenuation more closely fitted the field data compared to the CRIM-Fresnelmodel.
- The use of the TDR measured permittivity is suggested to improve the accuracy of the Modified-Friis model as it is based on measurements of the dielectric parameters of the soil at the WUSN location.In addition, it removes the need for laboratory-based tests for calculating the dielectric parameters, which makes it more suitable for field use.
- These comparisons showed that in all three field trial locations the Modified-Friis model with the complex permittivity extracted from TDR data of the soils provided a better estimation of the RF attenuation over the distances measured. 