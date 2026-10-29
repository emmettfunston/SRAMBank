# SRAMBank

**CE391 Lab 3 — Emmett Funston**

Schematic and layout views of an SRAM bank and the circuits that make it up. The bank is built from SRAM cells with precharge, sense amplifier, and write circuitry. These views were captured in Cadence Virtuoso; the verification screenshots come from Calibre.

**[View the design and verification report (PDF)](report/CE391_Lab3_design_and_verification.pdf)**

## SRAM bank

| Schematic | Layout |
| --- | --- |
| [![SRAM bank schematic](bank/schematic.png)](bank/schematic.png) | [![SRAM bank layout](bank/layout.png)](bank/layout.png) |

## Building blocks

### SRAM cell

The six-transistor storage cell uses cross-coupled inverters and word-line-controlled access transistors connected to complementary bit lines.

| Schematic | Layout |
| --- | --- |
| [![SRAM cell schematic](components/cell/schematic.png)](components/cell/schematic.png) | [![SRAM cell layout](components/cell/layout.png)](components/cell/layout.png) |

### Precharge

Precharges the complementary bit lines (`BL` and `BL_B`) under the `PC_B` control signal.

| Schematic | Layout |
| --- | --- |
| [![Precharge schematic](components/precharge/schematic.png)](components/precharge/schematic.png) | [![Precharge layout](components/precharge/layout.png)](components/precharge/layout.png) |

### Sense amplifier

Reads the differential bit-line pair and drives the `OUT` signal when enabled by `SE`.

| Schematic | Layout |
| --- | --- |
| [![Sense amplifier schematic](components/sense-amp/schematic.png)](components/sense-amp/schematic.png) | [![Sense amplifier layout](components/sense-amp/layout.png)](components/sense-amp/layout.png) |

### Write circuit

Drives the complementary bit lines for a write operation from the data and write-control signals shown in the schematic.

| Schematic | Layout |
| --- | --- |
| [![Write circuit schematic](components/write/schematic.png)](components/write/schematic.png) | [![Write circuit layout](components/write/layout.png)](components/write/layout.png) |

## Physical verification

| DRC | LVS |
| --- | --- |
| [![Bank DRC: zero results across 167 checks](verification/drc.png)](verification/drc.png) | [![Bank LVS: overall comparison correct](verification/lvs.png)](verification/lvs.png) |

The bank DRC screenshot reports **0 results across 167 checks**. The LVS report shows **CORRECT** for the overall comparison.

The PDF and images are selected from the lab report to show the bank, its component schematics and layouts, and physical verification. The screenshots document the design; native Cadence schematic and layout databases are not included.
