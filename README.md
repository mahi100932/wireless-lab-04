# wireless-lab-04

# Wireless Communication and Cellular Network Analysis

## Project Overview

This repository contains Python-based experiments related
to Wireless Communication and Cellular Network Analysis.

The project focuses on two important topics:

1. Cellular Frequency Reuse Analysis
2. Free-Space and Two-Ray Ground Reflection Models

Python, NumPy, and Matplotlib are used to perform numerical
calculations, analyze wireless communication parameters,
and generate graphical representations.

The experiments demonstrate how cellular network capacity,
frequency reuse distance, signal propagation, and antenna
height affect wireless communication performance.

---

# Experiment 01: Cellular Frequency Reuse Analysis

## Objective

To analyze cellular frequency reuse by calculating
reuse distance and the number of traffic channels
allocated per cell for different cluster sizes.

The experiment also identifies the smallest feasible
cluster size based on a required reuse distance.

## Given Parameters

| Parameter | Value |
|---|---|
| Total Traffic Channels (C) | 420 |
| Cell Radius (R) | 1 km |
| Cluster Sizes (N) | 3, 4, 7, 9, 12 |
| Required Reuse Distance | 4 km |

## Mathematical Formulas

### 1. Frequency Reuse Ratio

D/R = √(3N)

### 2. Frequency Reuse Distance

D = R × √(3N)

### 3. Channels Per Cell

Channels per Cell = C/N

Where:

- D = Frequency reuse distance
- R = Cell radius
- N = Cluster size
- C = Total available traffic channels

## Python Programs

### Program 1: Frequency Reuse Calculation

File: `frequency_reuse_calculation.py`

This program calculates:

- Frequency reuse distance.
- Channels allocated per cell.
- Smallest feasible cluster size.
- Reuse distance satisfying the design requirement.
- Final design conclusion.

### Program 2: Graphical Analysis

File: `frequency_reuse_graph.py`

This program generates two graphs:

1. Reuse Distance vs Cluster Size
2. Channels per Cell vs Cluster Size

These graphs show the relationship between cluster
size, frequency reuse distance, and channel allocation.

## Numerical Results

| Cluster Size (N) | Reuse Distance (km) | Channels per Cell |
|---|---|---|
| 3 | 3.00 | 140 |
| 4 | 3.46 | 105 |
| 7 | 4.58 | 60 |
| 9 | 5.20 | 47 |
| 12 | 6.00 | 35 |

## Design Challenge

Required Reuse Distance = 4 km.

The smallest feasible cluster size is:

- Cluster Size = 7
- Reuse Distance = 4.58 km
- Channels per Cell = 60

Therefore, N = 7 is the smallest feasible cluster
size for the given design requirement.

## Analysis

Increasing cluster size increases the reuse distance,
which can help reduce co-channel interference.

However, increasing cluster size decreases the number
of channels allocated per cell.

Therefore, cellular network design requires a balance
between network capacity and interference.

---

# Experiment 02: Free-Space and Two-Ray Ground Reflection Models

## Objective

To analyze received signal power using different
radio propagation models and investigate the effects
of distance and antenna height on wireless communication.

## Given Parameters

| Parameter | Value |
|---|---|
| Speed of Light (c) | 3 × 10⁸ m/s |
| Carrier Frequency (f) | 900 MHz |
| Transmit Power (Pt) | 1 W |
| Transmitter Gain (Gt) | 0 dBi |
| Receiver Gain (Gr) | 0 dBi |
| Transmitter Height (ht) | 20 m |
| Receiver Height (hr) | 2 m |
| Distance Range | 10 m – 5000 m |

## Mathematical Formulas

### 1. Wavelength

λ = c/f

### 2. Free-Space Propagation Model

Pr = Pt × Gt × Gr × (λ/4πd)²

### 3. Two-Ray Asymptotic Model

Pr = Pt × Gt × Gr × (ht² × hr²)/d⁴

### 4. Breakpoint Distance

d_break = 4π × ht × hr / λ

### 5. Received Power in dBm

Pr(dBm) = 10 log₁₀(Pr in watts) + 30

Where:

- Pr = Received power
- Pt = Transmitted power
- Gt = Transmitter antenna gain
- Gr = Receiver antenna gain
- λ = Wavelength
- d = Distance between transmitter and receiver
- ht = Transmitter antenna height
- hr = Receiver antenna height

## Propagation Models

The experiment uses three propagation models:

1. Free-Space Propagation Model
2. Two-Ray Asymptotic Model
3. Full Two-Ray Ground Reflection Model

## Python Program

File: `free_space_two_ray_propagation.py`

The program performs the following operations:

- Calculates the wavelength.
- Calculates the breakpoint distance.
- Compares free-space and two-ray propagation models.
- Calculates received power in dBm.
- Investigates the effect of different antenna heights.
- Generates three graphical comparisons.

## Graphical Analysis

### Graph 1: Free-Space vs Two-Ray Asymptotic Model

Compares received power against distance and identifies
the breakpoint distance.

### Graph 2: Full Two-Ray Ground Reflection Model

Compares the full two-ray model with the free-space
and asymptotic models.

### Graph 3: Effect of Antenna Heights

Investigates how different transmitter and receiver
antenna heights affect received signal power.

## Numerical Results

### Wavelength and Breakpoint Distance

| Parameter | Result |
|---|---|
| Wavelength | 0.3333 m |
| Transmitter Height | 20 m |
| Receiver Height | 2 m |
| Breakpoint Distance | 1507.96 m |

### Breakpoint for Different Transmitter Heights

| Transmitter Height | Receiver Height | Breakpoint |
|---|---|---|
| 10 m | 2 m | 753.98 m |
| 20 m | 2 m | 1507.96 m |
| 50 m | 2 m | 3769.91 m |

## Analysis

The free-space model follows an inverse-square
relationship with distance.

The two-ray asymptotic model follows an inverse-fourth-
power relationship at sufficiently large distances.

The breakpoint distance depends on wavelength and
the heights of the transmitter and receiver antennas.

Increasing antenna height increases the breakpoint
distance when the other parameters remain constant.

---

# Software and Libraries

The following technologies are used:

- Python 3
- NumPy
- Matplotlib

## Installation

Install the required libraries using:

```bash
pip install numpy matplotlib
```

## How to Run the Experiments

### Experiment 01

Run the frequency reuse calculation:

```bash
python Experiment-01/frequency_reuse_calculation.py
```

Run the graphical analysis:

```bash
python Experiment-01/frequency_reuse_graph.py
```

### Experiment 02

Run the propagation model:

```bash
python Experiment-02/free_space_two_ray_propagation.py
```

---

# Overall Conclusion

This project demonstrates important concepts in
wireless communication and cellular network design.

Experiment 01 explains the relationship between
cluster size, frequency reuse distance, channel
allocation, and network interference.

Experiment 02 demonstrates radio signal propagation
using free-space and two-ray ground reflection models.

Both experiments help develop a practical understanding
of wireless communication system analysis through
Python programming and graphical visualization.

---

## Author
Ahmudur Rahman 
ID-T241004

Department: Electronics and Telecommunication Engineering (ETE)
Semester-6th
course:Mobile and Wireless Communication sessional

Programming Language: Python

## Project Category

Wireless Communication | Cellular Networks |
Radio Propagation | Python Simulation
