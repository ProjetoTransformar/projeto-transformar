
# 🚀 SERVIDOR NODE NA BTV11 E10

---

## 🌐 Instalação do Servidor

### 🔹 Instalar NodeJS e NPM
```sh
sudo apt update
sudo apt install nodejs npm -y
# Verifique a instalação:
node -v
npm -v
```

### 🔹 Escolher local do projeto
```sh
mkdir -p ~/projetos/meu-servidor
cd ~/projetos/meu-servidor
```

### 🔹 Criar o arquivo index.js
```sh
nano index.js
```

**Conteúdo do arquivo `index.js`:**
```javascript
const express = require('express');
const app = express();
const PORT = 3000;

app.get('/', (req, res) => {
    res.send('Servidor Node.js na TV Box funcionando!');
});

app.listen(PORT, () => {
    console.log(`Servidor ouvindo na porta ${PORT}`);
});
```

### 🔹 Inicializar o projeto e instalar ExpressJS
```sh
npm init -y
npm install express
```

### 🔹 Rodar o servidor
```sh
node index.js
```

---

## 🌐 Instalação do Banco de Dados

### 🔹 Instalar MariaDB
```sh
sudo apt install mariadb-server -y
```

### 🔹 Iniciar e habilitar o MariaDB
```sh
sudo systemctl start mariadb
sudo systemctl enable mariadb
```

### 🔹 Verificar o status do MariaDB
```sh
sudo systemctl status mariadb
```

---

## 🚀 Deixar o Servidor Node Online

### 🔹 Instalar PM2
```sh
sudo npm install pm2 -g
```

### 🔹 Rodar o servidor usando PM2
```sh
pm2 start index.js
pm2 save
pm2 startup
```

---

## 🌐 Instalar e Configurar Nginx

### 🔹 Instalar Nginx
```sh
sudo apt install nginx -y
```

---

## 🔥 Configuração do Firewall (UFW)

### 🔹 Instalar UFW e liberar portas
```sh
sudo apt install ufw -y
sudo ufw allow 'Nginx Full'
sudo ufw allow 22/tcp    # Porta SSH
sudo ufw enable
sudo ufw reload
```

---

## 👥 Acesso Remoto via SSH

### 🔹 Pegar o IP da máquina
```sh
ip a
```
- Procure pelo IP que termina com `/24`, exemplo: `10.0.0.156/24`.

### 🔹 Conectar via VSCode
- Instalar a extensão **Remote - SSH**.
- No VSCode, conectar usando:
```
usuario@ip
```
- Aceitar (yes) e digitar a senha.

Depois de conectado, acesse o diretório onde está o projeto.

---

## ⚙️ Comandos Úteis

| Comando | Descrição |
|:--------|:----------|
| `htop` | Monitor de processos |
| `pm2 list` | Ver lista de apps no PM2 |
| `pm2 logs` | Ver logs das aplicações |
| `sudo systemctl status mariadb` | Verificar status do MariaDB |

---
