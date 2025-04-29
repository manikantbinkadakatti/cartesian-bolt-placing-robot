# Smart Cartesian Bot for Bolt Placing 🤖🔩

## Overview
This project presents a **Smart Cartesian Robot** designed to automate the bolt placement process in industrial environments. Built using a Raspberry Pi and controlled along Y and Z axes, the robot picks and places bolts using image processing with **YOLOv8 + OpenCV**. It ensures precise bolt placement and real-time validation, helping eliminate human error and speed up production.

## Features
- Cartesian movement with NEMA 17 stepper motors and lead screws
- Image recognition and bolt validation using YOLOv8
- Custom electric gripper powered by servo
- Raspberry Pi-controlled via Python
- Fully autonomous bolt picking and placing
- SolidWorks CAD design
- Real-time feedback system and error reporting

## Technologies Used
- Raspberry Pi
- YOLOv8 & OpenCV (Image Processing)
- NEMA 17 Stepper Motors
- TB6600 Motor Drivers
- Python
- SolidWorks (CAD)
- Geany IDE
- USB Camera

## Hardware Specifications
| Component           | Description                          |
|---------------------|--------------------------------------|
| Controller          | Raspberry Pi                         |
| Motors              | 2x NEMA 17 Stepper, 1x MG946R Servo  |
| Motor Driver        | TB6600 x2                            |
| Camera              | USB webcam for object detection      |
| Power               | 24V, 3A with Buck Converter           |
| Frame               | Iron Gantry with Lead Screw Drive    |

## File Structure
cartesian-bolt-placing-robot/
│
├── README.md
├── docs/
│   ├── system_flowchart.png
│   ├── block_diagram.jpg
│   └── system_architecture.png
│
├── code/
│   ├── bolt_picker_control.py
│   ├── motor_driver_interface.py
│   ├── yolov8_inference.py
│   └── raspberry_pi_setup.md
│
├── image_processing/
│   ├── training_images/
│   ├── annotations/
│   └── yolov8_model.pt
│
├── cad_models/
│   ├── gantry_model.png
│   ├── gripper_design.png
│   └── final_assembly.jpg
│
├── electronics/
│   ├── wiring_diagram_motor.png
│   ├── raspberry_pi_circuit.jpg
│   └── bill_of_materials.xlsx
│
└── report/
    └── Cartesian_Bot_Project_Report.pdf


## How It Works
1. The robot homes to the predefined bolt location.
2. Uses YOLOv8 model to detect bolt hole.
3. Gripper picks the bolt.
4. Robot moves along Y and Z axes to hole.
5. Places the bolt and uses camera to verify placement.
6. Logs the result and continues.
