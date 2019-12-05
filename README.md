# ROS multi gmsl camera on NVIDIA DRIVE PX2
## Reference
*    https://github.com/DavidTorresOcana/ros_gmsl_driver
*    https://github.com/xbasti07x/ros_gmsl_driver
*    https://github.com/oxoocoffee/gmslRosDriveworks

## NVIDIA DRIVE PX2 Setting and Installation
### Requirements Setting 
*    Driveworks 5.0.10
*    Ubuntu 16 LTS
*    ROS kinetic
*    OpenCV 3.4 for Opencv4CUDA branch
###  Installation Process
#### Install Driveworks 5.0.10.3
*    Using SDKManager
#### Install ROS kinetic
*    Follow this URL: [DRIVE PX2 ROS INSTALLATION](https://devtalk.nvidia.com/default/topic/1032204/faq/drive-px2-ros-installation/?ncid=afm-chs-44270&ranMID=44270&ranEAID=a1LgFw09t88&ranSiteID=a1LgFw09t88-dc7tsxObftd02.6HEU7yiw)
#### Install OpenCV 3.4 for Opencv4CUDA branch
*    Follow this URL: [OpenCV-3.4.3-Ubuntu-16.04-Cuda-9.2.md](https://gist.github.com/gachiemchiep/6461895ab494af1e584d67d71e086dbb), start from OpenCV Setup tag.
    *    May encourter some problem
            *   missing `cuda_gl_interop.h` 
                *  [fix](https://jkjung-avt.github.io/opencv3-on-tx2/) 
    
## Start process     
*    power on NVIDIA DRIVE PX2 
*    check LD_LIBRART_PATH
        *    `$echo $LD_LIBRART_PATH`
        *    it have to show  like: `/opt/ros/kinetic/lib:/opt/ros/kinetic/lib/aarch64-linux-gnu:/usr/lib`
*    open another terminal 
        *    `$cd catkin_ws`
        *    `$source /devel/setup.bash`
        *    `$roslaunch gmsl_n_cameras gmsl_n_cameras_two.launch`
*    open another terminal
        *    `$rviz`
* p.s. 
    * Sometime you have to check camera-type,and u should modify `.lauch` file.  

### Final Result
![](https://i.imgur.com/0GpJF1D.jpg)
### Yolo-V3 input: image_raw
![](https://i.imgur.com/O9KKduJ.jpg)ㄔ
