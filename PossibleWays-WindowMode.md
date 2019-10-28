# Research Ideas for realising IAV windowed app Ideas

## Manipulating stock Android Automotive Launcher

The sourcecode of Android Automotive OS is not yet publicly available but the sources of the App are available.
Googles repositorie is here https://android.googlesource.com/platform/packages/apps/Car/Launcher/

### Status
Compiling the App ourselfs and deploying it to the emulator failed. 

### Next Steps
- Get the App to compile and run
- Understand the different parts of the App


## Create a new Launcher using the freeform mode

Android has a feature called "Multi-Window" for displaying more then one App at a time. 
Docs: https://developer.android.com/guide/topics/ui/multi-window
One option there is to enable freeform mode to resize the Apps independently from each other
We could use that APIs to create a Launcher that fullfills the vision from IAV.

There is a App which utilizes this API to create a desktop-like expierience. The App is open-source so we could reuse parts of it or at least have a look at the source code to see how it works.
https://github.com/farmerbb/Taskbar

### Status
The App runns on Android Automotive OS inside the emulator. That means the necessary APIs are there.
Compiling the App ourselfs and deploying it to the emulator failed. 

### Next Steps
- Get the App to compile and run
- locate the code where apps are started inside a window and try to use predefined sizes and positions and to prohibit change of size and position by the user
- extract the Code responsible for windowed mode to later merge it into a launcher




## Changing the Android Window Mode API 

Since Android 7.0 (API level 24) displaying more than one app at a time is supported. Apps can be run side-by-side or one-above-the-other. The user can drag the dividing line separating the two to make one app larger and the other smaller. Possible configurations are activity's minimum allowable dimensions. An activity can use the intent flag FLAG_ACTIVITY_LAUNCH_ADJACENT. If the device is in split-screen mode, the system attempts to create the new activity next to the activity that launched it, so the two activities share the screen. The system is not guaranteed to be able to do this, but it makes the activities adjacent if possible.

### Status
- Only 2 Apps can be run at a time. Only the activity the user has most recently interacted with is active at a given time. All other visible activities are STARTED but are not RESUMED.
- Layout attributes: defaultWidth, defaultHeight

### Next Steps
- Picture-in-picture Support since Android 8


## Building our Window Manager and encapsulate Apps inside a contained environment

Instead of build ontop of the Android framework and use the default window manager, we could create our own one to escape the limitations that come with the official one. 
The Android App would then run inside a window ouf our own window manager and we could get full control of how the windows are resized

### Status
-

### Next Steps
- Research if it is possible and how it can be adressed
