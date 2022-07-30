# Using tmux

Also see Jeremy's "Live Coding 2" video here: https://www.youtube.com/watch?v=0pWjZByJ3Lk&t=2341s

## Installing tmux

`sudo apt install tmux`

## Using tmux

Use CTRL + B as the prime shortcut for tmux commands.

| Command   |  Action                                         |
|-----------|-------------------------------------------------|
| %         | split vertical                                  |
| "         | split horizontal                                |
| arrow     | move between panes                              |
| CTRL + D  | close pane                                      |
| z         | make pane full screen (press again to revert)   |
| d         | detach from session                             |

Run `tmux a` to attach to last session again.