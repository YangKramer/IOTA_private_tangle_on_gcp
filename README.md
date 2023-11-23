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
![image](https://github.com/YangKramer/IOTA_private_tangle_on_gcp/assets/151723322/f7d6308a-6c84-4588-b9af-512a13143552)
```
