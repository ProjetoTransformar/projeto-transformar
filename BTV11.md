# 🚀 Instalação BTV11

# **Baixe [aqui] (https://mega.nz/fm/srMiWBRZ) a imagem do sistema**

## 📌 DTB Utilizado
**meson-sm1-x96-air.dtb**

---

## 📖 Passo a Passo

### 1️⃣ Criar Usuário Root e Definir Senha

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
armbian-install (510; 1(EXT4))
```

---

## 🎯 Observações

