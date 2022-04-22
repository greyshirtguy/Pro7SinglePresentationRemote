# Pro7SinglePresentationRemote
A simple web app for someone to view and control a **single** specific presentation in Pro7
![Screenshot](ScreenShot.png)

Allows control of a **single** presentation _(currently by using a hard coded name in the script source)_.
The idea is that any device with a web browser can load this simple .html file to view the current Pro7 presentation as a grid of slide thumbnails - and if the current presentation has the right name - they are allowed to control it (click/tap any slide to trigger it).
If the current presentation does not have the correct name to be controllable - they will see a "ghosted" version of it.

Open the .hteml file in any modern web broswer.
You must include the following query strings in the URL to connect to ProPresenter:
```
address=[Network address of ProPResenter] (See Network Preferences)
port=[Network port of ProPResenter] (See Network Preferences)
presentation=[Name of presentation to allow control]
```

You can optionallt include the following query string in the URL
```
quality=[Quality of thumbnail images is the width in pixels of the image data (defaults to 600 if not provided)]
```

Click any slide to trigger it (Space Bar and Arrow keys also work!)

Tip: To use this on an iPad you will need to host it on a webserver that the iPad can access (I know of no way to copy the file to an iPad and open it).
There are many ways to setup a super simple HTTP server to host it on any computer on your network - (eg `python3 -m SimpleHTTPServer 8000` in a MacOS terminal folder that contains the .html file is a simple one-liner that works on modern MacOS)
