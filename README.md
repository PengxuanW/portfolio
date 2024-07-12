# Welcome to Shawn \(Pengxuan\)'s Portfolio 🏅
##### *Bachelor's in Computer Science & Engineering (2020 - 2024)*
Welcome to my personal portfolio! I am a new grad from University of California, Irvine. ![logo](https://github.com/PengxuanW/portfolio/blob/main/images/uci_logo.png?raw=true)


Both my academic and professional journeys are fueled by a passion for technology and innovation. Here, you'll find a showcase of my projects, skills, and experiences that reflect my commitment to learning and growth in embedded systems, electronics designs, software development and machine learning. Whether it's designing systems, coding applications, or exploring new tech frontiers, I am excited to share my work and progress with you. Thank you for visiting and happy exploring!

These projects involve various programming languages, namingly Python, Java, C/C++, Swift, and SQL. Some projects are done individually by me, and some projects are done collaboratively. 

##### Table of Contents  
[Electronics_Subsystem_Identification](#electronics_subsystem_identification)  
[Micro_HVAC_System](#micro_hvac_system)  
[LoRA_Finetuning](#lora_finetuning)  
[Text_Editor](#text_editor)  
[Hydro_Homie_Iphone_App](#hydro_homie_iphone_app)
    
# Electronics_Subsystem_Identification
https://github.com/PengxuanW/Electronics_System_SubSystem_Exploration

A co-op project with Cadence electronics done in a 4-member group. This algorithm / solution oriented program project aims to detect matched sub-systems as part of a large scale electronics system. Example: Checking and locating if mesh of connection exists in IC board and PCB systems. In order to represent a real-world electronics sytem, I proposed an abstraction view that used a graph structure of nodes and edges as the physical components and wire connections. With a graph topology, we applied different algorithms such as a modified BFS, Graph NN, and decision trees to detect the existence of sub-systems / sub-graphs. We used graph algorithms such as the "infamous" Dijkstra's and Kruskal's algorithms to extract useful features in different graphs. We also experimented with advanced graph theory ideas such as 1. Kőnig’s theorem to detect matchings (a graph feature), 2. chordal graphs to define a specific lexicographicBFS ordering as a unique feature, and 3. graph centrality and k-core numbers to detect a densely connected component. 

Tools used:
1. Intellij Idea for Java
2. Python and Tensorflow pip package for ML tasks

representing circuits and electronics as graph structure abstractions
<img src="https://github.com/PengxuanW/portfolio/blob/main/images/CadenceGraphIntro.png" alt="overview"/>

the program takes in csv and json files as graph inputs that record their features and attributes
![graphTableInput](https://github.com/PengxuanW/portfolio/blob/main/images/CadenceGraphTable.png?raw=true)

exploring the graph structures with BFS and feature analysis for applying decision tree

<img src="https://github.com/PengxuanW/portfolio/blob/main/images/CadenceBFSAlgo.png" alt="bfs" width="400"/> <img src="https://github.com/PengxuanW/portfolio/blob/main/images/CadenceDecisionTree.png" alt="dt" width="400" height="600"/>

displaying graphs and search results. 
for small graphs displayed to maximize visibility in connections between nodes: 
<img src="https://github.com/PengxuanW/portfolio/blob/main/images/CandenceSmallDisplay.png" alt="bfs" width="500"/>

for larger graphs (when the there are more than 30 vertices, graph becomes too crowded, so I abstracted the connections / edges away. Only the matching vertices and edges are displayed. If the users want to see the original connections, they can click on the components and edges to inspect their attributes individually). : 

<img src="https://github.com/PengxuanW/portfolio/blob/main/images/CadenceLargeDisplay.png" alt="dt"/>



# Micro_HVAC_System
https://github.com/PengxuanW/Mock-HVAC-System

This is a microcontroller & IoT system oriented project to mimick a Heating, Ventilation, Air Conditioning system, done individually. 
Tools used: 

1. a RaspberryPi 4B as the main microcontroller, RaspberryPi OS
2. a DHT-11 as the temperature sensor, a PIR motion sensor, a Hitachi HD44780U LCD as the main UI, and some pushbuttons + LEDs as secondary ways to interact with the system. 
3. other pieces of data such as local humidity, air quality index, and wind speed are gathered through the California Department of Water Resources API - https://et.water.ca.gov/Rest/Index. 
4. Python programming language

an overview of the system (lcd display is cutoff at the right of the image):

![overview](https://github.com/PengxuanW/portfolio/blob/main/images/hvac_overview.png?raw=true)

lcd display message example:

![lcd](https://github.com/PengxuanW/portfolio/blob/main/images/hvac_lcd.png?raw=true)

written report on the overall system:

[link](https://github.com/PengxuanW/Mock-HVAC-System/blob/main/report_final.pdf)

demo video link (Google Drive link):

[demo](https://drive.google.com/file/d/141ADcKhIx0Zh9J3aVPO4HO3q5jgL2FzZ/view?usp=sharing)


# LoRA_Finetuning 
https://github.com/PengxuanW/code_gen_with_LoRA_finetuning

A research project done in a 5-member group to finetune the Llama 2 7B large language model (LLM) and improve its coding ability, specifically Python code in algorithm and data structure related programs.
LLMs have revolutionary productivity in modern workflows, particularly in code generation. However, a lot of more widely used open-source models still focus on traditional
tasks. They do little training and optimization for code generation tasks. Llama 2 underperforms on code generation, as indicated by the Human-Eval pass@k code benchmark below (only 12.8% acceptance rate at 1st code generation and 45.6% acceptance rate after 100 instances). The Human-Eval pass@k metric [link][https://www.github.com/openai/human-eval] is an improved way of evaluating code correctness from the traditional match-based methods. The project uses finetuning on the LLM instead of training a completely new machine learning model to take advantage of its reduced requirement on memory and time, while achieving similar performance with less finetuning dataset. 


Tools used: 
1. Parameter-Efficient Fine-Tuning (PEFT): Low-Rank Adaptation(LoRA) technique
2. AlphaCode and Evol-Instruct-Code-80k-v1 to obtain and generate the dataset
3. Python programming language and packages including torch, transformers, peft, and accelerate 

research paper: [link](https://github.com/PengxuanW/code_gen_with_LoRA_finetuning/blob/main/Model%20Performance%20and%20Results%20Report.pdf)





# Text_Editor
https://github.com/PengxuanW/TextEditorProject

A solo programming project in C++ called BooEdit.
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
  - Ctrl + I = cursor up
  - Ctrl + M = new line
  - Ctrl + H = backspace
  - Ctrl + Z = undo
  - Ctrl + A = redo
  - ......

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


# Hydro_Homie_Iphone_App

An iOS based app implemented in a 4-member team. This is a wellness app that focuses on college students' hydration, exercise, and sleep habits. 
## Tools used
- Firebase DB
- Swift Programming Language and Xcode
- iOS Health App

Resources are included in the project report
report: [link](https://github.com/PengxuanW/HydroHomieIphoneApp/blob/main/HydroHomieReport.pdf)
