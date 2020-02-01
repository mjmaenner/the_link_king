---
layout: page
title: Downloads
---

These are the final programs released on the-link-king.com.  They are made available here with permission of the original author. We cannot provide any support or warranty for these materials.

### Versions:
* Windows SAS 9.X users should use Link King v9.0 [LinkKingv9pt0.zip](https://github.com/mjmaenner/the_link_king/releases/download/999/LinkKingv9pt0.zip)
* Linux / Unix SAS 9.X users should use Link King v6.5 for Unix [Link_King_for_Unix_Linux.zip](https://github.com/mjmaenner/the_link_king/releases/download/999/Link_King_for_Unix_Linux.zip)
* Windows SAS v8 users should use Link King v6.3.43 for SASv8 [Link_king_for_SASv8.exe](https://github.com/mjmaenner/the_link_king/releases/download/999/Link_King_for_SASv8.exe)

### Files and support materials
* Link King Demo Video [Link_King_Demo_video.zip](https://github.com/mjmaenner/the_link_king/releases/download/999/Link_King_Demo_video.zip)
* Link King user manual v5.2.4 [user_manual.zip](https://github.com/mjmaenner/the_link_king/releases/download/999/user_manual.zip)
* User Manual Addendum for V6.0 [Link_King_Edit_Features.pdf](https://github.com/mjmaenner/the_link_king/releases/download/999/Link_King_Edit_features.pdf)
* Original SAMHSA SAS Code [saspgms.zip](https://github.com/mjmaenner/the_link_king/releases/download/999/saspgms.zip)
* SAMHSA Monograph Zip file [SAMHSA.zip](https://github.com/mjmaenner/the_link_king/releases/download/999/SAMHSA.zip)
* Link King Screensaver [LK_Screensaver.exe](https://github.com/mjmaenner/the_link_king/releases/download/999/LK_Screensaver.exe)
* SAS Double Metaphone Macro [SAS_double_metaphone.zip](https://github.com/mjmaenner/the_link_king/releases/download/999/SAS_double_metaphone.zip)


#### UPDATE LOG:
3/9/18:
Optimized blocking and updated linking algorithm.

##### Installation Instructions:

1. Create a "C:\Link King" directory

2. Download LinkKingv9pt0.zip (The Link King v9.0 for SAS) and unzip into C:\Link King

3. For 64-bit installations copy "Summon Link King 64" (shortcut) to desktop.

You should be able to launch The Link King by double-clicking the shortcut.


##### If The Link King was not installed in c:\Link King or the shortcut does not work:

  a) modify the properties of the shortcut and/or lk_config_64.cfg (for 64 bit)

  or

  b)  Launch SAS and run the following code in a program editor to launch
   The Link King:
   
```SAS
    libname undup 'C:\link king';
    dm 'Af c=undup.undup_frames_64bit.intro.frame';
```

After launch, close the explorer/results windows on the left side of the screen and
maximize The Link King interface.


##### 4. For 32-bit/Unix installations

  a) After completing #2 (above), unpack the SAS transport file undup_frames.cpt:
  
```SAS
  libname output 'y:\buzz\delete';  /* change the path to the location where you want to save  undup_frames for the link king  */

  filename input 'y:\buzz\delete\undup_frames.cpt';  /* change the path to where you downloaded undup_frames.cpt */

  proc cimport infile=input lib=output;
  run;
```

NOTE: you must delete the undup_frames catalog before unpacking the transport file.

b)     See if the "Summon Link King 32" shortcut works.

If not, modify the properties of the "Summon Link King 32" shortcut and/or lk_config_32.cfg

   or

Launch SAS and run the following code in a program editor to launch The Link King:

```SAS 
   libname undup 'C:\link king';
   dm 'Af c=undup.undup_frames.intro.frame';
```

After launch, close the explorer/results windows on the left side of the screen and    
maximize The Link King interface.
