# ATmega328P SDB (Safe Deposit Box) Design

This project involves designing a Safe Deposit Box (SDB) system using the ATmega328P microcontroller. The SDB is intended to be used in hotels for secure storage of valuable items. The design includes a custom PCB layout and various features for control and monitoring.

## Features

- **ATmega328P** microcontroller as the core of the system.
- **Regulated 5V power supply** using AMS1117-5.0 for stable operation.
- Integration of **7-segment multiplexing** for display control.
- Use of **L293D motor driver** to control a motor.
- External **EEPROM 24LC256** for data storage via I2C.
- **Keypad matrix** for user input (PIN entry, etc.).
- **Buzzer control** via PWM for audible feedback.
- Connection to a **USB Type-A** for power or communication.
- **Simple control interface** with **74HC595 shift register** for extending output pins.

## How to Print the PCB Design

### Step 1: Prepare the PCB Design

1. Ensure your design files are ready in **KiCad** (or another PCB design tool).
2. Check your **netlist** and **schematic** to verify that all components are correctly placed.

### Step 2: Export Gerber Files

1. Open your PCB design in **KiCad** or your chosen design tool.
2. Export the design to **Gerber files** and the **Bill of Materials (BOM)**. These are standard files used by PCB manufacturers.
   - In KiCad: Use **Plot** to export the Gerber files.
   - Ensure that you export all layers (top, bottom, silkscreen, etc.).
   
### Step 3: Send to PCB Manufacturer

1. Choose a **PCB manufacturer** that supports the Gerber file format.
2. Upload the Gerber files and **BOM** to the manufacturer's website.
3. Specify the dimensions (for example, 6x5 cm) and any additional manufacturing options (e.g., surface finish, copper weight, etc.).
4. Place your order for the **PCB fabrication**.

### Step 4: Assemble the PCB

1. Once the PCBs are delivered, begin **assembling** the components based on the design.
2. Solder the **ATmega328P**, **L293D**, **74HC595**, and other components onto the PCB.
3. Test the assembly thoroughly to ensure correct functionality.

## Wiring and Pinout

### ATmega328P Pinout

- **Pin 1 (RESET)**: Connect to the reset circuit (optional).
- **Pin 2-13 (Digital I/O)**: Used for controlling the 7-segment display and interacting with the motor driver.
- **Pin A0-A7 (Analog I/O)**: Not used in this design but available for future expansion.
- **Pin AVCC**: Connect to the 5V supply.
- **Pin GND**: Ground connection.

### L293D Motor Driver

- **VCC1**: Connect to 5V from ATmega328P.
- **VCC2**: Connect to 6V battery for motor.
- **Enable Pin (EN1)**: Connect to 5V to enable motor control.
- **Control Pins (IN1, IN2, IN3, IN4)**: Connected to ATmega328P pins for motor control.

### EEPROM (24LC256) Connections

- **SDA**: Connect to ATmega328P SDA (pin A4).
- **SCL**: Connect to ATmega328P SCL (pin A5).
- **VCC**: Connect to 5V power supply.
- **GND**: Connect to ground.

## Components Used

- **ATmega328P** microcontroller
- **AMS1117-5.0** voltage regulator
- **L293D** motor driver
- **74HC595** shift register
- **24LC256** EEPROM (I2C)
- **7-segment display**
- **Keypad matrix**
- **Buzzer**
- **USB Type-A connector**
- **Various passive components (resistors, capacitors)**

## License

This project is open-source and licensed under the **MIT License**. Feel free to modify, share, and contribute!

---

For further information or questions, please open an issue in the GitHub repository.
