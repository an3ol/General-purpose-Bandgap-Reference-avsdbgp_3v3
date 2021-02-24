# General Purpose Bandgap Reference-avsdbgp_3v3

A Bandgap Reference is an analog circuit, which is used to provide a constant output reference voltage being independent of Temperature, Process and Supply voltage variations. The analog IP **avsdbgp_3v3** is a General Purpose Bandgap Reference ciruit, which is designed using **Sky130nm** technology in this project. The project is executed during **VSD IP Research Internship**  under **VLSI System Design (VSD) Corp. Pvt. Ltd.**

For detailed information regarding the Bandgap Reference circuit click [here](https://github.com/an3ol/General-purpose-Bandgap-Reference-avsdbgp_3v3/blob/main/Documents/General_purpose_BGR.pdf). The Design specifications provided for avsdbgp_3v3 can be found [here](https://github.com/an3ol/General-purpose-Bandgap-Reference-avsdbgp_3v3/blob/main/Documents/Specifications.pdf). 

<p>&nbsp;</p>

# Table of Contents
* Pre Layout Performance parameters Bandgap Reference IP
 
* Circuit Implementation of Bandgap Reference IP

  - Block Diagram of Bandgap Reference IP
  - Schematic of Bandgap Reference IP
* Pre-Layout Simulation of Bandgap Reference IP circuit using Ngspice
  - Ngspice
  - Simulation plots of Bandgap Reference IP circuit
  - Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot
  - Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot
  - Temperature Coefficient of Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot
  - Voltage Coefficient of Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot
  - Start-Up Time of Vbgp @ RL = 100M ohms plot
  - On-Off-Current of Vbgp wrt Enable @ RL = 100M ohms plot

<p>&nbsp;</p>

# Pre Layout Performance parameters Bandgap Reference IP
<p>&nbsp;</p>

|  Parameter  |        Description             |    Min      |     Type    |    Max      |     Unit    | Condition  |
|   :----:    |          :----:                |   :----:    |    :----:   |   :----:    |    :----:   |   :----:   |
|    VBGP     | Output reference voltage       |   1.20284   |    1.2056   |   1.20562   |     Volt    | T= -40 to 140C, VDD=3.3V |
|    VBGP     | Output reference voltage       |   1.12184   |   1.20552   |   1.22796   |     Volt    | VDD=2V to VDD=4V, T=27C |
|     VDD     |      Supply Voltage            |             |    3.3      |             |     Volt    | T=-40C to 125C|
|     IDD     |      Supply Current            |             |    22.005   |             |      uA     |    EN=1    |
|     IDD     |      Supply Current            |             |    37.3134  |             |      pA     |    EN=0    |
|     RL      |      Load Resistance           |             |     100     |             |      Mohm   |VDD=3.3V, T=27C|
<p>&nbsp;</p>

# Circuit Implementation of Bandgap Reference IP 
## Block Diagram of Bandgap Reference IP
![Block diagram](https://raw.githubusercontent.com/an3ol/General-purpose-Bandgap-Reference-avsdbgp_3v3/main/Results/block_diagram.png)

## Schematic of Bandgap Reference IP
<p>&nbsp;</p>

![Schematic](https://raw.githubusercontent.com/an3ol/General-purpose-Bandgap-Reference-avsdbgp_3v3/main/Results/Schematic.png)
<p>&nbsp;</p>

# Pre-Layout Simulation of Bandgap Reference IP circuit

The circuit implementation of Bandgap reference IP **avsdbgp_3v3** is simulated using Ngspice to analyse its performance according to the Design Specifications provided. 
<p>&nbsp;</p>

## Ngspice
Ngspice is an open source mixed-signal circuit simulator. To install Ngspice on Ubuntu, open terminal window and type :-
>`sudo apt-get install -y ngspice`

After successful installation, to invoke Ngspice type the following command on the terminal window.
>`ngspice <circuit file to be simulated>`

<p>&nbsp;</p>

## Simulation plots of Bandgap Reference IP circuit
<p>&nbsp;</p>

The files from this repository can be downloaded and used by the following commands :-
>`sudo apt install -y git`

>`git clone https://github.com/an3ol/General-purpose-Bandgap-Reference-avsdbgp_3v3.git`

>`cd Circuits`
<p>&nbsp;</p>

## Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot
<p>&nbsp;</p>
To observe the effect of temperature on the circuit, the temperature is varied from -40C to 140C. On the terminal window, type :-
<p>&nbsp;</p>

>`ngspice temp_avsdbgp_3v3.cir`
<p>&nbsp;</p>
The output plot as obtained can be seen below :-

<p>&nbsp;</p>

![Vbgp vs Temperature](https://github.com/an3ol/General-purpose-Bandgap-Reference-avsdbgp_3v3/blob/main/Results/temp.png?raw=true)
<p>&nbsp;</p>


![Vbgp Vptat Vctat vs Temperature](https://github.com/an3ol/General-purpose-Bandgap-Reference-avsdbgp_3v3/blob/main/Results/temp_all.png?raw=true)
<p>&nbsp;</p>

## Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot
<p>&nbsp;</p>
To observe the effect of Supply voltage on the circuit, the temperature is varied from 2V to 4V. On the terminal window, type :-
<p>&nbsp;</p>

>`ngspice vdd_variation_avsdbgp_3v3.cir`
<p>&nbsp;</p>
The output plot as obtained can be seen below :-
<p>&nbsp;</p>

![Voltage vs Vbgp](https://github.com/an3ol/General-purpose-Bandgap-Reference-avsdbgp_3v3/blob/main/Results/vdd_variation.png?raw=true)
<p>&nbsp;</p>

## Temperature Coefficient of Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot
<p>&nbsp;</p>
On the terminal window, type :-
<p>&nbsp;</p>

>`ngspice Temp_coeff_avsdbgp_3v3.cir`
<p>&nbsp;</p>
The output plot as obtained can be seen below :-
<p>&nbsp;</p>

![Temperature coefficient of Vbgp](https://github.com/an3ol/General-purpose-Bandgap-Reference-avsdbgp_3v3/blob/main/Results/temp_coeff.png?raw=true)
<p>&nbsp;</p>

# Voltage Coefficient of Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot
<p>&nbsp;</p>
On the terminal window, type :-
<p>&nbsp;</p>

>`ngspice voltage_coeff_avsdbgp_3v3.cir`
<p>&nbsp;</p>
The output plot as obtained can be seen below :-
<p>&nbsp;</p>

![Voltage coefficient of Vbgp](https://github.com/an3ol/General-purpose-Bandgap-Reference-avsdbgp_3v3/blob/main/Results/voltage_coeff.png?raw=true)
<p>&nbsp;</p>

# Start-Up Time of Vbgp @ RL = 100M ohms plot
<p>&nbsp;</p>
On the terminal window, type :-
<p>&nbsp;</p>

>`ngspice Start_up_avsdbgp_3v3.cir`
<p>&nbsp;</p>
The output plot as obtained can be seen below :-
<p>&nbsp;</p>

![Start up circuit](https://github.com/an3ol/General-purpose-Bandgap-Reference-avsdbgp_3v3/blob/main/Results/Startup.png?raw=true)
<p>&nbsp;</p>

# On-Off-Current of Vbgp wrt Enable @ RL = 100M ohms plot
<p>&nbsp;</p>
On the terminal window, type :-
<p>&nbsp;</p>

>`ngspice enable_current.cir`
<p>&nbsp;</p>
The output plot as obtained can be seen below :-
<p>&nbsp;</p>

![Enable](https://github.com/an3ol/General-purpose-Bandgap-Reference-avsdbgp_3v3/blob/main/Results/Enable_current.png?raw=true)
<p>&nbsp;</p>


# Acknowledgement

* [Kunal Ghosh](https://github.com/kunalg123), Co-founder of VLSI System Design (VSD) Corp. Pvt. Ltd
* [Sheryl Corina Serrao](https://github.com/sherylcorina), Undergraduate Student, Mumbai University.

# Contact Information
* Anmol Purty - nmlpurty@gmail.com
