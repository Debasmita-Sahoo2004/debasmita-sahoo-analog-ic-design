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
dynamics<img width="493" height="350" alt="image" src="https://github.com/user-attachments/assets/36c29a61-8c1f-46ec-98bd-d9ae5a88f504" />



 4. Current Mirror
The circuit is used to copy the flow of current in one active device and controlling the flow of current in another device by maintaining the output current stable instead of loading


<img width="931" height="394" alt="image" src="https://github.com/user-attachments/assets/cde52ead-6413-4132-a3c2-758ab694a16b" />


high-Pass Filter Circuit
This section explains the working and transfer function of a high-pass filter using an op-amp.
<img width="1080" height="630" alt="image" src="https://github.com/user-attachments/assets/8f525803-68dc-4ecd-bec3-93e7b451ef45" />

High-Pass Filter Circuit
🧰 Circuit Overview
Input Capacitor C_i = 4.7μF: Blocks DC
Resistors R_i = R_f = 5kΩ: Define gain and cutoff
Op-Amp in non-inverting configuration
🧮 S-Domain Transfer Function
H(s) = (Rf * s * Ci) / (1 + s * Ri * Ci)

At low frequencies → H(s) → 0 (attenuates low freq)
At high frequencies → H(s) → 1 (passes high freq)
🔻 Cutoff Frequency (fc)
fc = 1 / (2πRiCi) ≈ 6.77 Hz For Ri = 5kΩ, Ci = 4.7μF

🖼️ Op-Amp Schematic Diagram
Detailed internal schematic of the operational amplifier:
<img width="941" height="451" alt="image" src="https://github.com/user-attachments/assets/3632824a-8470-4881-bbf8-7bbcf2c4cbbb" />
Op-Amp Symbolic Diagram
Standard symbolic representation of an operational amplifier:
<img width="1015" height="667" alt="image" src="https://github.com/user-attachments/assets/44112f46-b39a-46b1-8e5d-a6be2d4df3d2" />
Opamp Symbol
📐 High-Pass Filter Circuit Using the Op-Amp
High-pass filter circuit built using the op-amp symbol shown above: High-Pass Circuit
<img width="791" height="621" alt="image" src="https://github.com/user-attachments/assets/a8c04e17-b2c7-4b1f-94b4-d43bb1ca61dd" />
Frequency Response Plot of the High-Pass Filter
The plot below shows the frequency response (gain vs frequency) of the high-pass filter circuit. Frequency Response
<img width="1411" height="508" alt="image" src="https://github.com/user-attachments/assets/47234eb4-f0d7-4a13-996a-437487d548ef" />















