# Remember to change the ssh password again if you just reinstalled the OS

### always start with updating current stuff
```
sudo apt-get update
```

### install php and git
```
sudo apt install libapache2-mod-php7.4 -y
sudo apt-get install git-all -y
```
say no to popup when running the second one

### give php writing access in our server
```
sudo chown -R www-data /var/www/html/
```

### make ssm and referral-suite auto-updaters
```
echo "<?php shell_exec('rm -r ssm; git clone https://github.com/ssmission/ssm.git'); die('gjort!'); ?>" >> /var/www/html/github_write_ssm.php
echo "<?php shell_exec('rm -r referral-suite; git clone https://github.com/ssmission/referral-suite.git'); die('gjort!'); ?>" >> /var/www/html/github_write_referral-suite.php
```
