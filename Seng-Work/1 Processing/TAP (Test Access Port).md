---
tags:
  - protocol
  - register
---
**Test access point** is composed of the TAP controller, an instruction register, and several test data registers, in addition to some glue-logic.

TAP is also responsible for interpreting the TCK and TMS signals of JTAG.

TAP is a 16-state [[FSM|finite-state machine]], meaning there are 16 legal operating modes.