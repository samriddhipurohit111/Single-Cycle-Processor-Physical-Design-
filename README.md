Physical Design Exploration of a Single-Cycle Processor using Cadence Tools
---

This project explores the physical design implementation of a modular single-cycle processor using Cadence EDA tools. The work focuses on the backend design flow, starting from RTL synthesis and proceeding through floorplanning, pin placement, and routing.

The RTL modules of the processor—including the Program Counter, Control Unit, ALU, Register File, Immediate Generator, and Memory Interfaces—were provided by a teammate from the 1TOPs team. My primary contribution involved performing the physical design implementation of the processor using Cadence tools.



Project Workflow

The project follows the standard ASIC physical design flow:

1. RTL Synthesis using Cadence Genus
2. Gate-Level Netlist Generation
3. Floorplanning and Macro Instantiation
4. Pin Placement
5. Placement and Routing using Cadence Innovus

To automate synthesis, a custom TCL script was used to read RTL modules, apply timing constraints, and generate the gate-level netlist.

A design challenge in the implementation was the memory architecture. The processor required 32-bit instruction and data memories, while the available memory macros were 16-bit wide, requiring multiple macro instantiations to construct the required memory structures.

Tools Used

Cadence Genus – RTL synthesis
Cadence Innovus – Physical design implementation
TCL scripting – Automation of synthesis flow

Design Snapshots
Gate-Level Netlist Generation via TCL-Based RTL Synthesis
---

Synthesis through Genus.jpeg


Gate-level representation of the single-cycle processor generated after RTL synthesis using Cadence Genus. The synthesis process was automated using a custom TCL script that reads RTL modules, applies timing constraints, and generates the synthesized netlist used for physical implementation.


Processor Floorplan with Memory Macro Instantiation
---

Processor Floorplan with Memory Macro Instantiation.jpeg


Initial floorplan of the processor design showing the instantiation and placement of memory macros.

The processor architecture required 32-bit instruction and data memories, while the available memory macros were 16-bit wide. Multiple macro instances were therefore used to construct the required memory structure within the floorplan.



Pin Placement and Macro Integration
---

Pin Placement and Macro Integration in Processor Layout.jpeg


Pin placement stage showing the positioning of input and output pins along with the instantiated memory macros within the processor layout.

This stage defines the locations of IO connections for the design prior to routing.




Routed Layout of the Processor
---
Routed Layout of Single Cycle Processor.jpeg

Final physical implementation stage showing placement and routing of the processor design using Cadence Innovus.

The layout illustrates multi-layer routing connecting datapath modules and memory macros within the processor architecture. Further layout refinement would improve routing quality and help satisfy physical design constraints.



Learning Outcomes
---
This project provided practical exposure to:
ASIC physical design flow

Processor datapath integration

Macro-based floorplanning

Memory macro instantiation strategies

Placement and routing considerations

TCL-based synthesis automation
