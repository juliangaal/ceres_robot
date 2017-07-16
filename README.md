# Ceres

![alt-text](http://i.imgur.com/jh4v97F.jpg)

## Maintainers
* Julian Gaal | [contact](mailto:gjulian@uos.de)
* Christopher Broecker | [contact](mailto:chbroecker@uos.de)

## Branches
* `kinetic`: basic setup, see image
* (Future branch `kinetic-xtion`: add xtion camera to your setup)
* (Future branch `kinetic-puck`: add Velodye Puck)

## Installation
For the installation script to work, you need to place the picoflexx driver `libroyale.zip` in `~/Downloads`, after downloading it manually from the [manufacturers website](http://pmdtec.com/picofamily/software/) with the costumer password provided in the pico flexx casing.

After that, install everything with the follwing scripts. save them to your machine 

`wget https://raw.githubusercontent.com/uos/ceres_robot/[insert_branch]/ceres_install/setup_ceres.bash` to set up ROS

and

`wget https://raw.githubusercontent.com/uos/ceres_robot/kinetic/ceres_install/setup_nuc.bash` so set up NUC

and execute them

## Remote Connection
We provide a script to do so (see /ceres_install/ceres.rc)
Add the `.ssh-config` file to your home directory for these commands to work

* On client: `ssh -X [insert_robot]`, e.g. `ssh -X blitza`
* On host:   `ceres-host`
* On client: `ceres-client-ip [insert_robot]`
* Use rviz on client!


