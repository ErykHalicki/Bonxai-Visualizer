# Bonxai Visualizer

This project provides a visualization tool for Bonxai voxel grids. It allows you to visualize and interact with voxel grids stored in the Bonxai format. Below are the installation and usage instructions:

## Installation

1. Clone the repository from GitHub:

   ```bash
   git clone https://github.com/ErykHalicki/Bonxai-Visualizer.git
Navigate to the project directory:

bash
Copy code
cd Bonxai-Visualizer
Create a build directory:

bash
Copy code
mkdir build && cd build
Configure the build with CMake:

bash
Copy code
cmake ..
Build the project:

bash
Copy code
make
Install the executables (optional):

bash
Copy code
sudo make install
Usage
Visualizer
To visualize a Bonxai voxel grid, run the visualizer executable followed by the path to the input file:

bash
Copy code
./visualizer <input_file>
Serialization Test
The serialization_test executable tests the serialization and deserialization functionality of the Bonxai voxel grids. You can run it without any arguments:

bash
Copy code
./serialization_test
Example
To create a sphere and store it in a file named test.bx, you can use the following command:

bash
Copy code
./serialization_test
Then, you can visualize the generated sphere using the visualizer:

bash
Copy code
./visualizer test.bx
Requirements
OpenGL
GLFW3
Ensure that these dependencies are installed on your system before building the project.

Feel free to reach out if you encounter any issues or have any questions!
