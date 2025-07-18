# TX16Wx


## Creating a samba instument

### Getting samples

- Get the samples from https://freesound.org/ or wherever and cut them into individual WAV files (Audacity is a good option).
- Audacity also allows recording the sound from your PC (loopback), so if you have a video playing you can open Audacity, and do the following:
  - Click Audio Setup for settings
  - Set Host: WASAPI
  - Set Recording Device: Earphones (loopback) or Realtek Speakers (loopback)
  - Create a stereo track and hit record

### Using the samples in the MIDI sampler

- Get TX16Wx. [It cannot be used standalone](https://www.tx16wx.com/f-a-q/), so download [SAVIHost](https://www.hermannseib.com/english/savihost.htm) aswell. I'll go for the VST2 version, with keyboard.
- When you run the savihost executable, it will open an explorer window. Find the installed TX16Wx plug in to open it. In my case, it is under `C:\Program Files\Steinberg\VSTPlugins\TX16Wx.dll`.

Opened plugin:

<img src="image.png" width="60%">

- Find your samples in the file explorer. Enable the sound button below to hear the samples when clicked.

<img src="image-1.png" width="30%">

- Open the regions tab and drag the samples. They will be mapped to midi keys.

<img src="image-2.png" width="60%">

- In the Goups tab, change the mode to Oneshot to play the whole sound when the midi key is played, instead of cutting the sound to the duration of the note.

- The Poly section can be used to set the max polyphony number.
- The Waves tab can be used to cut the samples, but we've used Audacity for that.

- To add more instruments, right-click an empty region of the plugin and click new slot.
- The newly created slot may be set to the same program as you just created, like shown below. In this case, click the gear icon and select New program.

Duplicate program:

<img src="image-3.png" width="60%">

New program:

<img src="image-4.png" width="60%">

- To delete a program or a program slot, simply right-click it and choose the option you need. Notice that deleting the program slot will only remove the slot, but the program can be reopened later from a new slot by selecting it from the program name dropdown menu.

<img src="image-5.png" width="60%">

- It is also possible to add all sounds into a single program, and perhaps create different groups in the program to differentiate and apply different rules. In this case all the rules are the same, but different groups were created for organization purposes.

<img src="image-6.png" width="60%">

### Exporting the program

- When you're done adding sounds to the instrument, you can export the program in `Plugin>Save Program`. If you used multiple programs, you can export the bank instead in `Plugin>Save Bank`. Make sure to choose a folder, as this might create several files.


## Importing the instrument in the DAW

- Now that you have the program or bank created, open your DAW (such as Pro Tools Intro, which is free at this time).
- In the daw, create a stereo instrument track and insert the TX16Wx instrument.
- Click load program and select the program you created
- Open this track's MIDI editor and add the sounds
- Note: the octave numbers in the DAW might not match the numbers in the TX16Wx plugin

<img src="image-7.png" width="60%">
