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

<img width="2539" height="934" alt="image" src="https://github.com/user-attachments/assets/d56fc785-f440-4074-9ddd-49e869e5504f" />
<img width="1037" height="481" alt="image" src="https://github.com/user-attachments/assets/2abc20e0-87de-4c9d-a292-f0039560c567" />
<img width="2542" height="1113" alt="image" src="https://github.com/user-attachments/assets/a0d89563-8179-40dc-8596-37bdf957817c" />
<img width="2546" height="1049" alt="image" src="https://github.com/user-attachments/assets/c8f1a741-a34b-42e9-bd51-1e0f165c562e" />






1)  wget https://repo.zabbix.com/zabbix/7.0/debian/pool/main/z/zabbix-release/zabbix-release_latest_7.0+debian11_all.deb
    dpkg -i zabbix-release_latest_7.0+debian11_all.deb
    apt update
2) apt install zabbix-agent
3) Далее меняем   ip адресс в конфиге заббикс агента и перезапускаем  забикс агент что бы он применил исправленный конфиг
4) systemctl restart zabbix-agent


## Задание 3)  

<img width="2536" height="782" alt="image" src="https://github.com/user-attachments/assets/d500f8ce-c3f0-491f-9c03-dbadd8d2c783" />
<img width="2523" height="1244" alt="image" src="https://github.com/user-attachments/assets/354acc78-d32c-4ec7-82c4-f32c20469d13" />

