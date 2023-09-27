__Linux:__
- In terminal: run `&` to run in background and still use command line input
- Replace strings in files throughout document: `sed -i 's/old-text/new-text/g' input.txt` 


__Potsdam cluster:__
- Tmux: new session, type `tmux new-session -s name`
- Tmux: go back to session, type `tmux attach-session -t name`
- Tmux: kill session, do `Ctrl + A`, `Ctrl + B`, and type `:kill-session`
- Tmux: detach, do `Ctrl + B` then `d`
