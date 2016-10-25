-- Link [https://docs.docker.com/engine/installation/linux/ubuntulinux/]

--docker
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates


Precise 12.04 (LTS)	deb https://apt.dockerproject.org/repo ubuntu-precise main
echo "deb https://apt.dockerproject.org/repo ubuntu-precise main" | sudo tee /etc/apt/sources.list.d/docker.list

Trusty 14.04 (LTS)	deb https://apt.dockerproject.org/repo ubuntu-trusty main
echo "deb https://apt.dockerproject.org/repo ubuntu-trusty main" | sudo tee /etc/apt/sources.list.d/docker.list

Xenial 16.04 (LTS)	deb https://apt.dockerproject.org/repo ubuntu-xenial main
echo "deb https://apt.dockerproject.org/repo ubuntu-xenial main" | sudo tee /etc/apt/sources.list.d/docker.list

sudo apt-get update
apt-cache policy docker-engine

sudo apt-get install linux-image-extra-$(uname -r) linux-image-extra-virtual


--docker-composer
curl -L "https://github.com/docker/compose/releases/download/1.8.1/docker-compose-$(uname -s)-$(uname -m)" > /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
docker-compose --version
