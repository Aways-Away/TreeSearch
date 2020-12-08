# block building approach for the SCLP
***
**We start with an empty container and a list of candidate blocks.**
- In the first step,we select a block and place it at one of the corners of the container.
The remaining free space in the container can be represented as a list of cuboids, which we call residual spaces. 
- In subsequent steps,we select one of the residual spaces and one of the available blocks,and then place the selected 
block at some corner of the selected space. 
- Once the block is placed, we update the list of residual spaces and available blocks. This process is repeated until 
the list of residual spaces is empty, whereupon we have produced a complete packing.
- We use a tree search procedure to generate several complete packings, and return the best packing found when the time 
limit is reached.
***
**In any step of our solution construction process, the state of the current partial packing can be fully described by:**
- R: a list of cuboids (residual spaces) representing the free space
     in the container.
- B: a list of candidate blocks.
- PB: a list of placed blocks and their locations.

