# Habitat6210 Code for Data Analysis

This repository contains example MATLAB code for extracting and analysing the ROS bag files contained in the Habitat6210 dataset.

## Getting Started

#### Prerequisites
MATLAB 2022a or later and ROS Toolbox are required to run the code contained in this repository.

#### Structure of the Repository
```bash
Habitat6210_Dataset_code
.
|-- README.md
|-- bags
|   `-- example.bag
|-- constants_initialization.m
|-- example_plots.m
|-- functions
|   |-- compute_battery_status.m
|   |-- compute_mission_status.m
|   |-- compute_motor_current.m
|   |-- compute_robot_state.m
|   |-- extract_topic_from_bag.m
|   |-- get_transforms.m
|   |-- slerp.m
|   |-- transform_data.m
|   |-- trim_in_time.m
|   `-- trim_tf_in_time.m
`-- main.m
```

#### How to Run
To extract data from a ROS bag file, perform the following:
- Open `main.m` in MATLAB 2022a or later.
- Modify the variables `bag_path` and `bag_file` so that `file_path` points to the desired ROS bag file.
- Run `main.m` and wait until all data has been extracted from the topics of the ROS bag.
- If required, run `example_plots.m` to plot the extracted data.

## Scripts

#### Main Scripts
- `main.m` - Base script file to extract data as structures from given ROS bag file.
- `constants_initialization.m` - Initialization script file that defines constants used by `main.m`.
- `example_plots.m` - Utility script file to plot the data extracted by `main.m`.

#### Main Functions
- `compute_battery_status.m` - Computes the battery SoC, Voltage, and Current.
- `compute_mission_status.m` - Computes the status of the mission goals denoting if the specified waypoints were reached.
- `compute_motor_current.m` - Computes the current absorbed by a specified motor.
- `compute_robot_state.m` - Computes the robot related quantities, mainly from the state estimator and navigation data.
- `extract_topic_from_bag.m` - Extracts the message structure from bag file and topic.
- `get_transforms.m` - Gets transforms between two frames.
- `slerp.m` - Computes the slerp of value t between quaternions q1 and q2.
- `transform_data.m` - Transforms vectorial signal into new coordinates.
- `trim_in_time.m` - Trims the structure from specified start to end times.
- `trim_tf_in_time.m` - Trims the TF structure from specified start to end times.