# Monitoring
## Задание 1)
Скриншоты входа в админку Zabbix  -server
<img width="1913" height="849" alt="image" src="https://github.com/user-attachments/assets/1424ffd6-705c-47b4-95e1-59671aeffcc6" />
<img width="1913" height="849" alt="image" src="https://github.com/user-attachments/assets/dd190650-2fa6-4a2b-a761-b2b89d72cab8" />

## Задание 2)
Список команд для  установки:

1) su - postgres -c "psql -c \"CREATE USER zabbix WITH PASSWORD '123456789';\""

2) su - postgres -c "psql -c \"CREATE DATABASE zabbix OWNER zabbix;"'

3)  wget https://repo.zabbix.com/zabbix/6.0/debian/pool/main/z/zabbix-release/zabbix-release_latest_6.0+debian11_all.deb
    dpkg -i zabbix-release_latest_6.0+debian11_all.deb
    apt update

4)   apt install zabbix-server-pgsql zabbix-frontend-php php7.4-pgsql zabbix-apache-conf zabbix-sql-scripts zabbix-agent
5)   sudo -u postgres createuser --pwprompt zabbix
     sudo -u postgres createdb -O zabbix zabbix
    
6)  zcat /usr/share/zabbix-sql-scripts/postgresql/server.sql.gz | sudo -u zabbix psql zabbix
7)  systemctl restart zabbix-server zabbix-agent apache2
    systemctl enable zabbix-server zabbix-agent apache2
