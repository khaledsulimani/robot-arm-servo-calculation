# 🤖 Robotic Arm Motor Selection

## 📋 Overview

This document outlines the steps followed to choose the appropriate motors for a robotic arm designed to lift a weight of 1 kg and 2 kg. The selected motors are:

- 🔧 **Power HD 1501MG**
- ⚙️ **Savox SC-0251MG**  
- 🎯 **SG90**

The calculations and considerations for lifting 1 kg and 2 kg are discussed, along with the limitations when trying to lift 2 kg using these motors without adding gears.

## 1️⃣ Weight Calculation (1 kg)

### 💪 Force Calculation

The force exerted by a 1 kg weight is calculated using the equation:

```
F = m × g = 1 kg × 9.81 m/s² = 9.81 N
```

Where:
- 📏 **m** is the mass (in kilograms)
- 🌍 **g** is the acceleration due to gravity (9.81 m/s²)

### 🔄 Torque Calculation for Each Arm Segment

We have three segments in the robotic arm, each with different lengths:

1. 🦾 **First Arm Segment**: 15 cm (0.15 meters)
2. 🦾 **Second Arm Segment**: 10 cm (0.1 meters)  
3. 🦾 **Third Arm Segment**: 4 cm (0.04 meters)

The torque (T) for each segment is calculated using the formula:

```
T = F × r
```

Where:
- 🔄 **T** is the torque (in N·m)
- 💪 **F** is the force (in Newtons)
- 📏 **r** is the length of the arm segment (in meters)

For the arm segments:

- **First Segment**: `T₁ = 9.81 N × 0.15 m = 1.4715 N·m`
- **Second Segment**: `T₂ = 9.81 N × 0.1 m = 0.981 N·m`
- **Third Segment**: `T₃ = 9.81 N × 0.04 m = 0.3924 N·m`

### 📊 Total Torque

The total required torque for lifting 1 kg across all three segments is:

```
T_total = T₁ + T₂ + T₃ = 1.4715 + 0.981 + 0.3924 = 2.8449 N·m
```

## 2️⃣ Motor Selection for 1 kg Weight

### 🎯 Motors Chosen

1. **Power HD 1501MG**:
   - 🔄 Torque: 10 kg·cm (around 0.98 N·m at 4.8V)

2. **Savox SC-0251MG**:
   - 🔄 Torque: 13 kg·cm (around 1.27 N·m at 6V)

3. **SG90**:
   - 🔄 Torque: 1.8 kg·cm (around 0.18 N·m at 4.8V)

✅ These motors are sufficient for lifting 1 kg since the required torque (2.8449 N·m) is manageable with the chosen motors. However, they are designed to lift smaller loads, and adding more weight (like 2 kg) will increase the torque requirements.

## 3️⃣ Weight Calculation for 2 kg

### 💪 Force Calculation for 2 kg

For a 2 kg weight, the force is:

```
F = 2 kg × 9.81 m/s² = 19.62 N
```

### 🔄 Torque Calculation for 2 kg

The torque for each arm segment when lifting 2 kg is:

- **First Segment**: `T₁ = 19.62 N × 0.15 m = 2.943 N·m`
- **Second Segment**: `T₂ = 19.62 N × 0.1 m = 1.962 N·m`
- **Third Segment**: `T₃ = 19.62 N × 0.04 m = 0.7848 N·m`

### 📊 Total Torque for 2 kg

The total torque required for lifting 2 kg across all three segments is:

```
T_total = T₁ + T₂ + T₃ = 2.943 + 1.962 + 0.7848 = 5.6898 N·m
```

### ⚠️ Conclusion for 2 kg

❌ The motors selected (Power HD 1501MG, Savox SC-0251MG, SG90) are **not sufficient** for lifting 2 kg without modification. The total torque required for lifting 2 kg exceeds the torque capabilities of these motors.

## 4️⃣ Gear Solution for Lifting 2 kg

### 🔧 Why Gears Are Needed

- ⚙️ **Gears (Reduction gears)** can be used to reduce the speed of the motors while increasing the torque
- 📈 For instance, a 2:1 gear ratio would reduce the speed of the motor by half but double the torque
- 🎯 Adding a gearbox will allow the motors to handle the increased torque required for lifting 2 kg

## 5️⃣ Issues and Solutions with Robotic Arm

### ⚠️ Issues

1. **Limited Torque**: 
   - 🚫 The selected motors do not provide enough torque to lift 2 kg directly
   - ⚡ This can result in motors struggling or stalling when attempting to lift heavier loads

2. **Speed Reduction**: 
   - 🐌 Adding gears will reduce the speed of the arm
   - 🎯 May affect precision and responsiveness, especially in applications requiring fast actions

3. **Increased Complexity**: 
   - 🔧 Incorporating gears introduces mechanical complexity
   - 📦 Could increase weight and bulk of the robotic arm

### ✅ Solutions

1. **Use of Gears**: 
   - ⚙️ Using reduction gears will increase torque and enable lifting 2 kg loads

2. **Upgrading Motors**: 
   - 🔋 Consider stronger motors with higher torque ratings (e.g., Dynamixel servos)
   - 💰 Note: This might increase cost

3. **Optimizing Arm Design**: 
   - 📏 Reduce arm lengths or adjust design to minimize required torque
   - 🎨 Streamline mechanical structure

4. **Improve Control Algorithms**: 
   - 🧠 Use advanced control algorithms (PID control)
   - ⚡ Manage speed and positioning more effectively despite gear reduction

---

## 📝 Final Notes

- ✅ **1 kg lifting**: The selected motors can lift 1 kg effectively
- ⚙️ **2 kg lifting**: Gears are necessary to achieve the required torque
- ⚖️ **Trade-offs**: While gears provide a feasible solution, they introduce speed trade-offs and mechanical complexity

---
  
## 🧑‍💻 Author
- **khaled mahmoud sulaimani** – [@khaledsulimani](https://github.com/khaledsulimani)

---

*🤖 Happy building your
