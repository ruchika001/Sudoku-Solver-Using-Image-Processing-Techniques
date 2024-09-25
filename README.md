Sudoku puzzles are well-known for their logical complexity, making manual solving quite challenging. This project offers an automated solution by combining image processing techniques and machine learning. The system uses image enhancement, segmentation, and a Convolutional Neural Network (CNN) to identify and solve Sudoku puzzles. The process includes turning the image grayscale, applying Gaussian Blur, adaptive thresholding, and contour detection. CNN is trained to recognize digits, and a backtracking algorithm is used for puzzle-solving. 
1. Read the image
• Selecting a Random Image:
We kick things off by randomly picking an image from our dataset. This adds variety for 
testing and showing different examples. The displayed image represents a snapshot of the 
diverse dataset we're working with.
2. Preprocessing the Sudoku Image
• Resizing the Image
To keep things consistent, we resize the Sudoku image to a standard size. This ensures 
uniformity for the subsequent steps.
• Image Enhancement through Preprocessing:
In the step to enhance the image quality, we applied grayscale conversion, Gaussian blurring, 
and adaptive thresholding for a clearer view.
3. Detecting the contour of the Sudoku puzzle
• Detecting the Contour:
We use contour detection to pinpoint the Sudoku puzzle in the image. The green contour 
visually highlights the identified puzzle area. This step sets the stage for accurate Sudoku 
recognition.
• Identifying the Largest Contour:
The goal is to find the largest contour, which we assume represents the Sudoku grid. The 
identified contour is reshaped and superimposed for a clearer perspective.
• Reshaping the Contour
The contour is reshaped for a well-aligned perspective. This reshaped version is crucial for 
accurate Sudoku recognition. The resulting image provides a clear, well-aligned view of the 
Sudoku puzzle.
4. Splitting Cells and Classifying Digits
Detected and classified digits using the CNN model.
• Splitting into 81 Cells:
The Sudoku puzzle is divided into 81 cells, each representing a digit or an empty space. This 
step sets the foundation for digit classification.
• Cropped Cell:
The cropped cell ensures better accuracy in digit recognition.
• Digit Classification with the Model
The trained neural network model classifies digits within each cell. Empty cells are treated as 
zeros. The function applies the model to classify digits, forming an array of 81 predicted 
values.
• Resulting Grid Array
Getting the detected output in the form of an array of 81 digits
s
