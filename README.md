# Genetic Algorithm Timetable Generator

## Introduction
This project leverages a genetic algorithm to create clash-free timetables. It outlines the challenges encountered and the methodologies adopted to overcome them.

## Methodology

### Implementation Details
The genetic algorithm treats each timetable entry as a chromosome, structured as follows:
- Course
- Theory/Lab
- Section
- Section-Strength
- Professor
- First-lecture-day
- First-lecture-timeslot
- First-lecture-room
- First-lecture-room-size
- Second-lecture-day
- Second-lecture-timeslot
- Second-lecture-room
- Second-lecture-room-size

The algorithm compares these chromosomes against an existing timetable to find non-clashing schedules.

### Initial Timetable
The process begins with an empty timetable, which is gradually filled as the algorithm runs.

### Class Generation
Classes for each course are generated sequentially. A clash-free chromosome is added to the timetable, which is then used to evaluate subsequent courses.

### Fitness Function
The fitness function assesses the timetable for clashes, inversely relating the number of clashes to the fitness score.

## Results

### Final Timetable
The algorithm produces a timetable with minimal clashes.

### Clashes and Fitness Scores
On average, 1 in 10 classes may clash due to the limitation of 1000 generations, which is the optimal performance my system can handle. The fittest individual is returned if the generation limit is reached.

### Fitness Scores
The final timetable's fitness scores are as follows:
- Perfect Scores: 1.0 (indicating no clashes)
- Partial Scores: 0.5, 0.333 (indicating fewer clashes)

