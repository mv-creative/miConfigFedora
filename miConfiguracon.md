´´´shell
sudo nano /etc/dnf/dnf.conf
´´´
fastestmirror=True
max_parallel_downloads=10
defaultyes=True



"sudo dnf install google-chrome-stable"

#rpmfusion
sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm

#paquetes de microsoft y vscode
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'

dnf check-update
"sudo dnf update"

#retoques
sudo dnf install gnome-tweak-tool

#Install GNOME Extensions:
sudo dnf install chrome-gnome-shell gnome-extensions-app

#vscode
sudo dnf install code

#java
https://docs.fedoraproject.org/en-US/quick-docs/installing-java   
sudo dnf install java-11-openjdk-devel.x86_64

#c#
https://docs.microsoft.com/es-es/dotnet/core/install/linux-fedora   
sudo dnf install dotnet-sdk-5.0

#vlc
sudo dnf install vlc.x86_64

#telegram
sudo dnf install telegram-desktop.x86_64

#discord
sudo dnf install discord.x86_64 -y

#grub customizer
sudo dnf install grub-customizer.x86_64

#codecs de audio
sudo dnf install gstreamer1-plugins-{bad-\*,good-\*,base} gstreamer1-plugin-openh264 gstreamer1-libav --exclude=gstreamer1-plugins-bad-free-devel
sudo dnf install lame\* --exclude=lame-devel
sudo dnf group upgrade --with-optional Multimedia

