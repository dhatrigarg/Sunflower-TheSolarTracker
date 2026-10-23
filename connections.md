# ESP32 Solar Tracker — Connections

## 1. LDR Connections

| LDR Sensor        | First Connection    | Second Connection        | Resistor Connection                     |
| ----------------- | ------------------- | ------------------------ | --------------------------------------- |
| Top Left (TL)     | One terminal → 3.3V | Other terminal → GPIO 34 | GPIO 34 junction → 10 kΩ resistor → GND |
| Top Right (TR)    | One terminal → 3.3V | Other terminal → GPIO 35 | GPIO 35 junction → 10 kΩ resistor → GND |
| Bottom Left (BL)  | One terminal → 3.3V | Other terminal → GPIO 32 | GPIO 32 junction → 10 kΩ resistor → GND |
| Bottom Right (BR) | One terminal → 3.3V | Other terminal → GPIO 33 | GPIO 33 junction → 10 kΩ resistor → GND |

## 2. Servo Motor Connections

### Servo 1 — X-Axis

| Servo Wire             | Connection                    |
| ---------------------- | ----------------------------- |
| Signal (yellow/orange) | ESP32 GPIO 13                 |
| Power (red)            | External regulated 5V (+)     |
| Ground (brown/black)   | External power supply GND (−) |

### Servo 2 — Y-Axis

| Servo Wire             | Connection                    |
| ---------------------- | ----------------------------- |
| Signal (yellow/orange) | ESP32 GPIO 14                 |
| Power (red)            | External regulated 5V (+)     |
| Ground (brown/black)   | External power supply GND (−) |

## 3. INA219 Connections

| INA219 Pin | Connection               |
| ---------- | ------------------------ |
| VCC        | ESP32 3.3V               |
| GND        | ESP32 GND                |
| SDA        | ESP32 GPIO 21            |
| SCL        | ESP32 GPIO 22            |
| VIN+       | Solar panel positive (+) |
| VIN−       | Load positive (+)        |

## 4. Solar Panel and Load Connections

| Component Terminal       | Connection        |
| ------------------------ | ----------------- |
| Solar panel positive (+) | INA219 VIN+       |
| INA219 VIN−              | Load positive (+) |
| Solar panel negative (−) | Load negative (−) |

## 5. Common Ground Connections

| Ground Connection        | Connect To                          |
| ------------------------ | ----------------------------------- |
| ESP32 GND                | INA219 GND                          |
| ESP32 GND                | External servo power supply GND (−) |
| Solar panel negative (−) | Load negative (−)                   |
