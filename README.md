# Welcome to Shawn \(Pengxuan\)'s Portfolio 🏅
##### *Bachelor's in Computer Science & Engineering (2020 - 2024)*
Welcome to my personal portfolio! I am a new grad from University of California, Irvine. ![logo](https://github.com/PengxuanW/portfolio/blob/main/images/uci_logo.png?raw=true)


Both my academic and professional journeys are fueled by a passion for technology and innovation. Here, you'll find a showcase of my projects, skills, and experiences that reflect my commitment to learning and growth in embedded systems, electronics designs, software development and machine learning. Whether it's designing systems, coding applications, or exploring new tech frontiers, I am excited to share my work and progress with you. Thank you for visiting and happy exploring!

Title and Description: A brief overview of the project and its purpose.
Technologies Used: List of programming languages, tools, and frameworks utilized.
Screenshots/Demos: Visual representations or links to live demos or GitHub repositories.
Contributions: Your specific role and contributions to the project.

##### Table of Contents  
[Headers](#headers)  
[Emphasis](#emphasis)  
[Lora](#lora)  
[TextEditor](#texteditor)  


...snip...    
<a name="headers"/>
## Headers
.
.
.
..
.
.
..
.
<b name="emphasis"/>
## Emphasis
.
.
.
..
.
.


<name="lora"/>
## Lora

## TextEditor
A programming project in C++ called BooEdit.
This project implements a simpler version of typical editors like vim or emacs. While it doesn't handle txt-file loading or saving, this program implements key features such as cursor movement, text insertion, deletion, and undo/redo functionality. BooEdit serves as a basis for exploring important C++ and object-oriented programming concepts. These include using C++ Standard Library classes to manage memory, handling exceptions safely, employing abstract base classes for customizable implementations, and implementing the Command pattern for undoable actions. BooEdit is partially implemented, requiring contributions to specific parts, simulating a common real-world software development scenario.

Tools used: 
1. VMware to emulate Linux OS
2. GoogleTest framework to guide unit testing
3. C++ programming language and its libraries

The program looks like this:
empty start
![demo0](https://github.com/PengxuanW/portfolio/blob/main/images/TextEditProjDemo0.png?raw=true)

inserting some chars
![demo1](https://github.com/PengxuanW/portfolio/blob/main/images/TextEditDemo1.png?raw=true)

User Interface:
1. Any keyboard press of printable character: inserts a char at the current line and column
2. Ctrl + certain upper case letters: operation on the text editor
  * Ctrl + I = cursor up
  * Ctrl + M = new line
  * Ctrl + H = backspace
  * Ctrl + Z = undo
  * Ctrl + A = redo
  * ...
![class files](https://github.com/PengxuanW/portfolio/blob/main/images/TextEditClassFiles.png?raw=true)

BooEdit follows the Command pattern:
while the user hasn't quit the program yet
/{
    read one command from the keyboard
    build the corresponding Command object to represent it
    execute the command by calling its execute() method
/}

With each command being an object (insert char, backspace), it's easy to implement undo and redo functions. First, in addition to an execute() method, a newly created Command object also has a corresponding undo() method (if the execution was to insert a char at line 3 column 4, then its undo will be to remove a char at line 3 column 4). Then we can just keep track of the user-issued Command objects in an undo stack, and if the user wants to undo, the program pops the first Command object in the stack, call its undo() method to complete an undo, and push it to the redo stack. The redo stack keeps track of all the undid commands, and if the user issues a redo command, the program pops the first object in the redo stack, call its execute() method to complete a redo, and push it back to the undo stack. 
![undo and redo](https://github.com/PengxuanW/portfolio/blob/main/images/TextEditUndoRedo.png?raw=true)

The program uses a custom EditorModel class to maintain the underlying data - the current lines of text, the cursor position, the number of chars, etc. It also provides public functions that allow the EditorView class to access that data, along with basic operations that allow the various Command objects to make the necessary changes when they're executed or undone.
![EditorModel class](https://github.com/PengxuanW/portfolio/blob/main/images/TextEditEditorModelClass.png?raw=true)

![alt text](https://github.com/PengxuanW/portfolio/blob/main/images/Screenshot%202024-06-14%20183854.png?raw=true)


