# MEng-VREP_TrajOpter
Robot Fabricator trajectory optimisation built with CoppeliaSim

both scenes were made for CoppeliaSim 4.02.

RobotFabricator PathPlanning CS4_02.ttt contains the path planning program in a script attached to the robot fabricator frame object.
filepaths will need to be changed to suit whatever computer is running the scene, in loadChassis() and outputFile()

RobotFabricator CS4_02.ttt contains a scene to test the instructions output by RobotFabricator PathPlanning CS4_02.ttt. it will need similarly changed filepaths.

additionally, due to differences in file reading between windows and linux, one reads lines with a \n, one strips the \n. if it breaks, this may be why.

included in In Use/diverseRobots are a selection of robot chassis and blueprints.
