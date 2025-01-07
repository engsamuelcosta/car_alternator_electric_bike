# Arduino Smart Odometer & Vehicle Sensor System

## Overview
This is an Arduino-based project designed to track distance, speed, and control relays for motor, generator, and regenerative brake modes. The system uses an I2C LCD to display data, has configurable parameters (like wheel radius) stored in EEPROM, and includes button controls and voltage monitoring.

## Features
- Tracks and displays **distance** and **speed**.
- Monitors **battery voltage**.
- Uses **EEPROM** to store configurations such as wheel radius.
- **Relay control** for motor, generator, and regenerative braking.
- Customizable through buttons for settings adjustments.
- Displays real-time data on a 16x2 I2C LCD.

## Components
- **Arduino Board** (e.g., Uno, Mega, or Nano).
- **16x2 I2C LCD** for real-time display.
- **Reed Switch** for detecting wheel revolutions.
- **Buttons** for adjusting settings (increment, decrement, select, etc.).
- **Relay Module** for controlling the motor, generator, and brakes.
- **Battery voltage sensor** for monitoring the power system.
- **Brake and throttle sensors** for controlling the motor and braking modes.

## Pinout
| Pin           | Function                                |
|---------------|-----------------------------------------|
| A0            | Button Shield                           |
| A1            | Throttle (accelerator) input            |
| A2            | Voltage sensor                          |
| D2            | Brake input                             |
| D3            | Relay for regulator control             |
| D4            | Relay for stator                        |
| D5            | Relay for rotor                         |
| D6            | Reed switch (wheel sensor)              |
| D7, D8, D9    | Buttons (increment, decrement, select)  |
| D0, D1        | Serial communication (Bluetooth)        |

## Setup
1. **Wiring**:
   - Connect the components (LCD, sensors, buttons, relays) to the corresponding pins as specified in the code.
   - Ensure proper power supply for the Arduino board and external components (e.g., relays).
   
2. **Arduino IDE**:
   - Install the required libraries: `LiquidCrystal_I2C`, `Wire`, `EEPROM`, and `SPI`.
   - Upload the code to the Arduino board.

3. **Configuration**:
   - The wheel radius can be set using the buttons. This value will be stored in EEPROM for future use.

## Usage
- Press buttons to interact with the system:
  - **Increment/Decrement**: Adjust the wheel radius.
  - **Select**: Access different modes (e.g., motor mode, generator mode, brake mode).
  - **Enter**: Confirm settings.

The LCD will display:
- Distance traveled (`Dist` in km).
- Current mode (e.g., motor active, regenerative braking).
- Voltage levels.
  
## Example Output on LCD




## License
This project is open-source and licensed under the MIT License.

## Contributions
Feel free to fork this project and submit pull requests. If you encounter any issues or have suggestions for improvements, please open an issue.

## Contact
- **Creator**: Samuel Alencar da Costa
- **Email**: samuel.alencar85@gmail.com
