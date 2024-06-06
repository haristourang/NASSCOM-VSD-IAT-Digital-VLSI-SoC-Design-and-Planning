# NASSCOM-VSD-IAT-Digital-VLSI-SoC-Design-and-Planning
This is the repository including the simple example of a Digital VLSI SoC Design and Planning workshop conducted by NASSCOM. The open source tool OpenLane was used to performed flow. Skywater130A tech file was used for the design.

OpenLANE  is an open-source, full-featured physical design flow tool for VLSI (Very Large Scale Integration). It is intended to help with every step of the integrated circuit (IC) design process, from register-transfer level (RTL) to general layout specifications (GDSII), which are needed to manufacture the chip. OpenLANE offers a complete and configurable design flow by integrating a number of open-source tools and components. 

The RTL2GDS flow can be broadly categorized into four main steps: Synthesis, Floorplanning and Placement, Routing, and Signoff. Here is an overview of each step:
1. Synthesis
Purpose: Convert the RTL code into a gate-level netlist.
* Input: RTL code (Verilog or VHDL).
* Process:
    * The RTL code is analyzed and optimized.
    * The high-level constructs are mapped to a technology-specific library of standard cells.
* Output: Gate-level netlist.
* Tools: Yosys (in OpenLANE).
2. Floorplanning and Placement
Purpose: Define the physical structure and arrangement of cells on the chip.
Floorplanning
* Input: Gate-level netlist.
* Process:
    * Define the size and shape of the chip.
    * Allocate areas for different functional blocks.
    * Plan the placement of major components and power/ground networks.
* Output: Floorplan with block placements.
Placement
* Input: Floorplan and gate-level netlist.
* Process:
    * Place the standard cells in the defined floorplan.
    * Optimize placement to meet timing and area constraints.
* Output: Placed netlist.
* Tools: OpenROAD for floorplanning and placement.
3. Routing
Purpose: Connect the placed cells according to the netlist.
* Input: Placed netlist.
* Process:
    * Create a routing plan to interconnect all the cells.
    * Optimize routing to minimize wire length, delay, and congestion.
    * Implement the power and clock distribution networks.
* Output: Routed design.
* Tools: OpenROAD for global and detailed routing.
4. Design Rule Check (DRC) & Layout Versus Schematic (LVS)
Purpose: Verify that the design meets all the necessary requirements and is ready for manufacturing.
* Input: Routed design.
* Process:
    * Design Rule Check (DRC): Ensure the layout complies with manufacturing rules.
    * Layout Versus Schematic (LVS): Verify that the layout matches the original netlist.
    * Timing Analysis: Ensure the design meets timing constraints.
    * Power Analysis: Verify power integrity and consumption.
* Output: Verified design ready for GDSII export.
* Tools:
    * Magic for DRC.
    * Netgen for LVS.
    * OpenSTA for static timing analysis


## Day 1: Inception of open-source EDA and OpenLANE and Sky130 PDK

First day session is on the synthesis process of a ‘picorv32‘  design employing the OpenLane flow. The netlist as well as essential reports are generated utilizing the folllowing synthesis process.

The commands below are used in to execute the synthesis and create a netlist.
Firstly, an environment is set for the design to be synthesized utilizing the Openlane. The following commands are used to create the environment:

Changing the directory to openlane:
cd /home/Desktop/work/tools/openlane_working_dir/openlane

Running the flow.tcl in the interactive mode-
 ./flow.tcl script -interactive

Loading the package openlane 0.9-
package require openlane 0.9

Preparing the design files (run)-
prep -design picorv32a

Carrying out the synthesis using the command-
run_synthesis

### Assignment 1


## Day 2: Good floorplan vs bad floorplan and introduction to library cells







Characterization of cell:
Find 4 values:
(a)	Rise transition: Time taken to transit from 20% to 80% of maximum signal value, VDD
Rise transition: 2.24696 ns – 2.18265 ns = 0.06431 ns

(b)	Fall transition: Time taken for output to fall from 80% to 20% of the signal VDD
Fall transition: 4.09551 ns – 4.05316 ns = 0.04235 ns
(c)	Rise cell delay: Rise delay through the cell based on the input slew and output load (time period between 50% rise in output and 50% rise in input)












Cell Rise Delay: 2.21155 ns – 2.15009 ns = 0.06146 ns


(a)	Cell fall delay: Difference in time period when the output has fallen to its 50% and when the input has raised towards 50%











Cell Fall Delay: 4.7835 ns – 4.05 ns = 0.02835 ns

Including the custom inverter in the picorv32a


