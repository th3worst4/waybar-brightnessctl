# What is it?
It's a simple bash script written to better integrate the `brightnessctl` utility with the [waybar](https://github.com/Alexays/Waybar) status bar. This script allows the user to define a mininum brightness to it's backlight so the monitor doesn't turn entirely off.

# How to configure?
The user can change the step and the mininum brightness by simply changing the values on **line 7**, **line 13** and **line 16**. Lines 7 and 16 sets the step up and step down respectively, line 13 defines the minimum brightness.

# How to integrate it with waybar?
The following snippet shows how to use it on the waybar
```
"backlight": {
        "format": "{percent}% {icon}",
        "format-icons": ["", "", "", "", "", "", "", "", ""],     
        "on-scroll-up": "/home/caioc/.config/waybar/brightnessoperation.sh +",
        "on-scroll-down": "/home/caioc/.config/waybar/brightnessoperation.sh -"
},
```
Just change the `on-scroll-up` and `on-scroll-down` configurations on your waybar's config.jsonc.
