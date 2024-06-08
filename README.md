# Spider-eMMC
KiCad 7.0 projects for SpiderUnifiedBoard and SpiderCarrierBoard, Xbox One eMMC replacement and repair boards.

_Note_: these projects are uncompleted and provided AS-IS. 

## Why?
Lack of time, resources and motivation to finish the project. Passing off the torch.
This was meant to be a complete solution to repair Xbox One consoles with damaged / degraded eMMCs. The main board would be put in the console (with minimal soldering needed), and then you could swap different eMMC modules.

- The form factor of the main board is for all Xbox One PHAT variations (Durango/Graybull, Carmel, Silverton) **and you can reuse it directly!** (this is the Edge Cuts layer in KiCad)
- The form factor is not adapted for Xbox One S nor Xbox One X

## Theory of Operation
- Xbox One's southbridge uses the whole 8-bit bus to connect to the eMMC, so it cannot be replaced by cheaper and easier eMMC compatible memories (i.e.: microSD cards)
- To minimize desoldering of ICs: You would cut the traces from the original eMMC in the board to the southbrige.
- Then you would solder this board and connect the new data and control lines, at which point the southbridge will start communicating with the new and fresh eMMC on the Spider board (or in the carrier board)

## Spider Unified Board
First prototype eMMC replacement board. This board did not feature a removable eMMC yet.
This board must be modified to replace the eMMC with a socket, where you can plug the Spider Carrier Board (see below)

![image](https://github.com/xboxoneresearch/Spider-eMMC/assets/100166926/05fadc75-578b-443d-8939-43b78596fc5c)
![image](https://github.com/xboxoneresearch/Spider-eMMC/assets/100166926/6d657a61-4ee6-4214-a1bf-e055d179b9e9)


## Spider Carrier Board
An attachable PCB carrying an eMMC memory. This board was meant to be plugged into the main Spider board, having a B2B socket in it.
![image](https://github.com/xboxoneresearch/Spider-eMMC/assets/100166926/8cc16f4b-c12e-4788-88c1-2a0ef9089904)

![image](https://github.com/xboxoneresearch/Spider-eMMC/assets/100166926/c21126a3-e06f-48fb-8726-c219aff7b20a)

## Credits
- TorusHyperV: Original design and iteration (and killing several consoles for science)
- XBR Team: invaluable feedback and idea of the removable eMMC board
- Betatesters: for their invaluable help and courage to test early board prototypes
  - SheezNeez
  - Wolf
  - ModzvilleUSA
  - mc_quezada
  - Heathenhkr
