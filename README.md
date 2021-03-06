# WhatsApp Tracker

## Introduction
The aim of this project is to track WhatsApp users' behavioral patterns by analyzing the time they are online using WhatsApp.

## How does this work
Unlike other services, WhatsApp does not provide any API to access and play with users data. This makes it relatively hard to create bots, track users and automate WhatsApp. It is hard but that does not mean it is impossible.

I am just scraping the screen pointing to the WhatsApp web interface and using OCR to check if the user is online. If it can read the user is online, it stores it to the database and we can plot it using any plotting tool and analyze the users behaviour.

So, for this to work, you may have to adjust the screen capturing coordinates according to your screen resolution and the browser position. This is a tricky part as you need to tune it everytime you setup. But if you are using a dedicated machine (I am planning to use my RaspberryPI), this should not be a problem as it will be a one time setup.

## What is it useful for?
It depends upon how you use it but once you grab the data, you will start finding a way to use that.
Let me warn you not to use this to invade anyone's privacy and use it in your legal limits. I am not resposible for how you use it.

## Limitations
- Each instance can track only single user at a time
- Each instance needs a WhatsApp Web Interface or Android VM with WhatsApp
- Screen capture solution is used and so it needs to be configured for different resolutions

## Windows Preconditions
 - Install Tesseract for Windows and add to PATH env (https://github.com/UB-Mannheim/tesseract/wiki)
 - Install Python environment (3.8.1 tested here) and pip install missing modules (image, pyscreenshot, pytesseract)
 - Install WhatsApp Web or Andyroid with WhatsApp running, authenticate and open Chat with target (Andyroid VM does not need QR Code to authenticate!)
 
 ## Setup
After all missing modules got installed and no further errors are visible after starting the script (use ../python.exe __main__.py depending on your python setup), a screenshot should appear to show the capture area. This should be targets name and some space on bottom where online state appears. Adjust screen area on top of the script with X and X positions. Depending on your needs you can adjust some more parameters in size and speed of checks.
