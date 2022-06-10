# FANUCRobot-Docs
Project Documentation and User's Guide for the FANUC Robot Project in Unity.

## Description
The latest Unity Project for the FANUC 2000iC robot contains 2 main scripts inside the "InteractiveRobot/RobotIKOptimized" folder<br />
Compared to the previous versions. The logic for the movement of the robot uses an in-house solution for the IK manager and the scripts can be instanciated several times <br />
The Robot can be move through FK or IK directions but all the joints have a rotation limit. <br />
While there are some extra functionalities added to this version, some of the robot functionalities have been deprecated from the previous one <br />

## Sections
  [Robot Joint](#robot-joint) <br />
  [Second Joint](#second-joint) <br />
  [Third Joint](#third-joint) <br />
  [Fourth Joint](#fourth-joint) <br />
  [Fifth Joint](#fifth-joint) <br />
  [Sixth Joint](#sixth-joint) <br />
  [Interactable Object](#interactable-object) <br />
  [Scripts Controller](#scripts-controller) <br />
   <br />
   [GrabTool (Top)](#Grab-Tool-Top) <br />
   [GrabTool (Bottom)](#Grab-Tool-Top) <br />

## Classes and Methods

### Robot Joint

|__Variables__|__Type__|__Default Value__|__Description__|
|:---|---|---|---:|
|Axis|Vector3|NA| axis of rotation for the joint |
|StartOffset|Vector3|NA| degrees of rotation of the joint|
|MinAngle|float|0| current rotation degree|
|MaxAngle|float|0.1f| degree movement value |
|speed|float|1.0f | speed of rotation|

|__Class__|__Method__|__Description__|__Key__|
|:---|---|---|---:|
|RobotJoint|getEuler()|returns a Vector3 with the local rotation of the joint| NA |
|FirstJoint|RotatePositiveX_Joint1()|rotates first joint in positive x axis by adding a float number (motion * speed) to the current x position| A |
|FirstJoint|RotateNegativeX_Joint1()|rotates first joint in negative x axis by substracting a float number (motion * speed) to the current x position| D |
|FirstJoint|setSpeed(float)|sets the speed of the movement of the joint. It is controlled through the ScriptController| NA |
|FirstJoint|getCurrentJoint1()|returns the local rotation of the Joint | NA |
|FirstJoint|setCurrent(float)|sets the current value for the joint rotation (it is useful to reset the value when changing from IK to FK)| I |

### Second Joint
|__Variables__|__Type__|__Default Value__|__Description__|
|:---|---|---|---:|
|max|float|76| maximum rotation degree |
|min|float|-60| minimum rotation degree|
|current|float|0| current rotation degree|
|motion|float|0.1f| degree movement value |
|speed|float|1.0f | speed of rotation|

|__Class__|__Method__|__Description__|__Key__|
|:---|---|---|---:|
|SecondJoint|getEuler()|returns a Vector3 with the local rotation of the joint| NA |
|SecondJoint|RotatePositiveY_Joint2()|rotates first joint in positive Y axis by adding a float number (motion * speed) to the current x position| W |
|SecondJoint|RotateNegativeY_Joint2()|rotates first joint in negative Y axis by substracting a float number (motion * speed) to the current x position| S |
|SecondJoint|setSpeed(float)|sets the speed of the movement of the joint. It is controlled through the ScriptController| NA |
|SecondJoint|getCurrentJoint2()|returns the local rotation of the Joint | NA |
|SecondJoint|setCurrent(float)|sets the current value for the joint rotation (it is useful to reset the value when changing from IK to FK)| I |

### Third Joint
|__Variables__|__Type__|__Default Value__|__Description__|
|:---|---|---|---:|
|max|float|40| maximum rotation degree |
|min|float|-60| minimum rotation degree|
|current|float|0| current rotation degree|
|motion|float|0.1f| degree movement value |
|speed|float|1.0f | speed of rotation|

|__Class__|__Method__|__Description__|__Key__|
|:---|---|---|---:|
|ThirdJoint|getEuler()|returns a Vector3 with the local rotation of the joint| NA |
|ThirdJoint|RotatePositiveX_Joint3()|rotates first joint in positive X axis by adding a float number (motion * speed) to the current x position| Z |
|ThirdJoint|RotateNegativeX_Joint3()|rotates first joint in negative X axis by substracting a float number (motion * speed) to the current x position| C |
|ThirdJoint|setSpeed(float)|sets the speed of the movement of the joint. It is controlled through the ScriptController| x|
|ThirdJoint|getCurrentJoint3()|returns the local rotation of the Joint | NA |
|ThirdJoint|setCurrent(float)|sets the current value for the joint rotation (it is useful to reset the value when changing from IK to FK)| I |

### Fourth Joint
|__Variables__|__Type__|__Default Value__|__Description__|
|:---|---|---|---:|
|max|float|360| maximum rotation degree |
|min|float|360| minimum rotation degree|
|current|float|0| current rotation degree|
|motion|float|0.1f| degree movement value |
|speed|float|1.0f | speed of rotation|

|__Class__|__Method__|__Description__|__Key__|
|:---|---|---|---:|
|FourthJoint|getEuler()|returns a Vector3 with the local rotation of the joint| NA |
|FourthJoint|RotatePositiveX_Joint4()|rotates first joint in positive X axis by adding a float number (motion * speed) to the current x position| Q |
|FourthJoint|RotateNegativeX_Joint4()|rotates first joint in negative X axis by substracting a float number (motion * speed) to the current x position| E |
|FourthJoint|setSpeed(float)|sets the speed of the movement of the joint. It is controlled through the ScriptController| NA |
|FourthJoint|getCurrentJoint4()|returns the local rotation of the Joint | NA |
|FourthJoint|setCurrent(float)|sets the current value for the joint rotation (it is useful to reset the value when changing from IK to FK)| I |

### Fifth Joint
|__Variables__|__Type__|__Default Value__|__Description__|
|:---|---|---|---:|
|max|float|125| maximum rotation degree |
|min|float|-125| minimum rotation degree|
|current|float|0| current rotation degree|
|motion|float|0.1f| degree movement value |
|speed|float|1.0f | speed of rotation|

|__Class__|__Method__|__Description__|__Key__|
|:---|---|---|---:|
|FifthJoint|getEuler()|returns a Vector3 with the local rotation of the joint| NA |
|FifthJoint|RotatePositiveY_Joint5()|rotates first joint in positive Y axis by adding a float number (motion * speed) to the current x position| UP (arrow_key) |
|FifthJoint|RotateNegativeY_Joint5()|rotates first joint in negative Y axis by substracting a float number (motion * speed) to the current x position| Down (arrow_ key) |
|FifthJoint|setSpeed(float)|sets the speed of the movement of the joint. It is controlled through the ScriptController| NA |
|FifthJoint|getCurrentJoint5()|returns the local rotation of the Joint | NA |
|FifthJoint|setCurrent(float)|sets the current value for the joint rotation (it is useful to reset the value when changing from IK to FK)| I |

### Sixth Joint
|__Variables__|__Type__|__Default Value__|__Description__|
|:---|---|---|---:|
|max|float|360| maximum rotation degree |
|min|float|-360| minimum rotation degree|
|current|float|0| current rotation degree|
|motion|float|0.1f| degree movement value |
|speed|float|1.0f | speed of rotation|
|pickObject|bool|false| picked up object |

|__Class__|__Method__|__Description__|__Key__|
|:---|---|---|---:|
|SixthJoint|getEuler()|returns a Vector3 with the local rotation of the joint| NA |
|SixthJoint|RotatePositiveX_Joint6()|rotates first joint in positive X axis by adding a float number (motion * speed) to the current x position| UP (arrow_key) |
|SixthJoint|RotateNegativeX_Joint6()|rotates first joint in negative X axis by substracting a float number (motion * speed) to the current x position| Down (arrow_ key) |
|SixthJoint|setSpeed(float)|sets the speed of the movement of the joint. It is controlled through the ScriptController| NA |
|SixthJoint|getCurrentJoint6()|returns the local rotation of the Joint | NA |

### Interactable Object
|__Variables__|__Type__|__Default Value__|__Description__|
|:---|---|---|---:|
|rb|Rigidbody| NA | self rigidbody |
|TriggerI|bool|false| boolean to know if it picked an object|
|SixthJoint|SixthJoint| NA | reference to sixth joint script|
|boxcollider|BoxCollider| NA | reference to collider |
|Joint6RB|Rigidbody| NA | reference to sixth joint rigidbody|
|grabtooltop|GrabToolTop| NA | reference to grabtooltop script |
|grabtoolbottom|GrabToolBottom| NA | reference to grabtoolbottom script |

|__Class__|__Method__|__Description__|__Key__|
|:---|---|---|---:|
|InteractableObject|OnCollisionEnter(Collision)|checks if the object is colliding by both sides| NA |
|InteractableObject|OnCollisionExit(Collision)|checks if the object is still colliding by both sides | NA |
|InteractableObject|OnTriggerExit(Collider)|sets TriggerI = false | NA |
|InteractableObject|getTriggerStatus()|returns status of the trigger| NA |

### Scripts Controller
|__Variables__|__Type__|__Default Value__|__Description__|
|:---|---|---|---:|
|RecordNumber|int|0| Number of the first line where the reader will get the coordinates from|
|joint1R|float| NA | float value where the rotation of the joint will be stored|
|joint2R|float| NA | float value where the rotation of the joint will be stored|
|joint3R|float| NA | float value where the rotation of the joint will be stored|
|joint4R|float| NA | float value where the rotation of the joint will be stored|
|joint5R|float| NA | float value where the rotation of the joint will be stored|
|joint6R|float| NA | float value where the rotation of the joint will be stored|
|pickUpObj|bool| NA | boolean that indicates wether an object was picked up or not|
|StringLength|int| NA | length of the coordinates |
|speed|float|1.0f | speed of rotation|
|lastStep|float| NA | stores the time between lastStep (used for shift key)|
|timeBetweenSteps|float| 0.1f| indicates the time to count before it accepts the same input again (used for shift key)|
|list1|List<string>| NA| List to store all the coordinates extracted from log.txt|
|firstJoint|FirstJoint| NA| Gets a reference to the First Joint Script|
|secondJoint|SecondJoint| NA| Gets a reference to the Second Joint Script|
|thirdJoint|ThirdJoint| NA| Gets a reference to the Third Joint Script|
|fourthJoint|FourthJoint| NA| Gets a reference to the Fourth Joint Script|
|fifthJoint|FifthJoint| NA| Gets a reference to the Fifth Joint Script|
|sixthJoint|SixthJoint| NA| Gets a reference to the Sixth Joint Script|
|Joint1Object|GameObject| NA| Gets a reference to the first Joint|
|Box|GameObject| NA| Gets a reference to the object|
|Target|GameObject| NA| Gets a reference to the Target for the IK|
|IKtoggle|bool| true| A boolean used to check and turn off/on IK|

|__Class__|__Method__|__Description__|__Key__|
|:---|---|---|---:|
|ScriptsController|createPositionRecord()|records the local rotation of all the joints| NA |
|ScriptsController|CreateText()|creates the log.txt file if it does not exists| U |
|ScriptsController|ReadString()|reads log.txt and adds every line to the list1| X|
|ScriptsController|IncreaseSpeed()|increases the speed of all joints of the robot| SHIFT |
|ScriptsController|DecreseSpeed()|decreases the speed of all joints of the robot| CTRL |
|ScriptsController|findIndex(char, string)|finds the index of # from list1 and returns an int[] with the locations of all of them | NA |
|ScriptsController|loadMovementRecord(int)|loads the coordinates for each joint based on list1 and findIndex| L |
|ScriptsController|rotateUntilReachPoint()|rotates each one of the joints until reaching the coordinates from list1| M |
|ScriptsController|toggleIK()|changes the IKtoggle value| I |

### Grab Tool Top

|__Variables__|__Type__|__Default Value__|__Description__|
|:---|---|---|---:|
|limitTranslation|float|185|limit translation point |
|currentTranslation|float|0| current translation point|
|move|bool|true| being able to move|

|__Class__|__Method__|__Description__|__Key__|
|:---|---|---|---:|
|GrabToolTop|localPosition()|returns a Vector3 with the local position of the grab tool at the top| NA |
|GrabToolTop|setMove()|Moves the tool until reach position| P |
  
### Grab Tool Bottom

|__Variables__|__Type__|__Default Value__|__Description__|
|:---|---|---|---:|
|limitTranslation|float|185|limit translation point |
|currentTranslation|float|0| current translation point|
|move|bool|true| being able to move|

|__Class__|__Method__|__Description__|__Key__|
|:---|---|---|---:|
|GrabToolTop|localPosition()|returns a Vector3 with the local position of the grab tool at the top| NA |
|GrabToolTop|setMove()|Moves the tool until reach position| P |
  
# List of errors (x means solved)
- [x] Picking multiple objects
- [x] Project not working on 2020.17 unity version
- [x] Not able to change speed of IK Target
- [ ] Storing "picking up" method inside log.txt
- [x] Picked object does not follow robot's movement
  
 # Log
  Documentation for Robot V2 created (06/10/2022)

