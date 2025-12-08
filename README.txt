AnalyseData is a C++ program designed to read TWO-COLUMN numerical data, perform common analysis
tasks, and store the results in output files. 
It, also, supports both space-separated and comma-separated input formats, making it suitable
for datasets exported from spreadsheets, simulations or measurements devices. 

As for the structure of the files here we have 3 code files:
AnalyseData.cxx is the main program, 
CustomFunctions.h is the Header which is doing the declarations
CustonFucntions.cxx is doing the implementations. 

To run everything, just compile the AnalyseData and the other two files feeding it whatever
needs to be feeded. 

Upon starting the program, you are prompted to provide a data filemname:
Then you are gonna see a menu of choice you can choose from:

1. Print N lines
	Prints the first N data points
	Saves all data to output_printN.txt
2. Compute magnitudes
	Computes sqrt(x^2+y^2) for each point
	Prints values
	Saves them to output_magnitudes.txt
3. Perform least–squares fit and chi^2/NDOF
	Computes slope p and intercept q
	Reads error values from error2D_float.txt
	Computes x^2/NDOF
	Saves results to output_fit.txt
4. Compute x^y (recursive)
	Rounds each y to the nearest integer
	Computes x raised to that power using a recursive algorithm
	Saves output to output_xpowy.txt 

Notes for Developers
	Input parsing is robust: commas are automatically converted to spaces.
	All numerical operations use double or long double precision.
	The code is modular, with all calculations encapsulated in CustomFunctions.cxx.




