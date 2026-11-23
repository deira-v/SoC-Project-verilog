# **System on Chip Project**
//Add pic of finished project

System on Chip Design Project using the *Artix-7 FPGA* board.  
An *FPGA board* is a Printed Circuit Board build around a Field-Programmable Gate Array chip, which allows engineers to configure the hardware's logic after manufacturing using Hardware Description Languages such as Verilog.

This _Markdown_ file shows weekly progresses for my 3rd year System on Chip Design and Verification Project.  
I modified the template file to create a moving image showing appearing horizontal and vertical lines using a state machine.  

---  

### **12/10/2026**
**First upload of the template Stripes file on the screen**  
<img src= "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/VGAPrjSum.png? raw=true" width="500">  
Understanding the importance of file Hierarchy.  

<img src= "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/VGAPrjSrcs.png?raw=true" width="300"> &nbsp; <img src= "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/20261012_174134.jpg" width="450">  
Inspecting the code to understand Verilog Syntax.  
Verilog is a Hardware Description Language, used to design and verify digital circuits like microprocessors, flip-flops, and switches.  



The code in the `VGAColourStripe.v` file 

---  
### **19/10/2026**  
**Practicing Verilog language**  
<img src = "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/20261019_160025.jpg" width="400">  
Playing around with the width of the colour stripes  
The VGA 640x480 displays images that are 640 pixels wide and 480 pxs in hight.  
<img src="https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/%7BB9C39D93-5868-4D9C-A7AC-7D695F0AAF60%7D.png?raw=true" width = "300">

---  
### **26/10/2026**
**Working around the row and the columns**  
<img src = "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/20261019_161938.jpg" width="400">  
---  
### **02/11/2026**
**Timing diagram**  
<img src= "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/Screenshot%202026-11-02%20171527.png?raw=true" width = "600">  
The timing diagram helped me understand the relationship between the **clock** counter, **hsync**, **vsync** and the rows and columns count.  

---  
### **09/11/2026**
<img src= "https://github.com/deira-v/SoC-Project-verilog/blob/main/docs/assests/images/image.png?raw=true">  
 
---  
### **16/11/2026**  
**state machine**  

