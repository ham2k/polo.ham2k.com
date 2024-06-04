---
title: "Callsign Notes"
weight: 3
description: Custom notes for callsigns that are shown while logging
---

"**Callsing Notes**" is a feature that allows you to show short notes for specific callsigns in the logging screen. This can be useful to remember the name of a friend, or to know if a station is a member of a club or a special event station.

PoLo comes with a built-in file, called "**Ham2K's Hams of Note**", but you can add as many additional files as you want, and enable and disable them as needed.

### Custom Files

Custom callsign notes are stored as simple text files, one call per line followed by information you wish to show in the logging screen.

If the information starts with an emoji, it will be shown in log and spotting entries.

Empty lines, and lines that start with `#` are ignored.

### File Format

An example of the simplest format used for the file would be:

```
VK1AO Alan
VK4KC Marty
KI2D Sebastián
# etc
```

The file also supports simplified markdown tags [similar to the ones used on GitHub](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax). So you may supply hyperlinks and text formatting which is then used by PoLo to display the text.

### File storage and access

<img align="right" src="clip0135.png" />Once this file is created, you may place the file in your favourite cloud storage folder and copy the perma link for the file to be installed into PoLo. 

**Step 1:** In the application Settings, tap Data Settings.

**Step 2:** In the Data Settings, tap Callsign Notes
![clip0136](https://github.com/ham2k/polo.ham2k.com/assets/61640726/03088400-c056-41b4-a864-59a2b85d01cd)


**Step 3:** In the Callsign Notes page, click on ```+ Add a new file``` then give the file a name and copy the url into the Location field. Act
ivate the file with the slider control.

![clip0137](https://github.com/ham2k/polo.ham2k.com/assets/61640726/f3b185af-ab1b-4449-8d14-530b99c55c4e)


**Step 4:** In the Custom window, provide a name for your files and paste the url for the file into the Location field
![Install](clip0138.png)

**Step 5:** Click Done to return to the Callsign Notes, then enable the file you have added by using the slider control
![clip0139](https://github.com/ham2k/polo.ham2k.com/assets/61640726/7a11f90c-2f2b-4366-9d93-05ab892b9ccf)


**Step 6:** From this point, you may return to the Offline Data page and click on the file name so you can Refresh the file. This action will pull the file onto the device. The date and time of the last update is shown in this dialog so future refresh actions can be managed as your wish. Click Done.

![Refresh](clip0140.png)

The URL you provide must be a direct link to the file in plain text, and not a link to a web page that contains the file as it's often the case for file sharing tools and cloud storage services.

However, PoLo knows how to handle some cloud storage services, and can automatically convert the link to a direct link.
This is currently supported for Dropbox, OneDrive, Google Drive and Google Docs.

