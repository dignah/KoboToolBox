# Dealing with KoboToolBox 
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

<b>Change directory to kobo install</b><br>
cd kobo-install/

<b> Execute</b>
run.py:  root@ip-172-31-40-195:/home/ubuntu/kobo-install# python run.py

<h5>Answer the following questions</h5>
<p>NB: The option is to select one for yes or two for no, for the place where i did not specify either yes or  no it means i leave the default selected answer in bracket</p><br> 

Where do you want to install? <br>
[/home/ubuntu/kobo-docker]: (default, press enter)<br>
Please confirm path [/home/ubuntu/kobo-docker]<br>
    1) Yes<br>
    2) No<br>
[1]: (default, press enter)<br>
Do you want to see advanced options?]<br>
    1) Yes<br>
    2) No<br>
[2]: 1<br>
What kind of installation do you need?<br>
    1) On your workstation<br>
    2) On a server<br>
[2]: (default, press enter)<br>
Do you want to use separate servers for frontend and backend?<br>
    1) Yes<br>
    2) No<br>
[2]: (default, press enter)<br>
Public domain name [kobo.local]: (your domain name)<br>
KPI sub domain [kf]: (default, press enter)<br>
KoBoCat sub domain [kc]: (default, press enter)<br>
Enketo Express sub domain name [ee]: (default, press enter)<br>
Do you use a reverse proxy or a load balancer?<br>
    1) Yes<br>
    2) No<br>
[1]: 2<br>
SMTP server: (default, press enter)<br>
SMTP port [25]: (default, press enter)<br>
SMTP user: <br>
From email address [support@nipefagio.org]: (Your Email)<br>
Super user's username [super_admin]: (name)<br>
Super user's password [TLY^lWX^E~Pzf3X]: (password)<br>
Docker Compose prefix? (leave empty for default): (default, press enter)<br>
Staging mode?<br>
    1) Yes<br>
    2) No<br>
[2]: (default, press enter)<br>
Postgres database [kobotoolbox]: (default, press enter)<br>
Postgres user [kobo]: (default, press enter)<br>
Postgres password [F46j7HAqb%0Y!%]: (default, press enter)<br>
Do you want to tweak PostgreSQL settings?<br>
    1) Yes<br>
    2) No<br>
[2]: 1<br>
Total Memory in GB?<br>
[8]: 4<br>
Number of connections?<br>
[100]: (default, press enter)<br>
Do you want to customize service ports?<br>
    1) Yes<br>
    2) No<br>
[2]: (default, press enter)<br>
Do you want to use AWS S3 storage?<br>
    1) Yes<br>
    2) No<br>
[2]: (default, press enter)<br>
Google Analytics Identifier: (default, press enter)<br>
Google API Key: (default, press enter)<br>
Intercom App ID: (default, press enter)<br>
Do you want to use Sentry?<br>
    1) Yes<br>
    2) No<br>
[2]: (default, press enter)<br>
Do you want to tweak uWSGI settings?<br>
    1) Yes<br>
    2) No<br>
[2]: (default, press enter)<br>
Do you want to activate backups?<br>
    1) Yes<br>
    2) No<br>
[2]: (default, press enter)<br>

NB: You can go for other options on the questions as long as you know what you are doing,<br> 


Then you will get this message<br>
//image section<br>
<p>
To check dns try these curl commands:<br>
curl -I https://public.domain/service_health/<br>
curl -I http://public.domain/service_health/</p>

https://www.digitalocean.com/community/questions/port-80-failed-connection-refused<br>
<p>Despite ufw or any other firewall rules on the Linux system. There are Firewalls rules in the DigitalOcean “Networking” panel. By default, there’s no 80 rule.<br>
You need to add HTTP/HTTPS to the firewall rules.</p>
<ul>
  <li>On DigitalOcean Control Panel page,</li>
  <li>Open “Droplets”, select the droplet used</li>
<li>Go to “Networking” and check “Firewalls”, make sure there’s a rule: HTTP, TCP, 80, All IPv4 | All IPv6</li>
  <li>If not, click the firewall group icon (the blue one above)</li>
  <li>Under “Inbound Rules”</li>
  <li>Add “New rule” and select HTTP (and HTTPS if needed)</li>
  <li>Save and the 80 port should be accessible.</li><br>
  </ul>
<p>‘sudo ufw allow 443’.</p>

<b>Updated version</b>

Docker-composer - install https://docs.docker.com/compose/install/

Docker engine install - https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository 













