![LAMP](conf/lamp.png)

Description
===========
[LAMP] est un script bash puissant pour l'installation d'Apache + PHP + MySQL / MariaDB / Percona Server, etc. Vous pouvez installer Apache + PHP + MySQL / MariaDB / Percona Server de manière très simple. Il vous suffit de choisir ce que vous souhaitez installer avant l'installation. Et tout sera fait dans quelques minutes.

- [Systèmes supportés](#systèmes-supportés)
- [Installation](#installation)
- [Mises à jour](#mises-à-jour)
- [Désinstallation](#uninstall)

- [Emplacement d'installation par défaut](#emplacement-dinstallation-par-défaut)
- [Quelques commandes de bases](#quelques-commandes-de-bases)

Systèmes supportés
===============
- Amazon Linux 2018.03
- CentOS-6.x
- CentOS-7.x (recommend)
- Fedora-29 (recommend)
- Debian-8.x
- Debian-9.x (recommend)
- Ubuntu-14.x
- Ubuntu-16.x
- Ubuntu-18.x (recommend)


Installation
============

- system: Debian/Ubuntu
```bash
sudo apt-get -y install wget screen git
git clone https://github.com/Midship62/lamp.git
cd lamp
chmod 755 *.sh
screen -S lamp
sudo ./lamp.sh
```

Mises à jour
=======
```bash

./upgrade.sh             // Select one to upgrade
./upgrade.sh apache      // Upgrade Apache
./upgrade.sh db          // Upgrade MySQL/MariaDB/Percona
./upgrade.sh php         // Upgrade PHP
./upgrade.sh phpmyadmin  // Upgrade phpMyAdmin
```

Désinstallation
=========
```bash
./uninstall.sh
```

Emplacement d'installation par défaut
=============================
| Apache Location            | Path                                           |
|----------------------------|------------------------------------------------|
| Install Prefix             | /usr/local/apache                              |
| Web root location          | /data/www/default                              |
| Main Configuration File    | /usr/local/apache/conf/httpd.conf              |
| Default Virtual Host conf  | /usr/local/apache/conf/extra/httpd-vhosts.conf |
| Virtual Host location      | /data/www/virtual_host_names                   |
| Virtual Host log location  | /data/wwwlog/virtual_host_names                |
| Virtual Host conf          | /usr/local/apache/conf/vhost/virtual_host.conf |

| phpMyAdmin Location        | Path                                           |
|----------------------------|------------------------------------------------|
| Emplacement d'installation      | /data/www/default/phpmyadmin                   |

| KodExplorer Location       | Path                                           |
|----------------------------|------------------------------------------------|
| Emplacement d'installation      | /data/www/default/kod                          |

| PHP Location               | Path                                           |
|----------------------------|------------------------------------------------|
| Install Prefix             | /usr/local/php                                 |
| Configuration File         | /usr/local/php/etc/php.ini                     |
| ini additional location    | /usr/local/php/php.d                           |

| MySQL Location             | Path                                           |
|----------------------------|------------------------------------------------|
| Install Prefix             | /usr/local/mysql                               |
| Data Location              | /usr/local/mysql/data                          |
| my.cnf Configuration File  | /etc/my.cnf                                    |

| MariaDB Location           | Path                                           |
|----------------------------|------------------------------------------------|
| Install Prefix             | /usr/local/mariadb                             |
| Data Location              | /usr/local/mariadb/data                        |
| my.cnf Configuration File  | /etc/my.cnf                                    |

| Percona Location           | Path                                           |
|----------------------------|------------------------------------------------|
| Install Prefix             | /usr/local/percona                             |
| Data Location              | /usr/local/percona/data                        |
| my.cnf Configuration File  | /etc/my.cnf                                    |

Quelques commandes de bases
==================
| Process     | Command                                                 |
|-------------|---------------------------------------------------------|
| Apache      | /etc/init.d/httpd  (start\|stop\|status\|restart)       |
| MySQL       | /etc/init.d/mysqld (start\|stop\|status\|restart)       |
| MariaDB     | /etc/init.d/mysqld (start\|stop\|status\|restart)       |
| Percona     | /etc/init.d/mysqld (start\|stop\|status\|restart)       |
| Memcached   | /etc/init.d/memcached (start\|stop\|restart)            |
| Redis-Server| /etc/init.d/redis-server (start\|stop\|restart)         |

| Command    | Description                     |
|------------|---------------------------------|
| lamp add   | create a virtual host           |
| lamp list  | list all virtual host           |
| lamp del   | remove a virtual host           |