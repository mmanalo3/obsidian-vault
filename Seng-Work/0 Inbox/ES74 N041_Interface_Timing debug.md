# TREH_IOA pattern
- Pattern is initially passing
- Pattern is failing if kDIG_LOAD of TOKEN_DIG is disabled

# TREH_IOB pattern
- 

# tws_func_iob_only
- Pattern is intermittently failing?
- Passes on longer delay. Set to Wait(200) from Wait(10) for now.

# Manual pin set for tREH
- Breakpoint right after DCMD set to 0x04
- Disconnected all pins except VL_CPE

1. Enabled IOA_CPE_DIG (driver), set to low -- reads ~1.8v
	- same reading when set to high
	- enabled load, set to low -- reads ~680mv
	- set to high, reads 1.8v
2. Enable PIOC_CPE_DIG (sensor) -- IOA still same readings as (1)
	- enabled load, IOA changed readings
	- with IOA set to low:
		- IOA driver only -- 390mv (IOA); 390mv (PIOC)
		- IOA driver and load -- 340mv (IOA); 340mv (PIOC)
	- with IOA set to high:
		- IOA driver only -- 1.8v (IOA); 1.8v (PIOC)
		- IOA driver and load -- 1.8v (IOA); 1.8v (PIOC)