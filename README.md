# Description

I got the task, where I have the image with sudoku puzzle. And I need to draw solution of puzzle on raw image.

My pipeline of work:

1) Read image, find field with puzzle, transform this field to get square.
2) Detect numbers in little squares.
3) With algorithm (https://github.com/maxme1/sudoku) solve puzzle
4) Draw solution on raw image.
