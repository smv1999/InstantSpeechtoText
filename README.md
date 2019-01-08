# InstantSpeechtoText
1. Configure Microphone (For external microphones): It is advisable to specify the microphone during the program to avoid any glitches.
Type lsusb in the terminal. A list of connected devices will show up. The microphone name would look like this
   USB Device 0x46d:0x825: Audio (hw:1, 0)
Make a note of this as it will be used in the program.

2. Set Chunk Size: This basically involved specifying how many bytes of data we want to read at once. Typically, this value is specified in powers of 2 such as 1024 or 2048

3. Set Sampling Rate: Sampling rate defines how often values are recorded for processing

4. Set Device ID to the selected microphone: In this step, we specify the device ID of the microphone that we wish to use in order to avoid ambiguity in case there are multiple microphones. This also helps debug, in the sense that, while running the program, we will know whether the specified microphone is being recognized. During the program, we specify a parameter device_id. The program will say that device_id could not be found if the microphone is not recognized.

5. Allow Adjusting for Ambient Noise: Since the surrounding noise varies, we must allow the program a second or too to adjust the energy threshold of recording so it is adjusted according to the external noise level.

6. Speech to text translation: This is done with the help of Google Speech Recognition. This requires an active internet connection to work. However, there are certain offline Recognition systems such as PocketSphinx, but have a very rigorous installation process that requires several dependencies. Google Speech Recognition is one of the easiest to use.
