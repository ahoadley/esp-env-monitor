# esp-env-monitor

ESP8266-based temp and light monitor used in Exosite's Minneapolis office.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Overview
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
This is a project that demonstrates how to do two-way secure communications 
with Exosite using the Sparkfun ESP8266 Thing Dev.  This project is used on 
around 50 Thing Dev systems at the Exosite Minneapolis office to monitor 
temperature through-out the office.  The User Interface used by multiple 
team members and groups is the Remote Condition Monitoring system - Exosite's 
leading application for IIoT network operations center and field service 
enablement efforts.

License is BSD, Copyright 2018, Exosite LLC (see LICENSE file)

Arduino code: Built/tested with Arduino 1.8.5.
Requires: Exosite Arduino library, Sparkfun ESP8266 Thing Dev Board Support

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Quick Start
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Install Arduino
  * https://www.arduino.cc/en/Main/Software

* Install Libraries
  * The Exosite Arduino library can be installed from within the Arduino tool
    at Sketch->Include Library->Manage Libraries...
  * Support for the Sparkfun ESP8266 Thing Dev board can be installed from 
    within the Arduino tool at Tools->Board:"NN"->Boards Manager...

* Create an Exosite account
  * Go to https://exosite.io and sign up!

* Create & Configure a Murano Product
  * From within Murano, go to your Solutions page and Create Solution -> choose 
    Product Type and "Start from Scratch"
  * Go to your Product's Settings page and choose "HTTP API" under Protocol, 
    "Opaque" under Identity, and check "Enable Provisioning" and "Allow devices
    to register their own identity" under "Provisioning"

* Copy your Product ID from Murano and update your Arduino code
  * Click on the "ID" icon in the upper left to copy the Product ID to your 
    clipboard and paste it over the value that says "PUTPRODUCTIDHERE"

* Configure your WiFi parmaters
  * Set the WiFi SSID by replacing "PUTWIFISSIDHERE" with the SSID, and set the
    WiFi Passphrase by replacing "PUTWIFIPASSPHRASEHERE" with the passphrase
    
* Upload the firmware and start communicating!
  * Plug your Sparkfun Thing Dev board into a USB cable and program from the
    Arduino tool
  * If you have all the settings correct, the board will start flowing data to
    your Murano account.  If you pull up your Product's "Devices" page, you'll
    see a list of devices you have provisioned under the Product - since you
    just created the Product, you'll either see none, or your new device listed
    there.  If you don't see your device yet, you can wait around to see if it
    will appear, or you can debug.
  * To debug, pull up the Arduino Serial Monitor and read the messages to see
    where you are getting stuck.  Could be WiFi settings, could be Product ID, 
    could be your router won't let the traffic through.  You can also open the
    "Logs" page under your Product area in Murano.  The Logs will show all
    valid communications with any device in your Product.
  
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
More Information
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Exosite Documentation -> https://docs.exosite.com

* More about RCM -> https://exosite.com/iot-solutions/condition-monitoring/

* For support, email: support@exosite.com (reference the github project, etc)
  * Web: https://support.exosite.com (forums, knowledge base, ticket system)
