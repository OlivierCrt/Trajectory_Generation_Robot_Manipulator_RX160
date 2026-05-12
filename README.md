# Circular Trajectory Generation with a Robot Manipulator - RX160

## Description  
This project focuses on modeling and simulating a 3-DOF RRR robot manipulator, specifically designed for generating and executing circular trajectories in 3D space. It includes tools for geometric and kinematic modeling, trajectory planning, and differential analysis, enabling precise control and simulation of the robot's movements.

---

## Key Functionalities  

### 1. **Geometric Modeling**  
   - **Direct Geometric Modeling (DGM):** Computes the end-effector position and orientation based on joint angles.  
   - **Inverse Geometric Modeling (IGM):** Determines the required joint angles to achieve a desired end-effector position.  

### 2. **Kinematic Modeling**  
   - **Transformation Matrices:** Computes transformation matrices between successive links using Denavit-Hartenberg (DH) parameters.  
   - **Global Transformation Matrix:** Calculates the overall transformation matrix from the base to the end-effector.  

### 3. **Differential Modeling**  
   - **Direct Differential Model (DDM):** Computes end-effector velocities from joint velocities using the Jacobian matrix.  
   - **Inverse Differential Model (IDM):** Computes required joint velocities to achieve a desired end-effector velocity.  

### 4. **Trajectory Generation**  
   - **Circular Trajectory Planning:** Generates smooth circular trajectories in 3D space between two points, with control over initial and final velocities and acceleration.  
   - **Operational and Joint Trajectories:** Provides both operational space (end-effector) and joint space trajectories for execution.  

### 5. **Simulation and Testing**  
   - Includes tools for validating the robot's geometric, kinematic, and trajectory planning models through simulations and tests.  

---

## Usage  

> **Note:** The parameters of the RRR robot can be edited in the file **config.py** to adapt to any configuration.


### 1. **Setup**  
   - Clone the repository:  
     ```bash  
     git clone https://github.com/OlivierCrt/Trajectory_Generation_Robot_Manipulator_RX160  
     cd Trajectory_Generation_Robot_Manipulator_RX160
     ```  
   - Create and activate a virtual environment:  
     ```bash  
     python3 -m venv venv  
     source venv/bin/activate  
     ```  
   - Install dependencies:  
     ```bash  
     pip install -r required.txt  
     ```  
   - Install the project in development mode:  
     ```bash  
     pip install -e .  
     ```  

### 2. **Running the Project**  
   - Execute the main file to interact with the functionalities:  
     ```bash  
     python -m Tests.main  
     ```  

### 3. **Inputs and Units**  
   - **Linear Velocities:** mm/s  
   - **Angular Velocities:** rad/s  
   - **Joint Velocities:** rad/s  
   - **Distances:** mm  

### 4. **Example Values**  
   For the trajectory generation (menu option 2), use the following values as a starting point:  

   | Parameter | Value |
   |-----------|-------|
   | V1 (initial velocity) | 500 mm/s |
   | V2 (final velocity) | 3000 mm/s |
   | K (acceleration) | 3000 mm/s² |
   | Point A (x, y, z) | 1000, -100, 600 |
   | Point B (x, y, z) | 1000, 200, 1200 |

   > **Note:** Points A and B must share the same x coordinate since the trajectory is a circular arc in the YZ plane.

---

This project provides a comprehensive framework for modeling, simulating, and controlling an RRR robot manipulator, with a focus on circular trajectory generation and execution.

For more details on the theoretical background and implementation, refer to the [project report (PDF)](Docs/BE-GT2024-Equipe6.pdf).


