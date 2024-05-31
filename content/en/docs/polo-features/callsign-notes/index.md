---
title: "Callsign Notes"
weight: 3
description: Custom notes for callsigns that are shown while logging
---

"Callsing Notes" is a feature that allows you to show short notes for specific callsigns in the logging screen. This can be useful to remember the name of a friend, or to know if a station is a member of a club or a special event station.

PoLo comes with a built-in file, called "Ham2K's Hams of Note", but you can add as many additional files as you want, and enable and disable them as needed.

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

![Define](clip0135.png)

Once this file is created, you may place the file in your favourite cloud storage folder and copy the perma link for the file to be installed into PoLo. In the Callsign Notes page, click on ```+ Add a new file``` then give the file a name and copy the url into the Location field. Activate the file with the slider control.

![Install](clip0138.png)

From this point, you may return to the Offline Data page and click on the file name so you can Refresh the file.

![Refresh](clip0140.png)

The URL you provide must be a direct link to the file in plain text, and not a link to a web page that contains the file as it's often the case for file sharing tools and cloud storage services.

However, PoLo knows how to handle some cloud storage services, and can automatically convert the link to a direct link.
This is currently supported for Dropbox, OneDrive, Google Drive and Google Docs.

