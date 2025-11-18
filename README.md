# Holostream Project

Holostream is a software application designed for processing off-axis DHM holograms, offering both serial and parallel versions for improved performance.

## Project Structure

This project contains the following folders:

Serial_version/executable_files/: This folder contains the complete serial Holostream in .exe files compressed in a .7z file. To install it on Windows, download the .7z file and decompress it.

Serial_version/Python_codes/: This folder contains the Python codes used to create the serial version. If you want to install it this way, please read the requirements.

Parallel_version/executable_files/: This folder contains the complete Holostream parallelized in .exe files. To install it on Windows, download this folder.

Parallel_version/Python_codes/: This folder contains the Python codes used to create the parallel version. If you want to install it this way, please read the requirements.

Other_codes/: This folder contains both the serial and parallelized SHPC codes in Python.

Examples/: This folder contains different holograms obtained and used for the development of this app, along with the expected results.

## Requirements

### General

64-bit Windows 10 or 11 for the precompiled executables.

A standard CPU with sufficient RAM to handle 1280 × 960 holograms. 
PubMed
+1

The Python codes are written in standard scientific Python and can, in principle, be run on any OS where the required libraries are available, although the GPU-accelerated version assumes NVIDIA’s CUDA stack.

Serial version (Python)

To run the Serial_version/Python_codes/ implementation you will need:

Python 3.8+ (3.9 or newer recommended).

A working scientific Python stack, for example:

numpy

scipy

matplotlib

opencv-python (for image I/O and basic visualization, if used)

A GUI toolkit such as PyQt5 / PySide (if you run the graphical interface).

You can install the required packages with pip or conda. The minimal set of imports can be checked directly from the scripts in Serial_version/Python_codes/.

### Parallel (GPU) version (Python)

To run the Parallel_version/Python_codes/ implementation you additionally need:

An NVIDIA GPU with CUDA support.

NVIDIA CUDA Toolkit installed and properly configured (matching your GPU drivers).

PyCUDA (GPU acceleration for the SHPC algorithm). 

Again, use pip or conda to install the Python packages, and make sure that pycuda can see your CUDA installation.

Note: Exact package versions may depend on your system. If you run into import or compatibility errors, please check the imports at the top of the Python files and install the corresponding libraries and versions.

## Installation

You can use Holostream either via the precompiled Windows executables or directly from the Python source codes.

### 1. Using the Windows executables (recommended for most users)

Serial version

Go to Serial_version/executable_files/ in this repository.

Download the .7z file containing the serial Holostream application.

Decompress the .7z file into a folder of your choice.

Run the main .exe file inside that folder to start the serial Holostream app.

Parallel (GPU) version

Go to Parallel_version/executable_files/.

Download the folder (or compressed file) containing the parallel Holostream executables.

Decompress it if needed.

Make sure you have an NVIDIA GPU with CUDA installed and up to date.

Run the main .exe file to start the GPU-accelerated Holostream app.

### 2. Running from Python source

Serial version

Install Python and the required packages (see Requirements above).

Clone or download this repository.

Open a terminal (or Anaconda prompt) and navigate to:

cd Serial_version/Python_codes


(Optional but recommended) Create and activate a virtual environment.

Run the main application script, for example:

python your_serial_main_script.py


Replace your_serial_main_script.py with the actual main script that launches the serial interface.

Parallel (GPU) version

Ensure that CUDA and pycuda are correctly installed.

Navigate to:

cd Parallel_version/Python_codes


(Optional) Activate the same or a dedicated virtual environment that includes the GPU dependencies.

Run the main script of the parallel version, for example:

python your_parallel_main_script.py

### 3. Using the example holograms

Go to the Examples/ folder and choose one of the provided holograms.

Load the selected hologram from within the Holostream app (serial or parallel version).

Compare your reconstructed phase maps with the expected results provided in the same folder to verify that the installation is working correctly.

## Citation

If you use Holostream in your research, please cite the corresponding Optics Express article:

J. Morales, S. Obando-Vásquez, A. Doblas, and C. Trujillo, “HoloStream: a GPU-powered high-speed user interface for holographic microscopy imaging,” Optics Express 33(7), 15648–15660 (2025). doi:10.1364/OE.546479.
