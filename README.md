# nginx setting & https

#### server update
```sh
sudo apt update
sudo apt upgrade
sudo apt autoremove
```

#### nginx install
```sh
sudo apt install nginx
```

#### certbot install & setting
```sh
sudo apt install snapd
sudo snap install core; sudo snap refresh core
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot

sudo certbot certonly --manual --preferred-challenges dns -d "*.example1.com" -d "example1.com"
```

#### nginx setting
```sh
sudo vi /etc/nginx/sites-available/default

sudo systemctl restart nginx
sudo systemctl status nginx
```