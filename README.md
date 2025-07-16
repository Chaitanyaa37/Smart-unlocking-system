# Authentication-Based Unlocking System Using 8051 Microcontroller

This project implements a password-protected door unlocking mechanism using a 4x3 keypad, LCD, and motors controlled by an 8051 microcontroller. The system verifies a user-entered password and controls door access accordingly.

# Project Overview

- Technology : Embedded C with 8051 (AT89C51)
- Tools : Keil µVision IDE, 8051 Programmer
- Interfaces : 16x2 LCD, 4x3 Keypad, DC Motors

# Features

- Secure 4-digit password entry using a keypad
- Visual feedback using a 16x2 LCD
- Motor-controlled locking/unlocking mechanism
- Denies access on incorrect password input

# Hardware Pin Mapping

# Keypad (4x3):
- Rows: P1.0, P1.7, P1.2, P1.3
- Columns: P1.4, P1.5, P1.6

# Motors:
- Motor 1: P3.3 (M1P), P3.4 (M1N)
- Motor 2: P3.5 (M2P), P3.6 (M2N)

# LCD:
- Data Lines: P2.0–P2.7
- RS: P3.0  
- RW: P3.1  
- EN: P3.2  

# Files

| File                                | Description                           |
|-------------------------------------|---------------------------------------|
| `authentiaction based unlocking system.c` | Main source code (Embedded C)         |
| `Authentication based unlocking system.hex` | Compiled HEX file for microcontroller |
| `Authentication based unlocking system.uvproj` | Keil project file                     |

# How It Works

1. System prompts user to enter a 4-digit password.
2. If password is correct (`1513` by default):
   - Displays "Access Granted"
   - Activates motors to unlock doors
   - Waits, then closes doors automatically
3. If incorrect:
   - Displays "Access Denied"

# How to Run

1. Open the `.uvproj` file in Keil µVision.
2. Compile the project.
3. Flash the `.hex` file to an 8051 microcontroller.
4. Connect hardware components per the pin diagram.
5. Power the board and test with the keypad.

# Notes

- You can change the default password in the `check()` function.
- Debouncing and additional security features (e.g., lockout on multiple failures) can be added for robustness.
