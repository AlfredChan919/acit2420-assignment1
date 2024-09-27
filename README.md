# How to Set up Arch Linux on a DigitalOcean Droplet

# Introduction
DigitalOcean is a cloud computing platform that allows you to create virtual machine instances called Droplets on their servers. This allows you to access your remote server from anywhere as well as relieving your own machine of its resources.

# Overview
This guide is desgined with the base knowledge of a CIT student entering term 2 in week 1. This guide will also take you through:

1. [Download Custom Arch Linux Image](#download-custom-arch-linux-image)
2. [Upload custom image onto DigitalOcean](#upload-custom-image-to-digitalocean)
3. [Creating and Connecting SSH Key Pair onto DigitalOcean](#creating-and-connecting-ssh-key-pair-onto-digitalocean)
4. Creating up your DigitalOcean Droplet with Arch Linux
5. Creating and implementing a cloud-init configuration file to automate initial setup tasks
6. Lastly, thos guide will show you how to connect to your remote server using the SSH keys.

## Download Custom Arch Linux Image
Before beginning, first you need to download a custom Arch Linux image from: 

https://gitlab.archlinux.org/archlinux/arch-boxes/-/packages/

Make sure to select the latest image post. Also, make sure the download contains the word "cloudimg" and ends with the file extension ".qcow2".

## Upload Custom Image to DigitalOcean
By uploading our own custom image, we can use it to create our Droplets with Arch Linux. This allows us to create a consistent environment by utilizing the custom image alongside our own cloud-init settings. 

1. Click **Manage** on the left-hand side menu
<img src="assets/digitalocean1.png" alt = "Digital Ocean Instruction">
<br></br>

2. Select **Backups & Snapshots** from the left menu
<img src="assets/digitalocean2.png" alt = "Digital Ocean Instruction">
<br></br>

3. Select **Custom Images**
<img src="assets/digitalocean3.png" alt = "Digital Ocean Instruction">
<br></br>

4. Select **Upload Image**
<img src="assets/digitalocean4.png" alt = "Digital Ocean Instruction">
<br></br>

5. Find the Arch Linux image that you downloaded and open it
<img src="assets/digitalocean5.png" alt = "Digital Ocean Instruction">
<br></br>

6. Click on **Distribution** and from the drop-down list, select **Arch Linux**
<img src='assets/digitalocean6.png' alt='Digital Ocean Instruction'>
<br></br>

7. Select a datacenter and click **Upload Image**
Note: You want to select the server closest to your location to reduce latency and improve response times.
<img src='assets/digitalocean7.png' alt='Digital Ocean Instruction'>

## Creating and Connecting SSH Key Pair onto DigitalOcean
In order for you to securely connect your current machine to the remote server, you must first create an SSH key pair from your current machine and upload the public key onto DigitalOcean for it to connect.

If you are running Windows and have never made an SSH key before, you may need to create a .ssh folder in your home directory. You can perform this by opening Windows PowerShell and typing the command:

```
mkdir .ssh
```
*mkdir - creates a new directory*
*.ssh - the name of the directory*

Double check that the directory was created or exists by typing the command:
```
ls
```
*ls - list directory contents*
<img src="assets/sshkey1.png" alt = "SSH key instructions">
<br></br>

1. Type the following command to create a new SSH key pair:
```
ssh-keygen -t ed25519 -f C:\Users\your-user-name\.ssh\name-of-key -C "your-email@email.com"
```
**Note**: Change "your-user-name" to the correct name in the terminal. Change the "name-of-key" to something relevant such as do-key as well as change "your-email.com" to your actual email.



2. 