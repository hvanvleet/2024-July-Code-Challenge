# 2024-July-Code-Challenge
## Magic Square Solver
### Approach
 
When solving a 3x3 Magic Square there are a few algorithms that work. The algorithm I chose utilizes a center square of X that can then calculate all the corners. One pair of diagonal corners will be (X+1) (X-1) and the other pair will be (X+3) (X-3). The orientation or these corners doesn’t matter as long as the pairs are diagonal from each other on the square. 
 
Once the corners and center are calculated, then the rest of the components are easy to find. By taking the sum of either completed diagonal we can calculate the Magic Constant. From there we simply find the difference between the total of the row and the Magic Constant. The middle row, however, only has one value therefore, taking the difference between the column total and Magic Constant is the best way to calculate those box’s.

### Challenges  

Using the algorithm to solve the Magic Square raises a few challenges. The first be the restrictions of what X can be. Since the numbers have to be an integer between 1 and 9 there can only be 3 possible X’s that can use the algorithm and fit the parameters. These X’s are [4, 5, 6]. A X value of 3 or lower would lead to a value outside the range as (X – 3) must be one of the corners. Likewise, a X value of 7 or above would raise the same concern as one of the corners must be (X + 3). This is not the only limitation of the algorithm. All the rows, columns, and diagonals must add up to the same Magic constant. With simple math we can decipher the Magic Constant from just knowing the X value. 

For X = 4:

(X-1)+(X)+(X+1) = (4-1)+(4)+(4+1) = 3+4+5 = 12 

(X-3)+(X)+(X+3) = (4-3)+(4)+(4+3) = 1+4+7 = 12 

Which we can see is also 3X.

For X = 5:

(X-1)+(X)+(X+1) = (5-1)+(5)+(5+1) = 4+5+6 = 15 

(X-3)+(X)+(X+3) = (5-3)+(5)+(5+3) = 2+5+8 = 15 

Which we can see is also 3X.

For X = 6:

The same logic applies and to save the math 3*6 = 18. 

Therefore, we know that the Magic Constant for (4 = 12), (5 = 15), and (6 = 18). Hopwever, this now arises the limitation of the algorithm. If X = 4 then we know the Magic Constant is 12. We also know that the 4 corners are a combination of (3,5,1,7). This leaves (2,6,8,9) as the remaining values for the outside middles. And if we have 4 and 9 in the same row/column our sum already exceeds the Magic Constant of 12. Therefore 4 does not work as a vale of X and the only possible values of X that will satisfy the algorithm are 5 and 6. 

The last challenge of using this algorithm is solving the square in the least number of steps. While it would be simple to set the middle square to 5 or 6 every time, this leads to potentially more moves than necessary. Furthermore, if some of the corners already align with values that satisfy the algorithm then it is best to leave those and change the other corners accordingly. This logic then must be translated into the code. 
