# Milton Static's Robot Documentation
This is a special guide, simplified to make coding the  
Milton High School's Robot a much easier task
---

---

First of all, we use a programming language called **Java**  
For those who care to know, Java is an object-oriented, statically-typed language.

Some basic rules for Java include always ending your code lines with semicolons, and always naming the type of you variables when creating them.

When programming this robot, there are some basic things you need to do.  
You need to use and make **Variables** and **Functions**.    
- **Variables** are used to represent motors, servos, and sensors on the robot.  
- **Functions** do things for the robot like controlling motors, servos and giving info on sensors.

---

The robot is controlled using different **opmodes**. These are **Java classes** that act as the blueprint for controlling the robot.  These opmodes are put together into an Android app that then is installed on a set of phones.  Two phones communicate with each other, one on the robot which we install and modify, and one phone with a driver who uses it to control the robot phone.

Each opmode has a set template which we programmers simply fill in.    
There are three sections, the **Variable Section**, the **Initialization Section**, and the **Loop Section**.  Each section represents a stage of the robot's control cycle. Variable Section is when the opmode is first chosen on the phones to use.  Then the robot is Initialized, starting its robot parts. Finally, the robot begins to run and loop a set of commands controlled by a game controller (we have those).

`//Variable Section`  
`DcMotor motorLeft;`  
`DcMotor motorRight;`  
`Servo servoArm;`  
`double motorPower = 0.55;`  
`boolean onTheGround = True;`

The **Variable Section** is where we define the variables (obviously). Variables can be devices on the robot, or they can store information, like a decimal value or a true/false.

`public static void init(){`  
`   motorLeft = hardwareMap.dcmotor.get("motor_1");`  
`   servoArm = hardwareMap.servo.get("bob");`  
`   onTheGround = False;`  
`}`   

The **Initialization Section** is a set of functions that the robot executes when it initializes.  This phase lets the robot activate its hardware - Motors, Servos, or Sensors.  You can also set other variables to store data at the beginning, numerical or boolean (true/false).

`public static void loop(){`  
`   servoArm.setPosition(0.33);`  
`   if(gamepad1.left_stick_y);`  
`       motorRight.setPower(motorPower);`
`}`

The **Loop Section** is a set of functions that will run continuously as part of controlling the bot.  Functions exist to set the power of motors, the position of servos, or to retrieve the data from sensors.  One can change or use other variables that store data as well.