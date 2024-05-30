# Our Implementation

Files that we have modified are located in scenes/sources/squashy_skinning and main

## skinning.cpp
| Lines Changed    | Implementation details |
| -------- | ------- |
| 125-129  | To calculate the new linear and angular acceleration    |

## velocity_tracker.cpp
| Lines Changed    | Implementation details |
| -------- | ------- |
| 87-93  | To calculate the average rotation acceleration    |
| 100  | Sets the last speed as the current rotation speed    |

## velocity_tracker.hpp
| Lines Changed    | Implementation details |
| -------- | ------- |
| 38  | Add last_speed variable for average_rotation_acceleration calculation    |
| 45  | Add avg_rotation_acceleration variable    |
| 49  | Add alpha_acceleration hyperparameter    |

## main.cpp
| Lines Changed    | Implementation details |
| -------- | ------- |
| 1-4 | Add user-defined file    |
| 31-62  |  Implement computation time, CPU and GPU memory usage   |
| 98-100  |  Initialise GPU time query    |
| 117-121  |  Set up GPU time query and computation time   |
| 131-150  |  Calculate computation time, CPU and GPU memory usage   |


# Velocity Skinning Code

- The actual implementation of velocity skinning is in the file scenes/sources/squashy_skinning/skinning.cpp

## Compilation on Windows system with Visual Studio 

- Use CMakeLists.txt with Visual Studio
- Precompiled version of GLFW3 is provided (precompiled/glfw3_win)

The executable directory need to be set to the root of the project
(Alternatively, you can copy assets/ and scenes/ directories in the executable directory)

## Compilation in command line using the Makefile (Linux/MacOS only)

$ make

$ ./scene


## Setup compilation in command line using CMake (Linux/MacOs)

This step create the build directory, call CMake to generate the Makefile, compile and execute the code. Note that the creation of the build directory and CMake call has to be done only once on a given system.

The following command assume you have opened a command line in the directory vcl/

### Create a build directory

$ mkdir build

$ cd build

### Execute CMake, compile

$ cmake ..

$ make

$ cd ..

### Execute

$ build/pgm



