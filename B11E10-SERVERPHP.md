# 🚀 SERVIDOR WEB NA BTV11 E10

---

## 🌐 Configuração do Servidor Web (LAMP Stack)

### 🔹 Instalar Apache
```sh
sudo apt install apache2 -y
```

### 🔹 Instalar MariaDB
```sh
sudo apt install mariadb-server -y
```

### 🔹 Instalar e Configurar phpMyAdmin
```sh
sudo apt install phpmyadmin
# Escolher Apache2
# Confirmar com Yes
# Definir senha e confirmar
```

### 🔹 Habilitar Serviços no Boot
```sh
sudo systemctl enable apache2
sudo systemctl enable mariadb
```

### 🔹 Proteger o MySQL
```sh
mysql_secure_installation
# Responder: senha, n, n, y, n, y, y
```
### 🔹 Criar novo usuário MySQL
```sh
sudo mariadb
CREATE USER 'meuusuario'@'localhost' IDENTIFIED BY 'MinhaSenha123!';
GRANT ALL PRIVILEGES ON *.* TO 'meuusuario'@'localhost' WITH GRANT OPTION;
```

### 🔹 Instalar PHP e Extensões
```sh
sudo apt install php php-mysql php-cli php-curl php-xml php-mbstring libapache2-mod-php -y
```

### 🔹 Configurar phpMyAdmin
```sh
sudo ln -s /usr/share/phpmyadmin /var/www/html/phpmyadmin
sudo systemctl restart apache2
```

---

## 🔥 Configuração do Firewall (UFW)
```sh
sudo apt install ufw -y
sudo ufw allow 80/tcp    # Porta Localhost
sudo ufw allow 443/tcp   # Porta HTTP
sudo ufw allow 22/tcp    # Porta SSH
sudo ufw allow 41641/tcp # Porta Firewall
sudo ufw enable
```

### 🔹 Ajustar Permissões do Diretório Web
```sh
sudo chown -R $USER:$USER /var/www/html
sudo chmod -R 755 /var/www/html
```

---

## 🛡️ Configuração de VPN (Opcional)
```sh
curl -fsSL https://tailscale.com/install.sh | sh
sudo tailscale up
```

---

## ⚙️ Comandos Úteis
```sh
htop  # Monitor de processos
```
