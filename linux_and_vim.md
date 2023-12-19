__Linux:__
- In terminal: run `&` to run in background and still use command line input
- Replace strings in files throughout document: `sed -i 's/old-text/new-text/g' input.txt`
- Same as above, but recursively applied to subdirectories: `find . -type f -name "*.txt" -exec sed -i 's/old-text/new-text/g' {} \;`

See which users are using the GPU, first run `nvidia-smi` to get process-id:
```bash
ps -eo user,pid,command | grep <process_id>
```
Nicely formatted, which also shows memory usage:
```bash
ps -eo user,pid,%mem,rss,vsz,command | grep 3145954 | awk '{print "User:", $1, "PID:", $2, "%MEM:", $3, "RSS:", $4, "VSZ:", $5, "Command:", $6}'
```
See the memory usage of files and directories in megabytes:
```bash
du -h -m /path/to/directory
```


__Potsdam cluster:__
- Tmux: new session, type `tmux new-session -s name`
- Tmux: go back to session, type `tmux attach-session -t name`
- Tmux: kill session, do `Ctrl + A`, `Ctrl + B`, and type `:kill-session`
- Tmux: detach, do `Ctrl + B` then `d`
- Tmux: list sessions: `tmux ls`
- Kill GPU from nvidia-smi: `nvidia-smi | grep 'python' | awk '{ print $5 }' | xargs -n1 kill -9`
- Copy files from Potsdam cluster to local (run in local terminal): `scp -r twouters@potsdam.enlil:/remote/dir/ /target/dir/`
