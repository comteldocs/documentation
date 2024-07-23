

CentOS is an open-source Linux distribution known for its stability and reliability, making it a preferred choice for web hosting environments.

## Prerequisites

Before you begin, ensure you have:
- Minimum 10GB free disk space
- CentOS 7 ISO install file

## Step-by-Step Installation Guide

### Step 1: Download CentOS 7 ISO

Download the CentOS 7 ISO file from [CentOS.org](https://www.centos.org/download/).

### Step 2: Create Bootable Media

Use a tool like powerISO to create a bootable USB or DVD with the CentOS 7 ISO.

### Step 3: Boot from CentOS ISO

Boot your system from the bootable media containing CentOS 7. (f8 key)

### Step 4: Start CentOS Installation

1. Select "Install CentOS 7" to begin the installation process.
2. Follow the on-screen instructions to proceed.

### Step 5: Configure Installation Settings

1. **Set Language and Localization**
   - Choose installation language as English India and configure date/time settings to Asia Kolkalta.

2. **Software Selection**
   - Select desired software packages based on your needs (e.g., Minimal Install, Server with GUI).

3. **Installation Destination**
   - Choose where CentOS will be installed and configure partitioning options, if want to configure partition manually then standard partition will  be  
    1GB for boot, 1GB for boot ufi, 8GB for Swap memory , remaning all in root memory represenated by / (DO NOT ENTER ANY VALUE IN MOUNT SECTION)

4. **Network Configuration**
   - Set hostname and configure network settings, including IP addresses. select DHCP for dynamic IP allocation

5. **Security Policy**
   - Choose a security profile for your system. (KEEP UNTOUCHED)

### Step 6: Define Users and Passwords

1. **Root Password**
   - Set a secure password for the root user. (usually 123456)

2. **Create User**
   - Create a new user account with administrative privileges. (KEEP UNTOUCHED)

### Step 7: Begin Installation

Review your settings and start the installation process.

### Step 8: Complete Installation

Once installation is complete, reboot your system and log in with your credentials.

## Conclusion

You have successfully installed CentOS 7 on your system. Start exploring and configuring your new environment as needed.


