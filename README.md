# Hi there, I'm Nami Maleki! 👋

<div align="center">

## About Me

</div>

### 🎓 Education
Computer Engineering and Mathematics
University of British Columbia
Expected Graduation: 2028

### 💡 Interests
I'm an ambitious and driven student who thrives on intellectual challenges and solving complex problems. My passion for understanding how things work at a fundamental level led me to pursue both computer engineering and mathematics. I'm constantly pushing myself to explore difficult concepts and expand my knowledge across multiple disciplines.

I'm particularly fascinated by robotics, machine learning, physics, game theory, and finance. Beyond academics, I enjoy playing basketball, soccer, and volleyball. I push myself physically through running and weight lifting, and in my free time, I enjoy reading, playing chess, and spending time with friends and family.



<div align="center">

## Design Teams

</div>

### 🤖 UBC Open Robotics

### Haptic Knob — Firmware Member *(Dec 2025 – Present)*
A 1-DOF rotational haptic interface that lets users **physically feel** electrical circuits (R, L, C, RLC, and diodes) by converting circuit equations into real-time force feedback through a motorized knob.

- Developing **ESP32 C/C++ firmware** for a deterministic real-time haptic loop that reads knob motion (angle/velocity/acceleration), computes a target response from circuit models, and commands motor torque so users can feel behaviors like damping, oscillation, and diode-like one-way resistance
- Implementing the electrical-to-mechanical mapping in code: **voltage → torque**, **current → angular velocity**, **charge → angular displacement**, and **dI/dt → angular acceleration**, enabling resistor/capacitor/inductor/RLC/diode modes with tunable parameters (R, L, C, diode threshold, torque/current limits)
- Implementing a Kalman filter for real-time state estimation to produce low noise angle and angular velocity from encoder measurements, reducing noise effects and improving control stability
- Designing a PID current controller that minimizes error between desired (model) current and measured current, outputting PWM through a 3-phase BLDC driver to achieve accurate torque control
- Integrating and validating low-level peripherals and drivers (encoder feedback, current sensing via external ADC, SPI bus configuration, motor driver control) and ensuring stable closed-loop behavior under real hardware constraints (sensor scaling, noise, saturation, timing jitter)
- Building safety-critical behavior around the control loop, including watchdog/heartbeat monitoring, fault detection and latching (invalid samples, missed deadlines, unsafe commands), and a safe-state motor disable path to protect users and hardware



### Panorama Telemetry System (ESP32) — Software Member *(Sep 2025 – Dec 2025)*
A robust, scalable **end-to-end telemetry platform** that collects, transmits, and displays sensor data, command information, and robot state through a custom GUI.

- Implemented a C++ **DataBuffer** module for efficient sensor/state logging and serialization to support reliable telemetry streaming
- Contributed to the end-to-end telemetry workflow (data collection → transmission → GUI visualization) designed to scale across future robotics projects and new sensor types



<div align="center">

## Projects

</div>

### ROS2 Autonomous Racing (F1TENTH) (Code available upon request)
A team-built ROS2 autonomous racing stack running on **Ubuntu** on an **NVIDIA Jetson**, combining **LiDAR geometry** and **vision** to achieve reliable autonomous driving with safety-first command arbitration.

- Worked in a 6-person team to design and integrate a modular Python ROS2 autonomy pipeline (perception → planning → control), coordinating interfaces across nodes and topics
- Implemented and tuned LiDAR-based navigation behaviors including wall-following PID and gap-following (open-path) driving using scan preprocessing and geometric reasoning
- Contributed to a safety-critical SafetyNode using time-to-collision (TTC) logic for automatic emergency braking, designed to override nominal driving when collision risk is detected
- Helped build a priority-based DriveMux multiplexer to arbitrate commands (safety > wall-follow > gap-follow) and publish the highest-priority recent command to `/drive`
- Integrated OpenCV vision pipelines (camera-based color/feature detection + landmark/lap logic) and supported on-car testing, debugging, and parameter tuning on real hardware

### [DeepChessEval](https://github.com/namimaleki/DeepChess.git)
- Built a convolutional neural network to evaluate chess positions, achieving ±0.23 pawn accuracy on 100K+ unseen positions (validation MSE: 0.048)
- Designed complete end-to-end ML pipeline from scratch: automated PGN parsing, Stockfish engine integration, custom tensor encoding (12×8×8), and PyTorch training with validation monitoring
- First ML project - learned full development cycle including data collection, preprocessing, model architecture design, training optimization, and debugging overfitting issues through validation analysis



### [Real-Time-Embedded-Control-Platform](https://github.com/namimaleki/Real-Time-Embedded-Control-Platform)
- Architected and implemented complete robotics-style firmware achieving <50µs timing jitter at 200Hz control frequency through FreeRTOS deterministic scheduling—performance matching commercial robotics platforms
- Engineered hardware drivers (I²C IMU sensor, PWM actuator control) and thread-safe inter-task communication pipeline (FreeRTOS queues/mutexes) with comprehensive error handling and safety systems (emergency stop, deadline detection, SAFE mode)
- Integrated PID control algorithm creating closed-loop sensor-to-actuator system, demonstrating professional embedded development practices directly applicable to autonomous robotics systems



### [OS/161 Kernel](https://github.com/namimaleki/OS161)
- A Unix-like operating system kernel built by extending OS/161 with real synchronization, system calls, and virtual memory.
- Implemented core synchronization primitives (locks built using binary semaphores, condition variables using wait channels) and used them as the foundation for safe, race-free kernel concurrency across the project
- Added essential system call functionality to support real user programs, including file I/O (open/read/write/close/lseek/dup2/chdir/getcwd) and process management (fork/execv/waitpid/getpid/exit)
- Built a custom virtual memory system to replace DUMBVM, handling TLB faults and page-level memory management, and supporting dynamic heap growth via sbrk so user programs can allocate memory at runtime


### [Simple RISC Machine](https://github.com/namimaleki/Simple-RISC-Machine)
A **custom 16-bit processor** designed and simulated on the DE1-SoC FPGA.

- Planned and implemented a 16-bit RISC processor in Verilog, beginning with block diagrams and cycle-level timing plans to design a modular datapath (ALU, register file, shifter, multiplexers) for arithmetic and logic execution
- Developed a Finite State Machine controller by mapping instruction cycles and drafting state-transition diagrams, implementing an instruction decoder and custom ISA for coordinated instruction control
- Used ModelSim to simulate and visualize processor signal waveforms, verifying correct instruction    execution and timing before synthesis and deployment on the DE1-SoC FPGA using Quartus
- Developed SystemVerilog test benches to validate branching, load/store, and memory-mapped I/O operations



### [UNIX Shell](https://github.com/namimaleki/Unix-Shell)
A simplified **Unix-style shell** focused on process management and job control.

- Built a functional shell supporting foreground/background execution using `fork`, `execvp`, and `waitpid`
- Implemented signal handling to support suspending, resuming, and terminating jobs reliably
- Designed job tracking structures and built commands like `jobs`, `fg`, `bg`, and `nuke` to manage running processes cleanly



### [Virtual Memory System Emulator](https://github.com/namimaleki/Virtual-Memory-System)
A simplified **virtual memory simulator** modeling real OS memory translation and paging behavior.

- Implemented two-level page tables with address translation and permission enforcement
- Added swapping + eviction policies to manage limited physical memory under pressure
- Extended the system with an accessed-bit eviction strategy that favors untouched pages for better efficiency



> **Note:** Code will be provided upon request for the following projects.

### Baccarat FPGA Datapath + FSM
A SystemVerilog datapath + controller implementing the Baccarat game flow on the DE1-SoC FPGA.

- Designed and implemented a hierarchical SystemVerilog datapath + FSM controller to execute the full deal/score sequence (reg-based card storage, scorehand compute, and winner LEDs) on the DE1-SoC
- Built self-checking ModelSim testbenches with assertions and exhaustive corner-case coverage for state machine/datapath logic, validating correct state transitions and hand scoring across draw-rule paths
- Ran RTL + post-synthesis netlist simulation in Quartus/ModelSim to verify synthesizable behavior and catch mismatches early, improving correctness before FPGA deployment



### Custom Memory Allocator
A lightweight, from-scratch **heap allocator** mirroring the core ideas behind `malloc/free/realloc`.

- Implemented `malloc()`, `free()`, and `realloc()` with realistic heap metadata and allocation behavior
- Added block coalescing and in-place reallocation to reduce fragmentation and improve performance
- Built a heap consistency checker + debugging utilities to detect header corruption, overlapping blocks, and alignment issues



### Stud-Bud — Project Manager
- Led a 5-person team building a productivity app to help university students plan schedules and manage tasks more effectively
- Designed and implemented the schedule-generation algorithm using weighted heuristics (priority, estimated effort, deadlines) to produce practical daily plans
- Integrated the scheduling engine with the app’s core workflow, ensuring it worked smoothly with the GUI and client–server structure
- Contributed to networking + UI development while managing project planning, version control, and team coordination



### [Multi-Client Server](https://cpen221-ubc.notion.site/Message-Queues-Pub-Sub-with-Twitter-c5965b28ed01482aad44dbaadac19b77)
A **multi-client server** designed for concurrent connections, fault tolerance, and secure communication.

- Built a server that supports multiple simultaneous clients, enabling concurrent requests and responses without blocking
- Implemented dual-server routing / failover so clients can connect to either server and continue operating if one server goes offline
- Secured user data by hashing + salting passwords and encrypting all incoming/outgoing messages using AES



### Image Processing
An image-processing mini-project where I built an `ImageTransformer` toolkit and implemented classic computer vision–style operations on pixel grids.

- Implemented a suite of image transformations from scratch (mirror, negative, posterize, denoise/median filter, weathering/min filter, and block-painting/mean filter) by directly manipulating RGB channels at the pixel level
- Built image comparison utilities using grayscale + cosine similarity, including a “best match” ranking function to sort a list of images by similarity to a target image
- Implemented a green-screen pipeline: detected the largest connected region of an exact target color, computed its bounding rectangle, and overlaid/tiled a background image onto that region; supported the project with method specs and robust unit tests/code coverage



### Submarine Design — Team Captain
- Led a 6-person team to design a fully modeled submarine in SolidWorks, earning **2nd place out of 70+ teams**
- Ran weekly meetings with clear agendas and timelines to keep progress consistent and responsibilities clear
- Scoped and delegated work based on effort estimates, while also contributing to floor plans, CAD modeling, and technical troubleshooting
- Coordinated regular progress updates with the instructor and ensured the design stayed aligned with competition requirements
- https://www.youtube.com/watch?v=fhy48U5torM



### Wildfire Response System — Team Captain
- Led a 6-person team building a wildfire-mitigation concept that integrates fire retardant into residential sprinkler systems triggered by a temperature sensor
- Contributed hands-on by designing mechanical components in SolidWorks and programming the Arduino-based temperature sensing workflow
- Planned the project timeline, assigned tasks, and organized weekly check-ins to maintain steady progress
- Directed and produced a short demo video to communicate the system’s design and real-world use case
- https://www.youtube.com/watch?v=2M2wOQ82V_I
