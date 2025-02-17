For a clock period of 10ns, with a setup uncertainty of 0.3ns, a hold uncertainty of 0.2ns,
an early derate of 5% and a late derate of 5%, the input constraint will be as follows:

create_clock -name main_clk -period 10 -waveform { 0  5} [get_port main_clk ]
set_clock_uncertainty -setup 0.3 [get_clocks main_clk]
set_clock_uncertainty -hold 0.2 [get_clocks main_clk]
set_timing_derate -early 0.95 -cell_delay
set_timing_derate -late 1.05 -cell_delay

Clk-Q is the clk to Q delay of a flip-flop

Enter the values into the corresponding fields and explore the tool.

Note: For the timing unit of the clock period, you can choose any unit you prefer.
Just ensure that the same unit is used consistently for all delay values.
