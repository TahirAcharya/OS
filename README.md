Module 1- ch-1: [Link](https://docs.google.com/presentation/d/1PkiFAAHL4q7UAi9jkXfaF31r-pfXwkL6/edit?usp=sharing&ouid=102189640680844426038&rtpof=true&sd=true)

Module 1- ch-2 [Link](https://docs.google.com/presentation/d/1SzKSyyd4E6jatnVnZGukljUPfMLJCXCH/edit?usp=sharing&ouid=102189640680844426038&rtpof=true&sd=true)
# 🧠 Operating Systems (OS) – Concepts & Implementation

Welcome to the **Operating Systems Repository** by **Mohammad Tahir Mirji**, Assistant Professor – AIML Department, **Acharya Institute of Technology**.  
This repository is curated for academic and practical understanding of **Operating System fundamentals, algorithms, and hands-on experiments**.

---

## 📘 Repository Overview

This repository is a collection of:
- Operating System algorithms implemented in **C / C++ / Python**.
- Demonstrations of **process scheduling**, **memory management**, **deadlock handling**, and **file management**.
- Course-aligned lab programs and documentation for undergraduate engineering students.

---

## 🧩 Folder Structure

```bash
OS/
├── Scheduling_Algorithms/
│   ├── FCFS.c
│   ├── SJF.c
│   ├── RoundRobin.c
│   └── PriorityScheduling.c
├── Memory_Management/
│   ├── FirstFit.c
│   ├── BestFit.c
│   └── WorstFit.c
├── Deadlock/
│   ├── BankersAlgorithm.c
│   └── ResourceAllocationGraph.c
├── File_Management/
│   ├── FileAllocation.c
│   └── DirectoryStructure.c
└── README.md
⚙️ Topics Covered
Module	Topic	Description
1	Process Management	Process creation, scheduling, synchronization
2	Memory Management	Allocation, fragmentation, paging, segmentation
3	File System	File operations, allocation methods
4	Deadlocks	Detection, avoidance, and prevention
5	I/O Systems	Device management, buffering, spooling

🧪 Sample Program – FCFS Scheduling
c
Copy code
#include <stdio.h>
int main() {
    int n, bt[20], wt[20], tat[20];
    float awt = 0, atat = 0;
    printf("Enter total number of processes: ");
    scanf("%d", &n);
    printf("Enter Burst Time for each process:\n");
    for(int i = 0; i < n; i++) {
        printf("P[%d]: ", i+1);
        scanf("%d", &bt[i]);
    }
    wt[0] = 0;
    for(int i = 1; i < n; i++)
        wt[i] = wt[i-1] + bt[i-1];
    for(int i = 0; i < n; i++) {
        tat[i] = wt[i] + bt[i];
        awt += wt[i];
        atat += tat[i];
    }
    printf("\nProcess\tBT\tWT\tTAT\n");
    for(int i = 0; i < n; i++)
        printf("P[%d]\t%d\t%d\t%d\n", i+1, bt[i], wt[i], tat[i]);
    printf("\nAverage Waiting Time: %.2f", awt/n);
    printf("\nAverage Turnaround Time: %.2f\n", atat/n);
    return 0;
}
💡 Learning Objectives
Understand core principles of operating systems.

Simulate various scheduling and memory management algorithms.

Implement deadlock detection and avoidance techniques.

Strengthen problem-solving and programming skills in C/C++.

🎓 Academic Context
This repository supports the Operating Systems Laboratory course under VTU Curriculum for:

B.E. – Computer Science and Engineering (CSE)

B.E. – Artificial Intelligence and Machine Learning (AIML)

B.E. – Data Science (DS)

Instructor: Mohammad Tahir Mirji
Department: Artificial Intelligence and Machine Learning
Institution: Acharya Institute of Technology, Bengaluru

📊 How to Use
Clone the repository

bash
Copy code
git clone https://github.com/TahirAcharya/OS.git
Navigate to the desired folder

bash
Copy code
cd OS/Scheduling_Algorithms
Compile and run any program

bash
Copy code
gcc FCFS.c -o FCFS
./FCFS

📜 License
This repository is licensed under the MIT License.
Feel free to use and adapt the code for educational purposes with proper attribution.

⭐ Star this repository if you find it helpful!
📧 For academic queries or collaborations: tahir2968@acharya.ac.in


