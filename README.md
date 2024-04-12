# GeneticsAlgorithm
Using a genetic algorithm to create a class schedule for your college major.

The posted code shows the use of a genetic algorithm to optimize classes in individual rooms. This also translates directly into an optimal plan for students and professors.

### Classes:
The following classes are used to initialize individual parts of the plan (e.g. professors, halls, universities) as objects:

- Weekdays
- Professor
- Poom
- Students
- Subject
- University

A class for preprocessing:

- Initializing

The class through which we calculate fitness. It contains two functions. One of them makes sure that no one has classes in two places at the same time and that only one class takes place in each room at a given time. The second one checks the assumptions regarding the schedule, i.e. days off on Monday mornings and Friday evenings. The fitnees_2 function can be modified very easily, which was part of the idea to solve this proble:

- fitness_class

A class that removes those from plans that do not meet the assumptions. This leaves only the 10 best plans (in terms of fitness)

- heuristic

A class for visualizing results

- plan

The code in the **genetic_algorithm** file contains, as the name suggests, the genetic algorithm. First, we create descendants based on 10 artificially generated plans. We will exchange classes between individual rooms in a random proportion, remembering the types of classes (whether it is a lecture/class/laboratory) and with a certain probability we will permute individual classes in the plan. In this way, we create offspring that are then sorted according to the highest fitness function result.

I also post the entire program as it was written, the file is called **"entire_program"**.
