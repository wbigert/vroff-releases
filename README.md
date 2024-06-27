# vroff
vroff is a modern digital office solution developed by TellusTalk AB.

# Installation

## Windows .exe
To install vroff on Windows using an executable file, download and run vroff.exe from the [latest release](https://github.com/wbigert/vroff-releases/releases). This executable is not signed, so antivirus programs may raise alarms when installing it.

## Windows Microsoft Store
To download and run vroff on Windows using the Microsoft Store go ...

## Linux .deb
### 1. Download the .deb Package and optionally its signature from the [latest release](https://github.com/wbigert/vroff-releases/releases).
    wget https://github.com/wbigert/vroff-releases/releases/download/<release_name>/vroff.deb
    wget https://github.com/wbigert/vroff-releases/releases/download/<release_name>/vroff.deb.sig 

### 2. Download and import the public key from this repository (optional, but recommended)
    wget https://github.com/wbigert/vroff-releases/blob/main/public-key.asc
    gpg --import public-key.asc

### 3. Verify the signature (optional, but recommended)
    gpg --verify vroff.deb.sig vroff.deb

### 4. Install the .deb package
    sudo dpkg -i vroff.deb
    sudo apt-get install -f

### 5. If running in WSL, additional dependencies may have to be installed, such as:
    sudo apt install libgbm1
    sudo apt install libasound2

## Linux .AppImage
### 2. Download the .AppImage and optionally its signature from the [latest release](https://github.com/wbigert/vroff-releases/releases).
    wget https://github.com/wbigert/vroff-releases/releases/download/v0.1.0-alpha/vroff.AppImage
    wget https://github.com/wbigert/vroff-releases/releases/download/v0.1.0-alpha/vroff.AppImage.sig

### 2. Download and import the public key from the repository (optional, but recommended)
    wget https://github.com/wbigert/vroff-releases/blob/main/public-key.asc
    gpg --import public-key.asc

### 3. Verify the signature (optional, but recommended)
    gpg --verify vroff.AppImage.sig vroff.AppImage

### 4. Make the .AppImage executable
    chmod +x vroff.AppImage

### 5. Run the .AppImage
    ./vroff.AppImage
