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



### Status
-

### Next Steps
- 


## Building our Window Manager and encapsulate Apps inside a contained environment

Instead of build ontop of the Android framework and use the default window manager, we could create our own one to escape the limitations that come with the official one. 
The Android App would then run inside a window ouf our own window manager and we could get full control of how the windows are resized

### Status
-

### Next Steps
- Research if it is possible and how it can be adressed






