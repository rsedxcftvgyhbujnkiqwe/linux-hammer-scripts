# Hammer scripts for linux
This is a collection of some hammer scripts I use to make my life easier when working with materials/maps in hammer.

# Scripts
## genvmt
Usage (supports wildcard for mass vmt creation):

```
genvmt vtf_file.vtf -s <shader type> -p [key value ...]
```
Parameters:
```
-s: Optional, Shader type. Default is LightmappedGeneric
-p: Optional, Key Value pair for additional shader parameters. 
    -p A B would become "$A" "B" in the vmt. 
    $basetexture is created by default and should not be specified.
    Used for things such as $decalscale, $ignorez, $alphatest, $envmap, etc.
    To add multiple parameters, add -p multiple times.
    Example: -p A B -p C D
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
```
alias mkvtf='vtex convert -f dxt1 --no-mips --pointsample'
```
