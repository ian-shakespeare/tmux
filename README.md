# Tmux Conf

```sh
# CONTROLS

# Remap prefix to `C-a`
unbind C-b
set-option -g prefix C-a
bind-key C-a send-prefix

# Split panes with `|` and `-`
bind | split-window -h
bind - split-window -v
unbind '"'
unbind %

# Add shortcut for reloading tmux config
bind r source-file ~/.tmux.config

# Allow pane switching with arrow keys
bind -n M-Left select-pane -L
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D

# Enable mouse control
set -g mouse on

# VISUALS

# Do nothing on alert
set -g visual-activity off
set -g visual-bell off
set -g visual-silence off
setw -g monitor-activity off
set -g bell-action none

# Clock
setw -g clock-mode-colour yellow

# Copy
setw -g mode-style 'fg=black bg=red bold'

# Panes
set -g pane-border-style 'fg=red'
set -g pane-active-border-style 'fg=yellow'

# Statusbar
set -g status-position bottom
set -g status-justify left
set -g status-style 'fg=red'
set -g status-left ''
set -g status-left-length 10
set -g status-right-style 'fg=black bg=yellow'
set -g status-right '%Y-%m-%d %H:%M '
set -g status-right-length 50
set -g window-status-current-style 'fg=black bg=red'
set -g window-status-current-format ' #I #W #F'
setw -g window-status-style 'fg=red bg=black'
setw -g window-status-format ' #I #[fg=white]#W #[fg=yellow]#F '
setw -g window-status-bell-style 'fg=yellow bg=red bold'

# Messages
set -g message-style 'fg=yellow bg=red bold'
```
