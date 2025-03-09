# Universal Timer PCB Project  

## Overview  
This project involves designing a PCB layout for a **universal timer** based on a given circuit diagram and specific parameters. The timer consists of:  
- A **relay** for switching the coil on and off in the circuit.  
- A **potentiometer** to adjust the timer's operating duration.  

The **circuit diagram** is provided below.  

## Project Structure  
The following files and folders contain essential project components:  
- **PCB Project** – The OrCAD project files.  
- **Catalog Sheets** – Datasheets for the components used.  
- **Fabrication Files** – Files required for PCB manufacturing.  
- **Footprints** – Custom footprints for the buttons and relay (not included in OrCAD's default library).  
- **Documentation** – A detailed description of the project and its functionality.  

## Circuit Description  
This miniature circuit, equipped with an **electromagnetic relay**, can be used in various applications. A few simple modifications allow adjustments to both **duration** and **maximum operating interval**.  

The **timing function** is based on the **LM555 timer IC**, a well-known component in the field. Here’s how it works:  
- The **Start (pin 2)** and **Stop (pin 4)** inputs are normally held at a **high voltage** by resistors R4 and R6.  
- In the idle state, the **timing capacitor (C2)** is short-circuited to ground by the chip’s internal electronics.  
- When the **Start button** is pressed:  
  - The **output (pin 3)** switches **ON**, activating transistor **T1**, which in turn energizes the relay.  
  - LED **LD1** lights up to indicate activation.  
  - **Capacitor C2** starts charging through **R1** and **RV1**.  

### Adjusting the Timer  
- The **larger the capacitance of C2** and the **resistance of RV1**, the **longer the delay** before the output resets.  
- If the **Stop button** is pressed before the delay ends, the circuit **immediately deactivates**, and **C2 discharges**.  
- To **increase the maximum delay**, you can:  
  - **Increase capacitor C2** (doubling its value doubles the timing period).  
  - **Increase potentiometer RV1**, though this may distort the scale for long delays.  

### Power & Relay Specifications  
- The **relay can switch up to 2A at 230V**.  
- A **stable 12V power supply** is required for proper operation.  

## Project Photos  
Below are images showcasing different aspects of the project.  
