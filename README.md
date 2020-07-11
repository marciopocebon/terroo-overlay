# terroo-overlay
Gentoo Portage Overlay for Layman

# Prerequisites
Do you have Layman already installed on your system? If '**No**', run the commands below before using this Overlay
```
sudo emerge layman
sudo mkdir -p /var/lib/layman/
sudo touch /var/lib/layman/make.conf
echo 'source /var/lib/layman/make.conf' | sudo tee -a /etc/portage/make.conf
sudo layman -S
sudo emerge --sync
```

# Use this Overlay
```
sudo mkdir -p /etc/layman/overlays
sudo wget https://raw.githubusercontent.com/terroo/terroo-overlay/master/terroo.xml -O /etc/layman/overlays/terroo-overlay.xml
sudo layman-updater -R
sudo layman -o https://raw.githubusercontent.com/terroo/terroo-overlay/master/terroo.xml -f -a terroo-overlay
sudo layman -S
sudo layman -a terroo-overlay
```
> Confirm: `layman -L 2>&1 | grep terroo`

# Install programs
> Example

```
sudo emerge -1 visual-studio-code
```

Report bugs: <https://github.com/terroo/terroo-overlay/issues>
