# Linux_Mint

# Things to do after install -

## Add user to sodoers

[Link](https://linuxize.com/post/how-to-add-user-to-sudoers-in-ubuntu/)

```
whoami
```
#### **`!important`** replace `<username>` with the result of the above command (i.e. your username)

```
usermod -aG sudo <username>
```

```
EDITOR=nano visudo
```

Scroll down to the end of the file and add the following line:

```
<username>  ALL=(ALL) NOPASSWD:ALL
```


## Change swappiness and swap size

i. swapiness
```

```
ii. swap size

[link](https://arcolinux.com/how-to-increase-the-size-of-your-swapfile/)

```.sh
sudo swapoff -a
```

#### **`!important`** replace `<new-size-in-b=gb>` with the size you want

@see [ideal size for swap](https://arcolinux.com/how-to-increase-the-size-of-your-swapfile/)
![image](https://github.com/Ayush-kathayat/Linux_Mint/assets/110550492/e1666675-3de9-4943-8919-fced0abf7ce8)

```.sh
sudo dd if=/dev/zero of=/swapfile bs=1G count=<new-size-in-gb>
```

Make the file usable as swap
```.sh
sudo mkswap /swapfile
```

Activate the swap file
```.sh
sudo swapon /swapfile
```

Check the amount of swap available
```.sh
grep SwapTotal /proc/meminfo
```


## Install multimedia codecs
1. Provided by mint
2. Not included in those provided by mint
```.sh
sudo apt install ffmpeg x264 x265 h264enc mencoder mplayer
````
```.sh
sudo apt install ubuntu-restricted-extras
 ```

## Set theme Adatpta nokto
## Set numix circle icons

[Link to article](https://www.ubuntupit.com/install-numix-circle-icon-theme-ubuntu-linux-mint-fedora-desktop-environment/)

```.sh
sudo add-apt-repository ppa:numix/ppa
sudo apt-get update
sudo apt-get install numix-icon-theme
sudo apt-get install numix-icon-theme-circle
```

## Set gestures


## Setup zsh

i. Install zsh
```.sh
  sudo apt install zsh
```
ii. Set zsh as default 
```.sh
  cat /etc/shells
  # check the path of zsh (probabally /usr/bin/zsh) 

  # changing the defafult terminal to zsh
  chsh
  # choose /usr/bin/zsh (or the path you found in previous step)

  cshsh -s /usr/bin/zsh
  # replace /usr/bin/zsh with the path you found
```
iii. Restart

iv. Run zsh4humans
```.sh
if command -v curl >/dev/null 2>&1; then
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/romkatv/zsh4humans/v5/install)"
else
  sh -c "$(wget -O- https://raw.githubusercontent.com/romkatv/zsh4humans/v5/install)"
fi
```
## Setup Nala

## Add git

```.sh
sudo apt install git
```

## Add nix
[Chris titus - Getting stated with nix](https://christitus.com/nix-package-manager/)

## Install node
 you can use the Node Package Manager (npm). However, before installing npm, you need to install the Node Version Manager (nvm) first. Here is how you can do it:

Install nvm:
```.sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | zsh
```

Update your shell's environment variables:

```.sh
exec zsh
```

Install the latest version of Node.js (which includes npm) with nvm:

```.sh
nvm install node
```

You can verify your npm installation with the --version option:

```.sh
npm --version
```

## Install gotop

```
sudo npm install -g gtop
```

## Make panel tranparent

## Setup vs code

## Install any clipboard manager (eg. Didon)



