# Technical detail (the boring part)
This script are based on installation script in [Russian forum 4pda](https://4pda.to/forum/index.php?showtopic=1001500&st=600#entry107246765), written for Russian variant Geely Coolray. 

Modification has been made to adapt Malaysian's Proton X50 Infortainment System.

Proton X50 Infotainment System are trying to run bash scripts at \b832bc61472727635baffcf25dd28e9f239273e2\d4ad0e797c738a44a9dd1b9231d201e8374dfda2.sh from USB drive.

Therefore, this bash script has been placed to trigger another bash script "done.sh" at root of USB drive. 

![image](https://user-images.githubusercontent.com/17538895/172923228-8c41490f-fde7-44e5-b073-a555e740fdfc.png)

In done.sh, it basically does things below:
- mount /data partition
- create new folder to place your APK file
- copy your APK file from USB root directory and paste in /data/app
- set correct permission
- delete "point of entry" to avoid loop
- sync file system changes and reboot after 10 seconds

![image](https://user-images.githubusercontent.com/17538895/172923573-18867149-4902-4a9a-ba6f-9d7f69d5b566.png)
