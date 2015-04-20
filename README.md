# startmux

A script that make easy tmux configuration bootstrap of a project

## Add your own custom configuration

To add a custom configuration, it's necessary to create a file with extension .startmux. When loaded, startmux select the right file by asking which one the user want to load.

## Example

Here an example. Windows will be opened with the order in the list. `first` parameter, is the name of the window. `second` parameter, is the command appended on that window.

    #!/bin/bash
    declare -A combo=()
    combo+=(['home']='cd ~')
    combo+=(['logs']='cd /var/log')

## Execute tmux from everywhere

To make startmux executable from everywhere, add a symbolic link your /usr/local/bin folder

    # ln -s ./startmux/startmux /usr/local/bin/
