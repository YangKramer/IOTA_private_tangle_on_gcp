## IOTA_private_tangle_on_gcp

### **Create the Virtual Instance**
* Create the Google Cloud Platform(GCP) account
* Access to **Compute Engine**, click the **VM Instance**  and Create Instance
#### Setting for the instance
* **Boot Disk:** Ubuntu 22.04 LTS x86/64 (amd64 jammy image built on 2023-10-25)
* **Identity and API access:** Click "Allow full access to all Cloud APIs"
* **Firewall:** Click "Allow HTTP traffic" and "Allow HTTPS traffic"
#### Setup Farewall Rules
Tangle exposes different functionality on different ports:
- 14265
- 15600
- 8081
- 1881
- 14626/UDP
- 4000

### Prerequesties
  To execute these scripts you need Docker and Docker Compose.Docker Compose is a tool for defining and running multi-container Docker applications. It allows you to describe the 
  services, networks, and volumes used by your application in a YAML file, and then use that file to create and start all the services with a single command. 
#### Installation
```
sudo apt install curl
curl -sSL https://get.docker.com | sh
```
#### Check the version
```
sudo docker --version
sudo docker-compose –version

```

### Getting start
* First you need to clone the repository
```git clone https://github.com/iotaledger/one-click-tangle```

#### Hornet 
* Afterwards you can install a Hornet Node by
```
cd hornet-mainnet
chmod +x hornet.sh
./hornet.sh install
```

#### Private tangle
* You can install a Private Tangle by
```
cd hornet-private-net
chmod +x private-tangle.sh
sudo ./private-tangle.sh install
```
#### Start/stop the Private Tangle
```
sudo ./private-tangle.sh start
sudo ./private-tangle.sh stop
```

#### Check the statement of container
```
sudo docker ps -a
```

### Private Tangle Explorer Setup
* Make the bash script executable by running
```
chmod +x tangle-explorer.sh
```
* Installation and start the net Tangle Explorer
*Warning: It will destory destory previous data*
```
./tangle-explorer.sh install [<network-definition.json> or <private-tangle-install-folder>]
```

* Start/Stop all the containers by running
```
sudo ./tangle-explorer.sh stop
sudo ./tangle-explorer.sh start
```
