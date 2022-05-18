# MEng-ARE-Trajectory-Optimisation
Robot Fabricator trajectory optimisation built with CoppeliaSim, for use with the Autonomous Robot Evolution project

both scenes were made for CoppeliaSim 4.02.

RobotFabricator Trajectory Generator contains the code to generate an assembly routine for a given robot body. This requires both a .csv file and a .stl file, both of which should be placed in the diverseRobots folder. The .csv file should be named BP----.csv, where ---- is the ID number of the body plan in question. The .stl file should be named mesh----.stl, with ---- being the same ID number. To run this, the 'modelID' variable on line 15 should be modified to match the ID number. Pressing play at that point will start the trajectory generation - this will take a while (around ten minutes with the PRM* algorithm, though that is obviously highly variable), particularly on slow hardware.
An error will occur if the scene is run from a recovered autosaved instance - this is because autosaved instances are saved in a different file, and it accesses the file location to get into the diverseRobots file.
The output of the trajectory generator is stored in the buildInstructions file, as a series of move_j commands. This is to match the api used by the arm.
The tempLog file exists to store console output. This is currently non-functional.

The RobotFabricator Simulator is a simulation of how the arm reacts to being provided with the buildInstructions file. As long as the scene is saved in the correct place and there is a buildInstructions.txt in the In Use folder, then it should simply run the commands in the buildInstructions file without any user input.

