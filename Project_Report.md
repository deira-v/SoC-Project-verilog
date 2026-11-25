# **System on Chip Project**
//Add pic of finished project

System on Chip Design Project using the *Artix-7 FPGA* board.  
An *FPGA board* is a Printed Circuit Board build around a Field-Programmable Gate Array chip, which allows engineers to configure the hardware's logic after manufacturing using Hardware Description Languages such as Verilog.

This _Markdown_ file shows weekly progresses for my 3rd year System on Chip Design and Verification Project.  
I modified the template file to create a moving image showing appearing horizontal and vertical lines using a state machine.  

---  

### **12/10/2026**
**First upload of the template Stripes file on the screen**  
<kbd><img src= "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/VGAPrjSum.png? raw=true" width="500"></kbd>  
Understanding the importance of file Hierarchy.  

<kbd><img src= "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/VGAPrjSrcs.png?raw=true" width="300">&nbsp;<img src= "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/20261012_174134.jpg" width="450"></kbd>  
Inspecting the code to understand Verilog Syntax.  
Verilog is a Hardware Description Language, used to design and verify digital circuits like microprocessors, flip-flops, and switches.  

The VGA 640x480 displays images that are 640 pixels wide and 480 pxs in hight.  

The code in the `VGAColourStripe.v` module is composed of both Combinational and Sequential Logic.  

---  
### **19/10/2026**  
**Practicing Verilog language**  
<kbd><img src = "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/20261019_160025.jpg" width="400"></kbd>  
To manipulate the with of the stripes I simply changed the value within the statement:  
_if(row >= 11'd0 && row = 11'd100) begin  
&emsp;red_next   <= 4'h0;  
&emsp;green_next <= 4'h8;  
&emsp;blue_next  <= 4'h0;  
end_  
The variable _row_ can have a value between 0 and 479, while _col_ can have a value between 0 and 639.  
  
<kbd><img src="https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/%7BB9C39D93-5868-4D9C-A7AC-7D695F0AAF60%7D.png?raw=true" width = "300">&ensp;<img src="https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/%7B0089A77B-D568-4D17-B9F7-35927F826996%7D.png?raw=true" width="325"></kbd>  
In `VGASync.v` we find the code that controls the variable _hcount_ which it can have a value between 0 and 799 (600 visible pxs + 15 front porch pxs + 47 back porch pxs + 96 sync pulses), and _vcount_ that goes from 0 to 524 (480 visible pxs + 10 front porch pxs + 33 back porch pxs + 2 sync pulses;  
  
The image above shows the incrementing of hcount (horizontal count) by one until it has reached the end of the row, and when that happens increments vcount (vertical count) by one until it reaches the bottom of the column.  
  
_hsync_ and _vsync_ are active low Synchronization Pulses...  
<kbd><img src="https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/%7B8D38CFE4-5A23-4EE6-86F7-AB06DE7FC3C3%7D.png?raw=true" width="300"> &ensp; <img src="https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/%7B642E0F48-F095-44BD-93F0-1D9DF7384766%7D.png?raw=true" with="250"></kbd>


---  
### **26/10/2026**
**Working around the row and the columns**  
<kbd><img src = "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/20261019_161938.jpg" width="400"></kbd>  

---  
### **02/11/2026**
**Timing diagram**  
Every rising edge of the clock other values are incremented, starting with rows which gets initialized with a value of 0, after the first rising edge the col goes from 0 to one and when it reaches a value of 0x31F (799 decimal) the row gets incremented.
of the 25Mhz clock with a period of 10ns between rising edges.  

<kbd><img src= "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/Screenshot%202026-11-02%20171527.png?raw=true" width = "600"></kbd>  
The timing diagram helped me understand the relationship between the *clock* counter, *vid_on*, *rows* and *columns* count.  
  

<kbd><img src="https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/Screenshot%202026-11-02%20172044.png?raw=true" width="600"></kbd>
  
<kbd><img src="https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/Screenshot%202026-11-02%20171940.png?raw=true" width="600"></kbd>

---  
### **09/11/2026**
<kbd><img src= "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/image.png?raw=true"></kbd>  
 
---  
### **16/11/2026**  
**state machine**  

