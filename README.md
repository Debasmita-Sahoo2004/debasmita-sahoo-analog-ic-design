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


📈 Output Response of the Microphone Circuit
The simulation below shows the voltage output (vout) across the load, after signal amplification and filtering.

Mic Output Plot

<img width="1415" height="708" alt="image" src="https://github.com/user-attachments/assets/13cbe469-3be9-41e5-ac2f-855d71489827" />
🧪 This waveform helps verify if the designed circuit properly amplifies the mic signal within expected voltage ranges.

📈 Frequency Response
The frequency response reveals the bandwidth and filtering effects of the analog stage. Mic Frequency Response
<img width="1600" height="659" alt="image" src="https://github.com/user-attachments/assets/24fdd596-088f-4ef6-8175-297d91308078" />


🔁 Simulink Output
The Simulink simulation confirms system-level behavior and time-domain signal dynamics.

<img width="488" height="347" alt="image" src="https://github.com/user-attachments/assets/75b136da-f742-49f7-8be8-70ceae41d0b6" />


Op-Amp Modeling as a Single Pole System
To better analyze the frequency response of the analog front-end, the operational amplifier is modeled using a single-pole transfer function. This provides insight into the bandwidth limitations and phase behavior of the amplifier.

<img width="1606" height="780" alt="image" src="https://github.com/user-attachments/assets/07f3dffb-134c-4849-957a-2b9cdea4d1b2" />

Simulink Output
The Simulink simulation confirms system-level behavior and time-domain signal
d<img width="493" height="350" alt="image" src="https://github.com/user-attachments/assets/36c29a61-8c1f-46ec-98bd-d9ae5a88f504" />
ynamics. 




