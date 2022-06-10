# FANUCRobot-Docs
Project Documentation and User's Guide for the FANUC Robot Project in Unity.

## Description
The latest Unity Project for the FANUC 2000iC robot contains 2 main scripts inside the "InteractiveRobot/RobotIKOptimized" folder<br />
Compared to the previous versions. The logic for the movement of the robot uses an in-house solution for the IK manager and the scripts can be instanciated several times <br />
The Robot can be move through FK or IK directions but all the joints have a rotation limit. <br />
While there are some extra functionalities added to this version, some of the robot functionalities have been deprecated from the previous one <br />

## Sections
  [Robot Joint](#robot-joint) <br />
  [IK Manager](#ik-manager) <br />

## Classes and Methods

### Robot Joint

|__Variables__|__Type__|__Default Value__|__Description__|
|:---|---|---|---:|
|Axis|Vector3|NA| axis of rotation for the joint |
|StartOffset|Vector3|NA| degrees of rotation of the joint|
|MinAngle|float|NA| min angle rotation|
|MaxAngle|float|NA| max angle rotation |
|current|float| 0 | current angle of rotation|
|motion|float| 1.2f | velocity of the motion of the robot|
|speed|float| 0.35f | speed of the robot|
|testjointP|bool| false | moves the robot in the positive degree (use only for testing purposes)|
|testjointN|bool| false | moves the robot in the negative degree (use only for testing purposes)|
|stopRobotTemporarily|bool| false |limits the movement of the robot when colliding|
|robotTip|GameObject| robotTip | game object that references the last joint of the robot|
|RobotTipColliding|class| robotTipDetection | class reference to robotTipDetection|
|PositiveJointBool|bool| false | moves the robot in the positive degree (only accessible through buttons)|
|NegativeJointBool|bool| false | moves the robot in the negative degree (only accessible through buttons)|



|__Class__|__Method__|__Description__|__Key__|
|:---|---|---|---:|
|RobotJoint|getEuler()|returns a Vector3 with the local rotation of the joint| NA |
|FirstJoint|RotatePositiveX_Joint1()|rotates first joint in positive x axis by adding a float number (motion * speed) to the current x position| A |
|FirstJoint|RotateNegativeX_Joint1()|rotates first joint in negative x axis by substracting a float number (motion * speed) to the current x position| D |
|FirstJoint|setSpeed(float)|sets the speed of the movement of the joint. It is controlled through the ScriptController| NA |
|FirstJoint|getCurrentJoint1()|returns the local rotation of the Joint | NA |
|FirstJoint|setCurrent(float)|sets the current value for the joint rotation (it is useful to reset the value when changing from IK to FK)| I |

the local rotation of the Joint | NA |

### IK Manager
|__Variables__|__Type__|__Default Value__|__Description__|
|:---|---|---|---:|
|TargetTransform|Transform| NA | reference to the transform values of the IK target |
|Joints|RobotJoint[]|NA| list of joints (gameobjects using the robot joint sript) |
|Angles|float[]| NA | list of angles of all the joints of the robot|
|SamplingDistance|float| 5f | distance sample for the grdient  |
|LearningRate|float| 100f | rate of tries that the system will use to get to the location |
|DistanceThreshold|float|  0.0001f | Distance at which the IK system will stop |
|IKToggle|bool| NA | switches between IK and FK systems |
|JointsSpeed|float| 0.35f | speed of the joints |
|SetIKSwitchVar|bool| false | sllows the Robot to switch to IK  |
|SetSpeedUPVar|bool| false | increases the speed of all the joints in FK |
|SetSpeedDOWNVar|bool|  false | decreases the speed of all the joints in FK |
|stopRobotTemporarily|bool| false |limits the movement of the robot when colliding|
|robotTip|GameObject| robotTip | game object that references the last joint of the robot|
|RobotTipColliding|class| robotTipDetection | class reference to robotTipDetection|
|SafetyButtonEnabbled|bool| false | if true disables all the functionalities of the robot |
#### Unity Events
|__Variables__|__Type__|__Default Value__|__Description__|
|:---|---|---|---:|
|IKToggleRobot|UnityEvent| NA | Event for IK Toggle|
|AddJointsScSpeed|UnityEvent| NA | Event For Increasing Speed|
|SubsJointsScSpeed|UnityEvent| NA | Event For Decreasing Speed |

|__Class__|__Method__|__Description__|__Key__|
|:---|---|---|---:|
|InteractableObject|OnCollisionEnter(Collision)|checks if the object is colliding by both sides| NA |
|InteractableObject|OnCollisionExit(Collision)|checks if the object is still colliding by both sides | NA |
|InteractableObject|OnTriggerExit(Collider)|sets TriggerI = false | NA |
|InteractableObject|getTriggerStatus()|returns status of the trigger| NA |

# List of errors (x means solved)
- [x] Picking multiple objects
- [x] Project not working on 2020.17 unity version
- [x] Not able to change speed of IK Target
- [ ] Storing "picking up" method inside log.txt
- [x] Picked object does not follow robot's movement
  
 # Log
  Documentation for Robot V2 created (06/10/2022)<br />
  
[Link to Documenation for Robot V1](https://github.com/Klaimtrev/RobotFanuc)

