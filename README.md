# ansible-pi

# Fresh install
sudo diskutil list
sudo diskutil umount /dev/disk6s1
sudo dd if=2016-03-18-raspbian-jessie-lite.img of=/dev/rdisk6 bs=1m
sudo diskutil umount /dev/disk6s1

vi rpi.hosts
# first pass requires password
ansible-playbook -i rpi.hosts site.yml --ask-pass
# subsequent passes do not
ansible-playbook -i rpi.hosts site.yml 
