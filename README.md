# Low-cost-mobile-navigation-using2D-SLAM-in-complex-environments

## Authors
Aicha Manar ABBAD, Ines HAOUALA, Amanzhol RAISOV, Roumaissa BENKREDDA

## Abstract
This research paper presents a low-cost mobile navigation system utilizing Simultaneous Localization and Mapping (SLAM) algorithms in complex dynamic environments. The study investigates the performance and effectiveness of four different SLAM algorithms: ORB-SLAM2, g-mapping, Hector SLAM, and Karto SLAM. The objective is to develop a cost-effective solution that enables accurate and real-time mobile navigation in challenging scenarios. We discuss and compare the strengths and limitations of these four algorithms to select the most appropriate one for a warehouse environment. Each algorithm is evaluated based on metrics such as Map and Pose Accuracy, CPU and Memory Utilization, Robustness, and Processing Time to ensure feasibility on low-cost mobile hardware.

## Introduction
Simultaneous Localization and Mapping (SLAM) is a fundamental problem in robotics, first introduced by researchers in 1986. SLAM addresses whether it is possible to deploy a mobile robot in an uncharted environment while simultaneously building a map and determining the robot's location using various sensors. SLAM faces challenges such as sensor noise and positional errors due to robot mobility.

### Purpose of this Research
With the growing needs of Industry 4.0, autonomous systems are becoming increasingly important. These systems must navigate complex environments, such as warehouses, which are dynamic and crowded with operators, packages, and vehicles. The aim of this research is to identify the best SLAM algorithm for mobile robots operating in such challenging environments, focusing on their ability to avoid deadlock states and maintain real-time coordination.

## Methodology

### Selection Criteria for SLAM Algorithms
Our research focuses on complex environments, specifically warehouses. Warehouses are dynamic spaces with numerous obstacles, varying lighting conditions, and unpredictable movement of objects. We selected the following five metrics to evaluate the SLAM algorithms and choose the optimal one for warehouse navigation:

- **Map Accuracy:** Assesses how accurately the algorithm maps the area by comparing the generated map with the ground truth.
- **Pose Accuracy (Relative Pose Error, RPE):** Measures the algorithm’s accuracy in estimating the correct pose based on the robot’s motion error.
- **CPU and Memory Utilization:** Evaluates the computational resources required by the algorithm to run SLAM.
- **Robustness:** Tests the algorithm's performance and consistency in challenging environments.
- **Processing Time:** Measures the real-time performance of the SLAM algorithm.

## Review of SLAM Algorithms

### Gmapping Algorithm
**Overview:** Gmapping is a widely used 2D-SLAM algorithm for indoor navigation using laser radar. It utilizes RBpf particle filtering for pose estimation and map creation.

**Advantages:**
- Efficient use of computational and memory resources.
- Accurate mapping in flat indoor environments.
- Strong performance in dealing with uncertainties.

**Limitations:**
- Computationally demanding in complex environments.
- Sensitive to sensor noise and odometry errors.
- Assumes a static environment, struggling with dynamic objects.

### ORB-SLAM2 Algorithm
**Overview:** ORB-SLAM2 is a visual SLAM algorithm that provides accurate camera trajectory and sparse 3D reconstruction. It supports monocular, stereo, and RGB-D cameras.

**Advantages:**
- Strong tracking capabilities with real-time performance.
- Supports multiple camera setups.
- Handles loop closures and relocalization effectively.

**Limitations:**
- Requires a trained vocabulary for feature matching.
- Dependence on relocalization for accurate localization.
- Unknown absolute scale in monocular mode.

### Karto-SLAM Algorithm
**Overview:** Karto SLAM is a graph-based SLAM algorithm optimized for 2D mapping. It uses Sparse Pose Adjustment (SPA) for efficient mapping and localization.

**Advantages:**
- Efficient and accurate mapping for 2D environments.
- Suitable for large environments due to graph optimization.
- Compatible with various platforms and hardware setups.

**Limitations:**
- Focused on 2D mapping, unsuitable for 3D applications.
- Computational complexity increases with the number of landmarks.
- Limited open-source development and community support.

### Hector-SLAM Algorithm
**Overview:** Hector SLAM is a mapping algorithm designed for LIDAR sensors, using grid mapping and pose matching to localize the robot.

**Advantages:**
- Real-time functionality, suitable for applications requiring swift navigation.
- Does not require odometry, reducing cumulative errors.

**Limitations:**
- May experience accumulated drift over time.
- Performance depends on sensor quality and limitations.

## Results

### Identification of the Most Efficient SLAM Algorithm
Based on the evaluation metrics:

- **Map Accuracy:** ORB-SLAM2 excels in accurate mapping.
- **Pose Accuracy:** g-mapping and Karto SLAM are more suited for 2D pose accuracy.
- **CPU and Memory Utilization:** ORB-SLAM2 is the most efficient.
- **Robustness:** ORB-SLAM2's versatility gives it an edge.
- **Processing Time:** ORB-SLAM2 performs best in real-time scenarios.

ORB-SLAM2 tends to be the best-performing algorithm overall. However, the choice of algorithm should consider specific application requirements, hardware constraints, and cost considerations. Further testing on real-world data is necessary to validate performance in the warehouse environment.

### Limitations and Future Research
- **Lack of Real-Time Testing:** Algorithms were not tested in real-time on concrete environments or platforms like MATLAB or ROS. Future work should focus on real-world testing.
- **Hardware Constraints:** Future studies should conduct experiments on a variety of low-cost mobile robot platforms.
- **Specific Environment:** The findings might not fully translate to other dynamic environments, requiring additional tests in various settings.

## Conclusion
This research aimed to develop a low-cost mobile navigation system using SLAM algorithms for complex dynamic environments, specifically warehouses. ORB-SLAM2 emerged as the top-performing algorithm, particularly in map accuracy, CPU and memory utilization, and real-time processing. However, g-mapping and Karto SLAM may be more suitable for certain 2D applications. Further real-world testing and validation are needed to confirm the effectiveness of the selected algorithm in the targeted environment.

For more detailed insights, you can [read the full paper on ResearchGate](https://www.researchgate.net/publication/372690429_Low_cost_mobile_navigation_using_2D-SLAM_in_complex_environments).


