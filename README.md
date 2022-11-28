# docker-compose-templates
Behold! My stuff!

This is where i keep all my docker-compose.yml templates incase i need to redeploy

## Getting started
clean ubuntu install

sudo apt update

sudo apt upgrade

sudo apt install vim nano cifs-utils docker.io docker-compose

mkdir /mnt/media

sudo nano /etc/fstab

```//<NAS_IP>/files/media /mnt/media cifs uid=user,gid=user,file_mode=0775,dir_mode=0775,credentials=/home/user/samba_creds,iocharset=utf8 0 0```


sudo nano /home/user/samba_creds

```username=<username>```

```password=<password>```

sudo chmod 600 /home/user/samba_creds


## starting with docker-compose
cd <folder>

docker-compose up -d

## Best Prcatices
always make sure your docker-compose.yml has restart: unless-stopped

always pin your docker image versions, latest images can always break
