# docker-compose-templates
Behold! My stuff!

This is where i keep all my docker-compose.yml templates incase i need to redeploy

clean ubuntu install

apt update
apt upgrade
apt install vim nano cifs-utils docker.io docker-compose

FSTAB
//<NAS_IP>/files/media /mnt/media cifs uid=user,gid=user,file_mode=0775,dir_mode=0775,credentials=/home/user/samba_creds,iocharset=utf8 0 0

create /home/user/samba_creds with your CIFS creds and chmod 600 it
username=<username>
password=<password>

starting with docker-compose
cd <folder>
docker-compose up -d

always make sure your docker-compose.yml has restart: unless-stopped
