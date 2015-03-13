# /!\ Robotis Dynamixel Noobs Traps

When you want to assemble a Poppy, the first thing to do is to ensure yourself **you assembled correctly the horn on the Dynamixel motors**. This is both the first step and maybe the most critical one. An error in the configuration or assembly here is really boring to change once a Poppy creature is assembled.

## 1. Fix the horn on the motor
**Warning! This step is critical!**

Dynamixel motors are sold unassembled, you have to add manually the horn HN07-N101 (for MX-28) and HN05-N102 (for MX-64).
The critical aspect is to put the horn correctly on the zero position. To do that, you have to correctly align the awl mark on the Dynamixel shaft and the snick on the horn:

<img src="../img/robotis_dynamixel_axe_mark.jpg" height="300"> <img src="../img/robotis_horn_mark.jpg" height="300">

When assembled, the horn is really difficult to remove and you will probably damage the motor, so check twice or thrice !

Also, it is pretty hard to push the horn on the shaft, you will probably have to use the screw (M2.5x8mm) and tighten it to correctly assemble the two elements.


## 2. Motor configuration
When you take out the motor out of its box, its internal id is 1. So before plug it on the communication bus you have to configure it. Otherwise you will have problems such as experimented in this [topic](https://forum.poppy-project.org/t/dynamixel-first-uses/91/5).

You have 3 parameters to tune:

 1. the **id must match our [convention][1]**
 2. the **baudrate** have to be **set to 1 000 000bps** instead of 57142bps
 3. the **return delay time** have to be set to **0 ms** instead of 0.5 ms

To tune these parameters you can either use the [Dynamixel Wizard][2] (windows) or [Herborist][3] (Unix/Windows).
<a class="attachment" href="http://www.robotis.com/xe/download_en/657775">RoboPlus v1.1.1.0 </a>

If you are using [USB2AX dongles][4] under windows, you will need to install it manually using the <a class="attachment" href="https://github.com/Xevel/usb2ax/raw/master/firmware/lufa_usb2ax/USB2AX.inf">USB2AX.inf</a> (2 KB) file.
For more info about the installation procedure, please consult the [QuickStart guide][5].


  [1]: https://forum.poppy-project.org/t/assembly-instructions-motor-naming-convention-and-configuration/87
  [2]: http://support.robotis.com/en/software/roboplus/dynamixel_monitor/quickstart/dynamixel_monitor_connection.htm
  [3]: http://poppy-project.github.io/pypot/herborist.html
  [4]: http://www.xevelabs.com/doku.php?id=product:usb2ax:usb2ax
  [5]: http://www.xevelabs.com/doku.php?id=product:usb2ax:quickstart
