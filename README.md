# Hammer scripts for linux
This is a collection of some hammer scripts I use to make my life easier when working with materials/maps in hammer.

# Scripts
## genvmt
Usage (supports wildcard for mass vmt creation):

```
genvmt vtf_file.vtf -s <shader type> -p [key value ...]
```
genvmt will automatically determine your file's path, so place it in the desired location first before you generate a vmt for best results.

Parameters:
```
-s: Optional, Shader type. Default is LightmappedGeneric
-p: Optional, Key Value pair for additional shader parameters. 
    -p A B would become "$A" "B" in the vmt. 
    $basetexture is created by default and should not be specified.
    Used for things such as $decalscale, $ignorez, $alphatest, $envmap, etc.
    To add multiple parameters, add -p multiple times.
    Example: -p A B -p C D
    Values with spaces in them can be used by encasing in quotes
    Example: -p spriteorientation "[ 0.50 0.50 ]"
```

# Aliases
List of some helpful aliases I use for hammer
## Hammer
Opens hammer, using proton-caller. See my [hammer linux tutorial](https://github.com/rsedxcftvgyhbujnkiqwe/HammerPlusPlus-Linux) for more information.
```
alias starthammer='proton-call -r "/home/user/.local/share/Steam/steamapps/common/Team Fortress 2/bin/hammerplusplus.exe"'
```

## [vtex2](https://github.com/StrataSource/vtex2)
Creates a vtf file from an image file, or for every image file if given a directory. Useful defaults.

Note that transparency for dxt1 files doesn't work on linux - so you'll want to use dxt5 instead for any textures with transparency. You don't have to break it into two different aliases, I just find this most convenient.
```
alias mkvtf='vtex convert -f dxt1 --no-mips --pointsample'
alias mkvtf5='vtex convert -f dxt5 --no-mips --pointsample'
```
