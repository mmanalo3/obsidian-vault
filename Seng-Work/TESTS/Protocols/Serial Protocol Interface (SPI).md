# CPOL (Clock polarity)
- [i] Clock polarity is 0 if SCK is 0 when CS_N shifts from high to active low. Otherwise, 1.
- [i] Idle state of clock while CS_N is idle. 

# CPHA (Clock phase)
- [i] Clock phase is 0 if data is already stable before the first edge and date does not change at the first edge, then first edge is used to sample. Clock phase is 1 if data changed at the first edge, data becomes stable after, then second edge is used to sample.