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


____


# Webmin Setup

```
nano /etc/webmin/miniserv.conf    //then change ssl=1 to ssl=0
sudo service webmin restart
sudo apt update; sudo apt upgrade -y

//install some things to make everything work after this
sudo apt-get install software-properties-common


//install php 7.3
sudo apt install software-properties-common
sudo add-apt-repository ppa:ondrej/php
sudo apt install php7.3 php7.3-common php7.3-opcache php7.3-cli php7.3-gd php7.3-curl php7.3-mysql php7.3-zip php7.3-xml php7.3-mbstring -y
sudo service webmin restart
sudo service apache2 restart

//go to webmin, search sql, follow the steps to install that. (it'll take a minute to load)

mysql





```
