# Vroff
Vroff is a modern digital office solution developed by TellusTalk AB.

# Installation

## Windows .exe (TODO: Sign the executable)
To install Vroff on Windows using an executable file, download and run vroff_installer.exe from [here](https://drive.google.com/drive/folders/13NssK8fSgM_vnT35vOopNOgkKHdZf2wL?usp=drive_link). This executable has not yet obtained a code signing certificate, so antivirus programs will raise alarms when installing it.

## Windows Microsoft Store (TODO: Add appplication to Microsoft Store)
To install Vroff on Windows using the Microsoft Store, download and run Vroff from [here](https://www.microsoft.com/store/productId/9NCBCSZSJRSB?ocid=pdpshare).

## Linux .deb
### 1. Download and import the public key from the repository
    wget https://github.com/wbigert/vroff-releases/blob/main/public-key.asc
    gpg --import public-key.asc

### 2. Download the .deb Package and its Signature
    wget https://github.com/wbigert/vroff-releases/releases/download/v0.1.0-alpha/vroff.deb
    wget https://github.com/wbigert/vroff-releases/releases/download/v0.1.0-alpha/vroff.deb.sig

### 3. Verify the signature
    gpg --verify vroff.deb.sig vroff.deb

### 4. Install the .deb package
    sudo dpkg -i vroff.deb
    sudo apt-get install -f

### 5. If there are missing dependencies, you may have to install them manually. When testing in WSL Ubuntu 22.04.3 LTS, the following libraries had to be installed:
    sudo apt install libgbm1
    sudo apt install libasound2

## Linux .AppImage
### 1. Download and import the public key from the repository
    wget https://github.com/wbigert/vroff-releases/blob/main/public-key.asc
    gpg --import public-key.asc

### 2. Download and import the public key from the repository
    wget https://github.com/wbigert/vroff-releases/releases/download/v0.1.0-alpha/vroff.AppImage
    wget https://github.com/wbigert/vroff-releases/releases/download/v0.1.0-alpha/vroff.AppImage.sig

### 3. Verify the signature
    gpg --verify vroff.AppImage.sig vroff.AppImage

### 4. Make the .AppImage executable
    chmod +x vroff.AppImage

### 5. Run the .AppImage
    ./vroff.AppImage
