# Deploy em VPS (Docker)

O deploy em uma Virtual Private Server (VPS) é a forma mais rápida de disponibilizar o Rhapsodia para sua equipe via internet, mantendo o controle total sobre a aplicação.

---

## 📋 Pré-requisitos

- **SO**: Ubuntu 22.04 LTS ou superior (Recomendado).
- **CPU**: Mínimo 2 vCPUs (4+ Recomendado).
- **RAM**: Mínimo 4GB (8GB+ Recomendado).
- **Disco**: 20GB+ SSD.
- **Ferramentas**: Docker e Docker Compose instalados.

---

## 🚀 Passo a Passo da Instalação

### 1. Preparação do Servidor
Atualize o sistema e instale as dependências básicas:
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install git curl -y
```

### 2. Clonando o Repositório
```bash
git clone https://github.com/pktech/rhapsodia-deploy.git
cd rhapsodia-deploy
```

### 3. Configuração do Ambiente
Crie o arquivo `.env` baseado no exemplo:
```bash
cp .env.example .env
nano .env
```
Defina as chaves de API (OpenRouter, OpenAI) e as URLs do sistema.

### 4. Inicialização via Docker Compose
```bash
docker-compose up -d
```
O Rhapsodia estará disponível na porta `8080` (padrão).

---

## 🔒 Configuração de SSL (Nginx + Certbot)

Para garantir o acesso seguro (`https://`), utilize o Nginx como Proxy Reverso:

1. **Instale o Nginx**: `sudo apt install nginx`
2. **Configure o Site**: Aponte o `proxy_pass` para `localhost:8080`.
3. **Instale o SSL**:
```bash
sudo apt install certbot python3-certbot-nginx
sudo certbot --nginx -d rhapsodia.suaempresa.com
```

---

## 🛠️ Manutenção e Logs

### Verificar Status:
```bash
docker-compose ps
```

### Visualizar Logs:
```bash
docker-compose logs -f
```

### Atualizar Sistema:
```bash
docker-compose pull
docker-compose up -d --remove-orphans
```

> [!TIP]
> Utilize um serviço de monitoramento como o **Uptime Kuma** para garantir que a plataforma esteja sempre online para seus usuários.
