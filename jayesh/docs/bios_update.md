# BIOS Update Guide

This guide provides step-by-step instructions on how to update the BIOS on a server using a USB drive.

## Prerequisites

- **A USB drive** formatted to FAT32
- **Access to the manufacturer's website** to download the latest BIOS
- **Basic knowledge** of accessing BIOS settings

## Step-by-Step Instructions

### 1. Identify the Current BIOS Version

#### Boot the Server
1. Power on the server and press the appropriate key to enter the BIOS setup (commonly `F2`, `F10`, `DEL`, or `ESC`).

#### Check the BIOS Version
2. Navigate to the BIOS Information section (this may vary based on the manufacturer).

### 2. Download the Latest BIOS

#### Visit the Manufacturer's Website
1. Go to the support or download section of the server's manufacturer website.

#### Identify the Correct BIOS
2. Enter the server model number or serial number to find the appropriate BIOS update.

#### Download the BIOS Update
3. Download the latest BIOS update file and any accompanying utilities to your computer.

### 3. Prepare the USB Drive

#### Format the USB Drive
1. Format the USB drive to FAT32 file system using your operating system's formatting tool.

#### Copy the BIOS Files
2. Extract the downloaded BIOS files and copy them to the root directory of the USB drive.

### 4. Update the BIOS

#### Boot from the USB Drive
1. Insert the USB drive into the server.
2. Restart the server and enter the boot menu (commonly `F12`, `ESC`, or `F8`).
3. Select the USB drive from the boot options.

#### Run the BIOS Update Utility
4. Follow the on-screen instructions to launch the BIOS update utility from the USB drive.
5. Select the BIOS update file and initiate the update process.

#### Complete the Update
6. Wait for the update process to complete. Do not power off the server during this process.
7. The server will restart automatically once the update is complete.

### 5. Verify the BIOS Update

#### Enter the BIOS Setup
1. After the server restarts, enter the BIOS setup again by pressing the appropriate key.

#### Check the BIOS Version
2. Verify that the BIOS version has been updated to the latest version as per the downloaded file.

## Troubleshooting

- If the server does not recognize the USB drive, ensure it is formatted correctly and the files are in the root directory.
- Refer to the manufacturer's documentation if specific errors occur during the BIOS update process.

## Conclusion

Updating the BIOS is a critical task to ensure your server operates efficiently and securely. Follow these steps carefully, and always ensure you have a backup before performing a BIOS update.

