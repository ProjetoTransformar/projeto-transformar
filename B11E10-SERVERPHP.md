# 🚀 Instalação BTV11 E10

## 📌 DTB Utilizado
**meson-g12a-sei510.dtb**

---

## 📖 Passo a Passo

### 1️⃣ Criar Usuário Root e Definir Senha
```sh
sudo passwd root
```

### 2️⃣ Atualizar Pacotes
```sh
sudo apt update && sudo apt upgrade -y
```

### 3️⃣ Reiniciar o Sistema
```sh
reboot
```

### 4️⃣ Instalar Interface Gráfica (MATE Desktop)
```sh
sudo apt install task-mate-desktop lightdm-gtk-greeter -y
```

### 5️⃣ Instalar Navegador Chromium
```sh
sudo apt install chromium chromium-l10n -y
```

### 6️⃣ Instalar LibreOffice, Drivers e Pacotes Essenciais
```sh
sudo apt install gvfs policykit-1 libreoffice-writer libreoffice-calc libreoffice-impress \
libreoffice-l10n-pt-br libreoffice-help-pt-br ttf-mscorefonts-installer network-manager-gnome \
caja pluma eom atril engrampa mate-utils mate-calc mate-screensaver mate-media mate-tweak \
dconf-editor drawing -y
```

### 7️⃣ Instalar Codecs de Áudio e Vídeo
```sh
sudo apt install gstreamer1.0-libav gstreamer1.0-plugins-base-apps gstreamer1.0-vaapi \
gstreamer1.0-plugins-bad gstreamer1.0-plugins-base gstreamer1.0-plugins-good \
gstreamer1.0-plugins-ugly lame libavcodec-extra libavcodec-extra59 libavdevice59 \
libgstreamer1.0-0 sox twolame vorbis-tools mpv vlc -y
```

### 8️⃣ Instalar Arduino e Scratch
```sh
sudo apt install arduino scratch -y
```

### 9️⃣ Instalar Sistema no Armazenamento Interno
```sh
armbian-install
```

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
# Responder: password, n, n, y, n, y, y
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

🔥 Agora seu ambiente está completamente configurado! 🚀
