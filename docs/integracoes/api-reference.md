# Referência de API (REST)

O Rhapsodia oferece uma API robusta baseada nos padrões do Open WebUI, permitindo que sistemas externos interajam com modelos, gerenciem documentos e orquestrem conversas de forma programática.

---

## 🔑 Autenticação

Todas as requisições devem incluir o token de autenticação no Header (Bearer Token).

```http
Authorization: Bearer <seu_token_de_api>
```

Você pode gerar este token em: **Painel do Admin** > **Configurações** > **API Keys**.

---

## 📡 Endpoints Principais

### 1. Modelos de IA
**GET** `/api/models`
- Retorna a lista de modelos (Cloud e Locais) disponíveis para o usuário.

### 2. Conversação (Chat)
**POST** `/api/chat/completions`
- Endpoint compatível com o padrão OpenAI.
- **Parâmetros**: `model`, `messages`, `temperature`, `stream`.

### 3. Base de Conhecimento (RAG)
**POST** `/api/knowledge/upload`
- Realiza o upload de documentos para indexação.
**GET** `/api/knowledge/search`
- Realiza busca semântica em documentos e retorna os trechos mais relevantes.

### 4. Gestão de Usuários
**GET** `/api/users`
- Retorna a lista de usuários e suas permissões (requer role `admin`).

---

## 🛠️ Exemplo de Chamada (cURL)

```bash
curl -X POST https://rhapsodia.empresa.com/api/chat/completions \
  -H "Authorization: Bearer sk-123456" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gpt-4o",
    "messages": [
      {"role": "user", "content": "Resuma os custos da nossa integração TOTVS."}
    ]
  }'
```

---

## 🪝 Webhooks

O Rhapsodia pode disparar eventos para URLs externas quando certas ações ocorrem:
- `conversation.created`: Novo chat iniciado.
- `document.processed`: Documento terminado de indexar.
- `limit.exceeded`: Usuário atingiu sua quota mensal.

![Editor de Funções (Pipes/Filters)](../assets/images/function-list.png)

---

## 🚦 Limites de Uso (Rate Limiting)

- **Default**: 60 requisições por minuto por API Key.
- Pode ser customizado no **Painel do Admin**.
