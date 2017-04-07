# Torso calibration of SERGIO

## Needed hardware/software
* Xsens IMU (Orange)
* This package (tue-get get install ros-sergio_torso_calibration)
* PC for Hardware, IMU driver and TF
* PC wit MATLAB

## Calibration
1. Run hardware
2. roslaunch sergio_torso_calibration start.launch
3. In MATLAB run [matlab/calibration_torso.m](/matlab/calibration_torso.m). The script shows what to do.
    * Change the parameters in [sergio_bringup](../../../sergio_bringup/tree/master/parameters/hardware/actuators) and [sergio_hardware](../../../sergio_hardware//tree/master/ops) in both 'torso_controller_ffw.ops' and 'torso_joint_publisher.ops'
