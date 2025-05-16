# ubuntu-setup

## kinto 


```bash
# Find line number
line_num=$(grep -n "if len(check_x11) == 0:" setup.py | cut -d: -f1)

# Apply change using the correct line number
sed -i "${line_num}s/if len(check_x11) == 0:/if False: # Bypassing X11 check\n    # Original code: if len(check_x11) == 0:/" setup.py
```

```bash
python3 setup.py
```

```bash
cd ~/workspace/kinto/xkeysnail
sudo pip3 install --upgrade .
./xkeysnail_service.sh
```

