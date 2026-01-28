# Digital Fort — Embedded Escape Room System

**Digital Fort** is an embedded system that simulates an interactive escape room. Players must complete three sequential challenges using switches, a potentiometer, and pushbuttons to "unlock" the room. The system integrates digital I/O, ADC, interrupt-driven timing, and display feedback to provide a responsive gameplay experience.

---

## Hardware Overview

- **Microcontroller:** PIC16F877A
- **Inputs:**
  - 4x Switches (PORTB RB4-RB7) for binary number entry
  - Potentiometer (PORTA RA0) for analog input
  - Start/Finish pushbuttons (PORTB RB0, RB1)
- **Outputs:**
  - LCD (PORTD) for status messages and math problems
  - 7-Segment Display (PORTC) for countdown timers and results
  - LEDs (PORTE RE0-RE2) indicating challenge success
  - Buzzer signaling final victory

---

## Gameplay Challenges

1. **Prime Number Check**  
   - Player inputs a 4-bit number. System evaluates primality (3, 5, 7, 11, 13).  
   - **Pass:** CORR1 LED lights, 7-segment shows 'P'  
   - **Fail:** System resets, LCD displays *"Hard Luck"*

2. **Potentiometer Range Matching**  
   - Player adjusts a potentiometer to match a predefined voltage range.  
   - **Pass:** CORR2 LED lights, LCD shows *"You are correct"*  
   - **Near miss:** LCD displays *"You are so close"*

3. **Math Problem Solving**  
   - Random math problem displayed on LCD; 9-second countdown on 7-segment.  
   - **Pass:** Correct answer entered before timer ends, CORR3 LED lights  
   - **Victory:** Completing all three challenges triggers flashing LEDs, buzzer, and *"YOU WIN! Escape"* message

---

## Software & Implementation

- **Language:** PIC Assembly  
- **Development Environment:** MPLAB  
- **Simulation:** Proteus  
- **Key Features:**  
  - Interrupt-driven ADC for responsive potentiometer readings  
  - Modular, subroutine-based design for timing and display logic  
  - Sequential challenge logic with immediate visual/audio feedback  

---

## Highlights

- Demonstrates low-level embedded system design with real-time input handling  
- Combines digital and analog I/O with user interaction  
- Integrates modular assembly programming and interrupt-driven control  
- Ready for simulation and extension with additional challenges

---

