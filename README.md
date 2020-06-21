# angband-retro-font
These files are an attempt to put the font used by the DOS version of Angband
2.9.6 in a form usable with Angband 4.2's frontends for Windows or SDL.  See
LICENSE.txt for the licensing details.

8x16retro.fon is a conversion of Angband 2.9.6's LIB/XTRA/ANGBAND.FNT.  It was
generated using tools from psftools-1.0.13 (from
http://www.seasip.info/Unix/PSF/ ) as follows:

    raw2psf --height=16 --codepage=CP1252 ANGBAND.FNT > 8x16retro.psf
    psf2fnt 8x16retro.psf 8x16retro.fnt
    fnts2fon 8x16retro.fnt 8x16retro.fon --winver=3.0

To use 8x16retro.fon with Angband 4.2, copy it to the lib/fonts directory of
the game's files.

retro.prf overrides the defaults for showing some objects and terrain features
in Angband 4.2 to try to match the mapping set up by Angband 2.9.6's
LIB/XTRA/GREDIT.INI.  To try out those preferences with Angband 4.2.0, put
retro.prf in the directory for Angband's user preferences (~/.angband/Angband
on Linux) and, when running Angband, load them via the '=' command's
"Load a user pref file" option.  For regular use, you'll have to configure
your preferences so retro.prf is automatically loaded.
