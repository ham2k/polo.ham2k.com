---
title: Logger Settings
weight: 54
description: Your list of Operations.
---

PoLo's settings are found behind the settings cog icon on the top of the operations list screen

![Settings](./loggersettings.png)

PoLo application Settings may include Developer Settings if [Developer Mode](../developer-mode/) is activated. Developer Settings are highlighted in orange.

![GenSettings](./gensettingsnodev.png)

You should first set your Operator's Callsign.

Then you should open each category and choose your preferred operating environment.

#### General Settings

The list of general settings avilable to your operating style should be self explanatory. The export settings are dealt with in more details in the [Log Exports & Privacy](../exports/) section.

![themetc](./gendarkmodeetc.png)

Refer also to [Privacy and Export settings](../exports/index.md#general-settings---privacy) for enabling data and app usage sharing.

#### Logging Settings

Logging settings refer to how you like to enter your data in the QSO entry screen and what additional information is shown in the QSO list.
You may be left-handed, in which case the send button will appear on the left side of the entry fields.
You may wish to see country flags only for DX stations, not your own.
You may not wish to collect or see the State field.
You may wish to record signal reports as Sent first or Received first.
You may like to see a bearing to the other station (requires gridsquare/paid QRZ account)
You may like the field entries to jump automatically to the next field during entry.
Finally, you may activate/enable more or less bands and modes to enlarge or shorten the band or mode drop down lists in the QSO entry form. A separate section is found here on [Bands and Modes](../bands-and-modes/).

#### Data Settings

PoLo relies on certain offline data files which are refreshed when the application is started up. Data files can also be refreshed manually if required. Depending on your chosen [supported acvtivity](../../supported-activities/), different offline Data files will be listed.
It is also possible to install your own offline data file. An ADIF file of contacts/log can be imported and used during QSO entry to obtain names and locations.
And finally , you may install your own Callsign Notes file as an extention to the default file. The format for this lookup file is explained on the [Callsign Notes](../callsign-notes/) page amd also elsewhere in this manual.

#### Sync Settings

Sycn settings refer to a feature which will be available as a 2-way service at esome time in the future. At this time, it is a 1-way service sending your data to the Ham2k LoFi Server. This may be used to investigate application/data issues.

#### App Features

App Features comprise [Location-based Activities](../../supported-activities/), Contests & Field Ops, Data Lookup sources and other logging features such as [Satellite Operations](../satellites/) and Worked All Britain.Ireland squares.
There are several sources for callsign lookups which are free, including HamDB, HamQTH. Some services are more comprehensive than others. It's your choice, activate the one(s) you prefer.
If you have enabled Developer Mode, you may also notice that it is possible to spot to a Discord server if you find this useful.

#### Developer Settings

These settings, if enabled, allow you to select the update track for the application, e.g. new features updates. It also allows you to import a QSON file which has been exported from another device. A QSON file is a single distinct operation which can be transported bewteen devices. It contains enaough information to generated a new ADIF export and it will merge into your existing operations list.
Refer to [Developer Mode](../developer-mode/) for more information.

### Accounts

#### QRZ

The most popular account to be used with any logging application is QRZ. Refer to [Data Lookups](../lookups/) for more information on setup and use of QRZ accounts.

#### SOTA (for SOTAWatch self Spotting)

If you are a SOTA activator, then you have an account with SOTAWatch. An account is not required for chasing SOTA activators. You are only required to activate the App Feature (see above). But to Spot yourself on SOTAWatch, you must have an account and have it active in PoLo.
The SOTAWatch authentication system relies on an initial loging to acquire a token. The token can be refreshed but may expire if not refreshed regularly. In this case, a fresh login is required to acquire a new token. When the text "Logged in as".. CALLSIGN is displayed, the token is current. When the token has expired, the text will display CALLSIGN only. Tapping the account will attempt to refresh the token. If a token refresh is not possible, you will be prompted to make a new login to activate the connection again. The authentication interface will remember your credentials for future login requirements.

Other accounts may be listed in this section when and if they are available or required. If SOTA is not an activity that you engage with, deactivating the SOTA activity in the App Features section, will remove SOTA from the accounts section.

---

<img style="float: right; margin-left: 20px" src="./entrysettings.png"/>

### QSO entry settings (Logging Settings)

From the elipsis button on the Operations QSO List panel, there are several options/actions that apply to the QSOs in the list.

### Entry Field visibility

Some operators choose not record RST values at all. Some operations do not require the excahnge at all. For these instances, you can choose to switch RST Fields off. When off, the RST fields are not visible in the QSO list, nor are they visible in the QSO entry panel. In this case, a default value is recorded for each QSO.

### State Fields

Many jurisdications around the world pay little attention to a State exchange during the contact. For those operations, the State fields can be turned off. It will not be shown in the QSO list, nor will it be seen in the QSO entry form.

### Show Deleted QSOs

Normally when QSOs are deleted, they are visibly present in the QSO list but are shown as a line-thru QSO. QSO's so deleted, can be edited and un-deleted at any time. The Show Deleted QSOs option can be turned OFF so deleted QSOs are not shown in the list at all. Deleted QSOs are also not part of any QSO count or operation statistics.

### Numbers Row

For some devices and some keyboards, the number row is not available or visible. Turning this option on will place a PoLo numbers row across the top of your existing keyboard.

---

### Lookup All

You may not have cell coverage during your operation and thus no ability to lookup callsigns. In these cases, you may be using a callsign notes or callsign history adif file for offline lookups. When you return to a cell coverage area or when the coverage improves, this option will force a lookup of all QSOs in your QSO list.

### Confirm Spots

While spots are available, and you think you may have entered callsign(s) incorrectly. This option will run through the spots list and compare your QSOs against the visible references and callsigns you have. Corrections may be applied to your QSOs. If spots for your QSOs have expired and are not present in the list, this action has no effect.

---

### General Settings - Privacy

The application provides a way for users to share usage data including app crashes. There is also the ability to share operation data if you wish to or consider it importatnt to do so when tracking down a system bug. These settings can be enabled or disabled at any time.

![privastchar](./privacydatashare.png)