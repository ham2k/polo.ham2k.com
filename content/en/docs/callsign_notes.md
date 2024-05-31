---
title: "Offline data file Extensions"
linkTitle: "Callsign Notes"
weight: 100
description: >-
     Using Builtin and/or Custom Callsign Notes extension files for offline names and details lookups whilst logging
---

## Callsign Notes
PoLo comes with a Builtin Callsign Notes file link, and also allows users to add their own file. You may leave all files active, or you may choose to use only your own list. The Builtin list is managed by the Developers.

### Custom Files
Custom callsign notes are stored as simple text files, one call per line followed by information you wish to show in the logging screen.

### File Format
An example of the simplest format used for the file would be:

```
VK1AO Alan
VK4KC Marty
KI2D Sebastián
etc
```

The file also supports simplified markdown tags [similar to the ones used on GitHub](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax). So you may supply hyperlinks and text formatting which is then used by PoLo to display the text.

### File storage and access
<img align="right" src="https://www.meta.com.au/apphelp/mparks/clip0135.png" />Once this file is created, you may place the file in your favourite cloud storage folder and copy the perma link for the file to be installed into PoLo. In the Callsign Notes page, click on ```+ Add a new file``` then give the file a name and copy the url into the Location field. Activate the file with the slider control.

![Install](https://www.meta.com.au/apphelp/mparks/clip0138.png)

From this point, you may return to the Offline Data page and click on the file name so you can Refresh the file.

![Refresh](https://www.meta.com.au/apphelp/mparks/clip0140.png)

Cloud sources which have been tested, are Dropbox, OneDrive and Google Drive.

### Dropbox url modification
To use a dropbox link, grab your file url which may appear like this:
```https://www.dropbox.com/scl/fi/7sr7qe75gvzlrrmejtxun/PoLo2K_namesUTF8.txt?rlkey=64mkmajye5v7rowqlgtrrfixd&dl=0```
but you must change the last query component ```dl=1``` to ```raw=1``` to make the link look like this
```https://www.dropbox.com/scl/fi/7sr7qe75gvzlrrmejtxun/PoLo2K_namesUTF8.txt?rlkey=64mkmajye5v7rowqlgtrrfixd&raw=1```

