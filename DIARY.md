# 12.09.25
<p>Created the Github Repo. Nothing else really.<br>
I am really excited to start adding some stuff to the repo and setting everthing up tomorrow!<br>
The plan is to write both code for the PC application (Windows for now) and the microcontroller that reads the imu data.<br>
I plan on creating the PC application with QT and QML/Widgets (not really sure how any of that works yet lol) and and the code for the microcontroller with the Arduino IDE since they support ESP chips hehe.<br>
Also, I was thinking of documenting how all the different phyisical components are to be wired together so people can recreate everything here. Not sure how to do that yet.</p>

<p>This seems to be a lot of different things to fit into a single repo so I might decide to split this up into multiple repos down the road depending on how messy it gets lol.<br>
The most important thing for me to do now before I start coding without a plan is.. to make a plan on what I need to tackle first and on what problems there are that I have to solve.<br>
Issues like, how do I get my IMU data from the microcontroller to my QT application and such (im thinking raw sockets and udp over wifi but honestly no clue).<br>
Also I wanna draw one of those fancy kindof diagrams that depict all your components and how they interact with each other (dont know the name lol)<br>
So the first step in this coding project is to establish a connection between the microcontroller and the QT application (It sounds so easy but I feel like its not)</p>

<br>Good night lol

# 14.09.25
<p>A few updates to my initial thoughts on how to transfer the IMU data from the microcontroller to my PC application: I will not be using raw sockets lol. I think they are something else entirely and I just thought they were something else.<br>
I will be doing normal socket programming and the udp protocoll since it makees the most sense for this application. I dont need the congestion controll and retransmission of lost packages with my continious stream of IMU data so UDP is the way to go.<br>
My first concrete plan is now to establish a connection between the microcontroller and the QT PC application. I might use a button with the microcontoller to test the connection to the applicaiton.<br></p>

<p>Since I keep talking about "the microcontroller" and "the IMU" I should probablt thing about what specific components to use.<br>
Since the only IMU's I own are the BMI160 by Bosch which features a gyroscope and an accelerometer.<br>
For the microcontroller I am faced with two options: 
-The first one is the standard ESP32 development board which is a rather large board for the simple task of sending IMU data over a socket connection.
-The second one is a the Wemos D1 Mini board which is based on an ESP8266 which is signifficantly smaller.
Both have wifi functionallity which I need for the socket communication and since this is gonna be a small handheld device when its done, I'll be going with the D1 mini.<br>
I havent gotten to do a lot of research on this project yet but I'll be looking into the datasheets of both the IMU and the microcontroller to figure out how to connect them and also into socket programming and the User Datagram Protocoll</p>
