# Harmonic-Drive-Dataset

Harmonic drives are precision components essential for motion performance in industrial robots, yet their fault diagnosis remains underdeveloped due to a lack of comprehensive reviews and publicly available real-world data.

Existing studies often focus on individual components or artificially induced faults, which do not fully represent the complex operational behavior and fault modes of complete drives under actual working conditions.

To address these gaps, we presents a systematic review of intelligent fault diagnosis and prognostics methods for harmonic drives. Furthermore, we release **GD-HDD**, among the first open-source, multimodal fault datasets for industrial robotic harmonic drives, collected and validated in collaboration with manufacturers.

The dataset includes:
- Synchronized vibration, servo motor, and high-precision metrology data
- 12 operating conditions
- 7 common faults, 3 dual compound faults, and 1 triple compound fault
- Associated technical documentation

By integrating a methodological review with a real-world benchmark dataset, this work aims to accelerate research and deployment of reliable health management systems for harmonic drives.

---

## 📊 Dataset 1

- **Setup and Data Collection**

The test platform includes an industrial robot with a rated load of 8 kg, 8 harmonic drives, an SKF vibration analyzer, 3 vibration acceleration sensors (SKF MODEL CMSS2200), and a laptop. The robot vibration experiment platform is shown in Fig. 1. The SKF vibration analyzer is set to Hanning-window sampling. The sampling frequency is 512 Hz and the lower bound cut off frequency is 0.1Hz.The experimental studies only focus on the operating state of the harmonic drive installed on the fifth axis of the robot. 
The fifth axis is used to perform a reciprocating rotary motion. A schematic diagram of the transmission chain of the fifth axis of the industrial robot is given in Fig. 2. The transmission route of Joint 5 of the industrial robot is that the motor drives the pulley, and transmits the motion to the harmonic drive through the belt drive, and finally transmits the motion to the tool end connected to the harmonic drive. The three acceleration sensors are respectively fixed on the end-load of the robot according to the mutually orthogonal directions of X, Y, and Z, and are used to record the vibration acceleration data of the end of the industrial robot during the movement.

<img width="525" height="393" alt="image" src="https://github.com/user-attachments/assets/e94332a0-6249-4f44-8eff-25f613d5ee5f" />

Fig. 1.  Robot vibration experiment platform.

<img width="452" height="195" alt="image" src="https://github.com/user-attachments/assets/b4ed2c65-eb33-4e2a-91b8-58495db73ab8" />

Fig. 2.  Schematic diagram of the fifth axis of the robot.

The loads to be tested are no-load, 3 kg, and 8 kg. The 5th-axis motor is tested under four levels of speeds, which are super high (S), high (H), medium (M), and low (L) corresponding to 4985, 3739, 2492, and 1247 r/min respectively. The 5-axis reduction ratio provided by the manufacturer is 84.1666.

Dataset 1 can be used for:
- **Exp. 1. Binary Health Classification**
- **Exp. 2. Multi-Class Fault Identification Under Noise**

📥 **Download link**: [Download Dataset 1](https://pan.baidu.com/s/1ds8mO8smnVkFmTcC-XEChw?pwd=r9qu) — **Access code:** `r9qu`

---

## 📊 Dataset 2

- **Setup of the Experimental platform**

The industrial robot vibration test bench includes a six-axis industrial robot, a servo controller, a SKF vibration analyzer (System: IMx-P), three vibration acceleration sensors (Model: CMSS2200), and a personal computer, as shown in Fig. 3. Three vibration acceleration sensors are installed orthogonally at the end of the industrial robot to collect the vibration signal of the robot. The 4th, 5th and 6th axes of industrial robots all use harmonic drives. During the experiment, the range of motion angles of the 4th, 5th, and 6th axes are ±1050, ±1230, and ±1100 respectively. The sampling frequency is 2560Hz.

The data-driven online intelligent fault diagnosis platform for harmonic drive mainly consists of an industrial robot (Model: RB08), control and servo systems, normal and fault harmonic drives, RS485 Fieldbus, laptop, and servo system online data acquisition software (the sampling frequency is 800Hz)

<img width="496" height="372" alt="image" src="https://github.com/user-attachments/assets/0c66c16c-dc91-46df-bbd3-7bffa9acb215" />

Fig. 3.  Industrial robot test bench.

To more clearly express the mechanical and physical mechanism of the 6-axis tandem industrial robot in the vibration test bench, the structure diagram of the whole machine is shown as follow:

<img width="447" height="247" alt="image" src="https://github.com/user-attachments/assets/2123eb32-1229-4bf6-a705-501717b7616d" />

Fig. 4.  Schematic diagram of the mechanical structure of an industrial robot.

The schematic diagram of the industrial robot is shown in Fig. 4. The 1st axis, the 2nd axis, and the 3rd axis are driven by RV gears. The RV reducer has the characteristics of simple structure, high reliability, and few failures. The harmonic drives of the 4th axis, 5th axis and, 6th axis adopts the principle of harmonic transmission instead of gear transmission. The harmonic drive is composed of a wave generator, flexspline, and circular spline. It relies on the elastic deformation of the flexspline to realize movement transmission. Besides, the harmonic drive is extremely sensitive to the manufacturing process and assembly errors. Therefore, multiple harmonic drives of industrial robots sometimes will cause abnormal vibrations at the same time.

The physical structures of the various types of harmonic drives in Fig. 4 are different, so their fault characteristics are also different. We use the frequency in Table II to observe their motion characteristics. The frequency spectrum of the collected vibration signal contains the frequency components of various parts, such as motor, pulley, camshaft, flexspline, and circular spline. The various input speeds of the motor will run under 3 different levels of payload (0/3/8Kg). In Table II, the motors used for driving have four speeds of 1247/2492/3739/4985 (r/min), corresponding to L/M/H/S respectively. These frequency components will be used for subsequent neural network analysis. The different types of harmonic drives are respectively installed in the 4th, 5th, and 6th axis of the industrial robot, and the reduction ratio of these products is 50/100/50 respective. Due to the consideration of external output connection (belt and pulley), the total revised reduction ratio of these products is 74.538/84.1666/50 respective.

### Sensors for Servo Systems — Multimodal Data

| Sensor | Data Type | Unit |
| :--- | :--- | :---: |
| **Electromotor Encoder** | Position command value | Pulse |
| | Position actual value | Pulse |
| | Position tracking error actual value | Pulse |
| | Actual speed feedback value | r/min |
| | Feedforward speed command value | r/min |
| **Hall Current Sensor** | Torque command value | mNm |
| | Actual torque observations | mNm |
| | Torque current command value | mArms |

Dataset 2 can be used for:
- **Exp. 3. Compound Fault Diagnosis**
- **Exp. 4. Semi-Supervised and Few-Shot Learning**
- **Exp. 5. Multimodal Learning with Missing Modalities**

📥 **Download link**: [Download Dataset 2](https://pan.baidu.com/s/18rAPZnf7yfrepi6iycIqLw) — **Access code:** `khfx`

---

## 📄 Dataset Access and Usage License

- **License**: This dataset is released under the [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/). 
- **Access**: The complete dataset, including sensor data, reports, and loader script, is available at: https://github.com/GDUT-YANGGUO/Harmonic-Drive-Dataset
- **Citation**: If you use this dataset, please cite the following paper:
  > G. Yang, Z. Zhao, Y. Deng, R. Du and Y. Zhong, "Artificial Intelligence for Fault Diagnosis in Harmonic Drives of Industrial Robots: A Comprehensive Real-World Dataset and a Review," in *IEEE/ASME Transactions on Mechatronics*, doi: 10.1109/TMECH.2026.3699839.
