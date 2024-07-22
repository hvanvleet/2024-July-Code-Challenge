# 2024-July-Code-Challenge
## Magic Square Solver
### Approach
 
When solving a 3x3 Magic Square there are a few algorithms that work. The algorithm I chose utilizes a center square of X that can then calculate all the corners. One pair of diagonal corners will be (X+1) (X-1) and the other pair will be (X+3) (X-3). The orientation or these corners doesn’t matter as long as the pairs are diagonal from each other on the square. The algorithm in turn looks like this.
 
  X  + 1		  X + 3  
          X    	
  X - 3  		  X - 1 
