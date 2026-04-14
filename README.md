# Synchronous FIFO RTL to GDSII ASIC Flow

This repository implements a parameterized synchronous FIFO and demonstrates a complete RTL-to-GDSII ASIC flow using open-source EDA tools.

## Tools Used
- Yosys (RTL synthesis)
- Synthesis by Yosys
- OpenSTA (Static Timing Analysis)
- OpenROAD (Floorplanning, Placement, CTS, Routing)
- KLayout (GDSII visualization)

## Design Overview
- Parameterized synchronous FIFO
- Full / Empty and Almost-threshold flags
- Single clock domain

## 2) Synthesis by Yosys
Paste these commands in Ubuntu:
```bash
cd ~/OpenLane
make mount
./flow.tcl -interactive
package require openlane
prep -design sync_fifo
run_synthesis
exit
```

## RTL-to-GDSII Flow
RTL → Synthesis → STA → Floorplanning → Placement → CTS → Routing → GDSII
