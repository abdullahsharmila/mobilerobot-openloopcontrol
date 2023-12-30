# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1: import time  and necessary libraries

<br/>

Step2:Depends one the size of the track place  the robot in the centre

<br/>

Step3:X moves forwar,-X moves Backward

<br/>

Step4:Y moves moves right wise,-Y moves left wise

<br/>

Step5:Z rotates to the angle we need,-Z rotates to reverse angle we need

<br/>
step 6:apply all the necessary x,y and z values use trial and error method make the robot move in the complete track

## Program
```python
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0.5, y=0, z=80, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=255,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=-1.6, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

   
    ep_chassis.move(x=0, y=0, z=55, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x=1.4, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")
    
    ep_chassis.move(x=0, y=0, z=45, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
    
    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")
    
    ep_chassis.move(x=0, y=0, z=95, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=192,effect="on")

    ep_chassis.move(x=2.1, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=102,g=0,b=204,effect="on")

    ep_chassis.move(x=0, y=0, z=83, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=204,effect="on")


    ep_chassis.move(x=0.8, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()



    
    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Insert image here


<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

[![IMAGE ALT TEXT HERE]https://youtu.be/8opPA__Ks38?si=e9Gdllm7RSzQDVoH

<br/>
<br/>
<br/>
<br/>

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
