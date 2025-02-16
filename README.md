# Install-ROS-melodic-on-Jetson-Nano

Prerequisites:

Before installing ROS Melodic on Jetson Nano, ensure the following:

You have Ubuntu 18.04 (Bionic) installed,
Your system is up to date and
You have sudo privileges.

----------------------------------------------------------------------------------------------------------
Step 1: Update and Upgrade the System.
Run the following commands to update and upgrade your system:
( sudo apt update && sudo apt upgrade -y )

Step 2: Set Up ROS Repository and GPG Keys:

1-Add the ROS package repository:
( sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list' )

2-Add the GPG key for authentication:
( sudo apt install curl
curl -sSL 'http://repo.ros2.org/repos.key' | sudo apt-key add - )

3-Update the package list:
( sudo apt update )

----------------------------------------------------------------------------------------------------------

Step 3: Install ROS Melodic
Choose one of the following installation options:

Full Desktop Installation (Recommended):
( sudo apt install ros-melodic-desktop-full )

Minimal Installation (Without GUI tools):
( sudo apt install ros-melodic-ros-base )


----------------------------------------------------------------------------------------------------------

Step 4: Set Up Environment Variables
To ensure ROS is available in every new terminal session, run:
 ( echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc )

--------------------------------------------------------------------------------------------------------
Step 5: Install Dependencies and Additional Tools
Install required dependencies:
( sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential )

Initialize and update rosdep:
( sudo rosdep init
rosdep update ) 

----------------------------------------------------------------------------------------------------------

Step 6: Verify the Installation

To verify that ROS is correctly installed, run:
( roscore )
If ROS starts successfully without errors it means ---> the installation is complete.


-------------------------------------------------------------------------------------------------------

Documenting the Installation Steps on GitHub

1-Create a GitHub Repository

Visit GitHub and create a new repository named ros-installation-guide,
Set the repository as public or private as needed.

2-Upload Installation Guide to GitHub

a- Initialize the repository locally and link it to GitHub:
( git init
git remote add origin https://github.com/YOUR_USERNAME/ros-installation-guide.git )

b- Create a README.md file and add the installation guide:
( echo "# ROS Melodic Installation on Jetson Nano" > README.md )

c- Stage and commit the files:
( git add .
git commit -m "Added ROS Melodic installation guide for Jetson Nano" )

d- Push the files to GitHub:
( git branch -M main
git push -u origin main )




