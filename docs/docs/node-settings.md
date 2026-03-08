# Node Configuration
*Through the Meshtastic app*

---

!!! info "Information"
    This website is very beta. Many pages are broken or they just don't exist. Please be patient, I am only one person. Thanks!

!!! note "Disclaimer"
    This guide is written by a local Ollama AI on my Computer, things may be inaccurate or wrong, this is also not the completed page either, there will be an update sooner or later making it look a bit nicer

---

Unfortunatly this part of the site isn't acutally done yet, however configuration of a meshtastic device is simple and a guide is below,

## Guide for Client Nodes

# Configuring Your Meshtastic Device

---

## Prerequisites

Before diving in, make sure you have the following ready:

* A Meshtastic device that is powered on and already flashed with the latest firmware. 
    (See [Getting Started](getting-started.md))
* The **Meshtastic app** installed on your phone.
* Bluetooth enabled on your smartphone.

---

## Step 1: Connect to Your Device via Bluetooth

To configure your node, your phone needs to establish a secure Bluetooth connection with it.

1. **Open the Meshtastic App:** Launch the app on your phone.
2. **Add a Device:** On Android, tap the **+** (plus) icon in the lower right corner. On iOS, navigate to the **Settings** tab, tap **Device**, and look for the Bluetooth menu.
3. **Select Your Node:** The app will scan for nearby Bluetooth Low Energy (BLE) devices. Tap your radio from the list (often showing its hardware name, like "Meshtastic_XXXX").
4. **Enter the Pairing PIN:** Look at the small OLED screen on your Meshtastic device. It will display a 6-digit pairing PIN. Enter this PIN into your phone to complete the pairing. 
5. **Set Your Region:** Set your region to EU_868 as that is what is legal in the United Kindom 

!!! tip "Default PIN"
    If your specific Meshtastic board does not have a screen, the default pairing PIN is almost always **123456**.

!!! warning "Region Settings"
    You must set the correct region for your physical location, as the radio will not transmit legally or effectively without it.

---

## Step 2: Set the Device Role to "Client"

The Device Role determines how your node behaves on the mesh. `CLIENT` is the standard role for a device you plan to carry with you or use for daily messaging. 

1. Tap the **Settings** icon (the gear in the top right or bottom navigation bar).
2. Select **Radio Configuration**.
3. Tap on **Device**.
4. Locate the **Role** dropdown menu.
5. Select **CLIENT**. 

!!! note "Why Client?"
    This is usually the default out of the box, but verifying it ensures your device will both send your messages and help efficiently route packets for other nodes on the network.

---

## Step 3: Configure LoRa Settings

Next, we need to adjust how the radio waves are structured and how far your messages are allowed to travel across the mesh.

1. Back out to the main **Radio Configuration** menu.
2. Tap on **LoRa**.
3. **Set Modem Preset:** Locate the **Modem Preset** setting and select **LONG_FAST**. This is widely considered the best balance between range and data speed, and it is the standard for the default public network.
4. **Set the Hop Limit:** Scroll down to find **Hop Limit** (sometimes labeled **Max Hops**) and change the value to **4**. 

!!! warning "A Note on Hop Limits"
    The default hop limit is 3. A limit of 4 means your message can bounce through up to 4 intermediate nodes before it is dropped. While this extends your range, be careful not to set it higher unless strictly necessary. High hop limits easily congest the network for everyone.

---

## Step 4: Save and Apply

1. Once you have made these changes, look for a **Save**, **Apply**, or **Send to Device** button (usually a small paper airplane or save icon in the top right corner). 
2. Tap it. The app will send these configurations to your node.

Your Meshtastic device will likely reboot to apply the new radio settings. This takes just a few seconds. Once it boots back up, it will automatically reconnect to your phone, and you are ready to communicate!

---

## Guide for Repeaters

# Configuring your Meshtastic Device

!!! note "Incomplete"
    I haven't gotten around to this one yet, stay tuned

---

