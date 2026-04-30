**OBSERVATIONS:**
1. Only 1 register is being checked 0x0400 -> 0x0F
2. Pattern is designed for 0x04 spi dummy cycles

**CHANGES MADE:**
1. Moved `RPTV 80 4` 1 cycle back
2. Set reset to 1 all throughout -- pattern passed