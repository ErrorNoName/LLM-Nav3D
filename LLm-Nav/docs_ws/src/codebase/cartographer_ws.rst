Cartographer Workspace
======================

This repository contains the codebase for setting up the Cartographer SLAM. In this project, we use the Cartographer SLAM to build a map of the environment and localize the robot within the map.

Building docker image
----------------------

1. Clone the repository::

    git clone https://github.com/YuZhong-Chen/LLM-Navigation.git

2. Build the docker image::

    cd LLM-Navigation/cartographer_ws/docker
    docker compose pull
    docker compose up -d --build

Building the workspace
----------------------

1. Attach to the container::

    docker attach ros2-cartographer-ws
    
2. Install the dependencies and build the workspace::
    
    cd /home/ros2-essentials/cartographer_ws
    rosdep update
    rosdep install --from-paths src --ignore-src --rosdistro humble -y
    colcon build

Simple test
----------------------

1. Attach to the container::

    docker attach ros2-cartographer-ws
    tmux

2. Run the simulation in tmux session::

    export TURTLEBOT3_MODEL=burger
    ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py

3. Open another tmux session and run the Cartographer SLAM::

    source install/setup.bash
    ros2 launch cartographer_ros cartographer.launch.py

4. Open another tmux session to control the robot (Optional)::

    rqt_robot_steering

.. note::

    For more details, please refer to the ``README.md`` file in the repository.