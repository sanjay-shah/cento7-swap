# centos7-swap
```
sudo dd if=/dev/zero of=/swapfile count=4096 bs=1MiB
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
sudo sh -c 'echo "/swapfile none swap sw 0 0" >> /etc/fstab'
sudo sysctl vm.swappiness=10
sudo sysctl vm.vfs_cache_pressure=50
sudo sh -c 'echo "vm.swappiness = 10" >> /etc/sysctl.conf'
sudo sh -c 'echo "vm.vfs_cache_pressure = 50" >> /etc/sysctl.conf'
```
