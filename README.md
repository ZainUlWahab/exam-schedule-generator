# Exam Schedule Generator Using Genetic Algorithm

This project aims to generate an optimal exam timetable for a set of courses and students using a genetic algorithm. The algorithm takes into account both hard and soft constraints to ensure the most efficient scheduling while maintaining fairness for students and teachers.

# Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Genetic Algorithm](#genetic-algorithm)
- [Constraints](#constraints)
- [Jupyter Notebook](#jupyter-notebook)
- [Installation](#installation)
- [Usage](#usage)
- [Future Work](#future-work)
- [Contributions](#contributions)
- [License](#license)

## Project Overview

The primary objective of this project is to find the best possible exam timetable by minimizing conflicts and adhering to predefined constraints. The optimization process is guided by a genetic algorithm, which iteratively improves the timetable based on a fitness function.

### Dataset

The project uses the following datasets:

1. **courses.csv**: Contains information about the courses that need to be scheduled.
2. **student-courses.csv**: Lists the students and their registered courses.
3. **studentnames.csv**: Contains the names and details of the students.
4. **teachers.csv**: Lists the teachers and their respective courses.

### Genetic Algorithm

A genetic algorithm (GA) is used to generate and evolve possible exam timetables. The GA mimics the process of natural selection by iteratively selecting the best-performing schedules and using them to produce the next generation of schedules. Over time, the algorithm converges towards an optimal or near-optimal solution.

### Constraints

The fitness of a timetable is determined by the following constraints:

#### Hard Constraints
- An exam will be scheduled for each course.
- A student is enrolled in at least 3 courses. A student cannot give more than 1 exam at a time.
- Exams will not be held on weekends.
- Each exam must be held between 9 am and 5 pm.
- Each exam must be invigilated by a teacher. A teacher cannot invigilate two exams at the same time.
- A teacher cannot invigilate two exams in a row.

The above-mentioned constraints must be satisfied.

#### Soft Constraints
- All students and teachers shall be given a break on Friday from 1-2 pm.
- A student shall not give more than 1 exam consecutively.
- If a student is enrolled in a MG course and a CS course, it is preferred that their MG course exam be held before their CS course exam.
- Two hours of break in the week such that at least half the faculty is free in one slot and the rest of the faculty is free in the other slot so the faculty meetings shall be held in parts as they are now.


### Jupyter Notebook

The Jupyter notebook provided in this repository includes the following sections:

1. **Data Preprocessing**: Loading and preparing the datasets for the genetic algorithm.
2. **Genetic Algorithm Implementation**: Details of the GA, including population initialization, selection, crossover, mutation, and fitness evaluation.
3. **Constraint Handling**: How the algorithm manages both hard and soft constraints.
4. **Results**: Visualization and analysis of the final exam timetable produced by the algorithm using a GUI.

### Installation

To run this project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/ZainUlWahab/exam-schedule-generator.git
   cd exam-schedule-generator
   
2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt

3. MAKE SURE TO UNZIP THE 'Dataset.zip'.
    
4. Run the Jupyter notebook:
   ```bash
   jupyter notebook
   
5. Open the Exams_Schedule_Generator.ipynb notebook and run the cells.

### Usage

The notebook is designed to be modular and easy to adapt. You can modify the datasets or constraints according to your specific needs. The notebook will guide you through each step of the optimization process.

### Future Work

- **Enhanced Constraints**: Incorporate additional constraints such as consecutive exams in different locations.
- **Heuristic Improvements**: Experiment with different selection, crossover, and mutation strategies to further improve the algorithm's performance.
- **Scalability**: Test the algorithm with larger datasets to assess its scalability and efficiency.

### Contributions

Contributions to this project are welcome! If you have suggestions for improvements or encounter any issues, please submit a pull request, open an issue on GitHub or you can contact me on my email 'ulwahabzain@gmail.com'.
### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
