# NASSCOM-VSD-IAT-Digital-VLSI-SoC-Design-and-Planning
This is the repository including the simple example of a Digital VLSI SoC Design and Planning workshop conducted by NASSCOM. The open source tool OpenLane was used to performed flow. Skywater130A tech file was used for the design.
Digital VLSI SoC Design and Planning
Sky130A_inv

Layout:




Characterization of cell:
Find 4 values:
(a)	Rise transition: Time taken to transit from 20% to 80% of maximum signal value, VDD
Rise transition: 2.24696 ns – 2.18265 ns = 0.06431 ns

(b)	Fall transition: Time taken for output to fall from 80% to 20% of the signal VDD
Fall transition: 4.09551 ns – 4.05316 ns = 0.04235 ns
(c)	Rise cell delay: Rise delay through the cell based on the input slew and output load (time period between 50% rise in output and 50% rise in input)












Cell Rise Delay: 2.21155 ns – 2.15009 ns = 0.06146 ns


(a)	Cell fall delay: Difference in time period when the output has fallen to its 50% and when the input has raised towards 50%











Cell Fall Delay: 4.7835 ns – 4.05 ns = 0.02835 ns

Including the custom inverter in the picorv32a


