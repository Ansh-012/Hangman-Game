ABSTRACT
This project, titled "Hangman Game using Trie Data Structure," is a C++ console-based word guessing
game with a unique integration of data structures for hint generation. The primary aim of this project
is to combine entertainment with educational programming concepts, especially focusing on Tries—a
tree- like data structure ideal for string manipulation. The game challenges the player to guess a hidden
word within limited attempts, visually represented as a stick figure being hanged with each incorrect
guess.
Unlike conventional Hangman games, this implementation features a hint system using the Trie data
structure. When the player inputs a '?', the program offers real-time hints based on prefixes of the word
being guessed, promoting both problem-solving and learning efficiency. This game demonstrates core
programming concepts such as dynamic memory allocation, object-oriented programming, and
algorithmic thinking.
The entire game is built using the C++ language, reinforcing knowledge of classes, structures, arrays,
pointers, and standard libraries. It also encourages learning through fun, making it suitable for
beginners and intermediate programmers. Additional enhancements such as randomized word
selection and ASCII art hangman visuals create a more immersive experience.
This report details the step-by-step development of the project, from initial design to testing and
analysis, and ends with suggestions for future improvements, including user tracking, file storage,
scoring systems, and a graphical interface.

INTRODUCTION
1.1. Client Identification/Need Identification/Identification of relevant
Contemporary issue
Need Identification In the digital era, word games like Hangman serve both as
recreational tools and educational aids. Most implementations focus on static gameplay
without incorporating advanced computer science concepts. This project was
conceptualized to bridge this gap by embedding a data structure (Trie) into a well-known
game format. The goal is not only to entertain but to deepen understanding of efficient
word handling and search operations.
1.2. Identification of Problem
The broad problem is the lack of accessible and engaging tools to help individuals
test, track, and improve their typing speed and accuracy in an offline environment. This
issue becomes more important for users who prefer not to rely on web-based tools due to
privacy, internet availability, or system resource limitations. There is a need for a solution
that is fast, lightweight, user- friendly, and can motivate consistent practice.
1.3 Objectives
 Develop a playable Hangman game in C++: The primary objective is to build a fully
functional console-based Hangman game using the C++ programming language.
 Integrate a Trie to provide real- time word suggestions: A unique feature of this project is
the implementation of a Trie data structure. This Trie stores all possible game words and
allows the user to request real-time hints by typing '?'.
 Visualize the game state using ASCII art: To enhance clarity and engagement, the game
uses ASCII art to visually represent the hangman. Each incorrect guess adds a part to the
stick figure (head, body, arms, and legs), giving a graphical sense of progression and
urgency within the constraints of a text-based interface.
Enhance user experience with interactive and responsive design: The game is designed to be
user- friendly and responsive. It displays incorrect guesses, current word progress, and provides
contextual prompts. Incorporating these features will not only make the game more complex and7
fun but will also turn it into a robust learning platform suitable for both recreational and
academic use

1.6 Organization of the Report
This project report is structured into well-defined chapters to offer a logical and
comprehensive walkthrough of the Hangman Game project. The organization follows a
natural flow of software development, from problem identification to system design,
implementation, validation, and conclusion.
 Chapter 1, Introduction: outlines the motivation behind developing this project, the
existing gaps in traditional Hangman games, and how the integration of a Trie data
structure improves gameplay. It also defines the project’s objectives, the tasks involved,
and the timeline followed during development.
 Chapter 2, Literature Review: surveys existing tools and systems related to Hangman
games and real-time word hinting. It highlights their limitations and shows how this
project provides a unique solution by combining a Trie with interactive game mechanics.
 Chapter 3, Design Flow / Process: explains the architectural layout and design decisions
made. It discusses the selection of the C++ language, the Trie structure, ASCII art for
visual feedback, and design constraints considered during the planning stage.
 Chapter 4, Implementation and Result Analysis: dives deep into the actual code
implementation. It breaks down the game into functional modules including the Trie
operations, user interaction, hint system, and Hangman drawing logic. It also includes
output samples and analyzes the testing results.
 Chapter 5, Conclusion and Future Work: reflects on the achievements of the project and
the challenges faced. It also proposes future improvements such as GUI support, difficulty
modes, scoring systems, and a multiplayer leaderboard.
 Finally: the Appendix section includes the complete source code, additional test outputs,
and a user manual that guides users through the installation and gameplay process.

CHAPTER 2.
LITERATURE REVIEW/BACKGROUND STUDY
2.1. Timeline of the reported problem
The need for efficient typing and word recognition tools has existed for decades, but the
significance of interactive educational games like Hangman grew especially during the early
2000s when digital literacy started gaining global focus. As mobile and desktop applications
emerged, many developers recreated Hangman in basic programming languages such as Java,
Python, and C++.
However, with the rapid shift to remote learning environments and online education
during the COVID-19 pandemic (2020 onwards), the importance of lightweight, offline-
friendly educational games resurfaced. Most tools developed during this period focused on
improving vocabulary and typing speed but lacked interactivity, hint systems, and data
structure-driven designs.
From 2020 to 2023, there was a significant rise in simple terminal-based games for
learning programming. But these applications typically offered limited features.
Observations made through usage and user feedback revealed the following gaps:
 Lack of scalable word suggestion mechanisms.
 Repetitive and predictable gameplay.
 Minimal use of data structures for performance enhancement.
In early 2024, the idea to develop a Trie-based Hangman was conceptualized to solve these
problems. During the planning and development phase (early 2025), the goal was clearly
identified—to create a C++ console game that combined entertainment with educational
value through efficient word retrieval. The current project is the result of that initiative.
2.2. Proposed solutions
To overcome the identified limitations of traditional Hangman games, this project proposes
a more robust, responsive, and educationally valuable solution. The proposed Hangman
game uses a Trie data structure for efficient prefix matching, allowing real-time word
hinting based on partial input. It is implemented in C++ as a command-line application and
offers features such as:
Randomized word selection from a predefined list.
 ASCII art for visualizing game progress.
 Input validation and interactive user prompts.
 Prefix-based hint retrieval using a dynamically built Trie.
 This approach makes the game not only entertaining but also a strong learning tool for
students studying

2.4. Review Summary
From the analysis of existing tools and related systems, it is evident that most traditional
and digital versions of Hangman fail to provide an adaptive and educative experience. The
majority are based on fixed word sets, lack customization, and do not use efficient data
structures. Our project addresses this gap by offering a Trie-based solution that balances
gameplay and computational intelligence.
The review confirms the uniqueness and potential impact of the proposed game.
2.5. Problem Definition
There is a lack of an interactive, offline-capable Hangman game that leverages data
structures like Trie for real-time hinting and enhanced user experience. Most available
versions are either online- only, lack engagement, or do not help improve computational
thinking. This project defines the problem as the need to design a learning-focused,
efficient Hangman game that offers both entertainment and educational value through
optimized string handling.
2.6. Goals/Objectives
The main goals and objectives of this project are:
 Create an interactive Hangman game using C++
 Employ a Trie data structure for prefix-based word hinting
 Ensure the game runs smoothly in terminal environments
 Use ASCII visuals to maintain lightweight gameplay
 Promote computational thinking and basic algorithm understanding through game
interaction.
This project is among the first attempts to integrate Trie-based prefix matching into a
Hangman game, making it both fun and intellectually enriching.
 data structures and algorithms.

CHAPTER 3.
DESIGN FLOW/PROCESS
3.1. Evaluation & Selection of Specifications/Features
The first and most critical phase in designing the Hangman Game project was the
evaluation and selection of essential features. The objective was to develop a classic
word-guessing game with improvements in efficiency, usability, and data handling.
Key specifications chosen included:
 Efficient word search using a Trie data structure.
 Real-time score tracking and leaderboard using a Max-Heap.
 User-friendly console interface with input validation.
 Timer feature to track how quickly the user solves the game.
 Hint feature that gives the first few letters of the word.
These features were chosen based on their practical relevance, programming complexity
suitable for a learning project, and their contribution to gameplay experience.
3.2. Design Constraints
During the planning and development phase, several constraints were identified that influenced
the final design:
 Platform Limitation: The game was implemented as a console-based application in
C++, which limited GUI elements and required reliance on text-based interaction.
 Data Structure Scope: The use of Trie and Heap structures was prioritized, which
influenced the selection and handling of game features.
 Time Constraint: The development had to be completed within the duration of the
academic training period.
 Memory Management: As C++ doesn’t provide built-in garbage collection, careful
management of dynamic memory (especially in the Trie) was required.
 User Input Handling: Ensuring robust input checking and ignoring invalid or
repeated guesses required additional logic.
3.3. Analysis and Feature finalization subject to constraints
After evaluating the requirements and constraints, a few features were either added,
removed, or modified for better compatibility and performance:
Added Features:
 Trie-based word storage: Allows fast prefix searches and hints.
 Score leaderboard using Max-Heap: Ranks players based on performance.
 Timer-based scoring: Faster guesses earn more points.
 Dynamic word suggestions: Hints based on Trie traversal.

Modified Features:
 Originally, a GUI version was considered, but due to C++ console limitation, it was
changed to a CLI-based interface.
 Difficulty levels were simplified (Easy/Medium/Hard) instead of implementing
advanced AI- based word prediction.
Removed Features:
 Multiplayer support and web-based interface were removed due to time and
complexity constraints.
 Full dictionary import (e.g., 1000+ words) was trimmed to a manageable list for simplicity.

<img width="626" alt="Screenshot 2025-06-26 at 4 33 28 PM" src="https://github.com/user-attachments/assets/ca97ba9e-ea6d-4627-b930-85e65567feb8" />
<img width="626" alt="Screenshot 2025-06-26 at 4 33 28 PM" src="https://github.com/user-attachments/assets/ca97ba9e-ea6d-4627-b930-85e65567feb8" />


3.5. Implementation Plan / Methodology
The development was divided into the following phases:
1. Planning & Research:
o Study of Trie and Heap implementations.
o Design of the game logic and structure.
2. Module Development:
o Implementing the Trie for word insertion, search, and suggestions.
o Creating the Max-Heap for the leaderboard system.
o Writing the main game logic (input handling, word masking, attempts logic).
3. Testing:
o Testing with different word lengths and game scenarios.
o Checking edge cases like repeated letters, invalid input, and full word guesses.
4. Debugging & Optimization:
o Ensured memory safety (destructors for dynamic structures).
Algorithm Summary:
Here is a high-level overview of key algorithms used in the project:
1. Trie Insertion (for word storage)
2. Trie Search (used for hints)
3. Max-Heap Insertion (for score leaderboard)
4. Hangman Game Loop (simplified):These algorithms formed the foundation of the gameplay logic and
ensured fast performance even as word list or scores grew.

CHAPTER 4.
RESULTS ANALYSIS AND VALIDATION
4.1. Implementation of solution
The implementation of this project was done using basic and easily available tools. Each
stage of the project—analysis, design, coding, testing, and documentation—was
completed step by step. Below is a clear explanation of how each part was carried out
using simple methods and tools.
Analysis
The Hangman game project was designed with the aim of integrating data structure logic (Trie)
into a fun and educational console application. The gameplay was kept minimal yet
functional—centered around word guessing, ASCII visuals, and hint generation using prefix
matching. A basic analysis of existing Hangman versions confirmed the lack of such data
structure integration, validating the project’s uniqueness.
Design
The design followed a linear, menu-free gameplay structure to maintain simplicity. Words were
stored in a Trie, and the player guessed letters, with missed attempts progressively visualized
using ASCII graphics. The prefix-based hint feature, made possible by Trie traversal, enhanced
user interaction. All variables and states (like attempts, incorrect guesses, word progress) were
maintained and updated in real-time.
Report Preparation
All modules were explained with clarity and logical flow in the report. From abstract to
conclusion, each section outlines the thought process, implementation, and final output of the
project. Code sections were kept modular and clean to aid understanding. Screenshots and
flowcharts were included to visualize the process and results.
Project Management and Communication
The project was planned and completed in multiple phases—starting from requirement
gathering and design, followed by coding, testing, and final documentation. Informal peer
feedback helped improve the hint system and logic flow. Communication and discussion were
mostly done during lab sessions and online meetings with peers.

Conclusion:
The Hangman game was successfully implemented with all intended features: word guessing,
hint system using Trie, and user feedback via ASCII visuals. It runs smoothly on any standard
terminal and provides an interactive experience while demonstrating Trie operations. The project
also strengthened skills in structured programming, recursion, and C++ string handling. All
components were tested for correctness, making it a reliable and educational mini-game.
