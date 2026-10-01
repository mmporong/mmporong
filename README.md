# Hi there, I'm Joo-young 👋

### Robotics software engineer (junior) | ROS 2 · C++ · Python · Linux

Mechanical engineering graduate with about five years of Unity/C# software development. I connect robot hardware, navigation and task execution, then check the results against real-robot runs and recorded logs.

[Portfolio](https://mmporong-portfolio.vercel.app/) · [Learning notes: hello, robot](https://mmporong.github.io/robotics-garden/) · [LinkedIn](https://www.linkedin.com/in/mmporong/)

Based in Korea. Attending Dongguk AI Campus's Physical AI Semi-Humanoid Engineer Program (July 6 to November 4, 2026); seeking junior robotics software integration and testing roles.

## Selected robotics projects

### AMR navigation and chassis integration

[Code](https://github.com/mmporong/jdamr_cube_ros) · [Navigation evidence](https://github.com/mmporong/jdamr_cube_ros/blob/main/jdamr_cube_navigation/README_JDAMR.md)

Integrated ESP32 firmware, a C++ ROS 2 base driver, Cartographer and Nav2. Verified an approximately 77 m corridor round trip, obstacle handling and resumption toward the same goal after stops. After moving the drive system to a dual-arm robot chassis, I updated its footprint and protective-stop region and ran 20 goals on the existing map. Recorded sensor, TF and navigation data in MCAP; rebuilt walls from the saved map in Gazebo to reproduce obstacle scenes.

### SO-101 manipulation and ACT data preparation

[Code](https://github.com/mmporong/so101-mobile-manipulation)

Built analytical IK and wrist-camera alignment for real-robot grasping and box placement. Prepared an ACT dataset with waiting segments removed (22 episodes, 4,503 frames). A separate ACT run produced one observed autonomous cube grasp; repeated success rate and the effect of the cleaned dataset remain unverified.

### Dual-arm serving robot (team)

[Code and experiment records](https://github.com/mmporong/bimanual-robot)

Connected ROS 2 Action workflows and integrated the robot in Isaac Sim; one planning-based order completed nine stages in simulation. I contributed to robot setup and pre-training integration. Policy training was handled by a teammate: the team's SmolVLA policy completed one real-robot water-pouring and cup-placement sequence using 40 demonstrations. The simulation workflow and the real-robot policy result are separate experiments.

### Go2 locomotion experiments in Isaac Lab

[Code](https://github.com/mmporong/isaac-walk-rl) · [Results and run records](https://github.com/mmporong/isaac-walk-rl/blob/main/docs/RESULTS_SUMMARY.md)

Compared reward terms and disturbances under fixed training budgets, with repeated seeds and evaluations across directions and terrain. Recorded trade-offs and experiments that showed no improvement. These are simulation results.

## Open source contributions

### Merged

| Project | Change | Pull request |
|---|---|---|
| Navigation2 | Fixed throttling of warnings for velocities not covered by a velocity polygon | [#6560](https://github.com/ros-navigation/navigation2/pull/6560) |
| MuJoCo Menagerie | Corrected the SO-101 wrist-roll joint's upper limit | [#324](https://github.com/google-deepmind/mujoco_menagerie/pull/324) |
| small_gicp | Orthonormalized the initial-guess rotation in registration | [#139](https://github.com/koide3/small_gicp/pull/139) |
| Nav2 documentation | Fixed VelocityPolygon examples in the Collision Monitor tutorial | [#980](https://github.com/ros-navigation/docs.nav2.org/pull/980) |

<details>
<summary>Selected pull requests under review (checked October 1, 2026)</summary>

| Project | Proposed change | Pull request |
|---|---|---|
| LeRobot | Configurable protection limits for SO follower grippers | [#4783](https://github.com/huggingface/lerobot/pull/4783) |
| ros2_control | Lifecycle transitions in the set_controller_state CLI verb | [#3641](https://github.com/ros-controls/ros2_control/pull/3641) |
| rosbag2 | Remove legacy ament export calls | [#2519](https://github.com/ros2/rosbag2/pull/2519) |
| MoveIt2 | Configuration hint when the legacy planning_plugin key is used | [#3895](https://github.com/moveit/moveit2/pull/3895) |
| Isaac Lab | Validate Gaussian scale randomization parameters as mean and standard deviation | [#8123](https://github.com/isaac-sim/IsaacLab/pull/8123) |
| Gazebo rendering | Respect arrow rotation visibility when showing a parent visual | [#1348](https://github.com/gazebosim/gz-rendering/pull/1348) |
| TurtleBot3 | Make LDS_MODEL optional in robot.launch.py | [#1152](https://github.com/ROBOTIS-GIT/turtlebot3/pull/1152) |

</details>

## Earlier software and hardware work

- Developed and operated mobile games and 80 WebGL science simulations. Built Python and Unity CLI parallel builds that reduced build time by about 80%.
- [BreakTok](https://github.com/mmporong/toython-hackathon): IMU device for detecting scrolling rhythms (TOYTHON 2026, top-20 final).
- [Robot dashboard](https://github.com/mmporong/robot-dashboard): replay and inspect ROS 2 execution records in MCAP.

## Tech stack

![ROS 2](https://img.shields.io/badge/ROS_2-22314E?style=flat&logo=ros&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat&logo=ubuntu&logoColor=white)
![Gazebo](https://img.shields.io/badge/Gazebo-F58113?style=flat&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyBmaWxsPSIjZmZmIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMjggMTI4Ij48cGF0aCBkPSJtMjAuOTA2IDM1LjE5NyA0My4wOTEgMjYuNzU3IDQzLjA5NS0yNi44MzUtNDMuMDktMjYuNjgyLTQzLjA5NiAyNi43Nk02My45OTMuNjRhMy41NjEgMy41NjEgMCAwIDAtMS44ODMuNTMzTDEyLjIxNiAzMi4xNDZhMy42MDUgMy42MDUgMCAwIDAtMS42OTMgMy4wNTh2NTcuNTkyYzAgMS4yNDIuNjQgMi40MDMgMS42OTMgMy4wNThsNDkuODkzIDMwLjk3M2MuMDI0LjAxMy4wNDQuMDI3LjA2OC4wNDEuMDI3LjAxNi4wNTUuMDM4LjA4Mi4wNTUuMDU4LjAzLjEyLjA0MS4xNzguMDY4LjA1OS4wMy4xMTguMDcyLjE3Ny4wOTYuMDkzLjA0LjE5Mi4wNjUuMjg3LjA5Ni4wNTYuMDE4LjEwNy4wMzkuMTY0LjA1NC4xMDcuMDMuMjE4LjA0OS4zMjcuMDY4LjA0Ny4wMDYuMDkuMDIuMTM3LjAyNy4xNTYuMDIyLjMwNy4wMjguNDY0LjAyOGEzLjQ4MSAzLjQ4MSAwIDAgMCAuOTctLjEzN2guMDEzYTMuMDE4IDMuMDE4IDAgMCAwIC4zNTUtLjEyMmMuMDM1LS4wMTMuMDcyLS4wMjYuMTA5LS4wNDEuMDk4LS4wNDQuMTktLjA5Ny4yODctLjE1LjA1Mi0uMDMuMTEyLS4wNTMuMTYzLS4wODNsLjA5Ni0uMDY4IDQ5Ljc5OC0zMC45MDVhMy41ODUgMy41ODUgMCAwIDAgMS42OTMtMy4wNThsLS4wOTYtMjguODcxYTMuNTggMy41OCAwIDAgMC0xLjg0My0zLjEyNiAzLjU4MyAzLjU4MyAwIDAgMC0zLjYzMS4wOTVsLTIxLjI0IDEzLjIyOC0xNi4zNjgtMTAuMTQzIDQxLjQ4NS0yNS44MjdhMy41OCAzLjU4IDAgMCAwIDEuNjkzLTMuMDQ0IDMuNTk2IDMuNTk2IDAgMCAwLTEuNzA3LTMuMDQ0TDY1Ljg5IDEuMTczQTMuNjA3IDMuNjA3IDAgMCAwIDYzLjk5My42NFpNMTcuNTY4IDQxLjU2NSA1My43IDY0LjAwNyAxNy41NjcgODYuNDM1Wm00OS45MzQgMjYuNjQ2IDE2LjM4IDEwLjE0My0yMS44NjggMTMuNjFhMy41NTYgMy41NTYgMCAwIDAtMS42OCAzLjA0NGwuMDU1IDIyLjMxOC0zOS40NzctMjQuNTMgMzkuNTg3LTI0LjU3MSAxLjYxLjk5NmEzLjU1OCAzLjU1OCAwIDAgMCAxLjg4NC41MzMgMy41NyAzLjU3IDAgMCAwIDEuODk4LS41MzN6bTQyLjc0IDIuMTcuMDU0IDIwLjQzNi00Mi43MjcgMjYuNTM3LS4wNjgtMjAuMzY2eiIvPjwvc3ZnPg%3D%3D)
![C#](https://img.shields.io/badge/C%23-239120?style=flat&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyBmaWxsPSIjZmZmIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMjggMTI4Ij48cGF0aCBkPSJNMTE3LjUgMzMuNWwuMy0uMmMtLjYtMS4xLTEuNS0yLjEtMi40LTIuNkw2Ny4xIDIuOWMtLjgtLjUtMS45LS43LTMuMS0uNy0xLjIgMC0yLjMuMy0zLjEuN2wtNDggMjcuOWMtMS43IDEtMi45IDMuNS0yLjkgNS40djU1LjdjMCAxLjEuMiAyLjMuOSAzLjRsLS4yLjFjLjUuOCAxLjIgMS41IDEuOSAxLjlsNDguMiAyNy45Yy44LjUgMS45LjcgMy4xLjcgMS4yIDAgMi4zLS4zIDMuMS0uN2w0OC0yNy45YzEuNy0xIDIuOS0zLjUgMi45LTUuNFYzNi4xYy4xLS44IDAtMS43LS40LTIuNnptLTUzLjUgNzBjLTIxLjggMC0zOS41LTE3LjctMzkuNS0zOS41UzQyLjIgMjQuNSA2NCAyNC41YzE0LjcgMCAyNy41IDguMSAzNC4zIDIwbC0xMyA3LjVDODEuMSA0NC41IDczLjEgMzkuNSA2NCAzOS41Yy0xMy41IDAtMjQuNSAxMS0yNC41IDI0LjVzMTEgMjQuNSAyNC41IDI0LjVjOS4xIDAgMTcuMS01IDIxLjMtMTIuNGwxMi45IDcuNmMtNi44IDExLjgtMTkuNiAxOS44LTM0LjIgMTkuOHpNMTE1IDYyaC0zLjJsLS45IDRoNC4xdjVoLTVsLTEuMiA2aC00LjlsMS4yLTZoLTMuOGwtMS4yIDZoLTQuOGwxLjItNkg5NHYtNWgzLjVsLjktNEg5NHYtNWg1LjNsMS4yLTZoNC45bC0xLjIgNmgzLjhsMS4yLTZoNC44bC0xLjIgNmgyLjJ2NXptLTEyLjcgNGgzLjhsLjktNGgtMy44eiIgZmlsbD0iI2ZmZiIvPjwvc3ZnPg%3D%3D)
![Unity](https://img.shields.io/badge/Unity-000000?style=flat&logo=unity&logoColor=white)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat&logo=anthropic&logoColor=white)
![Codex](https://img.shields.io/badge/Codex-412991?style=flat&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyBmaWxsPSIjZmZmIiByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJNMjIuMjgxOSA5LjgyMTFhNS45ODQ3IDUuOTg0NyAwIDAgMC0uNTE1Ny00LjkxMDggNi4wNDYyIDYuMDQ2MiAwIDAgMC02LjUwOTgtMi45QTYuMDY1MSA2LjA2NTEgMCAwIDAgNC45ODA3IDQuMTgxOGE1Ljk4NDcgNS45ODQ3IDAgMCAwLTMuOTk3NyAyLjkgNi4wNDYyIDYuMDQ2MiAwIDAgMCAuNzQyNyA3LjA5NjYgNS45OCA1Ljk4IDAgMCAwIC41MTEgNC45MTA3IDYuMDUxIDYuMDUxIDAgMCAwIDYuNTE0NiAyLjkwMDFBNS45ODQ3IDUuOTg0NyAwIDAgMCAxMy4yNTk5IDI0YTYuMDU1NyA2LjA1NTcgMCAwIDAgNS43NzE4LTQuMjA1OCA1Ljk4OTQgNS45ODk0IDAgMCAwIDMuOTk3Ny0yLjkwMDEgNi4wNTU3IDYuMDU1NyAwIDAgMC0uNzQ3NS03LjA3Mjl6bS05LjAyMiAxMi42MDgxYTQuNDc1NSA0LjQ3NTUgMCAwIDEtMi44NzY0LTEuMDQwOGwuMTQxOS0uMDgwNCA0Ljc3ODMtMi43NTgyYS43OTQ4Ljc5NDggMCAwIDAgLjM5MjctLjY4MTN2LTYuNzM2OWwyLjAyIDEuMTY4NmEuMDcxLjA3MSAwIDAgMSAuMDM4LjA1MnY1LjU4MjZhNC41MDQgNC41MDQgMCAwIDEtNC40OTQ1IDQuNDk0NHptLTkuNjYwNy00LjEyNTRhNC40NzA4IDQuNDcwOCAwIDAgMS0uNTM0Ni0zLjAxMzdsLjE0Mi4wODUyIDQuNzgzIDIuNzU4MmEuNzcxMi43NzEyIDAgMCAwIC43ODA2IDBsNS44NDI4LTMuMzY4NXYyLjMzMjRhLjA4MDQuMDgwNCAwIDAgMS0uMDMzMi4wNjE1TDkuNzQgMTkuOTUwMmE0LjQ5OTIgNC40OTkyIDAgMCAxLTYuMTQwOC0xLjY0NjR6TTIuMzQwOCA3Ljg5NTZhNC40ODUgNC40ODUgMCAwIDEgMi4zNjU1LTEuOTcyOFYxMS42YS43NjY0Ljc2NjQgMCAwIDAgLjM4NzkuNjc2NWw1LjgxNDQgMy4zNTQzLTIuMDIwMSAxLjE2ODVhLjA3NTcuMDc1NyAwIDAgMS0uMDcxIDBsLTQuODMwMy0yLjc4NjVBNC41MDQgNC41MDQgMCAwIDEgMi4zNDA4IDcuODcyem0xNi41OTYzIDMuODU1OEwxMy4xMDM4IDguMzY0IDE1LjExOTIgNy4yYS4wNzU3LjA3NTcgMCAwIDEgLjA3MSAwbDQuODMwMyAyLjc5MTNhNC40OTQ0IDQuNDk0NCAwIDAgMS0uNjc2NSA4LjEwNDJ2LTUuNjc3MmEuNzkuNzkgMCAwIDAtLjQwNy0uNjY3em0yLjAxMDctMy4wMjMxbC0uMTQyLS4wODUyLTQuNzczNS0yLjc4MThhLjc3NTkuNzc1OSAwIDAgMC0uNzg1NCAwTDkuNDA5IDkuMjI5N1Y2Ljg5NzRhLjA2NjIuMDY2MiAwIDAgMSAuMDI4NC0uMDYxNWw0LjgzMDMtMi43ODY2YTQuNDk5MiA0LjQ5OTIgMCAwIDEgNi42ODAyIDQuNjZ6TTguMzA2NSAxMi44NjNsLTIuMDItMS4xNjM4YS4wODA0LjA4MDQgMCAwIDEtLjAzOC0uMDU2N1Y2LjA3NDJhNC40OTkyIDQuNDk5MiAwIDAgMSA3LjM3NTctMy40NTM3bC0uMTQyLjA4MDVMOC43MDQgNS40NTlhLjc5NDguNzk0OCAwIDAgMC0uMzkyNy42ODEzem0xLjA5NzYtMi4zNjU0bDIuNjAyLTEuNDk5OCAyLjYwNjkgMS40OTk4djIuOTk5NGwtMi41OTc0IDEuNDk5Ny0yLjYwNjctMS40OTk3WiIvPjwvc3ZnPg%3D%3D)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000?style=flat&logo=notion&logoColor=white)
![SolidWorks](https://img.shields.io/badge/SolidWorks-CC1F35?style=flat&logo=dassaultsystemes&logoColor=white)


## Contact

[![Email](https://img.shields.io/badge/Email-mmporong%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:mmporong@gmail.com)
[![LinkedIn](https://custom-icon-badges.demolab.com/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin-white&logoColor=fff)](https://www.linkedin.com/in/mmporong/)
[![hello, robot](https://img.shields.io/badge/hello%2C_robot-garden-2E7D32?style=flat-square&logo=github&logoColor=white)](https://mmporong.github.io/robotics-garden/)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=flat-square&logo=youtube&logoColor=white)](https://www.youtube.com/@hardboiledexpress940)
[![Google Play](https://img.shields.io/badge/Google_Play-4FC3F7?style=flat-square&logo=googleplay&logoColor=white)](https://play.google.com/store/apps/dev?id=7488802924019572290)

<details>
<summary>Contribution animation</summary>

![Cat Snake](https://raw.githubusercontent.com/mmporong/running-cats/main/cat-snake.gif?v=6a04031)

</details>
