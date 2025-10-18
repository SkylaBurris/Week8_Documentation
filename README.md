# Week8_Documentation

## Purging MySQL 

> After following instructions found online to successfully install Omeka after running into problems myself, I installed MariaDB. I could see that installing this and accessing the code file within Omeka was not working right. My mysql databases were also deleted upon installation. I went back to my search engine, Microsoft Edge's default Bing, and looked up how to uninstall MariaDB.
> >
> After uninstalling MariaDB, I would attempt to access mysql again, only to find no commands were working and my /var/www/html was not recognized at all. I would reach out to Dr. Ridenour for help in fixing this problem
> >
> > Here are the steps used in order to completely purge the broken mysql and reinstall it in order to move on with Omeka installation in my pre-existing VM
> >
> - apt policy mysql-server
>   - mysql --version 
>   - cd /etc/mysql
>   - ls -a
> - mysql -- help | grep /my.cnf
> - sudo apt uninstall mysql
> - sudo apt remove mysql-server
>   - cd /var/log
>   - grep -r "error"
> - sudo dpkg --configure -a
> - sudo apt install -f
> - sudo apt install mysql-server
> - sudo apt remove --purge mysql-server
> - sudo apt install mysql-server
> - sudo apt install -f
> - sudo dpkg --configure -a
> - sudo systemctl unmask mysql.service
> - sudo service mysql start
> - sudo apt purge mysql*
>   - sudo apt autoremove
>   - sudo apt autoclean
>   - sudo rm -rf /etc/mysql /var/lib/mysql /var/log/mysql
>  - sudo apt install -f
>  - sudo dpkg --configure -a
>  - sudo apt install mysql-server
