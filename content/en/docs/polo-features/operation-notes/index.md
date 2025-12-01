---
title: "Operation Notes"
weight: 144
description: Adding notes to your operation including solar and weather readings
---
Keep a track of things.. grab the solar data, grab the current weather at your location or add a note for later.

Key words entered in the "Their Call" entry field will prompt either the collection of this data or further entry of a note.

#### NOTE
![alt text](note.png)

Type NOTE and you will be prompted to keep typing to add a free-form note into your operation.

![alt text](noteline.png)

#### WEATHER
Enter WEATHER to pull the current weather for your location.

![alt text](weather.png)


#### SOLAR
Enter SOLAR to pull the current solar data from https://www.hamqsl.com/solarxml.php and display the data in a QSO line of the operation.

![alt text](solardata.png)

Notes entered in this form are exported as additional ADIF fields in the export file. They contain multibyte characters. The field names are not part of the ADIF specification and will be ignored by your usual logging program.

The desktop version of PoLo will read this data and display it appropriately when your operations are accessed.

![alt text](adif.png)