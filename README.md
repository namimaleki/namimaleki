# Hi there, I'm Nami Maleki! 👋

<div align="center">

## About Me

</div>

### 🎓 Education
Computer Engineering and Mathematics  
University of British Columbia  
Expected Graduation: 2027

### 💡 Interests
I'm an ambitious and driven student who thrives on intellectual challenges and solving complex problems. My passion for understanding how things work at a fundamental level led me to pursue both computer engineering and mathematics. I'm constantly pushing myself to explore difficult concepts and expand my knowledge across multiple disciplines.

I'm particularly fascinated by robotics, machine learning, physics, and game theory. Beyond academics, I enjoy playing basketball, soccer, and volleyball. I push myself physically through running and weight lifting, and in my free time, I enjoy reading, playing chess, and spending time with friends and family.


<div align="center"> 

## Projects 

</div>

### 🧠 [DeepChessEval](https://github.com/yourusername/DeepChessEval)


- Built a convolutional neural network to evaluate chess positions, achieving 
  ±0.23 pawn accuracy on 100K+ unseen positions (validation MSE: 0.048)
  
- Designed complete end-to-end ML pipeline from scratch: automated PGN parsing,
  Stockfish engine integration, custom tensor encoding (12×8×8), and PyTorch
  training with validation monitoring
  
- First ML project - learned full development cycle including data collection,
  preprocessing, model architecture design, training optimization, and debugging
  overfitting issues through validation analysis
---

### 🤖 Real-Time-Embedded-Control-Platform (https://github.com/namimaleki/Real-Time-Embedded-Control-Platform)

- Architected and implemented complete robotics-style firmware achieving <50µs timing 
  jitter at 200Hz control frequency through FreeRTOS deterministic scheduling—performance 
  matching commercial robotics platforms

- Engineered hardware drivers (I²C IMU sensor, PWM actuator control) and thread-safe 
  inter-task communication pipeline (FreeRTOS queues/mutexes) with comprehensive error 
  handling and safety systems (emergency stop, deadline detection, SAFE mode)

- Integrated PID control algorithm creating closed-loop sensor-to-actuator system, 
  demonstrating professional embedded development practices directly applicable to 
  autonomous robotics systems


### ⚙️ [Simple RISC Machine (SRM) Processor](https://github.com/yourusername/SimpleRISC)
A **custom 16-bit processor** designed and simulated on the DE1-SoC FPGA.

- Planned and implemented a 16-bit RISC processor in Verilog, beginning with block diagrams and cycle-level timing plans to design a modular datapath (ALU, register file, shifter, multiplexers) for arithmetic and logic execution
- Developed a Finite State Machine controller by mapping instruction cycles and drafting state-transition diagrams, implementing an instruction decoder and custom ISA for coordinated instruction control
- Used ModelSim to simulate and visualize processor signal waveforms, verifying correct instruction    execution and timing before synthesis and deployment on the DE1-SoC FPGA using Quartus
- Developed SystemVerilog test benches to validate branching, load/store, and memory-mapped I/O operations


---

### 🤖 [Panorama Telemetry System](https://github.com/namimaleki/Panorama)
An **ESP32-based telemetry platform** for real-time sensor data acquisition.

- Implemented a C++ **DataBuffer class** for efficient data logging and JSON serialization  
- Built wireless data transmission over **Wi-Fi (ESP-IDF)** with live dashboard integration  
- Designed a modular backend for multiple sensor nodes (IMU, temperature, GPS)  

---
