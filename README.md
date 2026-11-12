# rex-state

Save and restore your whole [Rex](https://www.superlogical.com/rex) setup: sessions, tabs, panes (splits, cwd, focus, zoom), and the Claude Code / Codex agent running in each pane.

```sh
rex-state save      # writes ~/.rex-state.json
rex-state restore   # after a reboot: rebuilds everything, agents resume via --resume
rex-state show      # preview
```

Install: copy `rex-state` somewhere on your PATH. Needs Python 3 and the `rex` CLI.

Notes:
- Restore adds sessions; close the empty default one Rex starts with.
- Scrollback isn't restored (Rex can't load old output). Claude panes redraw on resume.
- Non-agent programs are typed into the pane but not run.
- Codex resume is untested.
