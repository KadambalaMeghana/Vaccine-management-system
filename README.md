# Vaccine-management-system

Here are some of the explanations of the headers,functions etc used in the code.

#include <iostream>
This is a C++ standard library header file for input output streams. 
It includes functionality to read and write from streams. 
You only need to include it if you wish to use streams.

#include <cstring>
<cstring> is the standard C string library (strcpy, strcat, etc) placed into the C++ std namespace.

#include <fstream>
C++ standard says nothing about includes of header-files in other header-files. 
For construct and use std::ofstream - you should include fstream header.
ofstream derives from ostream, the fstream header includes the iostream header, so you could leave out iostream and it would still compile.
But you can't leave out fstream because then you don't have a definition for ofstream.

#include <conio.h>
The conio.h header file used in C programming language contains functions for console input/output. 
Some of its most commonly used functions are clrscr, getch, getche, kbhit etc. 
They can be used to clear screen, change color of text and background, move text, check whether a key is pressed or not and to perform other tasks.

#include <iomanip>
The header <iomanip> consists of functions that are used to manipulate the output of the C++ program.
We can make the output of any program neater and presentable based on where we want to show it or who is going to use it.

#include <cstdlib>
Includes the C Standard library header <stdlib.h> and adds the associated names to the std namespace.
Including this header ensures that the names declared using external linkage in the C standard library header are declared in the std namespace.

#include <string>
Use #include <string> when you use a variable that has type std::string.

#include <unistd.h>
unistd.h is the C/C++ header file that is your code's entry point to various constant, type and function declarations that comprise the POSIX operating system API.
#include <unistd. h> gets you, among other things: the infamous NULL pointer definition.
C++ language does not provide a sleep function of its own. However, the operating system’s specific files like unistd.h for Linux and Windows.h for Windows provide this functionality.
When we use the Linux or UNIX operating system, we need to include “unistd.h” header file in our program to use the sleep () function.
While using the Windows operating system, we have to include “Windows.h” header to use the sleep () function.

#define TOTAL_VACCINE 400
#define allows you to make text substitutions before compiling the program.
Before compilation, if the C++ preprocessor finds TOTAL_VACCINE as one word, in the source code, it replaces it with the number 400.

system ("cls");
system() is a call to the OS command line, "cls" is a command on some operating systems that clears the screen.

sleep (x);
The sleep () function causes the program or the process in which it is called, to suspend its execution temporarily for a period of time(x) in seconds specified by the function parameter. 
Execution is suspended until the requested time is elapsed or a signal or an interrupt is delivered to the function.
However, if the system has scheduled any other activity, then the suspension time may be longer.

exit (0);
Exit Success is indicated by exit(0) statement which means successful termination of the program, i.e. program has been executed without any error or interrupt.

default:
switch statement: as the declaration of the default case label.
default case is optional.
This keyword is used to specify the set of statements to execute if there is no case match.

getch ();
This function takes in a single character from the standard input (stdin), and returns an integer.
This is there as part of the <conio.h> header file, so you must include it in your program.

goto A;
The goto statement is a jump statement which is sometimes also referred to as unconditional jump statement. 
The goto statement can be used to jump from anywhere to anywhere within a function.

srand (time (0));
srand() gives the random function a new seed, a starting point (usually random numbers are calculated by taking the previous number (or the seed) and then do many operations on that number to generate the next).
time(0) gives the time in seconds since the Unix epoch, which is a pretty good "unpredictable" seed (you're guaranteed your seed will be the same only once, unless you start your program multiple times within the same second).

rand ();
The rand() function is used in C/C++ to generate random numbers in the range [0, RAND_MAX). 
The srand() function sets the starting point for producing a series of pseudo-random integers. 
If srand() is not called, the rand() seed is set as if srand(1) were called at program start. 
Any other value for seed sets the generator to a different starting point. 

strcmp()
strcmp() is a built-in library function and is declared in <string.h> header file. 
This function takes two strings as arguments and compare these two strings lexicographically.

system ("PAUSE");
Note this the system("pause") command is only available in Windows Systems.
The system() function performs a call to the Operating System to run a particular command.
Note that we must include the <cstdlib> header file.
This is a Windows-specific command, which tells the OS to run the pause program.
This program waits to be terminated, and halts the exceution of the parent C++ program. 
Only after the pause program is terminated, will the original program continue.

ifstream file
When you code, sometimes you need to read some file to process the code to the next phase and for that, we need something in our code that can help us in reading the required file from any location. 
This is also known as file handling and for that, we need stream classes and it is done by using fstream, ofstream, and ifstream classes. 
Ifstream is an input stream for files and with it, we can read any information available in the file. 
For using these stream classes we need to add <iostream> and <fstream> header files in your code.

ofstream 
This class represents an output stream. 
It’s used for creating files and writing information to files.

ifstream 
This class represents an input stream. 
It’s used for reading information from data files.

fstream
This class generally represents a file stream. 
It comes with ofstream/ifstream capabilities. 
This means it’s capable of creating files, writing to files, reading from data files.

file.open()
If you need to write to the file, open it using fstream or ofstream objects. 
If you only need to read from the file, open it using the ifstream object.
There may be situations requiring a program to open more than one file. 
The strategy for opening multiple files depends upon how they will be used. 
If the situation requires simultaneous processing of two files, then you need to create a separate stream for each file. 
However, if the situation demands sequential processing of files (i.e., processing them one by one), then you can open a single stream and associate it with each file in turn. 
To use this approach, declare a stream object without initializing it, then use a second statement to associate the stream with a file
When you associate a stream with a file, either by initializing a file stream object with a file name or by using the open() method, you can provide a second argument specifying the file mode.

c_str ()
It returns a pointer to an array that contains a null-terminated sequence of characters (i.e., a C-string) representing the current value of the string object.

is_open ()
Check if a file is open.Returns whether the stream is currently associated to a file.

file.fail ()
The fail() method of ios class in C++ is used to check if the stream is has raised any fail error. 
It means that this function will check if this stream has its failbit set.

file.close ()
The close() function is used to close the file currently associated with the object. 
The close() uses ofstream library to close the file.

cin.ignore ()
The cin.ignore() function is used which is used to ignore or clear one or more characters from the input buffer.

getline (cin, username);
The C++ getline() is a standard library function that is used to read a string or a line from an input stream. 
It is a part of the <string> header. The getline() function extracts characters from the input stream and appends it to the string object until the delimiting character is encountered. 
While doing so the previously stored value in the string object str will be replaced by the input string if any.

seekg ();
seekg() is a function in the iostream library that allows us to seek an arbitrary position in a file. 
It is mainly used to set the position of the next character to be extracted from the input stream from a given file in C++ file handling.

seekg (0, ios::beg)
seek to 0th position from the beginning of the file

fflush (stdin)
The fflush() function in C++ flushes any buffered data to the respective device.
Buffered data is the temporary or application specific data stored in the physical memory of the computer until a certain time.
The fflush() function is defined in <cstdio> header file.

ios::in 
Allows input (read operations) from a stream.

ios::out 
Allows output (write operations) to a stream.

ios::binary
ios::out opens the file for writing.
ios::binary makes sure the data is read or written without translating new line characters to and from \r\n on the fly. 
In other words, exactly what you give the stream is exactly what's written.

sizeof ()
Sizeof is a much used operator in the C or C++. 
It is a compile time unary operator which can be used to compute the size of its operand.

Modifies the positioning of the fill characters in an output stream. left and right apply to any type being output, internal applies to integer, floating-point, and monetary output. Has no effect on input.
1) sets the adjustfield of the stream str to left as if by calling cout.setf(std::ios::left, std::ios_base::adjustfield)
2) sets the adjustfield of the stream str to right as if by calling cout.setf(std::ios::right, std::ios_base::adjustfield)
3) sets the adjustfield of the stream str to internal as if by calling cout.setf(std::ios::internal, std::ios_base::adjustfield)

setfill
Changes the fill character

eof ()
The eof() method of ios class in C++ is used to check if the stream is has raised any EOF (End Of File) error. 
It means that this function will check if this stream has its eofbit set.

file.write()
write(): to write data into a file.

system ("color B")
In C++ programming, the background of the output screen is black and text color is in white color. 
We can color both the background and text color in the output screen in the following ways.
system("Color XY")
Color id		Color	  Color id	  Color
1		         Blue	   9	        Light Blue
2		         Green	 0	        Black
3		         Aqua	   A	        Light Green
4		         Red	   B	        Light Aqua
5		         Purple	 C	        Light Red
6		         Yellow	 D	        Light Purple
7		         White	 E	        Light Yellow
8		         Gray 	 F	        Bright White

