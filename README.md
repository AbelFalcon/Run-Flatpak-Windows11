
# Running Flatpak Apps in Windows 10/11

Running flatpak applications on Windows has never been easier. Now with WSL and Xming you can do it in seconds. 

<p align="center">
  <img src="https://i.imgur.com/DFz8qMa.png"/>
</p>

## Setup Xming

Xming for Windows

 https://sourceforge.net/projects/xming/

- Install
- Run the program.

## WSL Setup

- Open "WSL Ubuntu" 
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
 sudo apt install Flatpak
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
