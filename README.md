# dockerRaspberryPI
setup Docker & portainer in Raspberry PI 4

## Docker Setup
### commands
    sudo apt update
    curl -SSL https://get.docker.com | sh
    sudo usermod -aG docker pi
    
## Portainer Setup
### commands
    sudo docker pull portainer/portainer-ce:linux-arm
    sudo docker run -d -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:linux-arm
    
## Access from browser
    ipAddress:9000
