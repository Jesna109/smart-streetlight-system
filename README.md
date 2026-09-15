# Smart Street Lighting System

An Arduino-based smart street lighting system that automatically controls street lights based on the surrounding light conditions and IR sensor inputs.

## 📌 Project Overview

The system uses an **LDR (Light Dependent Resistor)** to detect whether the surroundings are bright or dark and **two IR sensors** to control two individual street lights.

During bright conditions, the street lights remain OFF. When it is dark, the IR sensors activate their corresponding lights when an object is detected.

## 🔧 Components Used

- Arduino
- LDR (Light Dependent Resistor)
- 2 × IR Sensors
- 2 × LEDs
- Supporting components and connecting wires

## ⚙️ Working Principle

1. The LDR continuously measures the surrounding light intensity.
2. The Arduino reads the LDR value through an analog input.
3. When the LDR value is **100 or higher**, the system considers it to be bright and keeps both street lights OFF.
4. When the LDR value is **less than 100**, the system considers it to be dark.
5. During dark conditions:
   - **IR Sensor 1 HIGH → LED 1 ON**
   - **IR Sensor 2 HIGH → LED 2 ON**
6. The system also displays the sensor readings and light status through the Arduino Serial Monitor.

## 🔌 Pin Configuration

| Component | Arduino Pin |
|---|---|
| IR Sensor 1 | D2 |
| IR Sensor 2 | D3 |
| LED 1 | D5 |
| LED 2 | D6 |
| LDR | A3 |

## 🧠 Control Logic

```text
             LDR
              ↓
     Check Light Intensity
              ↓
       ┌──────┴──────┐
       ↓             ↓
  Bright ≥ 100    Dark < 100
       ↓             ↓
 Both LEDs OFF   Check IR Sensors
                     ↓
              ┌──────┴──────┐
              ↓             ↓
          IR1 HIGH       IR2 HIGH
              ↓             ↓
           LED1 ON        LED2 ON
```

## 🧪 Simulation

The system was simulated using **Tinkercad** to demonstrate the operation of the Arduino, LDR, IR sensors, and street lights.

The simulation was used to test the circuit and observe the response of the street lights under different light and IR sensor conditions.

## 💻 Programming

The system is programmed using **Arduino C/C++**.

The program continuously:

- Reads the LDR value.
- Determines the surrounding light condition.
- Reads the IR sensor inputs.
- Controls the corresponding street lights.
- Displays sensor values and system status through the Serial Monitor.

## 🛠️ Tools Used

- **Arduino IDE** – Programming and uploading the Arduino code
- **Tinkercad** – Circuit design and simulation

