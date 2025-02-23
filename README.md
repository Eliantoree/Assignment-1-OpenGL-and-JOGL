# Assignment-1-OpenGL-and-JOGL
Assignment #1 – OpenGL and JOGL

**Download Link:https://programming.engineering/product/assignment-1-opengl-and-jogl/**


Description
5/5 – (2 votes)
Overview

This objective of this assignment is to insure that you are sufficiently familiar with the structure of applications written in JOGL, OpenGL, and GLSL, that we will be using this semester.

The assignment is to make several relatively simple modifications to Program 2.6 from the textbook. Your program will draw an isosceles triangle that moves around the screen in various ways, and changes color, depending on input from the user (using keyboard, mouse, buttons, etc).

Java Program Structure

This program will become the framework for future assignments in the class. Note the following:

avoid allocating memory in the display() function

your Java program will define a class that extends JFrame and implements GLEventListener. It will attach a glCanvas and some buttons to the JFrame. If instead, you are using C++, please meet first with the instructor.

your Java program will incorporate an Animator to repeatedly invoke the display() method.

Your display() function can also send additional information as needed to the vertex shader, using uniform variables as shown in the textbook. For example, it could send values that the shader can use to modify the location of the triangle’s vertices, or its color(s).

GLSL Shaders

Your GLSL shaders must specify a version of “430”, and they must be read in from text files. The vertex shader should hardcode a simple triangle, and may receive some input from the Java program. The fragment shader should output the desired color(s).

Program Requirements

Your program will make these modifications to Program 2.6 from the textbook:

The triangle will be isosceles and narrow, rather than the right triangle in Program 2.6.

Movement must be based on elapsed time. Get the current time from Java, and use it to calculate the amount of time that has elapsed since the previous call to display().

Determine and display the current JOGL and OpenGL versions on the console at startup. The commands for doing this are on the CSc-155 “tech tips” page.

Your program will also add the following user controls:

a button that causes the triangle to move in a circle around the glCanvas window. Pressing the button again causes the triangle to stop moving in a circle.

a button that toggles the triangle between the solid color green, the solid color orange, and a gradient of three colors.

the key (1) cycles the triangle through four

directions: pointing up, left, down, and right.

7. mouse wheel control increases and decreases the size of the triangle.

The movement button, mouse wheel, and color toggle should all work correctly regardless of the direction that the triangle is pointing, and should not change the triangle direction.

You do not need to use transformation matrices to move the triangle. You can use the simple “offset” technique shown in Chapter 2 of the textbook. We will use transforms in homework #2.

You may add any additional features you like to the program, using additional buttons or keyboard input, so long as you document them in your PDF report. This is entirely optional, but learning more in this way could help you better prepare for homework #2 (which will be considerably more complex than homework #1).

Note: Swing menus may not be compatible with the JOGL GLCanvas object (so don’t use them).

Java Packages

Your program code must be contained in a Java package named “a1” (lower case). Each source file must contain the statement package a1; at the beginning. If you use an IDE that puts your code in a different package (or the “default package”), you must either change your IDE settings or, when the final version is finished, modify the package statements and recompile everything from a command line. All of your source code should be in a subfolder named “a1” and it should ber compiled/executed from the parent directory. Also, the “main” class in your program must be named “Code” (like in the textbook).

It must be possible to compile the program from a command prompt with: javac a1/*.java

Because of recent changes to Java and JOGL, there are several arguments that will need to be added to the “java” run command. It is found in the “TumblingCube” example, and looks like this:

java –add-exports java.base/java.lang=ALL-UNNAMED –add-exports java.desktop/sun.awt=ALL-UNNAMED –add-exports java.desktop/sun.java2d=ALL-UNNAMED -Dsun.java2d.d3d=false -Dsun.java2d.uiScale=1 a1.Code

Documentation

All code in assignments for this course must be well-documented, and you should follow standard Java coding conventions. Class names start with uppercase letters, package and variables start with lowercase, and names should use “CamelCase” (“MyClass”, “myMethod”, “myPackage”).

Deliverables

This is an INDIVIDUAL assignment. You may use code from the textbook, but everything else must be your own. No working in teams, and no use of code obtained from the internet.

Submit to Canvas TWO items:

a ZIP folder with your A1 submission, as described below

a TEXT file (.txt) indicating which RVR-5029 machine you used to test your program.

The ZIP folder contains the following:

 Java source (.java) and compiled (.class) files, in the proper “a1” folder hierarchy.  GLSL vertex and fragment shader files, also inside the a1 folder.

 compile.bat and run.bat files that work with your program.

 a .PDF report file consisting of the following numbered items:

your name, “assignment 1”, CSc-155, section number, and “Spring 2024”.

a screenshot of your running program

a list of which of the seven program requirements you were able to fully implement

a list of which of the seven program requirements you weren’t able to fully implement

instructions showing how to use your program, and which keys/buttons do what

indicate on which RVR-5029 (remote) machine you tested your program

It is a requirement that your program run properly on at least one machine in the 5029 lab. Your report AND text file must BOTH indicate which lab machine your program runs on!

