# 2024-July-Code-Challenge
## Magic Square Solver
### Approach
 
When solving a 3x3 Magic Square there are a few algorithms that work. The algorithm I chose utilizes a center square of X that can then calculate all the corners. One pair of diagonal corners will be (X+1) (X-1) and the other pair will be (X+3) (X-3). The orientation or these corners doesn’t matter as long as the pairs are diagonal from each other on the square. 
 
Once the corners and center are calculated, then the rest of the components are easy to find. By taking the sum of either completed diagonal we can calculate the Magic Constant. From there we simply find the difference between the total of the row and the Magic Constant. The middle row, however, only has one value therefore, taking the difference between the column total and Magic Constant is the best way to calculate those box’s.

