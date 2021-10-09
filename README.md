# OAIAR_projetNAO
This repo contains the WIP python script that makes a humanoid robot NAO to detect an orange ball, move towards it and pick it up.

## Brief
We implemented a navigation and grasping system for the humanoid robot NAO which was then able to locate an orange ping pong ball, navigate to and pick it up. The system used visual information acquired from its 2 cameras to firstly estimate the ball’s position with respect to the robot’s frame and then to navigate towards the orange ball. The navigation system accounted for a scenario where the ball was not within the humanoid robot’s visual range. When the ball was not detected, the robot rotated 180 degrees and check whether the ball was in its visual range. If the ball was not in its range after a rotation on itself, it would proceed to move around 10 steps forward and scan its environment for the orange ball. The main goals of this project were:  
* Make Nao detect an orange ping pong ball.
* Make Nao move towards the ball.
* Make Nao pick up the ball.

## Installation of naoqi
A guide is available at https://developer.softbankrobotics.com/nao6/naoqi-developer-guide/sdks/python-sdk/python-sdk-installation-guide.
1. Install naoqi
To install naoqi SDK, head over to https://developer.softbankrobotics.com/ and download and extract the relevant files.
2. Ensure that the PYTHONPATH is set to the extracted folder. 
3. Test if naoqi libraries are available by launching a terminal and typing the following:

```
$ python
$ import naoqi
```
## Run the script
Ensure the correct IP address is set for NAO on line 9 of the script. It is currently set to 11.0.0.24.  
In a terminal, run 
```
$ python nao.py
```
