# ansible-pi

# Fresh install
sudo diskutil list
sudo diskutil umount /dev/disk6s1
sudo dd if=20xx-xx-xx-raspbian-jessie-lite.img of=/dev/rdisk6 bs=1m
sudo diskutil umount /dev/disk6s1

vi rpi.hosts
# first pass requires password
```ansible-playbook -i rpi.hosts site.yml --ask-pass```

# confirm settings and reboot remote hosts

# subsequent passes do not need --ask-pass
```ansible-playbook -i rpi.hosts site.yml```

# additional step for detailed dump1090 configutation on remote host
```sudo dpkg-reconfigure dump1090-mutability```

# additional step for flightradar24 configuration on remote host
```fr24feed --signup```