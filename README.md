## Electronic Production and CNC 

### Introduction to Eagle

EAGLE is a scriptable electronic design automation application with schematic capture, printed circuit board layout, auto-router and computer-aided manufacturing features. EAGLE stands for Easily Applicable Graphical Layout Editor (German: Einfach Anzuwendender Grafischer Layout-Editor) and is developed by CadSoft Computer GmbH. Cadsoft Computer GmbH was acquired by Autodesk Inc. in 2016 .To know more [click here](https://en.wikipedia.org/wiki/EAGLE_(program))

#### Commands in Eagle

* > Change Mode/File Commands

    * EDIT	Load/create library element
    * WRITE	Save drawing/library
    * OPEN	Open library for editing
    * CLOSE	Close library after editing
    * QUIT	Quit EAGLE
    * EXPORT	Generate ASCII list (e.g. netlist)
    * SCRIPT	Execute command file
    * USE	Load library for placing elements
    * REMOVE	Delete files/library elements

* > Create/Edit Drawings or Libraries

    * ARC	Draw arc
    * CIRCLE	Draw circle
    * POLYGON	Draw polygon
    * RECT	Draw rectangle
    * WIRE	Draw line or routed track
    * TEXT	Add text to a drawing
    * ADD	Add element to drawing/symbol to device
    * COPY	Copy objects/elements
    * GROUP	Define group for upcoming operation
    * CUT	Cut prev. defined group
    * PASTE	Paste prev. cut group to a drawing
    * DELETE	Delete objects
    * MIRROR	Mirror objects
    * MOVE	Move or rotate objects
    * ROTATE	Rotate objects
    * NAME	Name object
    * VALUE	Enter/change value for component
    * SMASH	Prepare NAME/VALUE text for moving
    * SPLIT	Bend wires/lines (tracks, nets, etc.)
    * LAYER	Create/change layer<br/>
For more commands and their meaning [click here](http://web.mit.edu/xavid/arch/i386_rhel4/help/24.htm)

### Design using Eagle

   Here we designed a cicuit consisting two LEDs and a microcontroller . Capacitors were used to increase the life of the circuit .
    
#### Steps for designing using Eagle


### Milling using ShopBot

   Almost all machines accepts ".gcode" file for operations . Similarly the ShopBot also accepts the ".gcode" file for PCB milling . Hence the circuit design in any of the format must be converted to ".gcode" format . Thus we use [fabmodules.org](http://fabmodules.org/)

#### Steps for the generating ".gcode" file 

* Open fabmodules.org.
* Now select the input, either as image(.png or jpeg), drawing or mesh etc ...
* Now select the output format. Here we selected the ".sbp" format .
* Finally the process need to be selected. Here we selected "Foam(rough cut 1/8)".
*NOTE : Here ShopBot is not meant for PCB milling . Hence we need to set the measures by our own .Figure shows the measures.
<img src="http://jitheeshk.github.io/electronics.github.io/">

Once the ".gcode" file is obtained , go for the machine adjustements .

#### Steps for PCB milling

* First stick the material onto the sacrificial layer using a two side tape .
* Now we need to set the Zero point . For setting the zero point do the following :
         * First move the bit to the appropriate postion .
         * Now move the bit down and set the bit in such a position that it just touches the surface . Use a paper sheet to ensure this .
         * Once this is done select "Zero axis" and check all the three axis .(Refer the image)
         <img src="http://jitheeshk.github.io/electronics.github.io/control.png">
         * Now add the ".gcode file" and press start .(ShopBot key must be ON)
