# Travelling Salesman Problem (TSP) - Parallel AJ-PE Algorithm  

## 📌 About the Project  
This project implements a **parallel and concurrent solution** for the **Travelling Salesman Problem (TSP)** using the **AJ Pseudo-Evolutionary (AJ-PE) algorithm**.  
The goal is to find the **shortest possible route** that visits all cities exactly once and returns to the starting point.  

The implementation focuses on **parallel computing** techniques to improve performance, utilizing **shared memory** and **semaphores** for synchronization.  

---

## 🛠 Technologies Used  
- **C (GCC Compiler - Linux)**  
- **Parallel Processing (Fork & Multi-Processing)**  
- **Shared Memory (shmget, shmat, shmctl)**  
- **Semaphores (sem_init, sem_wait, sem_post)**  
- **File Handling for Input Processing**  

---

## 📂 Algorithm Implementation  

### **1️⃣ AJ Pseudo-Evolutionary (AJ-PE) Algorithm**  
✔ Starts with a **random path** across all cities  
✔ Applies **exchange mutation** (randomly swaps two cities in the path)  
✔ Evaluates the total path **distance** after each mutation  
✔ Repeats for a **fixed number of iterations or time limit**  
✔ Returns the **shortest path** found  

### **2️⃣ Parallel Implementation - Base Version**  
✔ **Creates m parallel processes** to run the AJ-PE algorithm  
✔ Each process independently searches for a better path  
✔ **Best path is stored in shared memory**  
✔ Uses **semaphores** to prevent race conditions  

### **3️⃣ Parallel Implementation - Advanced Version**  
✔ **Processes communicate** when a better solution is found  
✔ Parent process **broadcasts updates** to all child processes  
✔ Synchronization ensures **all processes use the best path**  

---
