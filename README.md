# Torso calibration of SERGIO

## Needed hardware/software
* Xsens IMU (Orange)
* This package (tue-get get install ros-sergio_torso_calibration)
* PC for Hardware, IMU driver and TF
* PC with MATLAB

## Calibration
1. Run hardware
2. (sudo chmod a+rwx /dev/ttyUSB0)
3. roslaunch sergio_torso_calibration start.launch
4. rostopic echo /sergio/caliphers
5. rostopic echo /imu/euler
6. In MATLAB run [matlab/calibration_torso.m](/matlab/calibration_torso.m). The script shows what to do.
    * Change the parameters in [sergio_bringup](../../../sergio_bringup/tree/master/parameters/hardware/actuators) and [sergio_hardware](../../../sergio_hardware//tree/master/ops) in both 'torso_controller_ffw.ops' and 'torso_joint_publisher.ops'

##
Calibration is not working correct: Matthijs 01-05-2017
