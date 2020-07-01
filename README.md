# Air-Mouse

Air-Mouse - Moves mouse cursor,Using ESP-32 & MPU6050(6-axis Accelerometer & Gyroscope) in 3D space with Bluetooth and Buttons support.

## Table of Contents

* [About the Project](#about-the-project)
  * [Tech Stack](#tech-stack)
  * [File Structure](#file-structure)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#usage)
* [Results and Demo](#results-and-demo)
* [Future Work](#future-work)
* [Troubleshooting](#troubleshooting)
* [Contributors](#contributors)
* [Acknowledgements and Resources](#acknowledgements-and-resources)
* [License](#license)

<!-- ABOUT THE PROJECT -->
## About The Project
* The Aim of the Project is to make a Mouse using the data fusion DMP(Digital Motion Processing) of MPU_6050 and ESP32 with Bluetooth support to actually make it    easier for the user to move pointer in any position they want.
* The Support for Right and Left click is also established using Capacitive touch pins of ESP32.
   
   [Air-Mouse](https://drive.google.com/file/d/1ngPo_A47NI5bO16B8QKe7McMDUR_fAav/view?usp=sharing)

### Tech Stack
The Technologies used for this project are
* [FreeRTOS](https://www.freertos.org/openrtos.html)
* [CMake](https://cmake.org)

### File Structure
    .
    ├── Components              # Contains files of specific library of functions or Hardware used
    │    ├──I2Cdev              # Library for I2C communication
    │    ├──MPU6050             # Library for MPU6050 sensor
    │    ├──CMakeLists.txt      # contains commands to include the given component in a esp-idf 
    ├── docs                    # Documentation files 
    │   ├── report.pdf          # Project report
    │   └── results             # Folder containing screenshots, gifs, videos of results
    ├── main                    # Source files (alternatively `lib` or `app`)
    │   ├──main.c               # Main Source code to be executed
    │   ├──kconfig.projbuild    # defines the entries of the menu for configuration
    │   ├──CMakeLists.txt       # contains commands to include the bluetooth library and main.c in esp-idf
    ├── CmakeLists.txt          # contains commands to include Components and main folder while executing
    ├── LICENSE
    └── README.md 
 



## Getting Started

### Prerequisites
Install ESP-IDF : https://github.com/espressif/esp-idf

### Installation
Clone the project
```
git clone https://github.com/n1rml/esp32_airmouse.git esp32_airmouse

cd esp32_airmouse
```
## Usage

Build
```
idf.py build
```
Flash
```
idf.py -p (PORT) flash monitor

```
### Configuration

```
idf.py menuconfig
```
* `Example Connection Configuration`
  * `Bluetooth Name` - Set Bluetooth Name
  
* `MPU6050 Configuration
  * `SDA Pin No.` - Set SDA Pin No.
  * `CLK Pin No.` - Set CLK Pin No.
  
## Results and Demo
The use of Right and Left Capacitive touch pins has been demonstrated in the following videos
 [Right/left click](https://drive.google.com/file/d/1xQOD4461v5NgVFQ_UL73FERE7jTVrADS/view?usp=sharing)
  
  
## Credits and many thanks to 
* @VedantParanjape
* Jeff Rowberg for the MPU6050 library for esp-idf :
  https://github.com/jrowberg/i2cdevlib/tree/master/ESP32_ESP-IDF   
  
  
  
