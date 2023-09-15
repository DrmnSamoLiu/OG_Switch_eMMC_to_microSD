**Disclaimer: I'm not a professional PCB designer so I can't guarentee it won't burn your eMMC or your SBC or even your house down. Use it at your own risk.**
<br><br>

![p1](https://github.com/DrmnSamoLiu/OG_Switch_eMMC_to_microSD/assets/36998819/44650766-0438-4a79-8592-4f1c36153e6f)
![p2](https://github.com/DrmnSamoLiu/OG_Switch_eMMC_to_microSD/assets/36998819/0b8555fd-21d0-4af2-967e-d59aa2bca407)


<br> <br>
This is basically a simpler and stripped down version of ![mmcblkNX](https://github.com/ignasurba/mmcblkNX), which requires a single board computer with micro SD slot to work. (It was tested with a raspberry pi 4.)
<br>Again, this tool does not enable any pirating or hacking of your Nintendo Switch. It's only meant for backup/restore/swapping eMMC chips.
<br><br>The micro SD outline of this board is modified from ![https://github.com/voltlog/emmc-wfbga153-microsd](https://github.com/voltlog/emmc-wfbga153-microsd), huge thanks to Voltlog for sharing it!

## BoM (Bill of Materials)
Molex 500913-0302 connector

## Usage
Simply put the Nintendo Switch eMMC board together with this adapter and insert it into your SBC. (Inserting BEFORE powering up is recommended.)
<br>You should see the eMMC chip recognized by your OS in `dmesg` like this:

![p3](https://github.com/DrmnSamoLiu/OG_Switch_eMMC_to_microSD/assets/36998819/08205856-219f-463f-bdaf-e960f3afd951)

<br>Then you can read/write to `/dev/mmcblk0` with whatever tool you like.
<br>It took about 11 minutes to fully dump a 32GB eMMC chip on a raspi4 with DDR52 SD clock speed: 
![p4](https://github.com/DrmnSamoLiu/OG_Switch_eMMC_to_microSD/assets/36998819/69e49def-9a6e-40bf-94f3-49e9a54616af)
