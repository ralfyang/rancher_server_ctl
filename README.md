# rancher_server_ctl
## Desc. 
* You can control the rancher server with several option by "service" command

## Install
*


## How to use
* ex) for start the rancher
```
service rancher start
```
* Option: `start` `stop` `restart` `status`

## Setup
* You can change the setup as you need like below
```
## Rancher setting
data_dir="/data/src/rancher_data/mysql"
port="8443"
rancher_image="rancher/server:v1.2.0-pre3"
```

