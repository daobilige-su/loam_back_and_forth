# loam_back_and_forth

This is a LOAM (Lidar Odometry and Mapping) ROS package for back and forth tilting 2D laser scanner. This package is a simple modified copy of the original one release by [Ji Zhang](http://www.frc.ri.cmu.edu/~jizhang03/). The only change on top of the original one is to make it a Catkin package and work under ROS Indigo. Please cite their paper if this package is used. 

Wiki Webpage: [http://wiki.ros.org/loam_back_and_forth](http://wiki.ros.org/loam_back_and_forth)

J. Zhang and S. Singh. LOAM: Lidar Odometry and Mapping in Real-time. Robotics: Science and Systems Conference (RSS). Berkeley, CA, July 2014.([PDF](http://www.frc.ri.cmu.edu/~jizhang03/Publications/RSS_2014.pdf)),([VIDEO](https://www.youtube.com/watch?v=8ezyhTAEyHs))

--
Original Introduction:

Lidar Odometry and Mapping (Loam) is a realtime method for state estimation and mapping using a 3D lidar, and optionally an IMU. The program contains four nodes. The “scanRegistration” node stacks laser scans within a sweep and publishes them as point cloud. The “laserOdometry” node estimates motion of the lidar between two sweeps, at a higher frame rate. The node corrects distortion in the point cloud from motion of the lidar. The “laserMapping” node takes the output of “laser_odometry” and incrementally builds a map. It also computes pose of the lidar on the map, at a lower frame rate. The state estimation of the lidar is combination of the outputs from “laserOdometry” and “laserMapping”, integrated in the “transformMaintenance” node. 

The program is tested on ROS Fuerte, on a laptop computer with 2.5 GHz quad cores and 6 Gib memory (the program consumes two cores). This version uses a lidar that spins back and forth.

Wiki Webpage: http://wiki.ros.org/loam_back_and_forth

