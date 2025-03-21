Add this to ~/.bashrc:
```bash
# Check if in a screen session and modify the prompt
if [ -n "$STY" ]; then
    PS1="(screen: $STY) $PS1"
fi
```