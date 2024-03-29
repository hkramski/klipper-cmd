# klipper-cmd

Project moved to Codeberg: https://codeberg.org/harveyk/klipper-cmd.

Bash script to transform and output clipboard content using KDE's Klipper.

## Installation

Put the script `klipper-cmd` into `/usr/local/bin`.

For Klipper actions and commands see below.

## Usage

```
klipper-cmd: Usage: klipper-cmd [OPTION] CMD [ARG]...

 Transform and output clipboard content (using KDE's Klipper) or ARG as indicated by CMD.
 
 Options:
  -h            Display this help and exit
  -v            Output version information and exit
 
 CMD:
  capitalize    Capitalize each word
  invertnames   Change "Firstname Lastname" to "Lastname, Firstname" and vice versa
  join          Join lines by replacing linebreaks with blanks
  join2         Like "join", but also remove trailing hyphens before joining lines
  lowercase     Transform content to lowercase
  print         Simply print the clipboard content (useful on command line only)
  underscores   Change all blanks to underscores and vice versa
  uppercase     Transform content to uppercase
  
 ARG:
  If present, work on ARG instead of current clipboard content.
  Use '%s' for current clipboard content when defining Klipper commands.

 This script may be run from the command line but is much more useful when called from Klipper actions, 
 see https://docs.kde.org/trunk5/en/kde-workspace/klipper/actions-page.html.
 
 To use this script with Klipper:
  Open the actions configuration page.
  Add an action with the following properties:
   Regular Expression: .*
   Description: Any content.
  Add one or more commands to this action like this (see CMD):
   Command: klipper-cmd capitalize '%s' 
   Output Handling: Add to Clipboard
   Description: Capitalize each word.
```

## Credits

This script is based on https://esisteinfehleraufgetreten.wordpress.com/2011/08/31/textsnippets-bei-kde-mit-und-ohne-klipper/
and https://github.com/RenatGilmanov/shell-script-template/blob/master/getopts/template-commands.sh.
