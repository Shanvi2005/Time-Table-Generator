🗓️ Time Table Generator using Genetic Algorithm
A Python-based Time Table Generator that utilizes Genetic Algorithms to find the most optimal timetable configuration. The project aims to automate the scheduling process in educational institutes while respecting hard constraints and optimizing soft constraints.

🚀 Features
Automated timetable generation using a Genetic Algorithm.

Handles hard constraints strictly (e.g., no teacher or class overlaps).

Attempts to satisfy soft constraints as much as possible (e.g., balanced teacher loads).

Modular object-oriented design.

Easily extendable for more complex academic scheduling needs.

📌 Problem Statement
Timetable generation is an NP-hard problem, with a massive number of possible configurations. The challenge is to find a feasible timetable (no hard constraint violations) and preferably an optimal one (with fewest soft constraint violations).

🧠 Genetic Algorithm Overview
The core of our scheduler relies on a Genetic Algorithm (GA), which mimics the process of natural selection:

Initialization: Random population of candidate timetables (chromosomes).

Evaluation: Fitness function evaluates how "good" each timetable is.

Selection: Fitter individuals are more likely to be selected for reproduction.

Crossover: Parts of two chromosomes are combined to create new ones.

Mutation: Random tweaks are introduced to maintain diversity.

Elitism: Best individuals are carried forward to the next generation.

Termination: Stop when an optimal solution is found or max generations are reached.

⚙️ Project Structure
Component	Description
StudentGroup	Represents each batch with subject load, teachers assigned, etc.
Teacher	Holds information about a faculty member and their assigned subjects.
Slot	Basic unit of scheduling, akin to a gene feature.
TimeTable	A timetable consists of a list of Slots for each student group.
Gene	Encodes the timetable of a student group as a sequence of slots.
Chromosome	A full timetable for all groups. Subject to crossover and mutation.
Utility	Logging, debugging, and printing helpful information.
InputData	Handles user input (from text or UI) to feed the algorithm.
SchedulerMain	The main controller that runs selection, crossover, and mutation processes.

🎯 Constraints
✅ Hard Constraints (must not be violated):
A teacher cannot be assigned to more than one class at the same time.

A student group cannot have multiple classes scheduled simultaneously.

♻️ Soft Constraints (preferably satisfied):
Balanced distribution of teaching hours among faculty.

All student groups receive their required subject hours per week.

🧪 Testing
Intermediate outputs such as population, fitness scores, and evolution history are printed to the console.

A sample input file is provided for quick testing.

Final timetable is output after convergence or maximum generations.

🛠️ Tech Stack
Language: Python 🐍

Algorithm: Genetic Algorithm (Roulette Wheel Selection, Single Point Crossover, Swap Mutation)

No external dependencies (pure Python implementation)

📈 Future Improvements
Classroom/lab capacity considerations

Professor preferences (e.g., preferred slots or days)

GUI for input and timetable visualization

Export options (PDF, CSV)

Individual print views for faculty and student groups

📂 Getting Started
bash
Copy
Edit
git clone https://github.com/palak-khanna/Time-Table-Generator.git
cd Time-Table-Generator
python main.py
Make sure to provide your own input data (students, subjects, teachers) in the specified format or adapt the sample provided.

🤝 Contributors
Shanvi
Palak Khanna
