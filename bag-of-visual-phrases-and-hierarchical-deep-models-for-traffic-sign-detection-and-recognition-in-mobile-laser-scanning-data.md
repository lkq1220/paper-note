##### The ISPRS Journal of Photogrammetry and Remote Sensing is the official journal of the International Society for Photogrammetry and Remote Sensing (ISPRS). The journal is to provide a channel of communication for scientists and professionals in all countries working in the many disciplines employing photogrammetry, remote sensing, spatial information systems, computer vision, and other related fields. 
ISPRS摄影测量与遥感杂志是国际摄影测量与遥感学会(ISPRS)的官方刊物。该杂志将为所有国家从事摄影测量、遥感、空间信息系统、计算机视觉和其他相关领域的许多学科的科学家和专业人员提供交流渠道。

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
- Dection result
  - a part of traffic sign detection results in 3-D point clouds. (a) A raw point cloud, and (b) detected traffic signs
  ![](/assets/pic5.jpg) 
  - a subset of detected traffic signs on 2-D images.
  ![](/assets/pic6.jpg)
  - (a) falsely detected non-traffic sign objects, and (b) undetected traffic signs.
  ![](/assets/pic7.jpg)
  - evaluated the traffic sign detection performance in challenging image scenarios(Examples of traffic signs detected in challenging scenarios. (a) Strong illuminations, (b) poor illuminations, (c) large viewpoints, (d) partial occlusions, and (e)cluttered backgrounds)
    - strong illuminations
    - poor illuminations
    - large viewpoints
    - partial occlusions,
    - cluttered backgrounds
  ![](/assets/pic8.jpg)
- conclusion
  - 3-D point clouds provide real-world 3-D geometric topologies of traffic signs and are immune to environmental illumination conditions, traffic signs can be effectively detected from 3-D point clouds without the impact of viewpoint variations and illumination variations that often occur in 2-D images.
##### 1.3.1 Performance evaluation
- four indices
  - recall
    - the proportion of true positives in the ground truth
  - precision
    - the proportion of true positives in the detected components
  - quality
  - F-score
    - 精确率和召回率都越高越好。但通常情况下，二者会此消彼长，不可兼得，所以我们使用调和平均数
- The quantitative evaluation results
  - an average recall, precision, quality, and F-score of 0.956, 0.946, 0.907, and 0.951
  ![](/assets/pic9.jpg)
  
##### 1.3.2 Comparative studies of using different 3-D descriptors
- three method in exploiting salient, distinctive features of feature regions
  - 3-D shape context (3DSC)
  - fast point feature histograms (FPFH)
  - DBM-based feature encoder
- result
  - the 3DSC and the FPFH descriptorscan only obtain low-order statistical features.
  -  the DBM-based feature encoder can obtain high-order abstract feature representations
 ![](/assets/pic10.jpg)

##### 1.3.3 Comparative studies with point cloud based traffic sign detection methods
-  traffic sign detection algorithm
  - Hough forest-based method (HF)
  - supervoxel neighborhood-based Hough forest method
  - 3-D object matching-based method (OM)
  - intensity-based pole-like object detection method (IPLO)

##### 1.3.4 Comparative studies with image-based traffic sign detection methods
- three image-based traffic sign detection methods
  - template matching (TM) method
    - regions of interests (ROIs) are extracted based on color segmentation
    - the shape of each ROI is fitted using simple geometric forms
    - a template matching process is performed to detect traffic signs
  - graph-based ranking and segmentation (GRS) method
    - a superpixel-based graph is designed to represent an input image
    - a ranking algorithm is applied to exploit the intrinsic manifold structure of the graph nodes 
    - a multithreshold segmentation approach is proposed to segment traffic sign regions.
  - color probability model (CPM) method
    - an input image is transformed to traffic sign probability maps by using a color probability model
    - traffic sign proposals are extracted by finding maximally stable extremal regions from the probability maps
    - an SVM is used to detect traffic signs from the traffic sign proposals.
- Result 
![](/assets/pic11.jpg)

#### 1.4 Traffic sign recognition on images
- classify these traffic signs into specific categories
  - projected them onto the images to obtain traffic sign regions
  - the obtained traffic sign regions were resized into a square shape with a size of 80  80 pixels
  -  constructed a 6400-1000-1000-500-35 hierarchical classifier to classify the detected traffic signs into 35 categories
- result
  - a totalnumber of 1227 traffic signs out of 1258 traffic signs were successfully assigned to correct categories.
- The misclassification was basically caused by the following three factors:
  - extremely strong or poor illuminations
  - very large viewpoints
  - serious occlusions
  
####1.4.1 Comparative studies
- Traffic sign recognition algorithm
  - MSERs method
  - SRGE method
  - Color Global LOEMP method
  - CNN method
    - have the capability of handling various traffic sign distortions
      - illumination variations
      - viewpoint variations
      - noise contaminations
      
![](/assets/pic12.jpg)
