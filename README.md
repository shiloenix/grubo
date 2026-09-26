# grubo

> A collection of GRUB themes.

It is my repository for custom GRUB themes, experiments, and different visual styles for the GRUB bootloader.

## Themes

Each theme is kept in its own directory:

```text
grubo/
├── theme-1/
├── theme-2/
├── theme-3/
└── README.md
```

More themes will be added over time.

## Installation

Clone the repository:

```bash
git clone https://github.com/shiloenix/grubo.git
cd grubo
```

Choose the theme you want to install and copy it to the GRUB themes directory:

```bash
sudo mkdir -p /boot/grub/themes
sudo cp -r <theme> /boot/grub/themes/
```

## Enable a theme

Edit `/etc/default/grub`:

```bash
sudo nano /etc/default/grub
```

Set `GRUB_THEME` to the theme's `theme.txt`:

```ini
GRUB_THEME="/boot/grub/themes/red/theme.txt"
```

Then regenerate the GRUB configuration:

```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

Reboot:

```bash
reboot
```

## Uninstall

Remove the theme from `/boot/grub/themes`:

```bash
sudo rm -rf /boot/grub/themes/<theme>
```

Then remove or change the `GRUB_THEME` entry in `/etc/default/grub`.

Regenerate the configuration:

```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

## Requirements

* GRUB 2
* A Linux system using GRUB
* GRUB theme support


