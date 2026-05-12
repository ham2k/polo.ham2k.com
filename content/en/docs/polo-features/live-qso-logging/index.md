---
title: Live QSO Logging
weight: 191
description: Live outbound QSO forwarding to other software and services.
---

Live QSO Logging sends newly logged QSOs out of PoLo, in real time, to other software or services.

This is a live forwarding feature, not a sync engine, backup system, or logbook merge tool. It takes a QSO the moment you log it and hands it off elsewhere. Nothing more exotic than that.

{{% pageinfo %}}
On both Android and iPhone, this feature appears as **Logging → Live QSO logging**.

On iPhone, `UDP ADIF` and `N1MM Message` use unicast targets. Broadcast and multicast are not supported there.
{{% /pageinfo %}}

## Software configuration guide

### Basic setup

PoLo sends each QSO to a destination written as `IP:port`, for example `192.168.73.73:2333`.

The only rule that really matters here is that both ends agree on the port. If PoLo sends to `2333`, the receiving software needs to be listening on `2333`, not on some other port.

1. Put the phone and the computer on the same local network.
2. Configure the receiving software first and note the port it uses.
3. In PoLo, select the matching output mode.
4. In PoLo, enter the computer IP address and that same port.
5. Use **Send test ADIF** from the settings screen until you have the desired settings locked in.

The example ports on this page are simply the ones used during testing. Use different ones if you like; just keep both sides in agreement.

Once that works, log QSOs in PoLo as normal during an operation and they will appear in the software you configured.

## Software guides

### N1MM

1. Go to **File → New log in database**.
2. Set **Log Type** to **DX**.
3. Set **Mode** to **SSB + CW + Digital**.
4. Go to **Config → Configure ports, mode control, winkey**.
5. Open the **WSJT/JTDX Setup** tab.
6. In **WSJT-X and JTDX UDP Settings**, click the **Enabled** checkbox.
7. Set the UDP port to `2333`.

Next, in PoLo:

1. Go to **Logging → Live QSO logging → UDP ADIF**.
2. Confirm **Enabled** is set.
3. Set the destination to the computer running N1MM, for example `192.168.73.73:2333`.
4. Choose either `Raw ADIF` or `WSJT-X type 12`.
5. Use **Send test ADIF** from the settings screen until you have the desired settings locked in.

Confirmed with N1MM v. 1.0.11031.0.

### Log4OM

#### Method 1: N1MM Message

1. Go to **Settings → Program Configuration → Software Integration → Connections → UDP Inbound**.
2. Add a new UDP inbound connection.
3. Set a connection name such as `PoLo N1MM XML`.
4. Set the port to `12060`.
5. Leave multicast disabled.
6. Set the service type to `n1mm_message`.
7. Enable **Use External Data** and leave the other options disabled.

Next, in PoLo:

1. Go to **Logging → Live QSO logging → N1MM Message**.
2. Confirm **Enabled** is set.
3. Set the destination to the computer running Log4OM, for example `192.168.73.73:12060`.
4. If desired, enable **Skip empty fields** on constrained connections.
5. Use **Send test ADIF** from the settings screen until you have the desired settings locked in.

#### Method 2: UDP ADIF using WSJT-X type 12

1. Go to **Settings → Program Configuration → Software Integration → Connections → UDP Inbound**.
2. Add a new UDP inbound connection.
3. Set a connection name such as `PoLo UDP WSJT format`.
4. Set the port to `2333`.
5. Set **Message format** to **WSJT-X compatible**.
6. Enable **Use External Data**.

Next, in PoLo:

1. Go to **Logging → Live QSO logging → UDP ADIF**.
2. Confirm **Enabled** is set.
3. Set the destination to the computer running Log4OM, for example `192.168.73.73:2333`.
4. Set **Message format** to `WSJT-X type 12`.
5. Use **Send test ADIF** from the settings screen until you have the desired settings locked in.

Confirmed with Log4OM v. 2.2.40.

### DXKeeper

1. Start **DXKeeper** and **SpotCollector** from the DXLab launcher.
2. In SpotCollector, open **Configuration**.
3. Go to the **Spot Sources** tab.
4. Find the **WSJTX** row.
5. Set the port to `2237`.
6. Enable that source.
7. In the tested setup, the indicator first turned yellow and then green.

Next, in PoLo:

1. Go to **Logging → Live QSO logging → UDP ADIF**.
2. Confirm **Enabled** is set.
3. Set the destination to the computer running DXKeeper, for example `192.168.73.73:2237`.
4. Set **Message format** to `WSJT-X type 12`.
5. Use **Send test ADIF** from the settings screen until you have the desired settings locked in.

If you need extra diagnostics, DXLab may show a **DXLab SC_WSJTX** status window with separate indicators for DXKeeper and WSJT connectivity, which can help confirm that packets are arriving even if they are not yet showing up where you expect.

Confirmed with DXKeeper v. 18.05.

### Swisslog

1. Go to **Options → Digital Modes/Interfaces → WSJT-X/JTDX**.
2. Enable the **main** checkbox.
3. Set the listening port to `2237`.
4. Leave forwarding disabled unless you specifically need it.

Next, in PoLo:

1. Go to **Logging → Live QSO logging → UDP ADIF**.
2. Confirm **Enabled** is set.
3. Set the destination to the computer running Swisslog, for example `192.168.73.73:2237`.
4. Set **Message format** to `WSJT-X compatible type 5`.
5. Use **Send test ADIF** from the settings screen until you have the desired settings locked in.

Confirmed with Swisslog v. 5.116.

### AC Log

1. Go to **Settings → Application Programming Interface**.
2. Enable **Listen for WSJT-X**.
3. Open the **Configure** dialog.
4. Set the listening port to `2237`.

Next, in PoLo:

1. Go to **Logging → Live QSO logging → UDP ADIF**.
2. Confirm **Enabled** is set.
3. Set the destination to the computer running AC Log, for example `192.168.73.73:2237`.
4. Set **Message format** to `WSJT-X compatible type 5`.
5. Use **Send test ADIF** from the settings screen until you have the desired settings locked in.

Confirmed with AC Log v. 7.0.12.

### HRD

#### Method 1: N1MM Message

1. Go to **Tools → Configure → QSO Forwarding**.
2. In **UDP Send**, disable **Forward logbook changes**.
3. In **UDP Receive**, enable **Receive QSO notifications using UDP5/ADIF XML (eg. TR4W, N1MM)**.
4. In the address dropdown, choose **All IPs (0.0.0.0)**.
5. Disable **Receive QSO notifications using UDP9/ADIF from other programs (eg. WSJT-X)**.

Next, in PoLo:

1. Go to **Logging → Live QSO logging → N1MM Message**.
2. Confirm **Enabled** is set.
3. Set the destination to the address and port used by the HRD UDP receive setting, for example `192.168.73.73:12060`.
4. Use **Send test ADIF** from the settings screen until you have the desired settings locked in.

#### Method 2: UDP ADIF

1. Go to **Tools → Configure → QSO Forwarding**.
2. In **UDP Send**, disable **Forward logbook changes**.
3. In **UDP Receive**, enable **Receive QSO notifications using UDP9/ADIF from other programs (eg. WSJT-X)**.
4. In the address dropdown, choose **All IPs (0.0.0.0)**.
5. Disable **Receive QSO notifications using UDP5/ADIF XML (eg. TR4W, N1MM)**.

Next, in PoLo:

1. Go to **Logging → Live QSO logging → UDP ADIF**.
2. Confirm **Enabled** is set.
3. Set the destination to the address and port used by the HRD UDP receive setting, for example `192.168.73.73:2237`.
4. Choose either `Raw ADIF` or `WSJT-X type 12`.
5. Use **Send test ADIF** from the settings screen until you have the desired settings locked in.

Confirmed with HRD v. 6.9.0.

## Troubleshooting

If the QSO does not appear where expected, check these first:

- PoLo is using the correct output mode for that software.
- The destination in PoLo uses the correct computer IP address and port.
- The receiving software is listening on that same port.
- The phone and computer are on the same network.
- The receiving software is not filtering out the phone's IP address.
- A local firewall on the computer is not blocking the chosen UDP port.
- Software not listed on this page should be treated as unverified until someone actually tests it.

### Advanced

- On Android, `N1MM Message` can use broadcast to feed more than one program at the same time, but that traffic ordinarily stays on the same network segment.
- You can send live UDP traffic to a computer at home while using mobile data. If you do that without a VPN, you will need to port forward the relevant UDP port on your home network to the receiving machine.
- The same approach also works for N1MM-style XML. In that case, send unicast traffic to your home IP and forward port `12060` to the machine receiving the XML stream.
- Not all ham software treats the IP field the same way. In some programs it acts as a filter, in others it selects the local interface to bind to, and a few become awkward when asked to bind to a non-RFC1918 address.
- The HTTP endpoint sends plain ADIF as `text/plain` in the request body. New QSOs go out as `POST`. If edit forwarding is enabled, PoLo uses `PUT` for edits; if delete forwarding is enabled, it uses `DELETE` for removals. That makes it useful for custom integrations, bridges, dashboards, or automation tools such as Node-RED, n8n, or Home Assistant.
- If you build something interesting with the HTTP path, I would genuinely like to hear about it. [Raise an issue on GitHub](https://github.com/yo3gnd/app-polo).
