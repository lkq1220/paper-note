## Bag-of-visual-phrases and hierarchical deep models for traffic signdetection and recognition in mobile laser scanning data
### 1. Results and discussion
#### 1.1  RIEGL VMX-450 system and MLS data sets
- RIEGL VMX-450 system
  - aim
    - collect both point clouds and images in Xiamen City, China.
  - composition
    - two RIEGL VQ-450 laser scanners
    - four 2452*2056 pixels CS6 color cameras
    - an integrated IMU/GNSS/DMI position and orientation system
  - ability
    - a maximum effective measurement rate of 1.1 million measurements per second
    - a line scan speed of up to 400 lines per second
    - a maximum valid range of 800 m
    
- data sets
  - where
    - Ring Road South (RRS)
    - Xiahe Road (XHR)
    - Zhongshan Road (ZSR)
    - Hubin Road West(HRW)
    
    ![](/assets/table1.png) 
 -  Build the visual phrase dictionary
   - selected a total number of 80 point cloud segments(50 m) at random
   - ground point removal
   - train the DBM-based feature encoder
 - train the supervised GaussianBernoulli DBM model(for traffic sign recognition)
   - collected a set of standard traffic sign pictograms
   ![](/assets/pic3.jpg)
   - resized into a square shape with a size of 80*80 pixel
   - each traffic sign pictogram was processed
     - illumination changes
     - rotations
     - Gaussian-noise contaminations 
   - 161,792 training samples was used to train the Gaussian-Bernoulli DBM model.
     
#### 1.2 Parameter sensitivity analysis
- Three parameters (impact traffic sign detection performance based on 3D point clouds)
  - feature region construction pattern
    - single supervoxels
    - the combination of supervoxels and their first-order neighbors
  - visual phrase dictionary size (K)
    - K = 90,000, 100,000,110,000, 120,000, 130,000, 140,000. 
  - spatial word pattern size (Np)
    - Np = 1, 2, 3, 4, 5, 6
- result
  - feature regions with first-order neighborhood information can produce more meaningful, salient, and distinctive feature encodings 
  -  the more the visual phrases in the dictionary, the higher degrees of distinctions between different categories of objects.(exceeds 120,000, performance is stable.)
  -  obtain salient, distinctive feature encodings(when Np P 5, the detection performance drops dramatically)
  ![](/assets/pic2.png)

#### 1.3 Traffic sign detection on point clouds and images
-  evaluate the performance of traffic sign detection algorithm
  - the aforementioned four data sets
  - the optimal parameter configurations
  
  ![](/assets/pic4.jpg)
  - constructed a 6480-1000-1000-100 DBM-based feature encoder(generate high-order feature encodings of feature regions)
  - detect traffic signs of different shapes
