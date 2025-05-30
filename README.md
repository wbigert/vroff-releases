# vroff
vroff is a modern digital office solution developed by TellusTalk AB.

# Installation

## Windows
To download and run vroff on Windows using the Microsoft Store, go to ... Optionally, download and run ```vroff.exe``` from the [latest release](https://github.com/wbigert/vroff-releases/releases). This executable is not signed, so antivirus programs may raise alarms when installing it.

## Mac
To install vroff on Mac, download the .dmg file from the [latest release](https://github.com/wbigert/vroff-releases/releases). For Intel-based Macs, use ```vroff_x64.dmg```, else use ```vroff_arm64.dmg```

## Android & iOS
To install vroff on Android or iOS, open [https://lab.vroff.com](https://lab.vroff.com) on your phone and open either your browser's settings or tap "Share", and select "Add to Home Screen".

## Linux (.deb)
### 1. Download the .deb Package and optionally its signature from the [latest release](https://github.com/wbigert/vroff-releases/releases).
    wget https://github.com/wbigert/vroff-releases/releases/download/v1.0.0/vroff.deb
    wget https://github.com/wbigert/vroff-releases/releases/download/v1.0.0/vroff.deb.sig 

### 2. Download and import the public key from this repository (optional, but recommended)
    wget https://raw.githubusercontent.com/wbigert/vroff-releases/main/public-key.asc

    gpg --import public-key.asc

### 3. Verify the signature (optional, but recommended)
    gpg --verify vroff.deb.sig vroff.deb

### 4. Install the .deb package
    sudo dpkg -i vroff.deb
    sudo apt-get install -f

### 5. If running in WSL, additional dependencies may have to be installed, such as:
    sudo apt install libgbm1
    sudo apt install libasound2

### 6. Run the program
    /opt/vroff/vroff

## Linux (.AppImage)
### 1. Download the .AppImage and optionally its signature from the [latest release](https://github.com/wbigert/vroff-releases/releases).
    wget https://github.com/wbigert/vroff-releases/releases/download/v1.0.0/vroff.AppImage
    wget https://github.com/wbigert/vroff-releases/releases/download/v1.0.0/vroff.AppImage.sig

### 2. Download and import the public key from the repository (optional, but recommended)
    wget https://raw.githubusercontent.com/wbigert/vroff-releases/main/public-key.asc
    gpg --import public-key.asc

### 3. Verify the signature (optional, but recommended)
    gpg --verify vroff.AppImage.sig vroff.AppImage

### 4. Make the .AppImage executable
    chmod +x vroff.AppImage

### 5. Run the .AppImage
    ./vroff.AppImage
