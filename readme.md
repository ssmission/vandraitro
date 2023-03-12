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

### navigate to webserver folder
```
cd /var/www/html/
```

### give php writing access in our server
```
sudo chown -R www-data /var/www/html/
```

### make ssm and referral-suite auto-updaters
```
git clone https://github.com/ssmission/ssm.git
git clone https://github.com/ssmission/referral-suite.git
```
