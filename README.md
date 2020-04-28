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
output:docker <br>
/*image section*/<br>
For more Information : https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04

https://www.hostinger.com/tutorials/how-to-install-docker-on-ubuntu updades version<br>

Reboot

<b>Clone Kobotoolbox script:</b>
git clone https://github.com/kobotoolbox/kobo-install

<b> Change to root</b> 
  <p>Changing to root use the following command</p>
  sudo su

<h3><b>Install Python</b></h3>
sudo apt install python

<b>Change directory to kobo install</b>
cd kobo-install/

<b> Execute</b>
run.py:  root@ip-172-31-40-195:/home/ubuntu/kobo-install# python run.py

<h5>Answer the following questions</h5>
NB: The option is to select one for yes or two for no, for the place where i did not specify either yes or  no it means i leave the default selected answer in bracket<br> 

Where do you want to install? <br>
[/home/ubuntu/kobo-docker]: (default, press enter)<br>
Please confirm path [/home/ubuntu/kobo-docker]
    1) Yes
    2) No
[1]: (default, press enter)<br>
Do you want to see advanced options?
    1) Yes
    2) No
[2]: 1
What kind of installation do you need?
    1) On your workstation
    2) On a server
[2]: (default, press enter)
Do you want to use separate servers for frontend and backend?
    1) Yes
    2) No
[2]: (default, press enter)
Public domain name [kobo.local]: (your domain name)
KPI sub domain [kf]: (default, press enter)
KoBoCat sub domain [kc]: (default, press enter)
Enketo Express sub domain name [ee]: (default, press enter)
Do you use a reverse proxy or a load balancer?
    1) Yes
    2) No
[1]: 2
SMTP server: (default, press enter)
SMTP port [25]: (default, press enter)
SMTP user: 
From email address [support@nipefagio.org]: (Your Email)
Super user's username [super_admin]: (name)
Super user's password [TLY^lWX^E~Pzf3X]: (password)
Docker Compose prefix? (leave empty for default): (default, press enter)
Staging mode?
    1) Yes
    2) No
[2]: (default, press enter)
Postgres database [kobotoolbox]: (default, press enter)
Postgres user [kobo]: (default, press enter)
Postgres password [F46j7HAqb%0Y!%]: (default, press enter)
Do you want to tweak PostgreSQL settings?
    1) Yes
    2) No
[2]: 1
Total Memory in GB?
[8]: 4
Number of connections?
[100]: (default, press enter)
Do you want to customize service ports?
    1) Yes
    2) No
[2]: (default, press enter)
Do you want to use AWS S3 storage?
    1) Yes
    2) No
[2]: (default, press enter)
Google Analytics Identifier: (default, press enter)
Google API Key: (default, press enter)
Intercom App ID: (default, press enter)
Do you want to use Sentry?
    1) Yes
    2) No
[2]: (default, press enter)
Do you want to tweak uWSGI settings?
    1) Yes
    2) No
[2]: (default, press enter)
Do you want to activate backups?
    1) Yes
    2) No
[2]: (default, press enter)

NB: You can go for other options on the questions as long as you know what you are doing, 


18. Then you will get this message












