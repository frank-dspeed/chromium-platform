# chromium-platform
This Repository Tracks the State of the Chromium Platform to be used as base for WebApps 


## Projects that try to enable it
- --ectron (using libchromium + nodejs binary + patch both) we do not write the full name here as the project is really not in shape anymore and should almost never get used
- NWJS (using libnode + chromium + patch chromium + cef) It is the most mature project using the C CEF implementation + a additional build libnode
- JCEF and JAVA CEF + SWT or AWT - This is maybe the game changer on the long run as this supports also GraalVM as Interpreter.
  - Spotify is using this method with great success Already.


## Goals
Getting Chromium into a shape that you can easy deploy apps on it via Open Pwa or a similar Concept. 

## What is this CEF?
Chromium Embedded Framework a set of wrapper methods for the existing chrome code to modify it for special deployment needes inside other applications. Everything till the WebContent Layer without the Additional Browser Layer.

## Enabled API's
- [ ] DirektSockets
- [ ] JSON Serialized Messaging ```\0``` terminated via process pipe
- [ ] Aura Window Manager Flags for App Start
- [ ] serving files via override folders for locations.


## Use Case 1
Serve a MultiPage App from a Profile Folder NativMessaging via devtools. 

- We Create and Handle a App Profile 
  - We deploy a extension to handle the app internal communication
