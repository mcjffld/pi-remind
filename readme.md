Raspberry Pi Appointment Reminder
=================================
I often find myself missing appointments because I'm engrossed in my work or because I've switched to a different computer and can't hear the reminder ping on my work laptop. I created this project to give me a visual reminder, an obnoxious, silent countdown timer I can set on my desk to flash lights at me as a warning before my next meeting starts.

The project uses a network connected Raspberry Pi and a [Pimoroni Unicorn HAT](https://shop.pimoroni.com/collections/raspberry-pi/products/unicorn-phat) to display the reminder. The Pi will connect to Google Calendar and check periodically for upcoming appointments then display the following alerts:

* White @ 10 minutes
* Yellow @ 5 minutes
* Red @ 2 minutes

For this project, the alert is simply all LEDs in the array lit with the same color for a period. If you're adventurous, you can change the code to use any of the sample patterns included with the [Unicorn HAT Sample Code](https://github.com/pimoroni/unicorn-hat/tree/master/python/examples).

Required Components
==================
For this project, I used the following components:

+ Raspberry Pi - I used a [Raspberry Pi 2 Model B](https://www.raspberrypi.org/), but most any Pi will work. Check the Unicorn HAT documentation for supported Pi devices.
+ Power Supply - [CanaKit 5V 2.5A Raspberry Pi 3 Power Supply / Adapter / Charger (UL Listed)](http://www.amazon.com/CanaKit-Raspberry-Supply-Adapter-Charger/dp/B00MARDJZ4) from Amazon.
+ [Pimoroni Unicorn HAT](https://shop.pimoroni.com/products/unicorn-hat) from Adafruit.
+ Raspberry Pi case - [Adafruit Raspberry Pi B+ / Pi 2 / Pi 3 Case - Smoke Base - w/ Clear Top](https://www.adafruit.com/products/2258) from Adafruit.

The only required component is the Unicorn HAT as the code in this project is hand crafted for that device. Otherwise, pick whatever Raspberry Pi device, case and power supply that works best for you.

Raspberry Pi Setup
==================
To setup the hardware, complete the following steps:

+ Mount the Pimoroni Unicorn HAT on the Raspberry Pi device
+ Place the Pi in a case
+ Plug it in
+ Optionally: assign a static IP address to the Pi.

That's it, you're done. Those steps should take about 5 minutes tops. 

When the Pi is all ready to go, update the device's software using the following commands:

	sudo apt-get update
	sudo apt-get upgrade

The first command updates the local software repositories and the second command updates the Pi OS and associated files. 

Next, copy the project's Python source code to the Pi using the following command:

	curl yada yada yada

Project Setup
==================
Before you can use the project's software, you have to setup an account with Google in order to be able to execute the Google Calendar APIs used in this project. To setup your account, read the [Google Calendar API Python Quickstart](https://developers.google.com/google-apps/calendar/quickstart/python).

Place your Google Calendar API `client_secret.json` file in the project folder. You'll need it to authorize the app to access your Google Calendar.

As part of that process, you'll install the [Google Calendar API Python files](https://developers.google.com/api-client-library/python/start/installation) using the following command:

    sudo pip install --upgrade google-api-python-client

Installation
==================

Install the Unicorn HAT libraries following the instructions on the [Pimoroni web site](http://learn.pimoroni.com/tutorial/unicorn-hat/getting-started-with-unicorn-hat):
basically opening a terminal window and executing the following command:

    curl -sS get.pimoroni.com/unicornhat | bash


***

You can find information on many different topics on my [personal blog](http://www.johnwargo.com). Learn about all of my publications at [John Wargo Books](http://www.johnwargobooks.com). 