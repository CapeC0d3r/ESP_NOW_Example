# ESPNOW P2P Example Code

Some slightly modified example code to mess around with ESPNOW PSP ESP Communication.

Right click the directory, open with VS Code, make sure you have the PlatformIO plugin installed.  

I've added a few different ESP modules to the platformio.ini file, if you click the platformIO icon (ant or alien head) you should see some "Project Tasks" and some different "Tasks" for "ESP32Dev" and "ESP12E".  These are board specifiers for building and uploading the code.  You may need to add some board info to the platformio.ini file in order to build for your particular board.  An easy way to do that is to start a new project from PlatformIO and select your board, when it creates a project, just grab the parameters from the "platformio.ini" file and add them to this project. Or read the documentation and add it manually... 

I am a hack, and I add libraries my own way.  It's not that I don't like the library manager, I just prefer to manage my own libraries by downloading them, and manually adding them to the "/lib" directory, and then including them with my "/include/include_these.h" file.  

Any CPP file in my project will have this at the top of the file.

```cpp
#ifndef INCLUDED
#include "..\include\include_these.h"
#endif
```

I will mess around with this some more when I have free time and add more documentation / repositories.  I had a few different versions, but I reverted back to just pressing a button to broadcast a packet.  It looks like the largest packet you can sent is ~250 bytes.  I didn't dive too deep into the ESP NOW library (in the "/lib" directory) so it's pretty much a black box with some API calls to me at the moment.  I do have a module in my basement communicating with one in my office right now, so that is cool. 

