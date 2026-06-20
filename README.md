# My Manjaro with Sway Config

Some config for using manjaro as my main workspace

## pacman to use local nexus

Add the homelab.conf to your pacman.conf and comment other sections.

```
Include = /etc/pacman.d/homelab.conf
```
## Visual Studio Code

There is a bug in opening vscode in manjaro sway version, as the electron can't work properly in wayland.
The solution is to set some initial config in vscode settings.json.

```
{
    "window.titleBarStyle": "custom"
}
```

## Fonts

For better rendering Persian characters in manjaro ui and apps, we should intall some third-party opensource fonts.
And we also have to set fonts.conf in fontconfig folder.

```
<alias>
  <family>sans-serif</family>
  <prefer>
   <family>Vazirmatn</family>
  </prefer>
 </alias>
```

Fonts can be installed in .local/share/fonts.

## Keyboard

To add persian layout for keyboard, there is this config file.

```
input * {
    xkb_options grp:win_space_toggle,grp_led:caps
    xkb_layout "us,ir"
    xkb_variant ","
    xkb_numlock "enable"
}
```

## Default Browser
To set default browser to microsoft edge

```
xdg-settings set default-web-browser microsoft-edge.desktop
```

## Microsoft Edge Problems with WayLand

Edit the edge flags config file. Please be ware that the default config file is a link to ~/.config/chrome-flags.conf.

```
--ozone-platform=x11
```