# 🚀 n8n Local Deployment with Docker + Neon or Local PostgreSQL

This repository helps you deploy **n8n** on a **local Linux laptop** using Docker, and connect it to either:
- 🟢 Neon (Free Cloud PostgreSQL)
- 🟠 Local PostgreSQL (hosted on the same machine)

---


## ✅ Prerequisites

- A Linux system (Ubuntu 22.04 recommended)
- Docker & Docker Compose installed
- A Neon account OR PostgreSQL installed locally

---

## 🐧 Step 1: Install Ubuntu on Second Laptop

1. Download ISO: https://ubuntu.com/download/desktop
2. Create bootable USB with Rufus or Etcher
3. Boot from USB, install Ubuntu
4. Update system after install:
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

---

## 🐳 Step 2: Install Docker & Docker Compose

```bash
sudo apt install docker.io docker-compose -y
sudo usermod -aG docker $USER
newgrp docker
```

---

## 📦 Step 3: Clone This Repo & Configure

```bash
git clone https://github.com/Abhishekjohn1507/n8n-local-deploy.git
cd n8n-local-deploy

cp .env.example .env
nano .env  # Add your DB credentials (Neon or local)
```

---

## ▶️ Step 4: Start n8n

```bash
docker-compose up -d
```

Access it from another device on the same network:

```
http://<your_local_ip>:5678
```

Get your local IP with:

```bash
ip a | grep inet
```

---

## 🔐 Optional: Add Domain + HTTPS (Nginx + Certbot)

Check [NGINX HTTPS Guide](https://github.com/Abhishekjohn1507/n8n-local-deploy.git/n8n-gcp-neon-free-hosting#-add-a-domain-name-with-https-using-nginx)

---

## 🤔 Neon vs Local PostgreSQL

| Feature              | Neon (Cloud)         | Local PostgreSQL         |
|---------------------|----------------------|---------------------------|
| 🔒 Security         | ✅ Encrypted          | ❌ Manual setup needed     |
| 🌐 Public Access    | ✅ Yes                | ❌ Local only              |
| 🧠 Ease of use      | ✅ Simple             | ⚠️ Needs install & config  |
| 💰 Cost             | ✅ Free Tier          | ✅ Free                    |
| 🚀 Speed            | ⚠️ Internet latency  | ✅ Fast (local disk)       |

---

## 🙌 Contributions

Pull requests welcome!

## 📜 License

MIT
     
