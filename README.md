# rancher_server_ctl
## Desc. 
* You can control the rancher server with several option by "service" command

## Install
* For rancher local use or HA(via externel mysql)
```
curl -sL bit.ly/rancher_ctl -o ./rancher
sudo chmod 755 ./rancher

sudo cp ./rancher /etc/init.d/
or
sudo cp ./rancher /usr/local/bin
```


* For Rancher HA (Use the rancher-ha mode only Manualy - Not recommended)
```
curl -sL bit.ly/rancher-ha -o ./rancher-ha
sudo chmod 755 ./rancher-ha
```



## How to use
* ex) For start the rancher in the local
```
service rancher start
or
rancher start

## Automatic check the setup at 1st time
 -- Please insert the "rancher_server_port" information --
8443
 -- Do you have database for Rancher server HA mode ? [ y / n ] --
y
 -- Please insert the "mysql_host" information --
10.0.0.2
 -- Please insert the "mysql_port" information --
3306
 -- Please insert the "mysql_db_name" information --
rancher_db
 -- Please insert the "mysql_user" information --
rancher
 -- Please insert a mysql "rancher" password --

```
* Option: `start` `stop` `restart` `status` `clear`


## Setup
* You can change the re-setup by clear option
```


* Clear the Rancher configuration if you need.
```
./rancher clear
=====================================================
 --  Do you want to clear the configuration of rancher_ctl ? [ y / n ]
y
 /tmp/rancher_tmp/rancher_ha.conf has been deleted !!
=====================================================
```

## You can change the Rancher setting manually as below
vi /etc.init.d/rancher
or
vi /usr/local/bin/rancher

data_dir="/data/src/rancher_data/mysql"
rancher_image="rancher/server:v1.2.0-pre3"
```

