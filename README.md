# tmux-config
Simple Tmux configuration with some style and key-binding changes 

# Get-Started
You need to just copy tmux config file to ${HOME}/.tmux.conf
```bash
git clone https://github.com/gr-an/tmux-config.git
cd tmux-config
mv config ~/.tmux.conf
```
# Tmux Key Binding Options
## Prefix Remapping
By default, Tmux uses C-b as the prefix key for issuing commands. This configuration changes the prefix to C-a.

```bash
unbind C-b
set-option -g prefix C-a
```

## Pane Management
 These key bindings make it easier to split panes and navigate between them using alternative keys.

Split horizontally with |: C-a |
Split vertically with -: C-a -
Unbind default bindings for ", % keys:

```bash
bind | split-window -h
bind - split-window -v
unbind '"'
unbind %
```
## Reload Configuration
Use C-a r to reload the Tmux configuration file (~/.tmux.conf).

``` bind r source-file ~/.tmux.conf ```
## Pane Switching
Switch between panes using Alt + arrow keys, without requiring the prefix key.

Move left: Alt + ←
Move right: Alt + →
Move up: Alt + ↑
Move down: Alt + ↓
```bash
bind -n M-Left select-pane -L
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D
```
