
# Running Flatpak Apps in Windows 10/11


<p align="center">
  <img src="https://i.imgur.com/DFz8qMa.png"/>
</p>

🪧 (Own Ad) How create Shortcut to Suspend Windows 11: [My Github Tuturial](https://github.com/AbelFalcon/Shortcut-to-Suspend-Windows11).

## Introduction

Flatpak is a system for building, distributing, and running sandboxed desktop applications on Linux. However, you might want to run Flatpak apps on Windows 10/11 for various reasons, including testing, development, or simply using your favorite Linux applications. This guide will show you how to do that.

## Prerequisites

Before you start, ensure you have the following:
- A computer running Windows 10 or Windows 11
- Administrator privileges
- [Windows Subsystem for Linux (WSL)](https://docs.microsoft.com/en-us/windows/wsl/install) installed
- A Linux distribution installed via WSL (e.g., Ubuntu)

## Step-by-Step Guide

## Setup Xming

Xming for Windows

 https://sourceforge.net/projects/xming/

- Install [(In-depth tutorial)](https://www.uwyo.edu/data-science/resources/knowledge-base/x11-with-windows-subsystem-for-linux.html)
- Run the program.

## WSL Setup

- Open "WSL Ubuntu"
> Actually. You can use other distros. I have bought that works on Ubuntu and Fedora (Microsoft Store
- Paste the following command

```bash
 export DISPLAY=:0
```
**If it does not work in the subsequent steps. Use your local ip address instead of 0.**

- Update the system 

```bash
 sudo apt update
```
- Install Flatpak

```bash
 sudo apt install flatpak
```

- Add Flatpak Flathub repo

```bash
 flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

```

- Ready! Now you can install any app and run it normally. 

# Example Usage

Install app

```bash
 sudo flatpak install flathub io.github.alainm23.planify
```

Run App

```bash
 flatpak run io.github.alainm23.planify
```

# Troubleshooting

If you encounter any issues, consider the following steps:

- Ensure WSL is properly installed and running
- Check for updates and upgrade your Linux distribution
- Verify the Flatpak installation and the Flathub repository addition
