# xrandr
This is a tool to create and configure your virtual & physical monitor using the below parameters:


Resolution
    1920x1080 
    
Refresh Rate
    75Hz 

Please execute in your terminal=

    sudo gtf 1920 1080 75 && sudo xrandr --newmode "1920x1080_75.00" 173.00 1920 2048 2248 2576 1080 1083 1088 1120 -hsync +vsync 

Identify the name of your virtual monitor connected

    sudo xrandr
    
In my case is= DisplayPort-0 for Virtual Monitor

    sudo xrandr --addmode DisplayPort-0 1920x1080_75.00 && sudo xrandr --output DisplayPort-0 --mode "1920x1080_75.00"
#
#
#
And for Physical External Monitor is= DP-1 also in my case

    sudo xrandr --addmode DP-1 1920x1080_75.00 && sudo xrandr --output DP-1 --mode "1920x1080_75.00"
