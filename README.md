# Text-to-Speech-to-Microphone
While on medical vocal rest, I needed to continue attending meetings. To do this, I leveraged a web-based text-to-speech app, VB-Cable, and VoiceMeeter. This tutorial illustrates how I achieved this on Windows 11.

## The Basics
You need a [text to speech app](url), then you'll use [VB-Cable](url) and [Volume Mixer](url) to re-direct the audio through [VoiceMeeter](url) so that it is a microphone for your [video conferencing program](url). This may sound complex, but hopefully, I can simplify it for you.

### Text to Speech app
1. I utilized [**Dani's Voice App** ](https://voice.db.rocks) because it is simple and, while in chat mode, can be configured to send the message when you hit enter. It is free and works on any platform. It uses the operating system's in-built speech generation system, which is nice. You can use any other text-to-speech program or app by using a different app in Volume Mixer. The Microsoft Aria Online (Natural) - English (United States) (en-US) voice is generally fine, but I find the pauses between sentences to be disconcerting.
2. If you are using a web-based text-to-speech app, run it in a browser that is not your default browser. This allows you to route its audio specifically, avoiding audio from your normal stuff (like a game or YouTube video) playing in your meeting.
3. You may also want to install the web-based app as an application on your computer so that it always opens in that other browser.
<img width="608" height="929" alt="dani&#39;s vocie app" src="https://github.com/user-attachments/assets/15e1a786-9a99-473a-a44c-09a69c977d47" />

### VB-Cables and VoiceMeeter Install
1. Download and install VB-Cable from here - **https://vb-audio.com/Cable/**
2. Download and install VoiceMeeter from here - **https://Voicemeeter.com** (you can use the Standard install for this).
3. After installing each, you will be asked to reboot your computer. You only need to reboot after installing them both.

### Volume Mixer
1. Open **Windows Volume Mixer** (Start > Mixer).
2. Expand the text to speech app or the browser you will be running it in.
3. Change the **Output device** to **CABLE Input (VB-Audio Virtual Cable)**.
4. Change the **Input device** to **CABLE Output (VB-Audio Virtual Cable)**.
<img width="1083" height="489" alt="mixer" src="https://github.com/user-attachments/assets/00073d63-8095-4e0d-8af3-49bd41071cb3" />

### VoiceMeeter
Now for the tricky parts:
> This is only necessary if you want to hear your text to speech playback in your headphones or speaker (the Hareware Out section)
1. For **Stereo Input 1**, I selected my **headset** (as a WDM (WASAPI) device).
2. Do the same on the other inputs for the other audio devices you use.
3. In the **Hardware Out** section, click **A1** and select the MME (Multimedia) device you wish to hear the text to speech though (I used my headphones).
4. In the **Hardware Out** section, click **A2** and select the MME (Multimedia) device **Cable Input (VB-Audio Virtual Cable)**.
5. Spaeck into the mic and use the Text-To-Speech program and observe the audio meeters moving for each.
6. Click **Menu** in the upper right and **Save Setting**s to your computer.
7. Click **Menu** again and then **Load Settings on Startup**, selecting the file you just saved.
8. Click **Menu** once more and check the following - **System Tray** and **Run on Windows Startup**.
9. Minimize the window.
>You can reference this screenshot:
><img width="1014" height="613" alt="dddd" src="https://github.com/user-attachments/assets/939b2b3c-7518-4f4c-b5d0-1cd943b203f7" />

### Your Video Conferencing Program
1. In the viceo conference program of your choice, set your **microphone** to  **CABLE Output (VB-Audio Virtual Cable)**.
2. You can set your speaker to the system default or whatever you normally use.
3. When you use your text to speach program, your video conference program will show the speech volume on the meter (if there is one).

# Conclusions
I really wish there was an easier way to do this. I've looked at many local and web-based text to speech programs, but most of them don't offer a return key sends message type feature. If I were really smart, I would make an app that can route it's audio as a microphone directly. 
