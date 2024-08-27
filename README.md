# Cisco-Packet-Tracer-Linux
You can download Cisco Packet Tracer from Cisco's official Networking Academy (NetAcad) website. To access the download, you'll need to sign up for a free account, which also provides access to resources such as tutorials and courses for using Packet Tracer effectively.



This guide explains how to install Cisco Packet Tracer on a Linux system using a `.deb` file and handle any missing dependencies.

## Steps to Install in Ubuntu

### First update you Ubuntu Machine
```bash
sudo apt update
sudo apt upgrade
```

### 1. Download the `.deb` File
Download the Cisco Packet Tracer `.deb` file from link below.

- [Cisco Packet Tracer](https://legacy.netacad.com/portal/resources/packet-tracer)
#### To access the download, you'll need to sign up for a free account, which also provides access to resources such as tutorials and courses for using Packet Tracer effectively.

### 2. Navigate to the Download Directory
Open a terminal and navigate to the directory where the `.deb` file is located:

```bash
cd ~/Downloads
```

### 3. Install the `.deb` Package

Use the `dpkg` command to install Cisco Packet Tracer:

```bash
# modify the file name with you file name
sudo dpkg -i CiscoPacketTracer822_amd64_signed.deb
```
#### If installed with no errors then Congratulations!

### 4. Resolve Missing Dependencies

If there are missing dependencies, you need to install them manually. For example, if you encounter an error related to `libxcb-xinerama0`, you can install the missing package using:

```bash
sudo apt-get install libxcb-xinerama0
```
If the packages are installed sucessfully then try to install Cisco Packet Tracer again.

```bash
# modify the file name with you file name
sudo dpkg -i CiscoPacketTracer822_amd64_signed.deb
```

If the packages are outdated or not installing then use the following links to download manually


- [ Download Missing Ubuntu Packages](https://ubuntu.pkgs.org/)

#### Select you distribution and then search for the package that is missing in the search

Download the packages with amd64 on your device and install it manually

```bash
# modify the file name with you file name
sudo dpkg -i <Package_Name>
```

### 5. Fix Remaining Dependencies

After manually installing all required packages, run the following command to automatically fix any remaining issues:

```bash
sudo apt-get install -f
```

This command will resolve any remaining unmet dependencies and finalize the installation of Cisco Packet Tracer.

### 6. Verify Installation

Once all dependencies are resolved, verify the installation by launching Cisco Packet Tracer from the terminal:

```bash
packettracer
```
If everything is installed correctly, Cisco Packet Tracer should launch successfully.

