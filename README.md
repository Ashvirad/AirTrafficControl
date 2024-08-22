**AirTrafficControlSystem-using-POSIX-API**

Summary:Simulating an air traffic control system where communication between planes, airport and control center happens using various aspects of posix-API with underlying multi-threading support used at entities for efficient communication.

# Air-Traffic-Controller
POSIX-compliant Air Traffic Control System simulation in C using OS concepts-MultiThreading/IPC/Pipes/MessageQueues
**Air Traffic Control System **

Welcome to the Air Traffic Control System project! This repository contains the implementation of an Air Traffic Control System using POSIX-compliant C programming. Below are the instructions for running and understanding the project.

### Project Overview:

The Air Traffic Control System consists of several components:
1. **plane.c**: A program to simulate the behavior of passenger and cargo planes.
2. **airtrafficcontroller.c**: Manages the flow of planes between airports.
3. **cleanup.c**: Responsible for initiating the termination of the entire system.
4. **airport.c**: Simulates the behavior of airports, including handling arrivals and departures.

### Running the Project:

To run the project, follow these steps:

1. Compile each C file separately using a POSIX-compliant compiler.
2. Execute each compiled binary file in separate terminals or processes.
3. Follow the prompts provided by each program to input relevant information.

### Understanding the Workflow:

The workflow of the Air Traffic Control System is as follows:

1. Plane Process Creation: 
   - A new instance of the `plane.c` program creates a plane process, simulating either a passenger or cargo plane.
   - User input regarding plane details, such as ID, type, weight, etc., is collected.

2. Air Traffic Controller Management:
   - The `airtrafficcontroller.c` process orchestrates the movement of planes between airports.
   - It communicates with airports and planes via a single message queue.

3. Airport Handling:
   - Each instance of `airport.c` represents an airport, managing arrivals and departures.
   - Runways are assigned to planes based on load capacity and availability.

4. Cleanup and Termination:
   - The `cleanup.c` process initiates the termination of the entire system upon user request.
   - It communicates with the air traffic controller to ensure safe termination.
