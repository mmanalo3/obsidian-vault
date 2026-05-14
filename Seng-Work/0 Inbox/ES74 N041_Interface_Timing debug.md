# TREH_IOA pattern
- Pattern is initially passing
- Pattern is failing if kDIG_LOAD of TOKEN_DIG is disabled

# TREH_IOB pattern
- 

# tws_func_iob_only
- Pattern is intermittently failing?
- Passes on longer delay. Set to Wait(200) from Wait(10) for now.

# tws_func_ioa_only
- 240ns is the original period for setup3
- 20ns is the minimum period for no error?
- 15ns will cause error -- need to adjust event1 to suppress error