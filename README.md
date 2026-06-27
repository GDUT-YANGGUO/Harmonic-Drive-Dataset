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

📥 **Download link**: [Download Dataset 1](http://xxxxx1122) 

---

## 📊 Dataset 2

Dataset 2 can be used for:
- **Exp. 3. Compound Fault Diagnosis**
- **Exp. 4. Semi-Supervised and Few-Shot Learning**
- **Exp. 5. Multimodal Learning with Missing Modalities**

📥 **Download link**: [Download Dataset 2](http://xxxxx1122) 

---

## 📄 Dataset Access and Usage License

- **Access**: The complete dataset, including sensor data, reports, and loader script, is available at:  
  https://github.com/GDUT-YANGGUO/Harmonic-Drive-Dataset

- **License**: The dataset is released for non-commercial, academic research purposes only. Use of the dataset requires citation of this article.

- **Citation**:
  > G. Yang, Z. Zhao, Y. Deng, R. Du and Y. Zhong, "Artificial Intelligence for Fault Diagnosis in Harmonic Drives of Industrial Robots: A Comprehensive Real-World Dataset and a Review," in *IEEE/ASME Transactions on Mechatronics*, doi: 10.1109/TMECH.2026.3699839.
