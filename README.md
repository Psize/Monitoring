# Monitoring
## Задание 1)
Скриншоты входа в админку Zabbix  -server
<img width="1913" height="849" alt="image" src="https://github.com/user-attachments/assets/1424ffd6-705c-47b4-95e1-59671aeffcc6" />
<img width="1913" height="849" alt="image" src="https://github.com/user-attachments/assets/dd190650-2fa6-4a2b-a761-b2b89d72cab8" />

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

## Задание  2)  

    <img width="2550" height="1047" alt="image" src="https://github.com/user-attachments/assets/a21a4a73-49e3-4530-b96f-6bd5e90c7afc" />
    <img width="2538" height="961" alt="image" src="https://github.com/user-attachments/assets/d7c9ef69-f8e7-4f74-85ed-ace7af94e7ff" />
    <img width="1028" height="482" alt="image" src="https://github.com/user-attachments/assets/25bbf86e-dd3c-4067-8da7-5073ee8719bc" />

1)  wget https://repo.zabbix.com/zabbix/7.0/debian/pool/main/z/zabbix-release/zabbix-release_latest_7.0+debian11_all.deb
    dpkg -i zabbix-release_latest_7.0+debian11_all.deb
    apt update
2) apt install zabbix-agent
3) Далее меняем   ip адресс в конфиге заббикс агента и перезапускаем  забикс агент что бы он применил исправленный конфиг
4) systemctl restart zabbix-agent


## Задание 3)  

    <img width="2545" height="1259" alt="image" src="https://github.com/user-attachments/assets/7c909ef1-c60b-422d-9049-fb6f21bc346b" />
    <img width="2547" height="937" alt="image" src="https://github.com/user-attachments/assets/74d4a0b6-711c-4110-904e-4beb7afdf32e" />

    <img width="2545" height="1259" alt="image" src="https://github.com/user-attachments/assets/0ce7ec67-7b3d-496d-ac48-8f2d01723fca" />
