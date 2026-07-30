# 🎙️ macOS Internal Audio & Microphone Recording Guide (BlackHole)

This guide covers setting up **BlackHole** on macOS to capture internal system audio and your microphone simultaneously, along with post-processing scripts and hotkeys.

---

## 💡 ELI5: How Mac Audio Routing Works

* **The Problem:** Audio in macOS is a one-way street. Sound goes out of your apps directly into your speakers and disappears into the air. macOS blocks apps from capturing system sound directly.
* **BlackHole (The Virtual Cable):** Think of BlackHole as an invisible audio cable. One end plugs into your app's sound output, and the other end plugs into a virtual microphone input so recording programs can "hear" it.
* **Multi-Output Device (The Y-Splitter):** If you route sound *only* to BlackHole, your speakers go silent. A Multi-Output Device splits the sound like a headphone Y-splitter, playing sound through your speakers **and** sending it into BlackHole at the same time.
* **Aggregate Device (The Audio Blender):** Recording apps (like QuickTime) usually let you select only *one* microphone input at a time. An Aggregate Device blends your physical microphone and BlackHole together into a single combined input stream.

---

## 🚀 Step-by-Step Setup Guide

### Step 1: Install BlackHole

#### Option A: Via Homebrew (Fastest)

Open **Terminal** and run:

```bash
brew install blackhole-2ch
```

#### Option B: Official Package Installer

1. Go to the [Existential Audio Website](https://existential.audio/blackhole).
2. Enter your email to receive the direct download link.
3. Download and open the **.pkg** file to install.

---

### Step 2: Create a Multi-Output Device (To Hear & Route Audio)

1. Press **`Cmd + Space`**, search for **Audio MIDI Setup**, and press **Enter**.
2. Click the **`+`** button in the bottom-left corner and choose **Create Multi-Output Device**.
3. Double-click the new entry in the sidebar to rename it: **`Speakers + BlackHole`**.
4. In the right-hand panel, check the boxes for:
   * **Built-in Output / Speakers** (or your headphones)
   * **BlackHole 2ch**
5. Ensure your primary speakers/headphones are listed **at the top** of the device list.
6. Check **Drift Correction** next to **BlackHole 2ch**.

---

### Step 3: Create an Aggregate Device (To Combine Mic + System Sound)

1. In **Audio MIDI Setup**, click the **`+`** button at the bottom-left again and choose **Create Aggregate Device**.
2. Double-click to rename it: **`Mic + Internal Audio`**.
3. In the right-hand panel, check the boxes for:
   * **BlackHole 2ch**
   * Your **Microphone** (e.g., *Built-in Microphone* or USB Mic)
4. Check **Drift Correction** next to your **Microphone**.

---

### Step 4: Configure Mac Sound Output

1. Open **System Settings** > **Sound**.
2. Under the **Output** tab, select **`Speakers + BlackHole`**.

> ⚠️ **Note:** macOS disables keyboard volume keys when outputting to a Multi-Output Device. Adjust your volume inside specific apps (e.g., YouTube player, Spotify) or set your desired speaker level before switching to the Multi-Output Device.

---

### Step 5: Record Both Sources

1. Press **`Cmd + Shift + 5`** to open the native screen recorder.
2. Click **Options**.
3. Under **Microphone**, select **`Mic + Internal Audio`**.
4. Hit **Record**. Your Mac will now capture both your voice and internal computer sound.
