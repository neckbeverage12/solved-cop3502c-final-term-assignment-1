Download Link: https://assignmentchef.com/product/solved-cop3502c-final-term-assignment-1
<br>
<strong>Introduction: </strong>For this assignment you have to write a c program that will utilize the merge sort and binary search algorithm.




<strong>What should you submit? </strong>

Write all the code in a single .c file and upload the .c file.




Please include the following lines in the beginning of your code to declare that you are the author of the code:




/* COP 3502C Final term Assignment 1

This program is written by: Your Full Name */

<strong> </strong>

<strong>Additional notes:</strong> The TAs and course instructor can call any students to explain their code for grading. <strong> </strong>

<strong>Problem </strong>

Given the center coordinate point (x,y) and the radius of a circle. Then there are N number of coordinate points of interests also provided as part of the data. You have to filter out all the points those are inside or on the line of the circle. Next, you have to apply merge sort to sort those filtered points in x-axis major order. If two points have same x, then you should sort them based on y.  After sorting, your program should continuously prompt the user for an input coordinate point x and y values and your program should perform binary search to determine whether the point exists in the given list of points or not. If the point is is found, the program should show the position of the number in the filtered sorted list.

<strong> </strong>

<strong>Required Input/Output format: </strong>

The inputs related to the circle and points are taken from a text file called in.txt.  You have to read the text file (in.txt). The first line of the file contains 4 numbers separated by space. The numbers are x coordinate of the center of the circle, y coordinate of the center of the circle, r the radius of the circle, and N that says how many points of interests are there in the file. The next N lines of the file contain x and y coordinate values. Note that all the numbers in this file are integer. They can be both negative and positive numbers (except the radius). After reading the data, you have to filter all the points inside or on the line of the circle. Let us call it filtered list. Next, you have to sort those filtered points in x-axis major order <em>(it means that the data will be sorted based on x first, if multiple point has same x, then it will sort based on y)</em> and then write the output into another file (out.txt) in the same format, i.e., each line contains one coordinate point x and y and they are space delimited. After writing the sorted points in the file, your program should display the message “filtered and sorted data written to out.txt”. After that your program should continuously prompt the user for an input coordinate point x and y values and your program should perform binary search to determine whether the point exists in the given list of points. If it is found, it should show “Found” and record number. The program will stop prompting for x and y, if the search input x=-999 or y=-999

<h2> Example</h2>

Consider the circle and the points in the figure. The center of the circle is (-1,1) and the radius = 5. N= 14 as there are 14 points of interest. However, only 9 out of 14 points fall inside the circle. In order to apply binary search on the points within the circle, we need to sort them and you will use merge sort to sort those points. The sorting criteria was discussed above. Let us see the sample input/output based on the given picture.

<strong> </strong><strong>Sample data in Input file in.txt (the red points are outside of the circle):  </strong>

<strong>              </strong>-1 1 5 14

3 1

-6 -2

-4 2

4 -4

2 4

-1 3

2 2

<sup>             </sup>0 -2

-4 -2

<strong><sup>             </sup></strong>-6 6

<strong>             </strong>4 4

-2 4

<strong>             </strong>2 -2

-4 6

<strong> </strong>

<strong>Sample output file out.txt:  </strong>

-4 -2

-4 2

-2 4

-1 3

0 -2

2 -2

2 2

<ul>

 <li>4</li>

 <li>1</li>

</ul>




“filtered and sorted data written to out.txt”  <em>//Note that you must close your file before going to search phase. Otherwise fill will not be generated with your data until yo complete all the search process.</em> Search input (x y): 2 -1

Output: Not found

Search input (x y): 3 1

Output: Found at record 9

Search input (x y): 2 -2

Output: Found at record 6

Search input (x y): -4 2

Output: Found at record 2

Search input (x y): -4 -2

Output: Found at record 1

Search input (x y): -999 10

Output: exit




<strong>Requirement: </strong>

You must use file IO, Merge sort and binary search for your solution.  Without using them, you will get zero. Your code should also have the following functions:

<ol>

 <li><u>ReadData():</u> this function reads the required data from the in.txt file and return the data that are stored <u>in</u> your preferred data structure. <u>Hints:</u> this function might require dynamic memory allocation and return pointer after reading the data. Also, you might need to, pass references of one or more variables when you call the function so that the function can update those variables.</li>

 <li><u>FilterData():</u> this function takes the data you received from ReaData() function and returns the filtered points that are inside or on the line of the circle.</li>

 <li>Standard <u>MergeSort(), Merge(), BinarySearch()</u> functions</li>

 <li><u>SearchPhase(): </u>This function takes your sorted data that was modified by the merge sort. Then it continuously prompts the user for search points and show the result or exit based on the provided criteria.</li>

</ol>




<u>Additional Requirement:</u>

Your program must compile in Eustis. Note that you can use &lt;math.h&gt; library if you need. In that case you have to use –lm option while compiling your code.

For example: $<em>gcc filename.c -lm</em>

<strong>Rubric</strong>:

<ul>

 <li>Filtering the points that are on the line or inside the circle: 2</li>

 <li>Applying Merge sort properly and writing results into out.txt file: 6.5</li>

 <li>Performing Binary search properly and output: failing each test case -1.5 points. Total 4.5</li>

</ul>

<strong> </strong>




<strong>Please see the lecture slides and uploaded codes for learning merge sort and binary search and File I/O. </strong>

<strong> </strong>

Remember, we had one lab on File I/O. We have used <strong><em>fscanf</em> </strong>and <strong><em>fprintf </em></strong>while reading and writing files, respectively.