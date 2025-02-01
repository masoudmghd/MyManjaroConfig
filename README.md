# My Manjaro with i3

Some config for using manjaro as my main workspace

## Terminal
Create a bash in ~/.local/bin/terminal.

```
#!/bin/sh

alacritty $@
```
Note : permission -> -rwxr-xr-x
## Picom

```
#################################
#
# Opacity
#
#################################

inactive-opacity = 0.80;
active-opacity = 0.80;
frame-opacity = 0.80;

opacity-rule = [
    #"100:name *= 'Chrome'",
    "99:class_g = 'Google-chrome'"
];

inactive-opacity-override = false;

# Dim inactive windows. (0.0 - 1.0)
# inactive-dim = 0.2;
# Do not let dimness adjust based on window opacity.
# inactive-dim-fixed = true;
# Blur background of transparent windows. Bad performance with X Render backend. GLX backend is preferred.
blur-background = true;
# Blur background of opaque windows with transparent frames as well.
blur-background-frame = true;
# Do not let blur radius adjust based on window opacity.
blur-background-fixed = false;
blur-background-exclude = [
    "window_type = 'dock'",
    "window_type = 'desktop'",
    "class_g = 'Google-chrome'"
];

#################################
```

## dotnet
dotnet3.1 : openssl1.1 - yay openssl-1.1 
dotnet3.1 : libicu70 - yay icu70
