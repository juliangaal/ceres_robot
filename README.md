# Ceres

## Maintainers
* [Julian Gaal](mailto:gjulian@uos.de)
* [Christopher Broecker](mailto:chbroecker@uos.de)
* [Sebastian Pütz](mailto:spuetz@uos.de)

## Installation

### Non ROS Dependencies

Install wstool
`sudo apt install python-wstool
mkdir -p ~/ceres_ws` 

### ROS Packages
Use wstool to pull all required packages:
`wstool init src https://raw.githubusercontent.com/juliangaal/ceres_robot/kinetic/ceres_install/ceres.rosinstall
wstool update -t src`

### Pico Flexx Royale Libary
You need to download the royale SDK `libroyale.zip` from the [manufacturers website](http://pmdtec.com/picofamily/software/) with the costumer password provided in the pico flexx casing. Extract the linux 64 bit archive from the extracted SDK to `ceres_ws/src/pico_flexx_driver/royale`

### UDEV Rules
Install the udev rules for the pico_flexx
`cd ~/ceres_ws/src/pico_flexx_driver/royale
sudo cp libroyale-<version_number>-LINUX-64Bit/driver/udev/10-royale-ubuntu.rules /etc/udev/rules.d/`

Install the udev rules for the sick tim
sudo cp ~/ceres_ws/src/sick_tim/udev/81-sick-tim3xx.rules /etc/udev/rules.d

Install the udev rules for the phidgets driver
sudo cp ~/ceres_ws/src/phidgets_drivers/phidgets_api/share/udev/99-phidgets.rules /etc/udev/rules.d


## Remote Connection
We provide a script for an easy remote connection setup `ceres_util/ceres.rc`. *Make sure it is sourced in `~/.bashrc`*

* robots: `ceres-host`
* client:
  * `ceres-client [robot_name]`
  * `ceres-client-ip [ŕobot_name]`

