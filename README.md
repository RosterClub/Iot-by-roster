Iot-by-roster

1.Finger print scanner using Raspberry pi IN CMD sudo bash

Download Necessary Packages

wget –O – http://apt.pm-codeworks.de/pm-codeworks.de.gpg | apt-key add –

wget http://apt.pm-codeworks.de/pm-codeworks.list -P /etc/apt/sources.list.d/

After installation of packages update Raspberry Pi

sudo apt-get update

sudo apt-get install python-fingerprint –yes

After installation of Libraries

Check your fingerprint sensor for the USB port connected by using the given command:

ls / dev / ttyUSB *

Now replace the USB port number with the USB port and replace it with python code. The completed Python code is given at the end of this project.

To download the python files and package files go to github and search the following url https://github.com/bastianraschke/pyfingerprint Click on clone and download to download the necessary files.

2.7 segment led to get time Go to following link to get the necessary python files

https://github.com/timwaizenegger/raspberrypi-examples/tree/master/actor-led-7segment-4numbers

3.RFID Make the following connections and run the following code to get output. import serial #import serial module

def read_rfid (): ser = serial.Serial ("/dev/ttyAMA0") #Open named port ser.baudrate = 9600 #Set baud rate to 9600 data = ser.read(12) #Read 12 characters from serial port to data ser.close () #Close port return data #Return data

id = read_rfid () #Function call print id
