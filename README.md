# Description

I got the task, where I have the image with sudoku puzzle. And I need to draw solution of puzzle on raw image.

My pipeline of work:

1) Read image, find field with puzzle, transform this field to get square.
2) Detect numbers in little squares.
3) With algorithm (https://github.com/maxme1/sudoku) solve puzzle
4) Draw solution on raw image.

How it looks like:

I get:

<img src="https://i.imgur.com/WkVP1Va.jpg?raw=true" alt="raw image of sudoku" width="300" height="400">

And should make this with some algorithm with python code (On example what I actually did):

<img src="https://i.imgur.com/o4UnRSY.jpg?raw=true" alt="Solved sudoku" width="300" height="400">


# Pipeline with image examples

1. Read image, find all contours and take maximum contour

<img src="https://i.imgur.com/TL1SIb0.jpg?raw=true" alt="Max contour" width="400" height="300">

2. Use homography matrix we can get square

<img src="https://i.imgur.com/YWxK2cU.jpg?raw=true" alt="Square of sudoku field" width="300" height="300">

3. In ~/template folder we have templates of numbers. I use it for detect numbers on sudoku field.

<img src="https://i.imgur.com/Et3pSFh.jpg?raw=true" alt="Number detecting" width="300" height="210"> 

4. With algorithm solve sudoku

<img src="https://i.imgur.com/IMaD3iX.jpg?raw=true" alt="Solution of sudoku" width="300" height="300">

5. Draw numbers on sudoku field

<img src="https://i.imgur.com/jI1cKm5.jpg?raw=true" alt="Solution om image" width="300" height="300">

6. On step 2 we got homography matrix, by using inverse matrix we can transform image on step 5 to draw solution on raw image

<img src="https://i.imgur.com/o4UnRSY.jpg?raw=true" alt="Solved sudoku" width="300" height="400">
