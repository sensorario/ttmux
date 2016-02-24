# ttmux

A script that make easy tmux configuration bootstrap of a project

## Install ttmux

To make ttmux executable from everywhere, add a symbolic link your /usr/local/bin folder

    # cd /usr/local/bin
    # ln -s ~/path/to/sensorario/ttmux/ttmux .

## tmux configuration

Add these lines to your tmux.conf file, ore create it if not exists.

```bash
# start windows and panes at 1, not 0
set -g base-index 1
set -g pane-base-index 1
```

This example create a basic configurtion where, ...

 - github checkout master branch
 - session is named "ttmux"
 - workspace windows will have a 20% pane, on the bottom


```bash
declare -A window_list=()
declare -A horizontal_panes=()
declare -A horizontal_panes_command=()
declare -A horizontal_panes_command_position=()

session_name="ttmux"
project_path='/path/to/project/folder'

window_list+=([workspace]="cd $project_path; vim")
window_list+=([mysql]="mysql -uroot sensorario")
window_list+=([console]="cd $project_path")

horizontal_panes+=([workspace]="")
horizontal_panes_command+=([workspace]="")
horizontal_panes_command_position+=([workspace]=2)

ordered_windows=(
    workspace
    mysql
    console
)
```
