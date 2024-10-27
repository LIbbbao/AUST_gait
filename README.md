# AUST_gait
AUST-gait数据集及介绍。(AUST-gait dataset and introduction.)
## 简介：
AUST-gait 数据集由安徽理工大学采集，专为步态分析设计，支持时间序列预测和分类任务。该数据集通过可穿戴髋关节外骨骼机器人收集，包含多种传感器数据，适用于研究缺失值处理和步态识别。

采集设备与传感器:
- **设备**：髋关节外骨骼机器人。
- **传感器**：
    - 6轴 IMU传感器：安装于背部，测量三轴加速度和角速度
    - 电机轴编码器和12位输出轴编码器：测量左右髋关节的角度和角速度

## 实验过程招募了65 名健康成年人（年龄23±2 岁，身高1.74±0.05 米，体重80±8.6 千克），排除特定条件人群（实验获得伦理委员会批准，参与者签署知情同意书）。
**参与者在监督下执行四种行走模式**：  
1. 平地行走（FG）：在6 米长、1.2 米宽的跑道上来回行走3 次。
2. 上楼梯（SA）：登上10级台阶楼梯（每级15 厘米），重复3 次。
3. 下楼梯（SD）：走下10级台阶楼梯，重复3 次。
4. 倾斜跑步机行走（IT）：在倾斜20°的跑步机上行走45 秒。  
**此外，进行了摔倒实验以模拟极端情况**。

## 数据说明- **特征格式**：每个时间点包含13 个特征，记录在 Excel 单元格内，时间间隔为20ms。        
**特征包括**：
 - 左髋角度
 - 右髋角度
 - 左髋角速度
 - 右髋角速度
 - 背部 IMU X轴加速度
 - 背部 IMU Y轴加速度
 - 背部 IMU Z轴加速度
 - 背部 IMU X轴角速度
 - 背部 IMU Y轴角速度
 - 背部 IMU Z轴角速度
 - 背部 IMU X轴欧拉角
 - 背部 IMU Y轴欧拉角
 - 背部 IMU Z轴欧拉角
 
**标签（最后一列标注行走类别）**：  
 - 0：平地行走
 - 1：上楼梯
 - 2：下楼梯
 - 3：倾斜跑步机行走
 - 4：摔倒实验  
 
**数据集结构**：  
 - 训练集：占比75%    
 - 测试集：占比25%  
 - 摔倒实验数据：可与其他数据集结合使用    
 
**任务**：   
 - 预测任务：学习前10 步数据，预测第11 步。    
 - 识别任务：分类不同的行走模式。    
 
**缺失值处理**：用户可使用多种算法模拟缺失值，数据集支持不同缺失率的实验。  

##许可证本数据集根据开放数据共享原则发布，用户可以自由使用、修改和分发，但需注明出处。

## 联系方式如有疑问或建议，请联系作者：mianchu.wang@warwick.ac.uk。

---
## Introduction
The AUST-gait dataset, collected by Anhui University of Science and Technology, is specifically designed for gait analysis, supporting time-series prediction and classification tasks. The dataset is collected through a wearable hip exoskeleton robot and contains various sensor data, suitable for research in missing value processing and gait recognition.

## Equipment and Sensors
- **Equipment**: Hip exoskeleton robot
- **Sensors**:
    - 6-axis IMU sensor: Mounted on the back, measuring three-axis acceleration and angular velocity
    - Motor shaft encoder and 12-bit output shaft encoder: Measuring angles and angular velocities of left and right hip joints

## Experimental Procedure
65 healthy adults were recruited (age 23±2 years, height 1.74±0.05 meters, weight 80±8.6 kg), excluding specific conditions. The experiment received ethics committee approval, and participants signed informed consent forms.

**Participants performed four walking modes under supervision**:
1. Flat Ground Walking (FG): Walking back and forth three times on a 6-meter long, 1.2-meter wide track
2. Stair Ascent (SA): Climbing a 10-step staircase (15cm per step), repeated 3 times
3. Stair Descent (SD): Descending a 10-step staircase, repeated 3 times
4. Inclined Treadmill Walking (IT): Walking on a treadmill inclined at 20° for 45 seconds  
**Additionally, fall experiments were conducted to simulate extreme conditions.**

## Data Description
**Feature Format**: Each time point contains 13 features, recorded in Excel cells with20ms intervals.

**Features Include**:
- Left hip angle
- Right hip angle
- Left hip angular velocity
- Right hip angular velocity
- Back IMU X-axis acceleration
- Back IMU Y-axis acceleration
- Back IMU Z-axis acceleration
- Back IMU X-axis angular velocity
- Back IMU Y-axis angular velocity
- Back IMU Z-axis angular velocity
- Back IMU X-axis Euler angle
- Back IMU Y-axis Euler angle
- Back IMU Z-axis Euler angle

**Labels (Walking categories in the last column)**:
- 0: Flat ground walking
- 1: Stair ascent
- 2: Stair descent
- 3: Inclined treadmill walking
- 4: Fall experiment

**Dataset Structure**:
- Training set: 75%
- Test set: 25%
- Fall experiment data: Can be combined with other datasets

**Tasks**:
- Prediction task: Learn from first 10 steps to predict the 11th step
- Recognition task: Classify different walking modes

**Missing Value Processing**: Users can employ various algorithms to simulate missing values, and the dataset supports experiments with different missing rates.

## License
This dataset is released under open data sharing principles. Users can freely use, modify, and distribute the data with proper attribution.

## Contact Information
For questions or suggestions, please contact the author: mianchu.wang@warwick.ac.uk


---

This README is formatted in Markdown and can be directly uploaded to a GitHub repository.
