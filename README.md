TMT SSA Controller

The TMT SSA Controller is a Python-based GUI application designed to interface with the India TMT Segment Support Assembly (SSA) system. This tool provides real-time serial communication, live sensor data visualization, and data logging. It was developed as part of a project at the Indian Institute of Astrophysics.
This system helps visualize microstrain and positional data from up to 21 sensor channels, offering engineers a convenient way to monitor and analyze stress, strain, position, and moment parameters.

Features

•	Serial Communication: Connects to COM ports and communicates via UART.
•	Data Receiving: Receives data in the format: channel_number, position, microstrain.
•	Live Plotting: Real-time plots of:
-	Position vs Time
-	Microstrain vs Time
-	Stress vs Strain
•	Calculated Values: Converts received values into:
-	Position (mm)
-	Microstrain
-	Moment (Nm)
•	Data Export: Saves received data in .csv format with timestamps.
•	Test Data Compatible: Sample datasets like NoiseTest.csv, ROTTest.csv, and Test.csv included for offline testing.
•	User Interface: GUI built with wxPython, designed in wxFormBuilder.


Getting Started
Prerequisites

Ensure Python is installed. Then install the required libraries using:

pip install -r requirements.txt

Manual Installation:

pip install wxPython vispy pyserial PyDispatcher numpy

Running the Application

Run the main Python file:

python TMT_SSA_Controller.py

You should see the GUI window open. You can now scan for COM ports, connect, and begin communication.

Test Data Usage

You can simulate input using the UART Send field.  
Format: channel_number, position_value, strain_value  
Example: 1,1200,0.002

The application will process the values and display calculated position and moment.

Data Logging

- Select a folder to save logs using the folder picker.
- Enable recording by toggling the Start Recording button.
- Data will be saved as a .csv file with the current timestamp.

 GUI Overview

- COM Port Scan: Detect available serial ports.
- Open COM Port: Open selected port for communication.
- Start/Stop: Toggle data listening.
- Clear: Reset graphs and data.
- Channel Selection: Choose channel to monitor.
- Plots:
  - Panel 1: Position vs Time
  - Panel 2: Microstrain vs Time
  - Panel 3: Strain vs Stress

 Exported CSV Format

Each line in the CSV log will contain one UART message received:
channel_number,position,strain

Project Contribution

This project was developed at the Indian Institute of Astrophysics as part of the India TMT (Thirty Meter Telescope) Segment Support Assembly (SSA) initiative.
I participated in the project as an intern and contributed to the development of the graphical user interface and data visualization components using Python and wxPython.

Support

If you have any issues running the app or want to contribute, feel free to open an issue or pull request on the GitHub repository.


