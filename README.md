32X32 SRAM ARRAY DESIGN (1kb)

A 6T SRAM cell is a widely used memory cell configuration in digital integrated circuits, offering high-speed performance and robust data stability. The "6T" designation refers to the six transistors that make up each cell: four for the core latch that stores a bit of data and two additional access transistors for reading and writing data. This structure provides a balance between area efficiency and data stability, making the 6T SRAM cell ideal for cache memory in processors, where speed and reliability are critical.

The basic operation of a 6T SRAM cell leverages the bistable nature of cross-coupled inverters to hold a stable logic state '0' and '1' without the need for refreshing, unlike dynamic RAM cells. When data is written, the access transistors enable the bit lines to set the state of the cell. During a read operation, these same transistors allow the stored state to be sensed on the bit lines, aided by pre-charged sense amplifiers. The design of a 6T SRAM cell allows it to retain its data as long as power is supplied, making it "static" in nature.

While the 6T SRAM cell is efficient in terms of read/write performance, it faces challenges with area and power consumption as technology scales down. Transistor dimensions must be carefully managed to ensure reliable performance, and leakage currents need to be minimized for power efficiency. As a result, ongoing research in SRAM technology aims to enhance the performance, stability, and density of 6T SRAM cells for modern applications in low-power and high-performance computing.

SCHEMATIC OF 6-T SRAM:

<img width="432" height="324" alt="image" src="https://github.com/user-attachments/assets/39f9c9c4-875b-4543-b685-c695ff84d54b" />

The schematic of the 6-T SRAM is as shown in the figure. The transistors M1 and M2 will form an inverter, and similarly the transistors M4 and M3 also forms an inverter. These 2 inverters will be inter connected to each other. This is the main circuit which is used for storing the bit. M5 and M6 are called the access transistors, where these two transistors gates are connected to each other. This control is called as the write line. When write line is high then the access transistors will be turned ON and if write line if low then then the access transistors will be turned OFF. The source or drain of these access transistors will be connected to the bit line and bit line bar. These bit line and bit line bar are crucial for the operation of the SRAM, because for read operation we will be accessing the data to this line and for write operation we will be giving the data from this line. Hence this line is very important. 

The points Q and Q bar are the 2 node points where the data can be taken out or written into the actual SRAM cell. Suppose if we are doing the write operation the data should be written to the point Q and while reading, we should be reading the data from this point. If Q is high then data read should be high else low. 

DESIGN METHODOLOGY:

The design and simulation of the 6T SRAM cell is conducted in Cadence Virtuoso software. First we will be doing the schematic design and then for the cell designed we are designing a testbench for analysis and simulation. For simulation we will be using ADEL simulator. Next after this we will be designing the layout of the cell and do the DRC and LVS test, later will do the quantus design and for the generated view we will be doing the post layout simulation again for the designed layout. Next for the design we will be checking the power analysis and SNA for the design. The complete details of the design will be given below.

32x32 SRAM ARRAY

SRAM CELL

<img width="700" height="700" alt="SRAM cell 6T" src="https://github.com/user-attachments/assets/98d5eb59-5dca-48a0-aecb-206615ae9005" />


PRECHARGE CELL

<img width="400" height="700" alt="Precharge Cell" src="https://github.com/user-attachments/assets/9ac4fa2b-f575-49a6-993a-02d92470a6c6" />


SENSE AMPLIFIER

<img width="500" height="500" alt="Sense Amplifier" src="https://github.com/user-attachments/assets/ac38cfed-a088-4a33-8316-d66b49201a26" />


COLUMN MULTIPLEXER

<img width="300" height="500" alt="Column Multiplexer" src="https://github.com/user-attachments/assets/c647a096-733b-4dec-9d9c-19f9084e11f7" />


COMPLETE SCHEMATIC

<img width="543" height="726" alt="Complete 32x32 SRAM array schematic" src="https://github.com/user-attachments/assets/ceaf2359-fcee-4929-a428-e7a508246fb4" />


COMPLETE LAYOUT

<img width="1162" height="657" alt="Layout Complete 32x32 SRAM 2 array" src="https://github.com/user-attachments/assets/579b42cf-bd94-4d48-af7e-daa6533895c5" />


REFERENCES

[1] Y. -B. Liao, M. -H. Chiang, N. Damrongplasit, W. -C. Hsu and T. -J. K. Liu, "Design of Gate-All-Around Silicon MOSFETs for 6-T SRAM Area Efficiency and Yield," in IEEE Transactions on Electron Devices, vol. 61, no. 7, pp. 2371-2377, July 2014, doi: 10.1109/TED.2014.2323059.
[2] V. Singh, S. K. Singh and R. Kapoor, "Static Noise Margin Analysis of 6T SRAM," 2020 IEEE International Conference for Innovation in Technology (INOCON), Bangluru, India, 2020, pp. 1-4, doi: 10.1109/INOCON50539.2020.9298431
[3] Y. -T. Chiang and Y. -J. Chang, "A New SRAM Cell Design for Both Power and Performance Efficiency," 2009 IEEE International Workshop on Memory Technology, Design, and Testing, Hsinchu, Taiwan, 2009, pp. 13-19, doi: 10.1109/MTDT.2009.13.
[4] Jan M, Rabaey, et al, Digital Integrated Circuits: A Design Perspective, Prentice Hall, 2003.
[5] Neil Weste and K. Eshragian, Principles of CMOS VLSI Design: A System Perspective, Pearson Education, 2000. 



