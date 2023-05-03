Download Link: https://assignmentchef.com/product/solved-cs224-lab-1-creating-and-running-simple-mips-assembly-language-programs
<br>



<strong>Purpose</strong>: <strong>1</strong>. Introduction to MIPS assembly language programming and MARS environment. <strong>2</strong>. Learning CS224 lab rules and procedures.

You are obliged to read this document word by word and are responsible for the mistakes you make by not following the rules. Your programs should be reasonably documented must have a neat syntax in terms of variable names, comments and spacing as you have learned in CS101 and as suggested by the programs in the textbook.




<strong>Summary </strong>

<strong>Preliminary Report/Preliminary Design Report:</strong>

<strong>Part 1</strong> (40 points): simple array operations and arithmetic expression calculation. (Due date of this part is the same for all groups).

<strong>Lab: (Note try and study lab part at home before coming to the lab. Make sure that you show the lab work to your TA before uploading in the lab.)</strong>

<strong> </strong>

<strong>Lab Work:</strong>

<strong>Part 2</strong>  (15 points): Using MARS with “hello world”: Program1.asm.

<strong>Part 3</strong> (25 points): Using breakpoints, fixing errors in a Fibonacci program; using jal (jump and link) and jr (jump register) instructions.

<strong>Part 4</strong> (20 points): Implementing an arithmetic expression given in lab.




<strong>DUE DATE OF PART 1 (PRELIMINARY WORK): SAME FOR ALL SECTIONS</strong>: <strong>No late submission will be accepted</strong>.

<ol start="17">

 <li>Please bring and drop your printed preliminary work into the box(es) provided in the lab EA-407 by 13:30 on Monday February 17.</li>

 <li>Please <strong>upload your programs of Part 1 (PRELIMINARY WORK)</strong> to the Unilica by 13:30 on Monday February 17. Use filename <strong>txt</strong> <u>Upload only the programs. Only a NOTEPAD FILE (txt file) is accepted. Any other form of submission receives 0 (zero).</u></li>

 <li>For preliminary work grading you have to complete both section a (preliminary work paper submission) and b (Unilica file upload) as defined If one of them is missing you get 0 (zero) from the preliminary part. This is valid for all labs.</li>

</ol>




<strong>DUE DATE PART 2-4 (LAB WORK): (different for each section) YOUR LAB DAY</strong>

You have to demonstrate your lab work to the TA for grade by <strong>12:15</strong> in the morning lab and by <strong>17:15</strong> in the afternoon lab. Your TAs may give further instructions on this. If you wait idly and show your work last minute, minimum 20 points will be taken off from your grade.




At the conclusion of the demo for getting your grade, you will <strong>upload your entire program work including Part 1 (Preliminary Work)</strong> to the Unilica Assignment, for similarity testing by MOSS. See Part 6 below for details.

<strong> </strong>

<strong>If we suspect that there is cheating we will send the work with the names of the students to the university disciplinary committee.</strong>




<strong>Part 1. Preliminary Work / Preliminary Design Report (40 points)</strong>

You have to provide a neat presentation prepared by <u>Word or a word processor with similar output quality such as latex</u>. At the top of the paper on left provide the following information and staple all papers. In this part provide the program listings with proper identification (please make sure that this info is there for proper grading of your work, otherwise some points will be taken off).

CS224

Section No.: Enter your section no. here

Spring 2020

Lab No. 1

Your Full Name/Bilkent ID

<strong>Important Note</strong>: In all lab works if it is not explicitly stated you may assume that program inputs are correct. Part 2 of this lab is also helpful for Part 1: Read that part as you attempt Part 1.




<ol>

 <li><strong>(20 points)</strong> Write a MIPS program that</li>

</ol>

<ul>

 <li>Initializes an array of maximum size of 20 elements: Do this by asking the user first the number of elements and then by getting the array elements one by one from the user.</li>

 <li>Displays array contents.</li>

 <li>Displays the summation of array elements.</li>

</ul>

Note that maximum array size is fixed and 20 elements which can be achieved by a declaration like as follows

array:      .space   80




<ol start="2">

 <li><strong> (20 points)</strong> Write a MIPS program that implements the following arithmetic expression for integer numbers.</li>

</ol>

x= a * (b – c) % d

In your program

<ul>

 <li>Read a, b, c, d in the main program (main program: the part that the execution begins).</li>

 <li>Pass a to d to a subprogram using the argument registers $a0, $a1, $a2, and $a3.</li>

 <li>Perform the computation in the subprogram using $t (temporary) registers and return the result to the caller/main program in $v0.</li>

 <li>Print the result in main.</li>

 <li>In doing these provide a reasonable user interface for input and output.</li>

</ul>

<strong> </strong>

<strong>Part 2, 3, &amp; 4. Lab Work (60 points)</strong>

<strong>Part 2. Using MARS, a MIPS simulator (15 points, A, B, C each part: 5 points)</strong>

<ol>

 <li><strong><u> Examine the controls and options in MARS</u></strong></li>

 <li>Open the MARS simulator. Take a few minutes to explore each of the windows (Edit &amp; Execute; MARS Messages &amp; Run I/O; Registers, Coproc 1 and Coproc 2). Look at each of the controls on the pull-down menus from the task bar at the top (File, Edit, Run, Settings, Tools, Help) and discuss what you think it does.  Change the run speed to 1 instuction/sec using the slide bar at the top.</li>

</ol>




<ol start="2">

 <li>Now, starting from the left, slowly put the mouse over each of the icons in the row across the top, to see the action that it will cause (but don’t click the icon). Determine which actions, represented by the icons, also can also be selected from a pull-down menu. Click the “?” icon (or choose it from the Help pull-down menu) and in the Help window that open, click each of the tabs and briefly look at the Help contents for that topic. Note that the MIPS tab offers a box with scroll bar, and 6 tabs of its own. Similarly, the MARS tab opens a window with 8 tabs. Be sure to look at each of these.</li>

</ol>




<ol start="3">

 <li>On the top menu, Tools offers a list of tools in the pull-down menu. Open each of these and look at it briefly to begin to understand the range of additional capabilities of MARS</li>

</ol>







<ol>

 <li><strong><u> Using a simple program in MARS</u></strong></li>

 <li>Load in Program1 (Generates “hello world”), using File &gt; Open, or the appropriate icon button. In the Edit window, examine this program, and learn what it does. Try to understand how it does it.</li>

</ol>




<ol start="5">

 <li>Assemble the program, using Run &gt; Assemble , or the appropriate icon button. In the Execute window, examine the code portion of memory (called Text Segment) and the data portion of memory (called the Data Segment). Note the beginning address of each, and the contents of each. Knowing that 2 hex characters represent one byte, and remembering  that ASCII characters are each coded as one byte,  determine which characters are stored in which locations in the Data Segment.  Examine the initial values of the registers—which ones are non-zero?  Make a note of their values. Read the messages in the MARS Messages window. Check the Run I/O window.</li>

</ol>




<ol start="6">

 <li>Set the Run Speed bar to 1 instruction/second. Now run the assembled program, using Run &gt; Go, or the appropriate icon button. What happens to the yellow highlight bar in the Text Segment during execution? What is written in the MARS Messages window? In the Run I/O window?  Compare the final values of the non-zero registers—did you expect to find $1, $4, and $2 changed by the program?  What is the final value of the $pc register?</li>

</ol>




<ol start="7">

 <li>Now edit the Program1 so that it produces a different output: Hello &lt;name of your TA&gt;   Choose one of the TAs names or the Tutor’s name, and make it print out that name. Then <u>call that TA or Tutor over to show your output</u>.</li>

</ol>




<ol>

 <li><strong><u> Finding and fixing errors in MARS</u></strong></li>

 <li>Load in Program2 (Conversion program), assemble it, and run it, providing the necessary input from the keyboard. What does this program do? Examine the MIPS assembly program to understand how it does it.</li>

</ol>




<ol start="9">

 <li>Edit the program by changing li $v0, 5 to li v0, 5 . Then assemble it and read the error message. Then fix the error and re-assemble it.</li>

</ol>




<ol start="10">

 <li>Edit the program by changing li $v0, 5 to $li v0 . Then assemble it and read the error message. Then fix the error and re-assemble it. Now run the program, at 1 instr/sec, and make note of the value of $v0 after the 2nd syscall is completed.</li>

</ol>




<ol start="11">

 <li>Edit the program by changing mul $t0, $v0, 9 to mul $t0, $t0, 9 . Then assemble it and run it, and explain why the output value is what it is. Then fix the error and re-assemble it and re-run it, to verify that Program2 again works correctly.</li>

</ol>




<ol start="12">

 <li>Change the Run speed back up to the maximum. Assemble the program, and instead of hitting the normal Run button, instead hit the “Run 1 step at a time” icon (looks like &gt;1) repeatedly, to single-step through the program. Notice that you can go slowly, examining the memory and registers after each step, or go quickly. This single-step mode is good for debugging. <u>Explain to the TA or Tutor</u> how you could use it to help find a logical error or typo error that accidently passed the assembler’s syntax check.</li>

</ol>




<strong>Part 3. <u>Using breakpoints in MARS, fixing logic errors and using jal and jr instructions</u> (25 points)</strong>




Load in Program3 (Fibonacci program), which says it is a fibonacci number finder, implemented using a loop (iteratively, not recursively).  The program has several errors, syntax and logical, that you must find and fix.  After getting it to assemble correctly, note that it runs, but gives the wrong value of fib(7), which should be 13.




To find and fix logical errors, you need to go through the code determining what the values are of the critical registers at the places in the program where they are changed.  In long programs, and especially programs with loops, it would take too long to single-step through the whole program. Instead, you must set breakpoints, and run up to those points and stop. Since the value of $v0 is where the fibonacci number is being accumulated in this program, you should set a breakpoint in the fib function wherever $v0 is changed. This way you can look at its value and determine if it is being caluclated correctly.  To set a breakpoint at an instruction, check the Bkpt box in the left-hand column next to the instructions you want to break at. Then hit Run.




[Hint: if you are not sure if the state of the machine at the breakpoint will include the effect of that instruction or not, you should experiment and learn by setting breakpoints in pairs, both at an instruction of interest, and after it, to see when the actual change in values takes place].




When you have the Program3 debugged and running correctly, <u>call the TA or Tutor to show</u> how breakpoints work, <u>and show that it calculates</u> any Fibonnacci number.




<strong>Part 4. Using MIPS for mathematical calculations Program 4(20 points)</strong>

Write a program that prompts the user for one or more integer input values, reads these values from the keyboard, and computes a mathematical formula such as (<strong><em>a different formula will be given on the board by the TA that includes all four operations and Mod</em></strong>):




A= (B * C + D / B  – C  ) Mod B




When the computation is finished, the program should print the result along with an explanatory comment to the user via the display.








