This project is part of [Udacity's Embedded Systems Advanced Nanodegree](https://github.com/mazarona/embedded-systems-advanced-nanodegree)

# Block Diagram
![block diagram](images/diagram.png?raw=true "block diagram")

# Static Design

### ECU 1 Layered Archeticture
![ecu1 static](images/ecu1_static_design.png?raw=true "ecu1 static")


### ECU 2 Layered Archeticture
![ecu2 static](images/ecu2_static_design.png?raw=true "ecu2 static")


> [!NOTE]
> For complete description of each software module API please check the [static design and folder structure pdf.](static-design/static_design_and_folder_structure.pdf)

# Dynamic Design


### ECU 1 Sequence Diagram
![ecu1 sequence diagram](images/ecu1_sequence_diagram.png?raw=true "ecu1 sequence diagram")

### ECU 2 Sequence Diagram
![ecu2 sequence diagram](images/ecu2_sequence_diagram.png?raw=true "ecu2 sequence diagram")

# CPU Load
## ECU 1
$$
U = \frac{E_1 + E_2 + E_3}{H} = \frac{1 \cdot 1 + 1 \cdot 2 + 1 \cdot 4}{20} \cdot 100 = 35\%
$$

## ECU 2
$$
U = \frac{E_1}{H} = \frac{1 \cdot 1}{5} \cdot 100 = 20\%
$$


# Bus Load

Assume:
- Frame = 32bit
- bitrate = 100kBit/s
1. 
$$
t_{\text{frame}} = \frac{32 \, \text{bits} \cdot 1}{100 \, \text{kBits/s}} = 320 \, \mu s
$$
2. 
$$
\#\text{frames/sec} = \frac{1000}{5} + \frac{1000}{10} + \frac{1000}{20} = 350
$$
3. 
$$
t_{\text{bus}} = 350 \cdot 320 \, \mu s = 112000 \, \mu s = 0.112 \, \text{s}
$$
4. 
$$
\text{Bus Load} = 0.112 \cdot 100 = 11.2\%
$$

