# debasmita-sahoo-analog-ic-design
📘 Analog IC Design Internship Report
Name: DEBASmita sahoo
SIC: 23BEEG23
Branch: Electrical & Electronics Engineering
Duration: June 2nd, 2025 – June 20th, 2025
Mentor: Dr. Saroj Rout

🛠️ Software Used
Xschem
Ngspice
Siliwiz
Git & GitHub



📑 Table of Contents
USB Microphone System Analysis
High-Pass Filter Circuit
Siliwiz Simulation
Current Mirror
FET Characterization
NFET Characterization


1. USB Microphone System Analysis
This section explains the analog front-end of a U<img width="1280" height="666" alt="Fig-d1-1-USBmic" src="https://github.com/user-attachments/assets/65b8bcad-cd76-4fae-9a87-7e56adb0e517" />
SB microphone setup and its role in signal conditioning and conversion.



🔧 System Overview
MEMS Microphone (SPH8878LR5H-1): Captures sound and outputs an analog voltage signal
Op-Amp (OPA344): Amplifies & filters
ADC + USB Output: Digitizes and sends to PC
🎧 This design enables real-time USB-MIDI output via analog signal conditioning.

🎛️ Thevenin Equivalent Model of the Microphone
To understand the microphone as a signal source, it can be modeled with its Thevenin equivalent:

This model helps in:

Analyzing signal strength and loading
Impedance matching for the amplifier input
Ensuring minimal signal loss at the interface
<img width="1423" height="788" alt="image" src="https://github.com/user-attachments/assets/37591836-3079-460e-8960-1e0830cc39d4" />


