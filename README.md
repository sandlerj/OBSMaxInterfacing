# Processing Video and Sound for Video Conferencing and Networked Performance
Sending video and audio from Max and Ableton in Zoom to make you the coolest person in the meeting/Make experimental music via networking.

*Tutorial assumes you are using Windows 10, since I don't own a Mac*

## Required Software:
- OBS Studio Download: https://obsproject.com/download
- Virtual Camera Download (click "Go to download" link on right): https://obsproject.com/forum/resources/obs-virtualcam.539/
- Max/MSP/jitter (there's a 30-day free trial if you don't have a license yet)

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

### Audio Processing
1. Within Ableton, or whatever, just make sure you're sending audio out to your headphones/speakers.
2. In Windows, open Sound Settings, and then select Sound Control Panel. Choose the "Recording" tab and make sure that Stereo Mix is enabled. Then go to the Volume Mixer (right click the icon in the tray) and mute any applications you don't want to send sound. Strangely enough, you don't need to mute Zoom, as it doesn't seem to create a feedback loop through your input when other people on the calls speak. Could be the built in echo cancellation but I'm not sure.
3. In Zoom, go to audio settings, and select "Stereo Mix" in the drop down for Microphone. You'll now be sending audio from Ableton which you should be able to monitor through your own speakers or headphones. Make sure you're actually sending audio.
4. You will probably also want to send "Original Sound", and turn off any noise cancellation, depending on what you're sending.
5. Switching back to your normal mic in Zoom is fine, unlike video.

It's very possible the audio quality may not be super great on the receiving end of Zoom. I'm assuming there's compression in Zoom that we can't get around, so it may be worthwhile to have someone on the receiving end to record what they're getting from you so you know what it "actually" sounds like, because in all likelihood it is not as pretty as what you're hearing.

If you found this helpful and want to support a starving artist who is currently out of work, I'd be happy to take your money via Venmo `@JoeSandals` :)))))