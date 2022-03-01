# Lab 2: Anton Tsyhanov ID:230336

### 2-bit comparator

1. Karnaugh maps for other two functions:

   Greater than:

   ![image](https://user-images.githubusercontent.com/99277478/156158656-4ec8a2d9-24b4-485d-8bde-e3fd52273468.png)
   
   Less than:

   ![kmap_empty (1)](https://user-images.githubusercontent.com/99277478/156159398-626fde0f-314d-486a-8e5b-772e2e490253.png)


2. Equations of simplified SoP (Sum of the Products) form of the "greater than" function and simplified PoS (Product of the Sums) form of the "less than" function.

   ![DE1](https://user-images.githubusercontent.com/99277478/156167558-e151b08b-abe8-4215-82f7-6b5ede734f48.jpg)


### 4-bit comparator

1. Listing of VHDL stimulus process from testbench file (`testbench.vhd`) with at least one assert (use BCD codes of your student ID digits as input combinations). Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

   Last two digits of my student ID: **xxxx??**

```vhdl
    begin
        -- Report a note at the beginning of stimulus process
        report "Stimulus process started" severity note;

        -- Input param my ID:230336
        
        s_b <= "0110"; s_a <= "0011"; wait for 100 ns;
        -- ... and its expected outputs
        assert ((s_B_greater_A = '0') and
                (s_B_equals_A  = '1') and
                (s_B_less_A    = '0'));

                
        -- If false, then report an error
        -- If true, then do not report anything
        report "Input combination 0110, 0011 FAILED" severity error;



        -- Report a note at the end of stimulus process
        report "Stimulus process finished" severity note;
        wait; -- Data generation process is suspended forever
    end process p_stimulus;
```

2. Text console screenshot during your simulation, including reports.

   ![image](https://user-images.githubusercontent.com/99277478/156167789-d19dd938-9194-41e9-9c53-9558e5067741.png)


3. Link to your public EDA Playground example:

   [https://www.edaplayground.com/x/wSHz]
