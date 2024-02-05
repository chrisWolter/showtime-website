+++ 
title = "Tech Stack" 
weight = 1
+++

{{<section title="Organisation and Communication">}}
We used Mattermost for our internal communication and for issue tracking.
{{</section>}}

{{<section title="Development">}}

#### HoloLens

To develop the AR/XR App that is running on the HoloLens 2 we used Visual Studio (Code) and Unity with MRTK2.

- Programming Language: C#

#### Raspberry

The Raspberry Pi runs the Debian Raspberry Distribution and is the communication middleware.
It serves as the MQTT broker and the Wi-Fi hotspot that the Arduino and HoloLens connect too.
The Raspberry Pi was set up with the CLI

- Programming Language: Bash

#### Arduino

The Arduino was developed using the Arduino IDE

- Programming Language: C++

{{</section>}}

{{<section title="Hardware">}}

#### Interactions

- Arduino UNO WiFi Rev2
- Button
- Potentiometer
- PN532 NFC/RFID Reader
- LED

#### Communication

- Raspberry Pi 3

#### XR/AR Apps

- HoloLens 2

{{<gallery>}}
{{<image src="Arduino.png" alt="Arduino Logo" caption="Arduino">}}
{{<image src="RPI.png" alt="Raspberry Pi Logo" caption="Raspberry Pi">}}
{{<image src="Hololens.png" alt="Hololens" caption="Hololens">}}
{{</gallery>}}
{{</section>}}
