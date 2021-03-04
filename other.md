# other stuff

## change GRUB background image if one exists before
```bash
A="cat textfile | grep -o "GRUB_BACKGROUND.*\""; 
```
**TODO:** make it work with an if block that checks whether *GRUB_BACKGROUND=* exists, perhaps using grep?


## change GRUB background image if none exist before
```bash
wget https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Tux.png/220px-Tux.png --output-file /usr/share/images/GRUB-bg.jpg;
echo GRUB_BACKGROUND="/usr/share/images/GRUB-bg.png" >> /etc/default/grub;
update-grub
```

# These are currently untested, since i use the superior rEFInd
