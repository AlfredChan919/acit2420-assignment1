# How to Set up Arch Linux on a DigitalOcean Droplet

# Introduction
DigitalOcean is a cloud computing platform that allows you to create virtual machine instances called Droplets on their servers. This allows you to access your remote server from anywhere as well as relieving your own machine of its resources.

# Overview
This guide is desgined with the base knowledge of a CIT student entering term 2 in week 1. This guide will also take you through:

1. [Download Arch Linux](#download-arch-linux)
2. [Upload custom image onto DigitalOcean](#upload-custom-image-to-digitalocean)
3. Creating and connecting SSH keys on your local machine
4. Creating up your DigitalOcean Droplet with Arch Linux
5. Creating and implementing a cloud-init configuration file to automate initial setup tasks
6. Lastly, thos guide will show you how to connect to your remote server using the SSH keys.

## Download Arch Linux
Before beginning, first you need to download a custom Arch Linux image from: 

https://gitlab.archlinux.org/archlinux/arch-boxes/-/packages/

Make sure to select the latest image post. Also, make sure the download contains the word "cloudimg" and ends with the file extension ".qcow2".

## Upload Custom Image to DigitalOcean
By uploading our own custom image, we can use it to create our Droplets with Arch Linux. This allows us to create a consistent environment by utilizing the custom image alongside our own cloud-init settings. 

1. Click <b>Manage</b> on the left-hand side menu.
<img src="assets/digitalocean1.png" alt = "Digital Ocean Instruction">
2. Select <b>Backups & Snapshots</b> from the left menu


## Create SSH keys