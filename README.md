# BlinkLed

Create a small application using Android Things, configure it with Firebase and control 
the blinking delay of an LED bulb realtime over the air for Raspberry Pi 3 board.


Steps:

Step 1: Create a new android project.

Step 2: Get the board schematics and hardware connection right.

Step 3: Grab the sample-simplepio as the starting point and refer the aplication file of blink.

Step 4: Main Activity file is BlinkLedActivity.java where firebase Listner is implemented.

Step 5: BoardDefaults.java is associated with SoC board in reference used and it GPIO pin configured.

Step 6: Modify these following files to suite your build correct:

Step 7: Project-level build.gradle (<project>/build.gradle):

  buildscript {
  dependencies {
    // Add this line
    classpath 'com.google.gms:google-services:3.0.0'
    }
  }

Step 8: App-level build.gradle (<project>/<app-module>/build.gradle):

  // Add to the bottom of the file
  apply plugin: 'com.google.gms.google-services' 

Step 9: Add Firebase to your Android app. https://console.firebase.google.com/

   This has 3 steps - 

   Step 1) Register app, download config file ( google-services.json) and Add firebase SDK

   I am using packages to register my androidthings app.

   package nickname : studioraga-1
   package name     :  com.ncs.studioraga.blinkled  /* This is important */

   step 2) Download  config file ( google-services.json)

   The step (1) generates a json file as mentioned and ask you to download it to your machine.

   Download the file and copy this to your project's app folder
   for me , it is at <PATH>/BlinkLed/app/

   Step 3) Add and setup firebase SDK   Ref: https://firebase.google.com/docs/android/setup


10) Thats all, sync the project in Android studio and build the project sucessfully. 



