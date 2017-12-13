<img src="https://raw.githubusercontent.com/guardianproject/haven/master/art/web_hi_res_512.png" width="25%">

# Haven: Protect Yourself

Haven is for people who need a way to protect their personal spaces and possessions without compromising their own privacy. It is an Android application that leverages on-device sensors to provide monitoring and protection of physical spaces. Haven turns any Android phone into a motion, sound, vibration and light detector, watching for unexpected guests and 
unwanted intruders. Designed originally to defeat the infamous “evil maid” attack, Haven can provide protection in a wide variety of situations: protecting sensitive computers, monitoring offices and homes, detecting "wild life", capturing evidence of human rights violations and disappearances, as well as common vandalism and harassment.

<img src="https://raw.githubusercontent.com/guardianproject/haven/master/art/screens/havenob1.png" width="25%"> <img src="https://raw.githubusercontent.com/guardianproject/haven/master/art/screens/havenob2.png" width="25%"> <img src="https://raw.githubusercontent.com/guardianproject/haven/master/art/screens/havenob3.png" width="25%">

Haven only saves images and sound when triggered by motion or volume, and stores everything locally on the device. You can position the device's camera to capture visible motion, or set your phone somewhere discreet to just listen for noises. Get secure notifications of intrusion events instantly and access the logs remotely or anytime later.

View our full [Haven App Overview](https://github.com/guardianproject/phoneypot/blob/master/docs/Haven%20App%20Presentation.pdf) presentation



### Sensors


<img src="https://raw.githubusercontent.com/guardianproject/haven/master/art/screens/haven-sound-config.png" width="25%"> <img src="https://raw.githubusercontent.com/guardianproject/haven/master/art/screens/haven-event-media.png" width="25%"> <img src="https://raw.githubusercontent.com/guardianproject/haven/master/art/screens/haven-event-list.png" width="25%">

The follow sensors are monitored for a measurable change, and then recorded to an event log on the device:

-   **Accelerometer**: phone's motion and vibration
-   **Camera**: motion in the phone's visible surroundings from front or back camera
-   **Microphone**: noises in the enviroment
-   **Light**: change in light from ambient light sensor
-   **Power**: detect device being unplugged or power loss  

## Building

The application can be built using Android Studio and Gradle. It relies on a number of third-party dependencies, all which are open-source.

## Usage

### Main view

Application's main view allows the user to set which sensors to use and the corresponding level of sensitivity. A security code must be provided, needed to disable monitoring. A phone number can be set, if any of the sensors is triggered a message is sent to the specified number.

### Notifications

When one of the sensors is triggered (reaches the sensibility threshold) a notifications is sent through the following channels (if enabled).

- SMS: a message is sent to the number specified when monitoring started
- Signal: if configured, can send end-to-end encryption notifications via Signal

Notifications are sent through a service running in background that is defined in class `MonitorService`.

### Remote Access

All event logs and captured media can be remotely accessed through a [Tor Onion Service](https://www.torproject.org/docs/onion-services). Haven must be configured as an Onion Service, and requires the device to also have [Orbot: Tor for Android](https://guardianproject.info/apps/orbot) installed and running. 

## ATTRIBUTIONS

This project contains source code or library dependencies from the follow projects:

* SecureIt project available at: https://github.com/mziccard/secureit Copyright (c) 2014 Marco Ziccardi (Modified BSD)
* libsignal-service-java from Open Whisper Systems: https://github.com/WhisperSystems/libsignal-service-java (GPLv3)
* signal-cli from AsamK: https://github.com/AsamK/signal-cli (GPLv3)
* Sugar ORM from chennaione: https://github.com/chennaione/sugar/ (MIT)
* Square's Picasso: https://github.com/square/picasso (Apache 2)
* JayDeep's AudioWife: https://github.com/jaydeepw/audio-wife (MIT)
* AppIntro: https://github.com/apl-devs/AppIntro (Apache 2)
* Guardian Project's NetCipher: https://guardianproject.info/code/netcipher/ (Apache 2)
* NanoHttpd: https://github.com/NanoHttpd/nanohttpd (BSD)
* Milosmns' Actual Number Picker: https://github.com/milosmns/actual-number-picker (GPLv3)
* Fresco Image Viewer: https://github.com/stfalcon-studio/FrescoImageViewer (Apache 2)
* Facebook Fresco Image Library: https://github.com/facebook/fresco (BSD)
* Audio Waveform Viewer: https://github.com/derlio/audio-waveform (Apache 2)
* FireZenk's AudioWaves: https://github.com/FireZenk/AudioWaves (MIT)
* MaxYou's SimpleWaveform: https://github.com/maxyou/SimpleWaveform (MIT)


