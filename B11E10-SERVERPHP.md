sudo apt install apache2 -y
sudo apt install mariadb-server -y
sudo apt install phpmyadmin (escolher apache2, yes, password, password confirm)

sudo systemctl enable apache2
sudo systemctl enable mariadb


mysql_secure_installation (password, n, n, y, n, y, y)

sudo apt install php php-mysql php-cli php-curl php-xml php-mbstring libapache2-mod-php -y

sudo ln -s /usr/share/phpmyadmin /var/www/html/phpmyadmin
sudo systemctl restart apache2

sudo chown -R $USER:$USER /var/www/html
sudo chmod -R 755 /var/www/html


### Se quiser VPN
curl -fsSL https://tailscale.com/install.sh | sh
sudo tailscale up
