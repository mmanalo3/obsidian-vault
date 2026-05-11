---
tags:
  - protocol
---
Joint Test Action Group is used for verifying designs and testing printed ciruit boards.

JTAG is used in boundary scan testing.

# Four main signals:
**TCK (test clock)** - clock signal for synchronization; driven by master
**TMS (test mode select)** - controls the state of the [[TAP (Test Access Port)]] controller. On every rising edge of TCK, the value of TMS (0 or 1) determines whether the controller moves to a new state or remains in the current one.
**TDI (test data in)** - serial input data line
**TDO (test data out)** - serial output data line

# Required data registers:
**BSR** *Boundary-scan register*, the main register for passing data to the boundary scan cells
**BYPASS**, a single-bit pass-thru register, connecting TDI to TDO without first passing through the boundary-scan cells

# Required instructions:
**EXTEST**, performs external boundary-scan test using the boundary scan cells
**SAMPLE** and **PRELOAD**, boundary scan while device is functional
**BYPASS**, bypasses the boundary scan cells altogether


All JTAG operations begin from either the [^1]`Test-Logic-Reset` state or the `Run-Test/Idle` state. From there, The protocol divides into two main, parallel branches:
1. 

[^1]: Reached by holding TMS=1 for 5 clock cycles.
