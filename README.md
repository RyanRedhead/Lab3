Lab 3
==========

#Pre Lab

##Schematic
![Alt Text](https://github.com/RyanRedhead/Lab3/blob/master/schematic.jpg?raw=true)
#Lab Functionality
Demonstrated Moore and Mealy Elevators so far
#Code Critique
## Bad Code
```vhdl
	if clk'event and clk='1' then
```
## Good Code
```vhdl
	if rising_edge(clk) then
```
## Bad Code
```vhdl
	floor_state_machine: process(clk)
```
## Good Code
```vhdl
	floor_state_machine: process(clk, up_down, stop, reset)
```
#Documentation
Berg helped me figure out the Mealy next state elevator output so that the next elevator floor could appear on the Nexys board.
