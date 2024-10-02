

          The project aim is to guarantee the flexibility of a parking garage to full and free its maximum capacity without any endangerment to time-consuming or space clashing as in dense environments it leads to social conflicts and over gas consuming which may lead to environmental and social issues. Our project functionality begin by checking the whether there is an available slot for the incoming vehicle. If there is available slot, it will enter the parking and the number of the available slots will decrease by one (or the number of the entering vehicles). If the available slots reach zero, then the parking will not allow any vehicle to enter. Unless, the vehicles inside started to leave, which will allow another vehicles to enter. The seven-segment module displays the number of the available slots according to every check in and out. 
        Since many cars nowadays, finding a parking lot is not easy sometimes. Many citizens must go through This generally frustrating and time-consuming process. In addition to parking is a daily pain, it also has a huge impact on the pollution of the land. Smart parking and smart parking sensors can be seen as part of a smart city. These smart cities are cities driven by IT infrastructure that can be used by cities to improve the quality of life of their inhabitants and improve their economic development. Being a smart city can be a good way to collect historical data in a relatively easy way. By collecting this data, cities can analyze how they can optimize processes such as parking. Because of using Smart parking, those looking for a parking space can find the parking space in the most efficient way possible, and businesses and local governments can optimize the parking space. It also makes the city more livable, safer and less crowded. Using a Smart Parking system saves a lot of time for drivers since they know where to find a vacant parking spot. The amount of time you spend while looking for a parking spot will be minimized. 
           In Section 1, we discuss the background and related work to the topic. In section 2, we give a detailed description of the project. Afterwards, we will discuss the implementation of the software architecture and coding, and the hardware features and its implementation. Lastly, we are discussing our future work and our scope for moving forward. 
 
Background and related work 
To compare our work and study its relation with other projects we must consider the main tools that is combined to reach our aim which is identify parking occupancy information to facilitate and improve parking efficiency which are, sensors, technologies, and applications that used to reach our aim. However, mostly the major tool is the sensor which will based our comparison on. 
Our main preference to our application is it depended on “LDR”, which helped us to function a stationary gate with main stationary sensors that their number will be based on the gate security logic, instead of specializing a sensor to each car like in “Ultra-sonic” based on project. And that with the help of the parallel function of a seven-segment display, which translated the situation externally to the driver to enrich his information about the parking status to help him in his decision. Illustrating our main toll position in the following comparison table, 

  	 
Detection 	 
Maintenance and Development 	 
Environmental responsivity 
 
Smart Parking  
(depend on LDR 
Sensor) 	Depend on the change of resistance as the change of the amount of it’s occupying light 	Does not need an expensive maintenance, just basic providing especially light source privacy. 	Suitable for indoors and outdoors in the terms of considering vehicles as the only effectives of the sensor light source that will not compared with human movement 
 
Smart Parking 
(depend on Infrared 
Sensor) 	Depend on  the amount of  infrared energy reflected from  any object or vehicle  	Requirement of advanced speculation and maintenance and to acquire the parking status as they should be placed in all the parking spaces  	sensitive to the change of an environment like rain or wind (not suitable to open areas) 
 
Smart Parking  
(depend on  Ultrasonic 
Sensor) 	Depend on  the amount of  a limited frequency sound waves reflected from an object or vehicle  	Available for low cost, multiple sensors connection and maintenance is expensive at the long run and To acquire the parking status, sensors will be located on all parking spaces. 	More suitable to open areas than IR but rather better in the indoors as the located ceiling may 
be sensitive to environment 
 
Specification of the project 
           The project function is to check whether there is an available slot for the incoming vehicle. If there is available slot, it will enter the parking and the number of the available slots will decrease by one (or the number of the entering vehicles). If the available slots reach zero, then the parking will not allow any vehicle to enter. Unless, the vehicles inside started to leave, which will allow another vehicles to enter. The seven-segment module displays the number of the available slots according to every check in and out. The Entrance gate has two LDR (light dependent resistor) the first one senses the vehicle and make the Arduino check if there is an available space or not. The gate opens if there is available space, the vehicle moves in, which will make it pass on the second LDR to signal the Arduino that the vehicle is already inside and we can close the gate. The Third LDR is fixed on the exit gate, which senses if there is an object in front of it, so it will open the gate to let it out. 
             We have learnt about many things in this project: firstly, Coding and managing the Arduino to get the desired input with the other components. Secondly, we have learnt how the LDR operates, which is dependent on the light. The intense light lowers the resistance; however, the less light concentration increases the resistance significantly. Thirdly, the seven segment has two types’ common anode and common cathode. In order to operate the common anode, the terminals need to read low to light the desired edges. On the other hand, the common cathode, its terminals need to read high to light the desired edges. 
 
 
 
 
 
 
 
Implementation 
Software simulation: 
Our choice to simulation software was “Proteus” due to its flexibility in importing our components and illustrating its functions and the main connections, our simulation functionality based on uploading a “hex file” our programming code to our microcontroller “Arduino Uno”, which we will talk about in software architecture and program code section.  
  ![image](https://github.com/user-attachments/assets/5b605df1-3766-449a-8022-a9842d806fe6)

  Fig1. Proteus Simulation components. 
  ![image](https://github.com/user-attachments/assets/07317769-1a81-4616-b0f1-a74d791e8c3f)

  Fig2. Proteus Simulation circuit. 
The most important components after the Arduino Uno is our three LDR sensors as they classify our process of smart parking into three main stages, 
The 1st stage is “gate opening”, 
   ![image](https://github.com/user-attachments/assets/08d593f4-0eb7-4f1e-b195-19e438fa9eb8)

As in Fig2, the 7-segment showing us that the maximum capacity is 5. Then by the passing of the first car in front of the sensor causing light change or light reducing in our cause, that will cause change in the resistance, sending signal to the Arduino causing the servo motor to rotate and open the gate 90 degree. 7-segment reducing the available spaces to 4, green light referring to a safe entering and finally an alerting buzzer. Moreover, that what is the mechanism will depend mainly on in the next two stages. 
 
 
 
 
The 2nd stage “gate closing, 
  ![image](https://github.com/user-attachments/assets/de06c39c-2603-4948-b489-e9198a81e9cc)

Car passing in front of the 2nd sensor causing light change, red led warning to gate closing, 7segment occurring that available space had been take and alerting buzzer. The 3rd stage “car leaving”, 
  ![image](https://github.com/user-attachments/assets/03b97b47-fbc2-4e9b-bc71-ac4cc77eb632)

 
Third sensor main is to confirm that there is an available space and to occur there will be no space clashes however, the parking area space was small and if there are zero space the gate will not open however there is a change of source of the light like the following figure, 
  ![image](https://github.com/user-attachments/assets/43672236-8aff-4055-9b96-5907d180e0c5)

 







The slots localization system
Depends on the digital high or low input from IR sensors using an indication output component (LED), as high input (LED is on) indicating free space and low input (LED is off) indicating that the slot is busy, having a full info about the slots state specifically before entering considering a position reference. That resulting in provide a full scalability aspect to the system.
 ![image](https://github.com/user-attachments/assets/24e3f924-2f49-41bf-a40f-aaa2e9de1af7)
![image](https://github.com/user-attachments/assets/9b2875bb-7ab7-4140-85d7-679c7c915385)

 
Hardware implementation (Architecture): 
Mainly our hardware components and its implementation based on the previous Proteus simulation as it was considered as out software testbed, so we proceeded to connections as following figures,

  
Fig3. Hardware Schematic. 
  ![image](https://github.com/user-attachments/assets/c1ddcc04-95c6-4c78-9c1f-c1d965b3e18f)
![image](https://github.com/user-attachments/assets/938de002-ddeb-44a2-9b01-66f017a7e796)

 Fig4. Hardware implementation. 
Hardware components: 

 



Prototype
 
 
Software Architecture and Program Code 
The coding algorithm begins with importing important libraries like servo library to support our motor. After that, we begin to define the Arduino pins according to our components that was illustrated in the previous Proteus simulation and defining the motor rotation angle initial position as in “motor.write(180);”, specifying that we have six cases, 0, 1, 2, 3, 4, 5. Where 0 means 1’no available spaces” and 5 is our “maximum capacity”, which is available. 
  
 
This the parts where our alerting devices functions the red, green led and the buzzer functions, as follows in the first figure is were the green led function instantly and the car go to the second process were red led function and returning to the green led function again at the exit. Buzzer functions for a very little amount of time “delay(20);” due to not cause distribution then stops. 
 
Finally, to the LDR Sensors function part of the code, for the first LDR, it goes through an if condition algorithm checks if there is a change in value if it take our variable “i”, which defined before as the value 5 and subtract an available space through “i--“ and opens the gate at 90 degree rotation. 
  
Continuing with if condition, it checks if there as value change in the second LDR it closes the gate returing the 90 degree rotation to 180 degree position “motor.write(180);”
  
Finally, with the last conditions when a car passes through the third LDR it indicates available space through “i++;” all three conditions attached with the alerting devices we discussed previously.  
 	 
 
 
 
 


A Comparison between different approaches of OCR
	
OCR Library, engine Library	
Code architecture and window interface	
Serial communication between     controller and operating system

Microsoft Visual Studio 2010 Express
	EMGU-CV is cross platform for Open CV Library.
Tesseract engine library for Text recognition.	Very flexible code flow with an easy window interface design, doesn’t give any compile errors.
Unstable functionality in running as it have run time errors.	Based on if conditions to check the availability of the serial port and connection between the code of controller and the .NET Language and based on that it will function.


 MATLAB	Self-built library, using extraction built-in function for detection and segmentation methods based on fixed sized characters templates for character matching.	Un-limited feature interface with an ease of access capable of multi-tasking, but very complicated and hard to build code architecture unlike Visual Basic.	As MATLAB have a Support Package for Arduino, you can internally communicate with your Arduino board, serial communication is a simple implantation depending on the USB wireless connection or WI-FI wireless.


Raspberry PI	Open cv library for simple detection and segmentation function for the 1st phase of the ocr and tesseract engine library for the last phase	Based on python, very clear code architecture depending on a major if condition that divides to more two if conditions control the whole flow of the image processing and I/O functions.	There is no serial communication as it’s a microcomputer the operating system and the GPIO of the inputs and outputs components work within the same device.
Microsoft visual basic OCR:
ElseIf InStr(data, "ABC1") Or InStr(data, " abc1") Or InStr(data, "Abc1") Then
            Label1.Text = "registered"
            Label2.Text = "Afaq"
            Label3.Text = "13401-6756284-2"
            Label4.Text = "HONDA 2004"
            Label5.Text = "552Cbv76676"

            CheckBox1.Checked = True

        ElseIf InStr(data, "RWP4") Or InStr(data, " RWP 4") Or InStr(data, "rwp 4") Then
            Label1.Text = "un registered"
            Label2.Text = "No record"
            Label3.Text = "No record"
            Label4.Text = "No record"
            Label5.Text = "No record"

“ABC1” plate is registered in the “if conditions” cases but “RWP4” was registered as not.

 ![image](https://github.com/user-attachments/assets/13a1a202-2e25-4bd6-b343-91fc44c71c8f)

 ![image](https://github.com/user-attachments/assets/0c8a930e-61d0-4cb7-b59c-a2da0b84fb24)

Serial communication between Arduino and Visual Basic methodology base on if conditions to check the availability of the serial port and the validity of the condition,
 Firstly, it check the validity of the checkbox as a method to control the gate and it’s linked as a true to the registered plate,
Private Sub CheckBox1_CheckChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Label1.Click
        If CheckBox1.Checked = True Then
            SerialPort1.Open()
            SerialPort1.Write("c")
            SerialPort1.Close()
        Else
            SerialPort1.Open()
            SerialPort1.Write("d")
            SerialPort1.Close()
        End If
    End Sub
Secondly, the Arduino checks the validity of the the serial port and if true it proceeds to real the serial information and then functions based on the related current condition,      
Optical Character Recognition Flow:
It’s to be referred that the process of plate recognition in the python implementation is divided considerably into two Phases,

 ![image](https://github.com/user-attachments/assets/d9c0d8b1-2d96-489e-9642-8bd9185da4cf)


The 1st phase is about recognition of a “plate” the standard rectangular shape that used in any car, which will be done manually and fully constructed depending on “OpenCV” functions of image processing. The flow of it starts directly after the start of the flow, which is the “if condition” controlling the start of capturing the frame that will be processed. Firstly starting by using a bilateral filter to remove the unwanted details and canny edge method to preform edge detection,
if key == ord("s"):
             gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY) #convert to grey scale
             gray = cv2.bilateralFilter(gray, 11, 17, 17) #Blur to reduce noise
             edged = cv2.Canny(gray, 30, 200) #Perform Edge detection


 Secondly preforming Image Classification by finding multiple contours and filter the license plate contour by searching for a rectangle shape contour with four sides and a closed figure,
  for c in cnts:
                peri = cv2.arcLength(c, True)
                approx = cv2.approxPolyDP(c, 0.018 * peri, True)
                if len(approx) == 4:
                  screenCnt = approx
                  break
Object Localization by finding the license plate and mask everything except it,
mask = np.zeros(gray.shape,np.uint8)
new_image = cv2.drawContours(mask,[screenCnt],0,255,-1,)
new_image = cv2.bitwise_and(image,image,mask=mask)
The two main process of the 2nd step in the flow represents and results of the 3rd step which is Object Detection, as we have achieved to recognize a plate from the whole frame.
Finally, the 4th step in the flow which is Image Segmentation as after masking the entire frame except the license plate area, it will be cropped and saved as a new image,
(x, y) = np.where(mask == 255)
             (topx, topy) = (np.min(x), np.min(y))
             (bottomx, bottomy) = (np.max(x), np.max(y))
             Cropped = gray[topx:bottomx+1, topy:bottomy+1]
The 2nd phase is mainly about depending on tesseract library to read the characters from the license plate image and store the recognized characters in the ‘text’ variable. There is also an IoT extension, which is responsible for sending the detected plate number to your mail using Simple Mail Transfer Protocol (SMTP)



Evaluation & Conclusion 
      The project is implemented and functioning+ mainly as it was planned. The LDR conditions for the light are sometimes not working properly. Moreover, sometimes it has delay issues, and the vehicle has to wait. Moreover, the OCR sometimes read garbage value depending on image orientation and quality, rather than that everything is working perfectly fine with each other. The Arduino is taking the readings from the LDRs, and based on it takes the required actions from changing or keeping the reading on the seven segment. Moreover, it signals to the servomotor, which is the gate mechanism, to open and close depending on these readings. 
 
 
KPI Name 	 
Description (What?) 	 
Relevance (Why?) 	 
Methodology (How?) 
 
Efficiency of the use of parking spaces 	This KPI measures the usage of parking spaces, in order to evaluate which parking areas are more flexible and demanded by clients. 	This measurement can help to re-determine the order and the function of the processes of parking, as its target the family’s home and the ease of their accessibility. 	By access to the parking occupation information regarding the exact time of a day or an hour which the value of measurements highly depends on. 
 
Service management satisfaction 	This indicator aim is to evaluate the satisfaction level using the technical 
Staff that are responsible of the management parking area. 	Due to the reliability of the information provided by the sensors deployed, as it is not defined by human error and the variability of it can be controlled. 	The methodology depends on discussions with the responsible for reviewing the flow of process, like technicians and parking, security of areas. Who observes and states the degree of achievement improvement by of the technologies in its tasks and the relation with human methods to perform similar tasks. 
Table1. Smart parking key performance indicators evaluated. 
	 
Future Works 
We have learned the validation of smart city concept and its facilities especially the smart parking project and the importance of the concept micro-controllers in our educational project and the development of the concept of controlled gates and mainly controlled civilian projects depended on smart system concepts in modern era and cities development. However, we are satisfied with concept of our project; we may look forward to develop a security dependent system in the process of opening and closing the gates to provide a controlled privacy to the parking area owners. We will look forward to add a LCD display as an advanced display for the indicator instead of constant number of leds to expand a wide range of scalability varying between different floors or even connecting different parking locations and different parking slots. Creating a wider range of database to be capable of knowing info of different parking locations far from you using an IoT concept.
 
 
 
 
 
 
 
 
 
 


References 
[1]	Lanza, J., Sánchez, L., Gutiérrez, V., Galache, J., Santana, J., Sotres, P., & Muñoz, L. (2016). Smart City 
Services over a Future Internet Platform Based on Internet of Things and Cloud: The Smart Parking 
Case. Energies, 9(9), 719. 

[2]	Alam, M.(2018). Real-Time Smart Parking Systems Integration in Distributed ITS for Smart 
Cities. Pisa, Italy: Institute of Information Science and Technologies 

[3]	Khanna, A.(2016). IoT based Smart Parking System. Pune: Conference: International 
Conference on Internet of Things and Applications 

[4]	Smart parking sensors, technologies and applications for open parking lots: a review. (n.d.). https://ietresearch.onlinelibrary.wiley.com/doi/epdf/10.1049/iet-its.2017.0406 

[5]	Revathi, G. (2012). Smart parking systems and sensors. Dindigul, India: IEEE 

[6]	Yamani,M.(2009). Car Park System: A Review of Smart Parking System and its Technology. Information Technology Journal 
 .  
 
