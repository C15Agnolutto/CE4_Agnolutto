CE4_Agnolutto
=============
CE4 was made up of three tasks. 
A) simply memory manipulations
B) mathematics
C) Loops
Program A required storing the value 9 in location B0, 8 in C4, and B in CB. The first thing I reconginzed I had to do was
label those locations in the RAM. After that it was simply loading the respective values into the labeled locations. The 
picture below shows how I did it in the program wizard. The only thing that was a little tricky with this was recognizing 
that the RAM locations had to be labeled. Other than that, there were no issues. The testing was simple. Reset PRISM and 
then press autoclock to see the correct values be stored in the RAM. 

insert pic

Program B required some simple mathematical manipulations of a value retrieved from B0. It had to be doubled, have 4 
subtracted from it, and have the output displayed to Port 2. I first ran into a problem trying to load the value from B0.
I was trying to use LDAI but after a little reading of the PRISM manual figured out I had to use LDAD to load the value
stored at the operand address. I labeled B0 in the RAM and used that as my operand to load the value. The way I handled 
doubling the number was simply add the number to itself using the label used in the previous steps. Subtracting 4 and 
attempting to meet the target program end was a bit harder. I originally attempted using ROR three times to get the 
two's complement of the number but that made the program too long. A little brainstorming and I realized I could just add
C which is the two's complement of 4 instead of using ROR three times. I read through the manual real quick to figure out
how to ouptut something to a port and plugged that command in. No problems there. I added a final command of JMP and 
made the program loop on that last command so it would end and not repeat the program. Testing was easy and similar to the
first program. Used autoclock to see the value that I selected (because I clicked the allow RAM values to be edited marker)
and checked to make sure the math was correct. I did this with 3 other values and found the program to be working correctly.

inset pic

Prgram C required displaying the value on the input port 3 and displaying it on outprt port 0. The program then had to do 
two iterations of displaying one less than that on port 1 and again one less than that on port 2; it had to continue this 
process in an infinite loop. The only tricky part was getting it to loop infinitely while still displaying the correct 
values. I subtracted 1 each time using a similar process as in program B; F is the two's complement of 1 so I added that 
to the values to be displayed at each port. I tested once I thought it would subtract correctly and display those values.
I went through step by step and it worked as I predicted. The value I choose to be in input port 3 went through the program
as expected. The final thing I had to figure out was looping it correctly. After a couple mintes of searching for a weird
command that might do this, I tried just adding one after the last iteration of subtracting and displaying to output port
2. I wrote it out on paper first and then programmed it. I looped from the end to the first output command and tested it.
I used the step by step method of checking. There were values in the CE4 handout that I used to check my answers against.
The program was giving me a weird error where the first number wasn't being displayed right but the others were. I figured
it was a bug with the program so I closed it and reopened PRISM. Loaded the program and continued testing. It worked 
correctly and matched the answers in the handout. 

inset pic
