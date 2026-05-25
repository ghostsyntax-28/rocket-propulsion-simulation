# rocket-propulsion-simulation
# 🚀 Interactive Two-Stage Rocket Propulsion Simulator

A real-time, interactive 3D physics simulation of a two-stage rocket journeying from launch pad to orbit. Built using **Three.js** for rendering and core aerospace equations for high-fidelity telemetry tracking.

🔗 **Live Demo:** [rocket-propulsion-simulation.netlify.app](https://rocket-propulsion-simulation.netlify.app/)

---

## 🌟 Features

* **Two-Stage Physics Engine:** Simulates real-time mass depletion, thrust-to-weight ratios ($TWR$), and stage separation dynamics.
* **Interactive 3D Environment:** Dynamic camera tracking, particle-based engine plumes, and a scale-accurate rendering of Earth and low-Earth orbit (LEO).
* **Real-Time Telemetry Dashboard:** Live data visualization including:
    * Altitude ($km$) & Velocity ($m/s$)
    * Current Mass ($kg$) & Fuel Consumption Rate
    * Dynamic Atmospheric Drag ($Q$)
* **Orbital Insertion Tracker:** Visualizes the transition from atmospheric flight to a stable orbital trajectory.

---

## 📊 Physics & Mathematical Model

The simulation computes the rocket's trajectory by solving the standard equations of motion at every frame step.

### 1. Thrust and Mass Flow Rate
The mass of the rocket decreases dynamically based on the engine's specific impulse ($I_{sp}$) and thrust ($T$):

$$\dot{m} = \frac{T}{g_0 \cdot I_{sp}}$$

### 2. Net Acceleration
The instantaneous acceleration ($a$) takes into account thrust, atmospheric drag, and a variable gravitational pull that decreases with altitude ($h$):

$$a = \frac{T - D}{m} - g(h)$$

Where:
* $D = \frac{1}{2} \rho v^2 C_d A$ is the aerodynamic drag force.
* $g(h) = g_0 \left(\frac{R_e}{R_e + h}\right)^2$ is the gravitational acceleration.

### 3. Atmospheric Reentry Dynamics
**Once the second stage exhausts its remaining fuel, the rocket transitions into a controlled reentry phase. Atmospheric drag increases rapidly as altitude decreases, slowing the vehicle before touchdown.
Freentry=D+mg
The simulation continuously adjusts velocity, descent rate, and orientation to ensure a smooth landing back at the launch site.**
---

## 🛠️ Tech Stack

* **Frontend Framework:** HTML5, CSS3, JavaScript (ES6+)
* **3D Rendering:** [Three.js](https://threejs.org/) (WebGL)
* **Deployment:** Netlify

---

## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites
You only need a modern web browser. To run a local development server, you can use Node.js or a simple Python HTTP server.

### Installation & Local Running

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/rocket-propulsion-simulation.git](https://github.com/your-username/rocket-propulsion-simulation.git)
   cd rocket-propulsion-simulation
