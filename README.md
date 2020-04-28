# KoboToolBox
<b><h3>Installing Docker</h3></b>
  a.sudo apt update<br>
  b.sudo apt upgrade
  <p>sudo curl -L https://github.com/docker/compose/releases/download/1.21.2/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose</p>
  https://docs.docker.com/compose/install/  update version<br>
  //image section
  
  <h4><b>Change the access permissions of of docker composer to be executable</b></h4>
sudo chmod +x /usr/local/bin/docker-compose

<h4><b>Verify installation</b></h4>
docker-compose --version

Sudo apt update<br>
sudo apt upgrade<br>
//Image Section
For more information for the first three procedure : https://www.digitalocean.com/community/tutorials/how-to-install-docker-compose-on-ubuntu-18-04

<h4><b>Install a few prerequisite packages which let apt use packages over HTTPS:</b></h4>
<p>sudo apt install apt-transport-https ca-certificates curl software-properties-common</p>

<b>Then add the GPG key for the official Docker repository to your system</b><br>
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

<b>Then add the GPG key for the official Docker repository to your system:</b>

 <b>Add the Docker repository to APT sources:</b><br>
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"

<b>update the package database with the Docker packages from the newly added repo:</b>    
sudo apt update<br>
sudo apt upgrade

*Make sure you are about to install from the Docker repo instead of the default Ubuntu repo:
apt-cache policy docker-ce*<br>
//image section<br>
*<b>Notice that docker-ce is not installed, but the candidate for installation is from the Docker repository for Ubuntu 18.04 (bionic)</b>.*
<b>Finally, install Docker:</b>
sudo apt install docker-ce

<p>Docker should now be installed, the daemon started, and the process enabled to start on boot. Check that it's running:
sudo systemctl status docker</p>

sudo usermod -aG docker ${USER}<br>

su - ${USER}<br>

The output should be similar to the following, showing that the service is active and running:<br>
//image section<br>

Is your docker running?<br>
sudo docker run hello-world
output:docker 









