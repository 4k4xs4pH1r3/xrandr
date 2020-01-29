# xrandr
This is a tool to create and configure your virtual & physical monitor using the below parameters:

Pre-Requisite: Have installed your Graphic Adapters Firmware & Drivers


Resolution
    1920x1080 
    
Refresh Rate
    75Hz 
#
#
#
1. Identify the name of your virtual monitor connected

    sudo xrandr
#
#
#
# For Virtual Monitor 75Hz

(In my case is= DisplayPort-0)

    sudo gtf 1920 1080 75 && sudo xrandr --newmode "1920x1080_75.00" 173.00 1920 2048 2248 2576 1080 1083 1088 1120 -hsync +vsync && sudo xrandr --addmode DisplayPort-0 1920x1080_75.00 && sudo xrandr --output DisplayPort-0 --mode "1920x1080_75.00"
#
# For Virtual Monitor 60Hz

(In my case is= DisplayPort-0)

    sudo gtf 1920 1080 60 && sudo xrandr --newmode "1920x1080_60.00"  172.80  1920 2040 2248 2576  1080 1081 1084 1118  -HSync +Vsync && sudo xrandr --addmode DisplayPort-0 1920x1080_60.00 && sudo xrandr --output DisplayPort-0 --mode "1920x1080_60.00"
#
# For External Monitor 75Hz
(In my case is= DP-1)

    sudo gtf 1920 1080 75 && sudo xrandr --newmode "1920x1080_75.00"  220.64  1920 2056 2264 2608  1080 1081 1084 1128  -HSync +Vsync && sudo xrandr --addmode DP-1 1920x1080_75.00 && sudo xrandr --output DP-1 --mode "1920x1080_75.00"
    
# For External Monitor 60Hz
(In my case is= DP-1)

    sudo gtf 1920 1080 60 && sudo xrandr --newmode "1920x1080_60.00"  172.80  1920 2040 2248 2576  1080 1081 1084 1118  -HSync +Vsync && sudo xrandr --addmode DP-1 1920x1080_60.00 && sudo xrandr --output DP-1 --mode "1920x1080_60.00"    
    
    
# For VMware Linux virtual machine 60Hz
(In my case is= Virtual1)

    sudo gtf 1920 1080 60 && sudo xrandr --newmode "1920x1080_60.00" 173.00 1920 2048 2248 2576 1080 1083 1088 1120 -hsync +vsync && sudo xrandr --addmode Virtual1 1920x1080_60.00 && sudo xrandr --output Virtual1 --mode "1920x1080_60.00"

# For VGA1 75Hz

    sudo gtf 1920 1080 75 && sudo xrandr --newmode "1920x1080_75.00" 173.00 1920 2048 2248 2576 1080 1083 1088 1120 -hsync +vsync && sudo xrandr --addmode VGA-1 1920x1080_75.00 && sudo xrandr --output VGA-1 --mode "1920x1080_75.00"

# For VGA1 60Hz

    sudo xrandr --newmode "1920x1080_60.00"  172.80  1920 2040 2248 2576  1080 1081 1084 1118  -HSync +Vsync && sudo xrandr --addmode VGA-1 1920x1080_60.00 && sudo xrandr --output VGA-1 --mode "1920x1080_60.00"
