Lab 3
==========

#Pre Lab

##Schematic
![Alt Text](https://github.com/RyanRedhead/Lab3/blob/master/schematic.jpg?raw=true)
#Lab Functionality
Demonstrated Moore and Mealy Elevators-->Capt Silva
#Code Critique
## Bad Code
```vhdl
	if clk'event and clk='1' then
```
This code can cause confusion later on when the person programming tries to be smart and add statements to this code, it wont work.
## Good Code
```vhdl
	if rising_edge(clk) then
```
This code has no confusion on what it does and is more simple than the bad code above.
## Bad Code
```vhdl
	floor_state_machine: process(clk)
```
This bad code creates memory for the other inputs, which is dependent on the machine and can have unique effects.
## Good Code
```vhdl
	floor_state_machine: process(clk, up_down, stop, reset)
```
This code includes all of the inputs so that there is no memory assocated with them.
#Notes to Self
Can change the inputs and outputs of Moore machine to make B or A functionalities.
Output logic-->what the machine outputs from the statements made above.

#Documentation
Berg helped me figure out the Mealy next state elevator output so that the next elevator floor could appear on the Nexys board.
http://daringfireball.net/projects/markdown/syntax was used to find out how to do the code blocks in the code critiques.
