# Extra features via a computer

Connect the phone to a computer with a cable once, run our helper — and XiaoDroidLink gets two abilities Android does not give to ordinary apps:

| What | Without the helper | With the helper |
|---|---|---|
| You lock the phone with the button | music in the car stops, the car reconnects | **music keeps playing, the connection stays** |
| "Allow screen casting" prompt | on every connection | **never** |
| Phone lies still during the drive | dim | **almost black** (normal in your hand) |
| Android stopped the car control service ("service is not working properly") | turn it off and on by hand | **restarts by itself** |

XiaoDroidLink works without the helper too — these are only improvements. Everything can be turned off with the same helper.

You need: a computer (Windows, Mac or Linux), a USB cable, XiaoDroidLink **8.26 or newer**. Takes 5 minutes.

---

## Step 1. Turn on "USB debugging" on the phone

You do this once.

**Samsung**
1. Settings → **About phone** → **Software information**.
2. Tap **"Build number" 7 times**. It may ask for the phone PIN. You will see "Developer mode has been turned on".
3. Back to Settings → at the very bottom **"Developer options"**.
4. Turn on **"USB debugging"**.

**Xiaomi, Redmi, POCO**
1. Settings → **About phone**.
2. Tap **"OS version"** (or "MIUI version") **7 times**.
3. Settings → **Additional settings** → **Developer options**.
4. Turn on **"USB debugging"** and **"USB debugging (Security settings)"**.
   For the second one Xiaomi requires a Mi account sign-in and a SIM card in the phone.

**Other phones** (Honor, vivo, OnePlus, Pixel, Motorola…)
1. Settings → **About phone** → tap **"Build number" 7 times**.
2. Settings → **System** → **Developer options** (or search the settings for "developer").
3. Turn on **"USB debugging"**.

## Step 2. Download the helper

**[⬇ XiaoDroidLink-Helper.zip](https://github.com/vvkovtun/xiaodroidlink-releases/raw/main/helper/XiaoDroidLink-Helper.zip)**

**Unzip** it (right-click → "Extract All" / double-click on a Mac). There are three files inside — you only need the one for your computer.

## Step 3. Connect the phone with the cable and run it

**Windows**
- Double-click **`XiaoDroidLink-Helper-Windows.bat`**.
- If a blue "Windows protected your PC" window appears → **"More info"** → **"Run anyway"**.

**Mac**
- **Right-click** (or Control-click) **`XiaoDroidLink-Helper-Mac.command`** → **"Open"** → **"Open"** again.
- If the Mac says it cannot open it: System Settings → **Privacy & Security** → at the bottom **"Open Anyway"**.

**Linux**
- Open a terminal in the folder with the file and type: `bash XiaoDroidLink-Helper-Linux.sh`

The helper downloads the Android tools it needs from Google (about 7 MB) by itself — nothing to install.

## Step 4. Answer the helper

1. Choose the language: **1** and Enter.
2. The phone shows **"Allow USB debugging?"** → tick **"Always allow"** → **"Allow"**.
3. The helper says "Phone found" and shows a menu. Type **1** and Enter.
4. You see **"Done ✓"**. Unplug the cable — that's it.

---

## How to turn it off

Run the helper the same way and choose:
- **2** — turn everything off, back to normal;
- **3** — only switch off the dark screen.

You can switch off the dark screen without a computer too: pull down the phone's quick settings → **"Extra dim"** button.

## If something does not work

| The helper says | What to do |
|---|---|
| "The phone is not visible" | Another cable (some only charge). Check that "USB debugging" is on. On the phone choose "File transfer" for USB. |
| "The phone is not visible" only on Windows | Windows needs the phone driver. Samsung: install "Samsung USB Driver" from samsung.com. Others usually install by themselves — wait a minute after plugging in. |
| The "Allow USB debugging" window does not appear | Unplug and plug the cable in again, unlock the phone. |
| "XiaoDroidLink is too old" | Update XiaoDroidLink in Google Play and run the helper again. |
| "Partly done" on Xiaomi | Turn on "USB debugging (Security settings)" (step 1) and run again. |
| "Did not work" | Send the text from the helper window via "Something not working? Send report" in the app. |

The permissions stay after XiaoDroidLink updates and disappear only when it is uninstalled.
