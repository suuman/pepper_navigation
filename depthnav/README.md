## *depthnav*

### Free space navigation using depth image
Bista SR, Ward B, Corke P. Image-Based Indoor Topological Navigation with Collision Avoidance for Resource-Constrained Mobile Robots.   

## Dependencies
* [OpenCV](https://opencv.org/),
* [Boost](https://www.boost.org/),
* [naoqi_libqi](http://wiki.ros.org/naoqi_libqi), [naoqi_libqicore](http://wiki.ros.org/naoqi_libqicore) and [pepper_qi](https://github.com/suuman/pepper_navigation/tree/main/pepper_qi) (Please refer to [*../pepper_qi*](https://github.com/suuman/pepper_navigation/tree/main/pepper_qi) folder for details).

## Usage
### Standalone usage 
Refer [*depthnav_Pepper.cpp*](https://github.com/suuman/pepper_navigation/blob/main/depthnav/depthnav_Pepper.cpp)  
  
`$ mkdir build $$ cd build  `  
`$ cmake .. && make -j8  `  
`$ ./pepper_fsnav --ip < Pepper_IP >`  

### As library
1. To use the depthnav library, please refer to class ***freespacenavigation*** (*[freespacenavigation.h](https://github.com/suuman/pepper_navigation/blob/main/depthnav/freespacenavigation.h)*, *[freespacenavigation.cpp](https://github.com/suuman/pepper_navigation/blob/main/depthnav/freespacenavigation.cpp))*.  
2. Other classes and functions:  
3. - ***depthimagescanner*** ([*DepthImageScanner.h*](pepper_navigation/depthnav/DepthImageScanner.h), [*DepthImageScanner.cpp*](https://github.com/suuman/pepper_navigation/blob/main/depthnav/DepthImageScanner.cpp)) => Creats 2D grid map from depth image. 
4. - ***depth_traits*** ([*depth_traits.h*](https://github.com/suuman/pepper_navigation/blob/main/depthnav/depth_traits.h)) => Template function to process depth image obtained from [ros *depthimage_to_laserscan*](https://github.com/ros-perception/depthimage_to_laserscan) library.
5. - ***pepperlaser*** ([*pepperlaser.h*](https://github.com/suuman/pepper_navigation/blob/main/depthnav/pepperlaser.h)) => Defines Pepper Robot's Laser Memory Keys.
6. - ***alpose2d*** ([*alpose2d.h*](https://github.com/suuman/pepper_navigation/blob/main/depthnav/alpose2d.h), [*alpose2d.cpp*](https://github.com/suuman/pepper_navigation/blob/main/depthnav/alpose2d.cpp)) => *[libalmath](https://github.com/aldebaran/libalmath )* Pose2D library used to process odometry data from the Pepper robot.


