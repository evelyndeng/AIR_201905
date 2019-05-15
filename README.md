# AIR_201905
AIR Coding Assignment

This assignment uses two csv files that are uploaded here along with the .rmd code file and final knitted html file.

In this assignment, I created an interactive scatter plot, ran and interpreted multiple linear regressions, made adjustments for the hamming edit-distance algorithm, and performed data cleaning tasks.

The specific assignment instructions are below:



1. Regression Modelling

For this exercise, we are interested in better understanding the shapes of iris flowers. Specifically, we are interested in whether the petal length and sepal length are related. We will use the “iris” data set which is available in both R and Python (and also attached as a csv, “Iris_Data.csv”) which includes the petal and sepal lengths and widths and the species of iris to which each example belongs.
    a)	How many irises belong to each species? 
    b)	Make a scatterplot of petal length vs sepal length. Color the dots according to species. Document your observations (2-3 sentences) 
    c)	Fit a regression model predicting sepal length based on petal length, petal width and sepal width (you do not need to test any of the regression assumptions). 
    d)	Describe the results of your regression, focusing on the relationship between sepal length and petal length.
    e)	Extra Credit: Fit a regression model predicting sepal length based on petal length, petal width, sepal width and species (you do not need to test for any of the “classical” regression assumptions).  This is the same as part c but also with species as a predictor. Describe the results.

2. Implementing an Edit-Distance Algorithm

Write a program to calculate a variant of the Hamming distance with two key modifications to the standard algorithm. In information theory, the Hamming distance is a measure of the distance between two text strings. This is calculated by adding one to the Hamming distance for each character that is different between the two strings. For example, “kitten" and “mitten" have a Hamming distance of 1. See https://en.wikipedia.org/wiki/Hamming_distance for more information. 

Modifications to the standard Hamming distance algorithm for the purposes of this exercise include: 

1)	Add .5 to the Hamming distance if a capital letter is switched for a lower case letter unless it is in the first position.  Examples include: 
    a.	"Kitten" and "kitten" have a distance of 0 
    b.	"kitten" and "KiTten" have a Hamming distance of .5.
    c.	"Puppy" and "POppy" have a distance of 1.5 (1 for the different letter, additional .5 for the different capitalization). 
    
2)	Consider S and Z (and s and z) to be the same letter. For example, "analyze" has a distance of 0 from "analyse".
    Test cases with expected outputs: 
    First Word	        Second Word	        Distance Score
    make	              Mage	              1
    MaiSY	              MaiZy	              .5
    Eagle	              Eager	              2
    Sentences work too	Sentences wAke too	3.5

Use the program you wrote to score the following strings:
    a)	"data Science" to  "Data Sciency"
    b)	"organizing" to "orGanising"
    c)	"AGPRklafsdyweIllIIgEnXuTggzF" to "AgpRkliFZdiweIllIIgENXUTygSF")
Then:
    a)	Describe a scenario (3-4 sentences) where implementing the standard Hamming distance algorithm would be applicable. 

3. Data Cleaning

Perform some data cleaning using the provided file, “patent_drawing.csv”. “Patent_drawing.csv” contains a list of patents and a short description of each drawing included with a patent grant. For example, patent number 0233365 (https://patents.google.com/patent/US20030233365A1/en) has 16 images. For each image, there is a brief description of the drawings. The description is included in the “text” field in patent_drawing.csv. 

Let’s say that we are interested in understanding:

    a)	How many of the field descriptions reference a perspective that is not standard (i.e. viewed from the top, bottom, front or rear)? Specifically, write code to count how many of the rows have the words "view" or "perspective" but do not include "bottom", "top", "front" or "rear" in  in the text field?

    b)	What is the average number of drawing descriptions per patent? 
