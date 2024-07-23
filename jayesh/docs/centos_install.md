# Instructions Guide

This guide provides step-by-step instructions on various tasks related to system setup and configuration.

## Prerequisites

- **A CentOS system**
- **Root access**

## Step-by-Step Instructions

### 1. How to Copy CD

#### Create Directory
1. Create a directory to store the copied CD content:
    ```sh
    mkdir -p /home/tools/centos7.9
    ```

#### List Block Devices
2. List block devices to identify the CD drive:
    ```sh
    lsblk
    ```

#### Mount CD Drive
3. Mount the CD drive:
    ```sh
    mount /dev/sr0 /media/
    ```

#### Copy CD Content
4. Copy the content from the CD to the created directory:
    ```sh
    cd /media
    ls
    cp -r * /home/tools/centos7.9/
    ```

#### Verify Content
5. Verify the copied content:
    ```sh
    du -sh /home/tools/centos7.9/
    ```

### 2. How to Create Repo

#### Navigate to Repos Directory
1. Change to the YUM repository configuration directory:
    ```sh
    cd /etc/yum.repos.d
    ```

#### Create Repo File
2. Create a new repository file:
    ```sh
    vi local.repo
    ```

#### Add Repo Details
3. Add the following content to the file:
    ```text
    [local]
    name=local
    baseurl=file:///home/tools/centos7.9
    enabled=1
    ```

#### Import GPG Key
4. Import the RPM GPG key:
    ```sh
    rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-centos-7
    ```

#### Organize Repo Files
5. Organize existing repo files:
    ```sh
    cd /etc/yum.repos.d
    ls
    mkdir tmp
    mv C* tmp
    ```

### 3. How to Set Firewall

#### Stop Firewall Service
1. Stop the firewall service:
    ```sh
    service firewalld stop
    ```

#### Disable Firewall Service
2. Disable the firewall service to prevent it from starting at boot:
    ```sh
    systemctl disable firewalld
    ```

#### Check Firewall Status
3. Check the status of the firewall service:
    ```sh
    systemctl status firewalld
    ```

### 4. How to Set Kernel

#### Edit GRUB Configuration
1. Edit the GRUB configuration file:
    ```sh
    vi /etc/default/grub
    ```

#### Add Kernel Parameters
2. Add the following parameters to the GRUB_CMDLINE_LINUX line:
    ```text
    selinux=0 intel_idle.max_cstate=0 processor.max_cstate=0
    ```

#### Update GRUB Configuration
3. Update the GRUB configuration:
    ```sh
    grub2-mkconfig -o /boot/grub2/grub.cfg
    ```

### 5. How to Disable Selinux

#### Edit Selinux Configuration
1. Edit the SELinux configuration file:
    ```sh
    vi /etc/sysconfig/selinux
    ```

#### Disable Selinux
2. Set SELINUX to disabled:
    ```text
    SELINUX=disabled
    ```

### 6. How to Run Different Profiles

#### Run Latency-Performance Profile
1. Run the latency-performance profile:
    ```sh
    tuned-adm profile latency-performance
    ```

#### Run Network-Latency Profile
2. Run the network-latency profile:
    ```sh
    tuned-adm profile network-latency
    ```

### 7. How to Install Packages Using Yum

#### List Available Packages
1. List all available packages:
    ```sh
    yum list
    ```

#### Install Specific Packages
2. Install the desired packages:
    ```sh
    yum install nano net-tools telnet pciutils lsof libxml2-python
    ```
