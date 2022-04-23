# Pro7SinglePresentationRemote
A simple web app for someone to view and control a **single** specific presentation in Pro7  
** Please note this is BETA and it may change/break at any time! (I've only put a few hours into it so far) **
![Screenshot](Screenshot.png)

Allows control of a **single** presentation in Pro7 using the new API in versions 7.9 and later.
The idea is that any computer with a web browser can load this simple .html file to view the current Pro7 presentation as a grid of slide thumbnails - and if the current presentation has the right name - they are allowed to control it (click/tap any slide to trigger it).
If the current presentation does not have the correct name to be controllable - they will see a "ghosted" version of it and cannot control it.

It's all in a single .html file - just copy the file to a computer and open the Pro7SinglePresentationRemote.html in any modern web broswer!

You must include the following query strings in the URL to connect to ProPresenter:
```
address=[Network address of ProPResenter] (See Network Preferences)
port=[Network port of ProPResenter] (See Network Preferences)
presentation=[Name of presentation to allow control]
```

You can optionally include the following query string in the URL to control the image quality:
```
quality=[Quality of thumbnail images is the width in pixels of the image data (defaults to 600 if not provided)]
```

Example URL of file on a MacOS computer, in my home folder, with parameters to connect to Pro7 on the same machine with port 50001 and to control a presenation called "Message":  
file:///Users/dan/Pro7/New%20API/Web/Pro7SinglePresentationRemoteTablet.html?pro7Address=127.0.0.1&pro7Port=50001&controlPresName=Message&slideQuality=440

Click any slide to trigger it (Space Bar and Arrow keys also work!)


You can also host the file on a local web server and use that instead of copying to the computer.
For example, if you hosted it on a compuer on your LAN with IP address 192.168.1.50 and port 8080 AND your ProPresenter machine has IP address 192.167.1.7 and with port 50001 and you wanted to control a presentation called "Message" then the URL to use this on any other devide would look like this:  
http://192.168.1.50:8080/Pro7SinlgePresentationRemote.html?address=192.168.1.7&port=50001&presentation=message  

Tip: To use this on an iPad you *must* host it on a webserver - iPads cannot open locally saved .html files like computers can.
Ideally you would host it on a local http server on your lan (It's simplier from a browser security prespective).
It's easier than you think to run up a tiny HTTP server on a computer on your LAN - use the Google!  
For example: On MacOS you can run this one-liner in the terminal within a folder that has the .html: `python3 -m http.server --cgi 8080)`
For those that cannot host the file on a local web server - I have hosted at my personal website at http://pro7api.greyshirtguy.com/Pro7SinglePresentationRemote.html  

Example URL to connect to ProPresenter 7 with IP address 192.168.1.7 and port 50001 and control the presentation that is called "Message":  
http://pro7api.greyshirtguy.com/Pro7SinglePresentationRemote.html?address=192.168.1.7&port=50001&presentation=message  
This online verion is for Ipads - It does not work in desktop browsers - due to security restrictions in most desktop browsers.
