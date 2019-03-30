# elementary-setup

This is a description of my setup process of elementary OS including tools and settings. 
It is the only linux distro I tested that allows me to get the scaling on my laptop right how I want it in no time. 

# After a fresh install
Run `sudo apt install software-properties-common` once to get support for the `add-apt-repository` command.
Install [elementary tweaks](https://github.com/elementary-tweaks/elementary-tweaks) for custom themes and better font scaling.

Set the scaling for text and the dock size in `Settings/Desktop/Appearance` and change font size in `Settings/Tweaks/Fonts`.
Adjust terminal and files behaviour in `Settings/Tweaks`.
Install and choose theme in `Settings/Tweaks/Appearance`. I recommend [Ant Nebula](https://github.com/EliverLara/Ant-Nebula) as gtk+ theme and [Papirus](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme) for icons.

Change the behaviour of the `Super` key in `Settings/Keyboard` to `Applications Menu` and enable a `Compose key` to be able to write German Umlaute with my US keyboard.

Install `GNOME Disks` and use it to automount my data partition. 

Install 'tlp' for power saving on my laptop.

Add my SSH keys to `~/.ssh` and set the correct permissions with: 
```
chmod 700 ~/.ssh
chmod 644 ~/.ssh/authorized_keys
chmod 644 ~/.ssh/known_hosts
chmod 644 ~/.ssh/config
chmod 600 ~/.ssh/id_rsa
chmod 644 ~/.ssh/id_rsa.pub
chmod 600 ~/.ssh/github_rsa
chmod 644 ~/.ssh/github_rsa.pub
```
Finally, add ssh keys:
```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
ssh-add ~/.ssh/github_rsa
```
