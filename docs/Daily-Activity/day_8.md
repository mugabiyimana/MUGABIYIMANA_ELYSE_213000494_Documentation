# 8. Activity of Day 8

## PCB Milling & Cutting

PCB milling is a **subtractive fabrication process** hat carves circuits from a copper-clad board.

Designing with milling in mind ensures a smooth transition from the digital PCB design to a functional physical board.

Milling-friendly designs are typically **single-sided** to simplify fabrication and reduce errors.  
Due to tool size limitations, **through-hole components or large SMD components** are preferred.  
Key design considerations include **tool diameter, trace spacing, clearance, and board thickness**.


### The Essence of PCB Milling

PCB milling allows designers to:

- Precisely remove copper from a copper-clad board to define circuit traces (**subtractive process**).  
- Rapidly prototype and test PCB designs in-house.  
- Fabricate boards independently without relying on external manufacturers, reducing time and cost.


### Understanding Traces, Clearance, Pads & Vias

1. **Trace Width**  
   Determines current-carrying capacity and machinability. Wider traces are stronger and easier to mill.

2. **Clearance**  
   Maintains isolation between traces and copper areas to prevent short circuits.

3. **Pads**  
   Are large enough to support reliable soldering and maintain mechanical stability.

4. **Vias**  
   Are difficult to mill on single-sided boards and are often replaced with wire jumpers in prototypes.



### Phyical fabrication process

Phyical fabrication  involves three main stages:

- Trace Isolation– The milling tool removes copper around traces, creating the circuit paths.  
- Hole Drilling – Holes are drilled for component leads and mounting points.  
- Board Profiling – The PCB outline is cut to separate the board from the raw material.


## Implementation 

!!! info "Recap from Day 3"
    This activity builds on **Day 3**, where a single-sided PCB is designed in KiCad:
    
    - ATtiny45 microcontroller  
    - LED controlled using a push button  
    - 6-pin ISP header for programming  
    
    ![](../images/day_3/view2_route.png){ width=400 }

    The schematic, component placement, and routed tracks are verified and prepared for fabrication.  
    This same design file is used for the PCB milling process.


== "Step 1: Preparation"

- The milling tool is mounted onto the machine.  
- **Carbide Motion** software is downloaded and installed.  
- The copper-clad board is secured on the cutter bed using double-sided tape.  
- In the project folder (in our case :Microcontroller_PCB_Design), the **Gerber folder** containing Gerber files is located.  
- The cutter is connected to Carbide Motion.  
- Gerber files are imported into Carbide Motion, which combines them into a single milling job.  
- Tool position, cutting depth, and speed parameters are carefully configured in Carbide motion.  


== "Step 2: Milling the Traces"

- The machine origin is set correctly.  
- Once all configurations are verified, the machine engraves the copper traces according to the PCB design.  

![Milling Traces](../images/day_7/day7_1.jpeg)

---

== "Step 3: Cutting the Board Outline"

- The milling bit is changed to the tool used for board profiling.  
- Tool position and depth are re-adjusted.  
- The machine cuts the PCB outline from the copper-clad board.  

![Cutting Outline](../images/day_7/day7_2.jpeg)

---

== "Result"

- The final PCB is successfully fabricated.  
- The board is ready for cleaning and component soldering.  

### Final PCB
![](../images/day_7/day.jpeg)
