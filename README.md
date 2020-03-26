# Processing Video and Sound for Video Conferencing and Networked Performance
Sending video and audio from Max and Ableton in Zoom to make you the coolest person in the meeting/Make experimental music via networking.

*Tutorial assumes you are using Windows 10, since I don't own a Mac*
N.B. There's very likely a better way to do this. If you know what it is, I would love to know.

## Required Software:
- OBS Studio Download: https://obsproject.com/download
- Virtual Camera Download (click "Go to download" link on right): https://obsproject.com/forum/resources/obs-virtualcam.539/
- Max/MSP/jitter (there's a 30-day free trial if you don't have a license yet)
- Virtual Audio Cable (use the lite version): https://vac.muzychenko.net/en/download.htm

Additionally, you'll probably want something to create/process fun and exciting experimental sounds.

Link to video tutorial: (non-existent yet because I haven't made a video yet)

## Instructions
0. Install required software and Virtual Camera plugins. Take some time to explore OBS if it's new to you.
### Video Processing
1. Open twoWorldCam.maxpat in Max
2. Go to Profile->Import and choose "OBS_Max_Interfacing/Configuration Settings/basic" (may not be needed, just what I had my settings at)
3. Go to Scene Collections->Import and choose "OBS_Max_Interfacing/MaxCam.json"
4. Go to Tools->VirtualCam and start OBS-Camera (choose auto-start if you'd like the camera to start broadcasting when you open OBS)
5. There should be 4 options for Scenes - Max Out should be the delayed camera feed, web cam should be clean, Ableton will be Ableton (if you have it open), and Desktop should be that with clean camera feed in the corner.
6. If any of the actual windows (Ableton, the jit.world windows) are minimized, they will not display updated video.
7. If in Studio mode, select any scene to be displayed in the "Program" view. This is what is being sent to the OBS-Camera virtual camera.
8. Open Zoom (or whatever you're using) and when selecting video source under settings, choose OBS-Camera. This will display whatever is in the "Program" view.
9. In order to display clear/unprocessed camera output, select the scene "Webcam" in OBS. Because Max is using your webcam, you will not be able to select your built in webcam within Zoom (or whatever). Doing so may cause issues or may just not work, since Max is already using it and doesn't like to share.
10. To change the video processing, just replace the vizzle delay module with something else. Go wild.

### Audio Processing (For Windows)
0. If VAC changed your system settings so that the virtual cable was you main audio i/o, reset that to the default (or whatever input and output you plan on using).
1. Within your DAW, or whatever, set your output to your virtual audio cable (line 1 probably). Unless you don't plan on speaking, make sure you have a way to send clean vocal audio through this.
2. Open up the audio repeater (If this is Windows you're probaby using MME so make sure to open that one). Set Wave In to the virtual cable and Wave Out to the output device you want to monitor sound with (for example, built in speakers)
3. Start the audio repeater. Adjust the sample rate as necessary. You'll also probably want to bring down the buffer size or you will have beaucoup delay but be aware of clipping.
4. Within Zoom (or whatever) set microphone input to the virtual cable.
5. Be sure to turn on original sound if using Zoom - otherwise much of your audio may be wrecked by compression and machine learning algos that get rid of "noise".

It's very possible the audio quality may not be super great on the receiving end of Zoom, since this is a video conferencing platform which by definition means they're aiming for low latency at the expense of quality. it may be worthwhile to have someone on the receiving end to record what they're getting from you so you know what it "actually" sounds like, because in all likelihood it is not as pretty as what you're hearing.

### Notes and Further Comments
- I've experienced that if you start max while already in a call, you lose sound from Zoom; it seems that the easiest way around this is to just open Max first.


If you found this helpful and want to support a starving artist who is currently out of work, I'd be happy to take your money via Venmo `@JoeSandals` :)))))
