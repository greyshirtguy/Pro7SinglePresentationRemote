# Pro7SinglePresentationRemote
A simple web app for someone to view and control a single specific presentation in Pro7

Allows control of a single presentation (by using a hard coded name).
The idea is that any device with a web browser can load this simple html file to see the current presentation in Pro7 - and if the current presentation has the right name - they can tap any slide to remote control it!

Update the following hardcoded values in the script to suit your Pro7 machine:
var ipAddressOfProPresenterComputer = '127.0.0.1' // Hostname can used used here also if you have hostname resolution for your ProPresenter computer
var networkPortOfProPresenter = '50001' // See ProPresenter network prefs
var nameOfPresentationToControl = "Message" // This web page will be able to control a presentation is the name matches

And then open in your fav web browser.
