### Volcanic Rock and Chipped Rock

These two text styles are extremely similar internally due to the fact that they share most of the same GEGL syntax, so they were both combined into one plugin; as opposed to making two plugins. 
Obviously they look very different, but under the hood GEGL is doing the same graphical text theory and applying a "dark lava coat" on the volcanic text
and not the chipped rock. For those classic Gimp fans "Chipped Rock" is directly inspired by the classic alpha to logo "chip away".

![image](https://github.com/LinuxBeaver/ChippedRock_VolcanicText_Gimp_Plugin/assets/78667207/63a439b4-e8a2-4d60-acc4-cfd4787ac39c)

![image](https://github.com/LinuxBeaver/ChippedRock_VolcanicText_Gimp_Plugin/assets/78667207/eb680ab3-6bc2-4763-b82e-1329d062d4f3)

## Directory to put Binaries (They do NOT go in the normal plugins folder)

**Windows**

 C:\Users\(USERNAME)\AppData\Local\gegl-0.4\plug-ins
 
 **Linux** 

 /home/(USERNAME)/.local/share/gegl-0.4/plug-ins
 
 **Linux (Flatpak includes Chromebook)**

 /home/(USERNAME)/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins

Then Restart Gimp and go to GEGL Operations and look for "Volcanic Rock / Chipped Rock" in the drop down list
Gimp 2.99.16+ users will find the filter in filters>Text Styling, 2.10 
users will only see it in the GEGL operations drop down list.


## Compiling and Installing

### Linux

To compile and install you will need the GEGL header files (`libgegl-dev` on
Debian based distributions or `gegl` on Arch Linux) and meson (`meson` on
most distributions).

```bash
meson setup --buildtype=release build
ninja -C build

```

If you have an older version of gegl you may need to copy to `~/.local/share/gegl-0.3/plug-ins`
instead (on Ubuntu 18.04 for example).

BEAVER RECOMMENDS YOU USE A MODERN VERSION OF GEGL. NO GUARANTEE DATED VERSIONS OF GIMP WILL WORK WITH THIS PLUGIN 

### Windows

The easiest way to compile this project on Windows is by using msys2.  Download
and install it from here: https://www.msys2.org/

Open a msys2 terminal with `C:\msys64\mingw64.exe`.  Run the following to
install required build dependencies:

```bash
pacman --noconfirm -S base-devel mingw-w64-x86_64-toolchain mingw-w64-x86_64-meson mingw-w64-x86_64-gegl
```

Then build the same way you would on Linux:

```bash
meson setup --buildtype=release build
ninja -C build
```

## More Previews of this based plugin
![image](https://github.com/LinuxBeaver/ChippedRock_VolcanicText_Gimp_Plugin/assets/78667207/5975cfb4-bd85-434c-b1da-9d4ce6dc4cb4)

![image](https://github.com/LinuxBeaver/ChippedRock_VolcanicText_Gimp_Plugin/assets/78667207/415877df-8be6-440e-90bf-1d195f465669)

![image](https://github.com/LinuxBeaver/Chipped_Rock_Volcanic_Text_Style_Gimp_Plugin/assets/78667207/c8aa342c-20bb-4ea6-9c38-9d5a6eeea96e)


## note this plugin ships with many other plugins of mine as dependencies.

Most notically Ocean's Surface which is a background wallpaper design plugin
https://github.com/LinuxBeaver/Ocean-s-Surface---Gimp-background-design-plugin/



