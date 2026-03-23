Evolutionary Car Racer
This project implements a simulation in which virtual cars learn to navigate a custom-designed track using evolutionary algorithms. Each car is controlled by a small neural network, and successive generations evolve to travel farther, survive longer, and complete more checkpoints. The project demonstrates concepts in machine learning, evolutionary optimization, simulation design, and performance tracking.


Features
- Custom-built 2D racetrack with collision detection
- Population-based evolutionary algorithm
- Neural network–controlled cars with sensor inputs
- Fitness evaluation based on distance traveled, checkpoints reached, and survival time
- Automatic generation cycling with mutation and selection
- Real-time visualization of all cars in the population
- Detailed metrics for each generation, including best fitness, average fitness, and survival statistics


Technologies Used
- Programming language: python
- Rendering/graphics: Pygame
- Neural network implementation
- Evolutionary algorithm with mutation and selection
- Collision detection and geometric modeling of the track
- Performance logging and visualization


How to Run
- Clone the repository:
git clone https://github.com/yourusername/evolutionary-car-racer.git
- Navigate into the project directory:
cd evolutionary-car-racer
- Run the main simulation:
python main.py


Controls and Usage
- The simulation begins with a full population of cars.
- Each car receives sensor inputs (distance to walls, angle to track, etc.) and outputs steering and acceleration commands.
- When all cars have crashed or timed out, a new generation is created using the top performers.
- The simulation continues automatically until stopped manually.
- Parameters such as mutation rate, population size, and sensor configuration can be adjusted in the configuration file.


Implementation Overview
Each car is represented by a neural network that maps sensor readings to control outputs. During each generation, cars are evaluated based on a fitness function that incorporates distance traveled, checkpoints reached, and time survived. After all cars have finished, the top performers are selected to produce the next generation through mutation-based reproduction. The track is defined as a polygonal boundary, and collision detection is performed using ray casting and geometric intersection tests.The simulation is optimized to run many cars simultaneously while maintaining real-time visualization. Metrics are displayed on-screen to track progress across generations.

Example Output
Below is an example screenshot from the simulation showing multiple cars navigating the track and the generation statistics panel.
<img width="1594" height="923" alt="Screenshot 2026-03-23 174200" src="https://github.com/user-attachments/assets/8ab56e4b-9bc1-49fd-bd8c-360e1d29b903" />


Future Improvements
- Add crossover in addition to mutation for more complex evolutionary behavior
- Implement multiple track layouts and randomized environments
- Add a replay system for best-performing cars
- Introduce more advanced neural network architectures
- Add a training-only mode without visualization for faster evolution
- Export and load trained models
