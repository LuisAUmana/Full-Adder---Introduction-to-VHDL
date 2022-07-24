# Full-Adder---Introduction-to-VHDL
Assignment provided by Introduction to VHDL (ECGR 4146)
In this lab you will follow the step-by-step instructions provided and can also refer to the lecture slides 3-UNCC-VHDL-lecture_2_Introduction (slide no: 29-38) to design a full adder.

spring-2022-lab 2 fulladder.pdf

Deliverables:

1. Take a screenshot of Vivado screen after you have run synthesis, and the simulation (Include the snapshot of the simulation waveform).

2. Once done with the simulation you need to make some changes in the adder.vhd code to generate the bitstream. 

Change the highlighted area:

entity FullAdder is
    Port ( A : in STD_LOGIC_vector(1 downto 0);
           B : in STD_LOGIC_vector(1 downto 0);
           sum : out STD_LOGIC_vector(1 downto 0);
           carry : out STD_LOGIC);
end FullAdder;

architecture Behavioral of FullAdder is
signal temp : std_logic_vector(2 downto 0);
begin
sum <= std_logic_vector( unsigned(A) + unsigned(B));
temp <= std_logic_vector( "0" & unsigned(A) + unsigned(B));
carry <= temp(2);

3. Add the constraint file provided in the constraint tab of vivado.

ZYBO_Master.xdc 

4.  Run synthesis, post place, and route 
