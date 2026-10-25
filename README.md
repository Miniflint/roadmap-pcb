# PCB Design Roadmap - Foundations to Professional Hardware

## Final goal: Design a PCB from scratch, understand every important electrical and physical decision, manufacture it, test it, debug it, and explain why the design works.

### Phase 0 - PCB Foundations
 - [ ] Understand the purpose of a printed circuit board.
 - [ ] Understand copper, substrate, solder mask, and silkscreen.
 - [ ] Understand PCB layers and copper thickness.
 - [ ] Understand tracks, pads, vias, and plated through-holes.
 - [ ] Distinguish through-hole and surface-mount components.
 - [ ] Understand nets, symbols, footprints, and schematics.
 - [ ] Understand electrical continuity and current return paths.
 - [ ] Understand the difference between a visually complete board and a functioning circuit.
 - [ ] Understand basic PCB manufacturing processes.
 - [ ] Learning resources
 - [ ] How PCBs Work - Layers, Copper, Vias, and Manufacturing
 - [ ] PCB Design for Beginners
 - [ ] How Electronic Components Are Mounted on PCBs
 - [ ] Practical work
 - [ ] Identify every connector, capacitor, and functional block on an existing PCB.
 - [ ] Identify the purpose of each copper layer.
 - [ ] Trace several connections from their physical pads back to the schematic.
 - [ ] Explain how current flows through a simple circuit and returns to its source.
 - [ ] Completion criteria

Phase 1 - KiCad Fundamentals
 - [ ] Navigate the KiCad project manager.
 - [ ] Create and organize a new project.
 - [ ] Use the schematic editor.
 - [ ] Place symbols and connect wires.
 - [ ] Annotate components.
 - [ ] Assign footprints to schematic symbols.
 - [ ] Understand symbol pins versus footprint pads.
 - [ ] Synchronize schematic changes with the PCB editor.
 - [ ] Draw the board outline.
 - [ ] Configure the grid, layers, and design rules.
 - [ ] Place components and interpret ratsnest lines.
 - [ ] Route tracks and add vias.
 - [ ] Create copper zones.
 - [ ] Use electrical and design rule checks.
 - [ ] Inspect the PCB in the 3D viewer.
 - [ ] Generate manufacturing files.
 - [ ] Learning resources
 - [ ] KiCad Beginner Tutorials - Complete Workflow
 - [ ] DigiKey - KiCad Tutorials
 - [ ] KiCad Official Learning Resources
 - [ ] KiCad Documentation
 - [ ] Practical project

Exercice:

Create a simple PCB containing:

 - [ ] A power input.
 - [ ] An LED and current-limiting resistor.
 - [ ] A connector.
 - [ ] A decoupling capacitor.

Completion criteria

 - [ ] You can independently create a simple KiCad project and understand how its schematic and PCB correspond.

Phase 2 - Electronics Fundamentals
Objective

Understand the electrical principles that determine whether a PCB works correctly.

Concepts
Voltage, current, resistance, and power.
Ohm's law.
Kirchhoff's current and voltage laws.
Series and parallel circuits.
Pull-up and pull-down resistors.
Capacitors and inductors.
RC time constants.
Diodes and transistors.
Voltage regulators and power supplies.
Logic levels and voltage compatibility.
Decoupling and bypass capacitors.
Current consumption and power budgets.
Voltage drops and trace resistance.
Reading component datasheets.
Understanding reference designs.
Learning resources
Afrotechmods - Electronics Fundamentals
Electronics Fundamentals - Voltage, Current, and Resistance
Decoupling Capacitors Explained
How to Read Electronic Component Datasheets
Practical project

Design a small power and indicator circuit.

Calculate the LED current and resistor value.
Estimate the circuit's power consumption.
Select appropriate components from datasheets.
Determine where the decoupling capacitor should be placed.
Check voltage and current requirements for each component.
Completion criteria

You can explain why components are present in a schematic and calculate basic electrical quantities without relying on a tutorial.

Phase 3 - Component Placement and PCB Routing
Objective

Learn to design layouts that are electrically sound, manufacturable, readable, and easy to debug.

Concepts
Place mechanical connectors and mounting holes first when their positions are constrained.
Group components by functional block.
Optimize component placement before routing.
Understand ratsnest lines and connection density.
Choose appropriate trace widths and clearances.
Configure net classes.
Understand vias and layer transitions.
Learn when 45-degree bends are useful.
Understand copper pours and ground planes.
Understand thermal reliefs and copper clearances.
Avoid unnecessary routing detours.
Preserve useful ground return paths.
Improve silkscreen readability.
Avoid overlapping labels and component markings.
Make connectors easy to identify and use.
Learning resources
PCB Placement and Routing Best Practices
KiCad Routing, Track Widths, Vias, and Copper Zones
PCB Ground Planes and Return Paths
PCB Layout Mistakes to Avoid
Practical project

Redesign an existing PCB without changing its electrical functionality.

Identify the major functional blocks.
Review component placement before changing any tracks.
Reduce unnecessary trace detours.
Review via usage.
Inspect ground-plane continuity.
Improve silkscreen and connector labeling.
Compare the original and revised layouts.
Completion criteria

You can explain why you placed each important component where it is and justify your routing decisions electrically, mechanically, and practically.

Phase 4 - Design Rules and Manufacturing
Objective

Prepare a PCB for fabrication and assembly, and understand the checks needed before ordering it.

Concepts
Understand Electrical Rules Check (ERC).
Understand Design Rules Check (DRC).
Interpret clearance violations.
Check minimum trace widths and spacing.
Check drill sizes and annular rings.
Check copper-to-edge clearances.
Verify footprints against mechanical drawings.
Verify connector orientation and pin numbering.
Understand solder mask and silkscreen constraints.
Understand PCB fabrication tolerances.
Generate Gerber files.
Generate drill files.
Inspect manufacturing outputs in a Gerber viewer.
Create a bill of materials (BOM).
Understand assembly drawings and pick-and-place files.
Review the PCB in 3D before fabrication.
Learning resources
KiCad DRC and Gerber Generation Tutorial
PCB Design for Manufacturing (DFM)
PCB Manufacturing Explained
KiCad Official Documentation
Practical project

Prepare a manufacturing package for your PCB.

Run ERC and investigate relevant errors.
Run DRC and resolve unintended violations.
Document intentional exceptions.
Verify connector pinouts and component footprints.
Generate Gerber and drill files.
Inspect all exported layers.
Generate a BOM and assembly drawing.
Verify the manufacturing files before ordering.
Completion criteria

You can produce and inspect a manufacturing package and explain what each file is used for.

Important: A clean DRC report does not guarantee that a circuit is electrically correct. Design checks must be combined with schematic review, datasheet verification, and appropriate testing.

Phase 5 - Power Integrity and Signal Integrity
Objective

Understand how electrical behavior, electromagnetic fields, and current return paths affect PCB performance.

Concepts
Understand current return paths.
Understand ground-plane continuity.
Understand why ground-plane gaps can cause problems.
Understand decoupling capacitor placement.
Understand power distribution and voltage drop.
Estimate trace resistance and copper heating.
Understand switching noise.
Understand crosstalk and electromagnetic interference (EMI).
Distinguish clock frequency from signal rise time.
Understand when transmission-line effects matter.
Understand characteristic impedance.
Understand signal termination.
Understand when controlled impedance is required.
Understand two-layer and four-layer stackups.
Learning resources
Phil's Lab - PCB Design and Signal Integrity
Robert Feranec - PCB Stackup and Return Paths
High-Speed PCB Design Fundamentals
PCB Power Integrity Explained
Practical project

Review your PCB's important power and signal paths.

Identify the current return path for each important signal.
Check for routes crossing gaps in their reference ground plane.
Review the placement and connections of decoupling capacitors.
Estimate voltage drops on important power traces.
Identify signals that may need special routing constraints.
Determine whether a two-layer board is adequate for the application.
Completion criteria

You can explain why grounding, decoupling, and return paths matter, and identify when ordinary routing practices are insufficient.

Phase 6 - Embedded Hardware and Digital Interfaces
Objective

Learn how microcontrollers, sensors, storage devices, and communication interfaces influence PCB design.

Concepts
GPIO inputs and outputs.
Logic-level compatibility.
Input protection.
UART communication.
SPI communication.
I2C communication.
Clock signals and timing.
Reset circuits.
Boot configuration.
Programming and debugging headers.
SD-card interfaces.
Connector pinouts.
ESD protection.
Power requirements of embedded modules.
Reading module reference designs.
Learning resources
Phil's Lab - Embedded Hardware and PCB Design
SPI Communication Explained
I2C Communication Explained
SD Card Hardware Interface Design
GNSS Module Hardware Design
Practical project

Document and verify every connector on your existing PCB.

For each pin, record:

Field	Description
Pin number	Physical pin identifier
Signal	Signal name
Direction	Input, output, bidirectional, or power
Voltage	Expected logic or supply voltage
Function	Purpose of the signal
Source	Schematic, datasheet, or reference design
Verify every connector pin against the schematic.
Check voltage compatibility between connected modules.
Identify programming and debugging access.
Verify reset and boot requirements.
Check signal routing against the interface requirements.
Completion criteria

You can explain how the major interfaces operate and identify the electrical requirements that affect their PCB implementation.

Phase 7 - RF and Antenna Design
Objective

Learn the fundamentals of radio-frequency circuits and antenna integration.

Prerequisite: Basic electronics and an understanding of PCB routing, grounding, and signal integrity.

Concepts
Frequency, wavelength, and electromagnetic fields.
Antenna types and their operating principles.
PCB antenna geometry.
Ground-plane and keep-out requirements.
RF feed lines.
Controlled impedance.
Matching networks.
S-parameters and reflection.
Antenna placement and nearby conductive materials.
GPS/GNSS antenna requirements.
Vector network analyzer (VNA) measurements.
Antenna tuning and validation.
Learning resources
PCB Antenna Design Tutorials
RF PCB Layout Fundamentals
GNSS Antenna Design and Integration
Antenna Tuning with a VNA
Practical project

Investigate the antenna section of your PCB.

Identify the actual antenna technology.
Find the antenna or module manufacturer's reference design.
Review the recommended ground plane and keep-out area.
Verify the RF feed and any matching components.
Review the placement of nearby copper and components.
Determine how antenna performance should be measured.
Completion criteria

You can explain the antenna implementation and justify the layout against its documented design requirements.

Warning: Do not assume that a meandered trace is a correctly designed antenna. Antenna performance depends on geometry, frequency, ground structure, matching, nearby materials, and the complete physical design.

Phase 8 - Testing, Measurement, and Debugging
Objective

Learn to verify that a manufactured PCB works and diagnose problems systematically.

Concepts
Multimeter continuity measurements.
Resistance and voltage measurements.
Identifying power-to-ground shorts.
Safe first power-up procedures.
Current-limited bench supplies.
Oscilloscope fundamentals.
Logic analyzer fundamentals.
Debugging SPI, I2C, and UART.
Identifying incorrect supply voltages.
Diagnosing noise and communication failures.
Inspecting solder joints.
Diagnosing connector and assembly faults.
Reproducing faults systematically.
Recording test results.
Creating and validating corrective revisions.
Learning resources
EEVblog - Electronics Troubleshooting
Oscilloscope Fundamentals
Logic Analyzer - SPI and UART Debugging
How to Debug a PCB That Does Not Work
Practical project

Create and execute a test plan for your PCB.

Inspect the board visually before applying power.
Check for shorts between power rails.
Confirm supply polarity.
Identify expected supply voltages.
Power the board using an appropriate current limit.
Measure the important power rails.
Test each communication interface.
Record observed results and compare them with expectations.
Document and resolve any faults.
Retest after making modifications.
Completion criteria

You can bring up a board safely, verify its main functions, and diagnose common hardware failures using measurements rather than guesswork.

Phase 9 - Professional Hardware Engineering
Objective

Develop the workflow and engineering judgment needed to produce maintainable, repeatable, and reliable hardware.

Concepts
Component selection and lifecycle management.
BOM management and component alternatives.
Version control for hardware projects.
Schematic and PCB revision management.
Hardware design reviews.
Test points and serviceability.
Manufacturing documentation.
Four-layer PCB stackup design.
High-current routing and thermal design.
Advanced interface constraints.
EMC design and compliance.
Reliability and environmental considerations.
Automated checks and design workflows.
Production testing and test fixtures.
Learning resources
Professional PCB Design and Review
Four-Layer PCB Design
PCB Design for Manufacturing and Assembly
KiCad Official Learning Resources
Practical project

Prepare a complete hardware repository.

Publish the schematic and PCB files.
Include a BOM.
Include fabrication outputs.
Include assembly documentation.
Include a test plan and measured results.
Document design decisions and known limitations.
Track revisions using version control.
Record any hardware modifications.
Explain what changed between revisions and why.
Completion criteria

Someone else can inspect your project, understand the design decisions, manufacture the board, assemble it, and reproduce the documented tests.

Capstone Project - Redesign My PCB
Objective

Apply the roadmap to an existing PCB and produce a demonstrably improved revision.

Starting project: Roadmap-EPFL repository is the inspiration for the learning structure. Use your existing KiCad PCB as the actual hardware project.

Stage 1 - Understand the existing design
Document the purpose of the board.
Identify all functional blocks.
Trace the schematic to the PCB.
Document every connector pinout.
Identify power rails and current requirements.
Identify the antenna and module requirements.
Check component datasheets and footprints.
Stage 2 - Improve the layout
Reconsider component placement.
Reduce unnecessary routing detours.
Review track widths and clearances.
Inspect via usage.
Verify ground-plane continuity.
Review decoupling capacitor placement.
Improve silkscreen and connector markings.
Check mounting holes and mechanical clearances.
Stage 3 - Verify the design
Run ERC.
Run DRC.
Resolve unintended errors and document exceptions.
Verify connector numbering and orientation.
Verify component footprints.
Inspect the board in 3D.
Generate Gerber and drill files.
Inspect the exported manufacturing files.
Stage 4 - Manufacture and test
Order the PCB.
Assemble the components.
Inspect solder joints and component orientation.
Check power rails before connecting sensitive hardware.
Perform a safe first power-up.
Test every important interface.
Verify antenna performance if applicable.
Record test results.
Fix any issues and produce a new revision if necessary.
Stage 5 - Publish the final project
Include the source project.
Include a BOM and manufacturing outputs.
Include clear board images and a 3D render.
Include the design verification checklist.
Include test results.
Document the main design decisions.
Document known limitations.
Explain what you learned and what you would improve next.
Final deliverable

Final Principles
Understand before copying. Tutorials teach techniques; engineering requires understanding when and why to use them.
Design from the schematic outward. The PCB must implement the circuit correctly before it can be considered visually successful.
Read datasheets. Never assume that a component or module behaves a certain way based only on its appearance.
Verify everything important. Use calculations, design checks, physical measurements, and tests.
Learn by building. Each major phase should result in a tangible improvement or a working project.
Treat failures as engineering data. Document what happened, determine the cause, and verify the correction.
Optimize for correctness first. Shorter traces and cleaner visuals are valuable only when the electrical, mechanical, and manufacturing requirements are satisfied.

The ultimate goal is not to become someone who can route a PCB. It is to become someone who understands why the PCB is designed that way-and can prove that the resulting hardware works.