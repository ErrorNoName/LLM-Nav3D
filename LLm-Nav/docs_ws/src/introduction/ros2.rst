ROS2
============

For more information about ROS2, please visit the official ROS2 website: `ROS2 Humble <https://docs.ros.org/en/humble/index.html>`_.

What is ROS?
------------

ROS (Robot Operating System) is a flexible framework designed to build robot applications. 
It enables developers to create complex robotics systems by providing tools and libraries for building, testing, and deploying robotic software. 
As an evolution of ROS (ROS1), ROS2 introduces major improvements, focusing on scalability, real-time performance, and improved communication mechanisms.

Why Use ROS2?
-------------

ROS2 offers a robust platform for those developing both simple and complex robot applications. 
It is especially useful in environments that require distributed systems, real-time control, or that use heterogeneous hardware.

Key reasons to adopt ROS2 include:

- **Cross-platform compatibility**: Works on Linux, Windows, and macOS.
- **Modularity**: Provides a component-based architecture, allowing developers to reuse existing modules and customize them for their needs.
- **Scalability**: Capable of handling large-scale distributed systems across multiple machines.
- **Real-time capabilities**: ROS2 is designed with real-time communication in mind, enabling more predictable and timely responses.
- **Flexible communication layers**: ROS2 supports different communication middleware, such as DDS (Data Distribution Service), making it more versatile for various applications.

ROS2 is ideal for robotics researchers, hobbyists, and companies building robotic systems in diverse industries such as agriculture, healthcare, logistics, and manufacturing.  
It is particularly well-suited for:

- Developers building real-time systems.
- Teams working with distributed robotics applications.
- Anyone needing a scalable platform that supports multiple robots and machines working in sync.

Core Features of ROS2
----------------------

1. **Node-based Architecture**  
    ROS2 applications are divided into *nodes*, where each node performs a specific task. 
    These nodes communicate with each other using topics, services, or actions, providing a clear and maintainable structure for building complex systems.

2. **Data Distribution Service (DDS) for Communication**  
    ROS2 uses DDS, a standardized middleware, to ensure reliable communication between nodes, 
    whether they are on the same device or distributed across multiple machines. 
    DDS offers better performance for real-time systems and is capable of handling high-volume data transfers, crucial for robotics applications.

3. **Real-Time Systems**  
    Unlike ROS1, ROS2 can meet real-time constraints, making it suitable for applications that require fast and deterministic responses, 
    such as autonomous vehicles, drones, and industrial robots.

4. **Multi-Robot Support**  
    ROS2 is designed to support multiple robots operating together in the same environment. 
    This is achieved by leveraging DDS, which allows communication across multiple networks, making it easy to scale up robot fleets.

Basic ROS2 CLI Commands
------------------------

To interact with ROS2, you can use several command-line interface (CLI) commands. Here are some fundamental commands to get you started:

1. **Listing Topics**  
    To see all active topics: ``ros2 topic list``

2. **Echoing Topic Data**  
    To view messages published on a specific topic: ``ros2 topic echo <topic_name>``

3. **Publishing to a Topic**  
    To publish messages to a specific topic: ``ros2 topic pub <topic_name> <message_type> "<message_data>""``

4. **Launching the Node by Launch File**
    To start a set of nodes defined in a launch file: ``ros2 launch <package_name> <launch_file>``

5. **Listing Nodes**  
    To see all active nodes: ``ros2 node list``

6. **Inspecting Node Information**  
    To get information about a specific node: ``ros2 node info <node_name>``