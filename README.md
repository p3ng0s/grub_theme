# grub_theme
p3ng0s grub theme

## Install the theme:
```bash
sudo mkdir -p /usr/share/grub/themes/
sudo git clone https://github.com/p3ng0s/grub_theme.git /usr/share/grub/themes/p3ng0s/
```

## Activate grub theme in the grub.cfg file:
```grub.cfg
if loadfont ($root)/usr/share/grub/themes/p3ng0s/fonts/hacknerd_12.pf2; then
    loadfont ($root)/usr/share/grub/themes/p3ng0s/fonts/hacknerd_14.pf2
    loadfont ($root)/usr/share/grub/themes/p3ng0s/fonts/hacknerd_16.pf2
    set theme=($root)/usr/share/grub/themes/p3ng0s/theme.txt
    export theme
fi
```
Make sure `GRUB_THEME` is not set in `/etc/default/grub` or it will override this config on next `grub-mkconfig` run.
