# ⚙️ Rust Real-Time Actuator Control System  

## 📌 Overview  
This project demonstrates the design, implementation, and performance evaluation of a **Rust-based real-time actuator control system for robotic arms**. It was developed as part of the **Real-Time Systems module (CT087-3-3-RTS)** at **Asia Pacific University of Technology & Innovation (APU)**.  

The system is engineered to operate under **strict millisecond deadlines** commonly required in industrial automation and robotics. Using Rust’s unique blend of **memory safety, concurrency, and deterministic execution**, the system ensures **1–2ms cycle-time accuracy** when processing sensor inputs and generating actuator commands.  

By integrating **Tokio async runtime**, **RabbitMQ message broker**, and **custom PID controllers**, the project highlights how **next-generation robotics systems** can be developed in Rust with guarantees of **safety, scalability, and performance predictability**.  

---

## 🎯 Objectives  
The main objectives of this project were:  
- To design a **real-time control loop** (1–2ms) for robotic actuators using direct sensor feedback.  
- To leverage Rust’s **compile-time safety features** to prevent common runtime errors.  
- To implement **asynchronous and concurrent task management** for parallel robotic operations.  
- To ensure **safe prioritization of emergency tasks** through scheduling mechanisms.  
- To benchmark and validate system performance under **normal, high-stress, and emergency conditions**.  

---

## 🏭 Problem Background  
In industrial automation, even **microsecond-level delays** can compromise robotic safety and efficiency. Modern robots operate with control loop cycle times of **0.5–1ms**. Missing deadlines can result in:  
- **Positional inaccuracies** (causing defective products).  
- **Oscillations or unsafe movements** (endangering operators).  
- **Collisions** between multiple robots on the same production line.  

Traditional languages like **C/C++** offer performance but are prone to memory safety issues (buffer overflows, dangling pointers, race conditions). Rust solves this by:  
- Enforcing **ownership and borrowing rules** at compile time.  
- Eliminating **garbage collection pauses** that could break real-time deadlines.  
- Preventing **data races** through strict concurrency checks.  

This project proves that **Rust is suitable for mission-critical, real-time robotic systems**.  

---

## 📐 System Design  

### 🔹 System Architecture  
The system follows a **data flow pipeline** where sensor data is continuously processed and transformed into prioritized actuator commands.  

<img width="439" height="765" alt="image" src="https://github.com/user-attachments/assets/cb3a08b3-b5c4-48d0-941e-49cebac4cc4b" />


