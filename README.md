# startmux
A script that make easy tmux configuration bootstrap of a project

## Add your own custom configuration

This scripts, by default, loads config.dist file. If you want to load your custom configuration, just create a file named `config`. To do this, just copy config.dist file, renaming the copy `config`.

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


