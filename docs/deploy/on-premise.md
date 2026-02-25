# Deploy On-Premise (Local com GPU)

O deploy On-Premise é a escolha ideal para empresas que exigem máxima privacidade de dados e querem utilizar modelos de código aberto (Open Source) sem custos de tokens.

---

## 🖥️ Requisitos de Hardware (GPU)

Diferente do deploy em nuvem, modelos locais exigem poder de processamento gráfico:

| Perfil | GPU Recomendada | VRAM | Objetivo |
|--------|-----------------|------|----------|
| **Light** | RTX 3060 / 4060 | 8GB - 12GB | Llama 3.1 8B, Mistral 7B |
| **Pro** | RTX 3090 / 4090 | 24GB | Llama 3.1 70B (Quantizado), Qwen 32B |
| **Enterprise** | A100 / H100 | 40GB+ | Modelos Full-Precision e alto volume |

---

## 📦 Estrutura do Deploy

O Rhapsodia On-Premise utiliza dois componentes principais:
1. **Ollama**: Motor de execução dos modelos locais.
2. **Rhapsodia WebUI**: Interface de usuário e sistema de governança.

---

## 🚀 Guia de Instalação (Linux/Windows com WSL2)

### 1. Instalação do Ollama
Visite [ollama.com](https://ollama.com) e siga as instruções de instalação para o seu sistema operacional. No Linux:
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### 2. Baixando Modelos Iniciais
```bash
ollama pull llama3.1:8b
ollama pull nomic-embed-text  # Essencial para RAG (Documentos)
```

### 3. Executando o Rhapsodia com GPU
Se estiver usando Docker, garanta que o plugin `nvidia-container-toolkit` esteja instalado.
```bash
docker run -d -p 3000:8080 \
  --add-host=host.docker.internal:host-gateway \
  --name rhapsodia \
  ghcr.io/open-webui/open-webui:main
```

---

## 🧠 Indexação Local (RAG)

Ao usar On-Premise, até a indexação de documentos é feita localmente.
- O modelo `nomic-embed-text` transformará seus PDFs em vetores dentro do seu servidor.
- Os dados **nunca** atravessam a internet, garantindo compliance total com políticas de sigilo industrial.

---

## 🏁 Verificação de Performance

Após a instalação, teste a velocidade:
1. Inicie um chat usando o modelo `llama3.1:8b`.
2. Peça um resumo de um documento longo.
3. Observe a taxa de **tokens por segundo (t/s)**. Acima de 15 t/s é considerado uma excelente experiência de uso.

> [!IMPORTANT]
> Mantenha os drivers da NVIDIA sempre atualizados para garantir a compatibilidade com as versões mais recentes dos modelos.
