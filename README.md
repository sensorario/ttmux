# startmux

A script that make easy tmux configuration bootstrap of a project

## Add your own custom configuration

To add a custom configuration, it's necessary to create a file with extension .startmux. When loaded, startmux select the right file by asking which one the user want to load.

## Example

Here an example. Windows will be opened with the order in the list. `first` parameter, is the name of the window. `second` parameter, is the command appended on that window.

    #!/bin/bash
    combo=()
    combo+=('docs'    'cd ~/Documents; clear; pwd')
    combo+=('desktop' 'cd ~/Desktop; clear; pwd')

## Example two

In this example, first window is named docs, and is opened running vim

    #!/bin/bash
    combo=()
    combo+=('docs'    'vim')
    combo+=('desktop' 'clear')


